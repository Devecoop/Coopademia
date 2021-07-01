---
layout: post
title: Django ORM - prefetch_related
subheading: optimización para django ORM.
author: FedeG
image: assets/images/posts/prefetch_related/0.jpg
categories: django python
tags: django python orm optimize
sidebar: []
---

Para optimizar el tiempo de iteración de tus listas en Django hay varias herramientas que te permiten llegar a tu objetivo.
Hay toolbars de debug y varias funciones.

Hoy te enseñaremos a usar la función **prefetch_related** para reducir la cantidad de queries y su tiempo de ejecución para búsquedas en atributos de relaciones.

## Decorador para debugger

Utilizaremos este decorator para contar cuántas queries son realizadas y los segundos que tardan en ejecutarse

```python
from django.db import connection, reset_queries
import time
import functools
 
def query_debugger(func):
 
   @functools.wraps(func)
   def inner_func(*args, **kwargs):
 
       reset_queries()
 
       start_queries = len(connection.queries)
 
       start = time.perf_counter()
       result = func(*args, **kwargs)
       end = time.perf_counter()
 
       end_queries = len(connection.queries)
 
       print(f"Function : {func.__name__}")
       print(f"Number of Queries : {end_queries - start_queries}")
       print(f"Finished in : {(end - start):.2f}s")
       return result
 
   return inner_func
```

## Ejemplo sin prefetch_related

Sin **prefetch_related** esa función hace 1 query para obtener los posts y por las relaciones hace 3 queries para obtener el name:

- Una para la relación con **Signature**
- Otra para la relación con **Author**
- La relación con **Country**

Por ende, hace `1 + 3 * cantidad_de_posts queries`.

```python
@query_debugger
def test_no_prefetch():
   posts = Post.objects.filter(signature__author__country__name__in=['Argentina', 'Uruguay'])
 
   for post in posts:
       name = post.signature.author.country.name
       print(name)
```

## Ejemplo con prefetch_related

Con **prefetch_related** solo hace en total 4 queries:

1 - Una para los **Posts**
2 - Una para los **Signatures** de esos **Posts**
3 - Una para los **Authors** de esas **Signatures**
4 - Una para **Countries** de esos **Authors**

```python
@query_debugger
def test_prefetch():
   posts = Post.objects.filter(signature__author__country__name__in=['Argentina', 'Uruguay'])
   posts = posts.prefetch_related('signature__author__country')
 
   for post in posts:
       name = post.signature.author.country.name
       print(name)
```
