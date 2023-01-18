# Placa 1 - Introducción
Hoy en coopademia: CSS Grid Parte I

# Placa 2 ¿Cómo nace CSS grid?
Surge de la necesidad de algo más potente, y toma las ventajas del sistema Flexbox, sumándole muchas mejoras y características que permiten crear muy rápido cuadrículas sencillas y potentes. 
Grid y Flexbox pueden convivir perfectamente, de hecho son grandes aliades.

# Placa 3 ¿Cuáles son las diferencias entre Flexbox y Grids?
La diferencia básica entre CSS Grid Layout y CSS Flexbox Layout es que Flexbox se creó para diseños de una dimensión, en una fila o una columna. En cambio CSS Grid Layout se pensó para el diseño bidimensional, en varias filas y columnas al mismo tiempo.

(Imagen de referencia 1)

# Placa 4- ¿Cómo comenzamos a generar nuestra grilla?
Activamos la cuadrícula Grid utilizando, sobre el elemento contenedor, la propiedad display con el valor grid o inline-grid. El primero de ellos permite que aquella aparezca encima/debajo del contenido exterior (en bloque), mientras que el segundo permite que la cuadrícula se vea a la izquierda/derecha (en línea) del contenido exterior.

(Imagen de referencia 2)

 # Placa 5-Luego le podemos aplicar cualquiera de las siguientes propiedades para generar filas y columnas y sus respectivos tamaños.

 grid-template-columns:
Establece el TAMAÑO de cada columna (col 1, col 2...).
grid-template-rows:
Establece el TAMAÑO de cada fila (fila 1, fila 2...).
grid-column-gap
Establece el TAMAÑO de los huecos entre columnas (líneas verticales).
grid-row-gap
Establece el TAMAÑO de los huecos entre filas
(líneas horizontales).


 # Placa 6-Luego le podemos aplicar cualquiera de las siguientes propiedades para generar filas y columnas y sus respectivos tamaños.

grid-column-gap
Establece el TAMAÑO de los huecos entre columnas (líneas verticales).
grid-row-gap
Establece el TAMAÑO de los huecos entre filas
(líneas horizontales).

# Placa 7- Veamos un ejemplo de como crear una grilla simple

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

# Placa 8- ¿Cómo se vería esta grilla en el browser?
(Imagen 3)

# Placa 8- ¿Podemos usar medidas relativas en grid?
Sin ningún problema, de hecho existe la unidad fr (fraction) propia de grid para generar grillas que se adapten a diferentes tamaños de pantallas.

.grid {
    display: grid;  
    grid-template-columns: 2fr 1fr; 
    grid-template-rows: 3fr 1fr; 
}

# Placa 9 -Reflexiones finales
CSS grid es una de las herramientas más potentes para hacer layout complejos y bidimensaionales, este es un primer acercamiento.

¡Pronto tendremos la segunda parte de grid!
10- Placa con el logo de Devecoop

# Placa 10 - Imagen final con el logo de Devecoop.

¿Sabías la importancia de testear la compatibilidad?

¡Hasta la próxima!
