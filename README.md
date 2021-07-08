# Coopademia

Este repositorio recopila información de los post realizados por devecoop para la coopademia

## Estructura

```bash
.
├── docs -> Carpeta con el proyecto de jekyll del blog
│   ├── 404.html
│   ├── about.html
│   ├── archives.html
│   ├── assets -> Carpeta de assets para el sitio (css, js e imagenes)
│   │   ├── css
│   │   ├── images
│   │   └── js
│   ├── categories.html
│   ├── _config.yml -> Archivo de configuración de jekyll
│   ├── _posts -> Carpeta con los posts realizados que se publican en el sitio
│   │   └── YYYY-MM-DD-<tema>.md
│   ├── _sass -> Archivos SASS
│   └── tags.html
├── posts -> Temas preparados o en preparación con este repositorio
│   ├── YYYY-MM-DD-<tema>
│   │   ├── post.md -> Archivo final del post para diseñar post de instagram
│   │   └── README.md -> Información previa del tema, links, detalles, responsable, etc
│   └── pending.md -> Lista de temas pendientes para futuros posts
└── README.md -> Readme general del repository -> el que estas leyendo
```

## Proceso

- Revisar el archivo `posts/pending.md` para seleccionar el tema (o agregarlo en su defecto) y borrarlo de la lista
- Crear la carpeta `posts/YYYY-MM-DD-<tema>` con un `README.md` con la información del tema
- Ir agregando informacíon, links, cosas importantes, etc al `README.md` creado anteriormente
- Darle forma al post y crear el archivo `post.md` en `posts/YYYY-MM-DD-<tema>`
- Cuando ya este definido el post, se comienza con el proceso de diseño de la publicación
- Cuando se publique en instagram, tomar la caratura y crear el post para jekyll
  - Crear el archivo `docs/_posts/YYYY-MM-DD-<tema>.md` con la estrutura de post de jekyll (definida mas abajo en este **README.md**)
  - Cargarle la imagen del post poniendo el archivo en `docs/assets/images/posts/<tema>/0.jpg`
  - Subir los cambios al repostirio (automaticamente se actualiza el sitio, puede tardar unos minutos)

## Estructura de post de jekyll

La estructura para los archivos `docs/_posts/YYYY-MM-DD-<tema>.md`:

```yml
---
layout: post
title: <titulo>
subheading: <Subtitulo>
author: <Nombre de autor>
image: assets/images/posts/<tema>/0.jpg
categories: <categorias separados con espacios>
tags: <tags separados con espacios>
sidebar: []
---
```

## Prueba local de jekyll

- Instalar **ruby** y **gem**
- Instalar **jekyll** y **bundle** con **gem**: `gem install jekyll bundler`
- Entrar a la carpeta `docs/`
- Instalar las dependencias del proyecto: `bundle install`
- Ejecutar el servidor de desarrollo: `bundle exec jekyll serve`
- Entrar en `http://127.0.0.1:4000/Coopademia/` (no tiene live-reloading, hay que usar F5)
