---
layout: post
title: CSS Grid parte II
subheading: 
author: ayecampot
image: assets/images/posts/coopademia/0.png
categories: CSS , Frontend
tags: images
sidebar: []
---

# Hoy en coopademia: CSS Grid Parte II

# Propiedades del padre y propiedades del hije

# ¿Cómo acomodamos los elementos hijos desde el elemento padre?
Es posible distribuir los elementos de una forma muy sencilla y cómoda: justify-items y align-items, que ya conocemos del módulo CSS Flexbox aplicándolo al elemento padre:

```
.padre {
   justify-content: start;
}

```

# Recordemos que...
justify-items
start | end | center | stretch
Distribuye los elementos en el eje horizontal.


align-items
start | end | center | stretch
Distribuye los elementos en el eje vertical.
Es importante tener en cuenta que mueve a todo el contenido de la grilla si queremos mover alguno en particular lo veremos en las siguientes propiedades.


# Llegó el turno de los hijes
Ahora vamos a ver ciertas propiedades que se aplican a cada ítem hijo de la cuadrícula:

```
.hijo {
   justify-self: start;
}

```
justify-self
Altera la justificación del ítem hijo en el eje horizontal.
align-self
Altera la alineación del ítem hijo en el eje vertical.

(Imagen de referencia 2)


# Te esperamos para la parte 3 de grid!

# ¡Hasta la próxima!

# Links
https://developer.mozilla.org/es/docs/Web/CSS/CSS_Grid_Layout
https://css-tricks.com/snippets/css/complete-guide-grid/
https://lenguajecss.com/css/maquetacion-y-colocacion/grid-css/













