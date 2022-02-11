# Placa 1 - Introducción
Hoy en coopademia: Media queries en CSS

# Placa 2 - Qué son las media queries?

Las media queries son un metodo de CSS que nos permite aplicar diferentes estilos basandose en características del
dispositivo (tamaño de pantalla, orientación, entre otras).

Utilizando la regla **@media**, podemos incluír un bloque de propiedades de CSS si las condiciones dadas son verdaderas.

En el desarrollo de sitios responsive, las usamos para adaptar el contenido a diferentes tamaño de pantalla.

<img src="images/media-queries-1.png" width="400">

# Placa 3 - Cómo están compuestas las media queries?

Las media queries consisten de una o más **mediatypes** y **mediafeatures**.
El **mediatype** es el tipo de medio en el que se aplicará la query. El que utilizamos para sitios responsive es `screen`,

Y las **mediafeatures** son una o mas expresiones que indicarán sobre qué características se aplicará la query. Si nos interesa
el ancho de la pantalla, utilizaremos `max-width` y `min-width`.

En este caso, el valor que le demos a `max-width` dará verdadero si el ancho de la pantalla es menor, mientras que `min-width` si es mayor.

# Placa 4 - Sintaxis

<img src="images/media-queries-2.png" width="800">

En este caso, el header desaparecerá en pantallas que tengan menos de 500px de ancho.

El `only` previene que navegadores viejos ejecuten el código.

# Placa 5

Próximamente más tips de CSS

# Links
