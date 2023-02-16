
# Placa 1 - Introducción
Hoy en coopademia: Formas de incorporar imágenes en SVG a un proyecto web


# Placa 2 -  Pero primero ¿Qué es un SVGsta

SVG es el acrónimo de ‘Scalable Vector Graphics’, en la práctica es utilizado como un etiquetado especial para dibujar vectores, describiendo coordenadas dentro de un lienzo​ que nos permite generar ilustraciones escalables sin pérdida de resolución.

# Placa 3 - Sus ventajas

Son muy livianas y lo mejor de todo es que los atributos de sus etiquetas son accesibles y manipulables mediante CSS o JS.

# Placa 4 - ¿Cómo incorporar un SVG en tu proyecto web?

Existen diferentes formas que nos van a dar mayor o menor grado de manipulación, por eso la decisión va a estar basada en nuestro propósito las cuales veremos a continuación…


# Placa 5 - SVG Como imagen en un HTML 

Podemos incorporarla como cualquier imagen referenciando un ```<svg>​ ```con una etiqueta ``` ​<img>​ a través su atributo source​. En este caso la ilustración no será accesible ni manipulable más allá de lo que podemos hacer con una etiqueta  <img>```.


```

<img alt="Un" height="48" src="​enlace-a-la-imagen.svg​" width="48" />
```
# Placa 6 - SVG como imagen decorativa con CSS

También podemos llamar al ``` <svg> ```mediante la función ​url() de CSS a través de la propiedad background-image, de esta forma  tampoco son manipulables lo atributos propios del SVG.

```
.svg ​{
 ​width: 40rem;
 ​height: 22.5rem;
 ​background-image​:​ url(enlace-a-la-imagen.svg)​;
 ​background-size​:​ cover​;
}
```

# Placa 7 - SVG como un sprite de imágenes

Se recomienda cuando tenemos varias imágenes y no queremos perjudicar la performance de la aplicación​ al realizar un alto número de peticiones al servidor para recuperar estos recursos.

Sprite.svg

```
<svg version="1.1" xmlns="http://www.w3.org/2000/svg"> 
<defs> 
<symbol ​id=”avestruz”​ viewBox="0 0 512 512"> 
<circle cx=”10” cy=”10” r=”30” /> 
<path d=”...” /> 
</symbol> 
</defs> 
</svg>
```

Index.html

``` 
 <svg width=”48” height=”48”>
 <use ​xlink:href=”enlace-al-recurso/sprite.svg#avestruz”
 />
 </svg>
``` 

 # Placa 8 - SVG en línea

 Si queremos manipular el SVG por CSS o JS esta es la que más control nos da, ya que todas las etiquetas y atributos propios que conforman la etiqueta SVG quedan accesibles.

 Index.html

```
<svg width="300" height="300" viewbox="0 0 300 300">
 <circle cx="150" cy="150" r="100"></circle>
</svg>
```

Styles.css

```
circle​ ​{ ​
 transition​:​ fill 250ms​;
}
svg:hovercircle​ ​{ ​
 fill​:​ #f06​; 
} 
```

 # Placa 9 - Imagen final con el logo de Devecoop.
Imagen final con el logo de Devecoop.

¿Sabías estos beneficios?

¡Hasta la próxima!