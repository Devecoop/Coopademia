---
layout: post
title: CSS Grid parte 1
subheading: 
author: ayecampot
image: assets/images/posts/coopademia/0.png
categories: CSS , Frontend
tags: images
sidebar: []
---

# Hoy en coopademia: CSS Grid Parte I

# ¿Cómo nace CSS grid?
Surge de la necesidad de algo más potente, y toma las ventajas del sistema Flexbox, sumándole muchas mejoras y características que permiten crear muy rápido cuadrículas sencillas y potentes. 
Grid y Flexbox pueden convivir perfectamente, de hecho son grandes aliades.

# ¿Cuáles son las diferencias entre Flexbox y Grids?
La diferencia básica entre CSS Grid Layout y CSS Flexbox Layout es que Flexbox se creó para diseños de una dimensión, en una fila o una columna. En cambio CSS Grid Layout se pensó para el diseño bidimensional, en varias filas y columnas al mismo tiempo.


# ¿Cómo comenzamos a generar nuestra grilla?
Activamos la cuadrícula Grid utilizando, sobre el elemento contenedor, la propiedad display con el valor grid o inline-grid. El primero de ellos permite que aquella aparezca encima/debajo del contenido exterior (en bloque), mientras que el segundo permite que la cuadrícula se vea a la izquierda/derecha (en línea) del contenido exterior.

# Luego le podemos aplicar cualquiera de las siguientes propiedades para generar filas y columnas y sus respectivos tamaños.

grid-template-columns:
Establece el TAMAÑO de cada columna (col 1, col 2...).

grid-template-rows:
Establece el TAMAÑO de cada fila (fila 1, fila 2...).

grid-column-gap
Establece el TAMAÑO de los huecos entre columnas (líneas verticales).

grid-row-gap
Establece el TAMAÑO de los huecos entre filas
(líneas horizontales).


# Luego le podemos aplicar cualquiera de las siguientes propiedades para generar filas y columnas y sus respectivos tamaños.

grid-column-gap
Establece el TAMAÑO de los huecos entre columnas 
(líneas verticales).

grid-row-gap
Establece el TAMAÑO de los huecos entre filas
(líneas horizontales).

# Veamos un ejemplo de como crear una grilla simple

```
grid {
   display: grid;  
   /* 2 columnas */
   grid-template-columns: 300px 100px; 
   /* 2 filas */
   grid-template-rows: 40px 100px; 
}

<section class="grid">
   <div>Item 1</div>
   <div>Item 2</div>
   <div>Item 3</div>
   <div>Item 4</div>
</section>

```

# ¿Podemos usar medidas relativas en grid?
Sin ningún problema, de hecho existe la unidad fr (fraction) propia de grid para generar grillas que se adapten a diferentes tamaños de pantallas.

```
.grid {
    display: grid;  
    grid-template-columns: 2fr 1fr; 
    grid-template-rows: 3fr 1fr; 
}
```

# Reflexiones finales
CSS grid es una de las herramientas más potentes para hacer layout complejos y bidimensaionales, este es un primer acercamiento.

¡Pronto tendremos la segunda parte de grid!
10- Placa con el logo de Devecoop

# ¿Sabías la potencia de CSS grid?

¡Hasta la próxima!


# Links
https://developer.mozilla.org/es/docs/Web/CSS/CSS_Grid_Layout
https://css-tricks.com/snippets/css/complete-guide-grid/
https://lenguajecss.com/css/maquetacion-y-colocacion/grid-css/













