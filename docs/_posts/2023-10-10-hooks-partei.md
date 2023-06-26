---
layout: post
title: Hooks parte I
subheading: 
author: ayecampot
image: assets/images/posts/coopademia/0.png
categories: React , Frontend
tags: images
sidebar: []
---

# Placa 1 - Hoy en coopademia: React ¿Qué son los Hooks? - Parte I


# Un poco de historia

 Luego de 5 años de existencia de la biblioteca, el equipo de React había encontrado varios problemas para los cuales era necesario un componente más simple que las clases, capaz de tener estado y ciclo de vida. Estas deben utilizarse siempre en el nivel superior de los componentes.

# ¿Qué viene a sumar Hooks?

La posibilidad de crear funciones que permiten unir nuestros componentes funcionales a características propias de un componente de clase. Es decir, proporcionan un estado y un ciclo de vida a estos componentes permitiendo evitar el uso de las clases.

# Diferentes tipos de Hooks,

Los más utilizados son los de: estado, de efecto y de contexto.

Hoy veremos el useState que nos permite agregarle un estado local a un componente funcional y cambiar ese estado.


# Veamos un ejemplo

```
import React, { useState } from 'react';
 
function ShowTextExample() {
 const [showText, setShowText] = useState(false);
 
 return (
   <div>
     <button
       type="button"
       onClick={() => setShowText(true)}
     >
       Mostrar Texto
     </button>
     {
       showText && ¡Se muestra el texto!
     }
   </div>
 );
}
 
export default ShowTextExample;

```

#  ¿Qué podemos observar en el mismo?

En primer lugar, declaramos dos variables utilizando desestructuración de array: la primera, showText, representa el estado del componente; la segunda, setShowText, representa la función con la que cambiaremos el valor de ese estado. Además, le asignamos un valor inicial (false).
Finalmente, utilizamos un manejador para el evento onClick del botón, setShowText, para cambiar el estado pasándole el valor true, lo que permite que se muestre el texto.

# Para tener en cuenta

Es importante considerar que los hooks suponen una adición a lo que ya existía y por lo tanto no implican el fin de los componentes de clase, es importante ir conociendo esta nueva función porque simplifica mucho el trabajo de desarrollo.

#  ¿Conocías Hooks?

¡Proximamente parte II!

# Links

https://es.reactjs.org/docs/hooks-intro.html
https://www.paradigmadigital.com/dev/hooks-como-utilizarlos-react/

























# Hoy en coopademia: Compatibilidad de los navegadores con un sitio web


# ¿Qué significa que nuestra web sea compatible?

Significa que se vea igual (o muy similar) en la mayoría de los navegadores. Si se consigue que se vea bien en: Chrome, Firefox, Opera, Safari, Mozilla y Edge, significa que el 99% de tus usuaries van a ver tu web correctamente.

# ¿Por qué hay incompatibilidad entre los navegadores?

Porque no todos los navegadores interpretan en código HTML y CSS de la misma manera, entre ellos existen pequeñas diferencias que hacen que el resultado no sea el mismo de unos a otros.

# ¿Cómo mejorar la compatibilidad de un sitio web?

Validar el código de la web en base a los estándares del W3C, te permite escanear en busca de errores de programación para una vez detectados poder corregirlos. A su vez nos permite saber que estamos haciendo las cosas correctamente más allá de la funcionalidad.


# Algunos consejos de CSS que mejorar la compatibilidad

-> Reseteá tu css para anular los valores por defecto de cada navegador.

```
*​{
margin:o;
padding;
}
```
-> Usar reglas de CSS que sean soportadas por la mayoría de los navegadores, una buena herramienta para conocerlas es caniuse.com

# Testear la web en diferentes navegadores.

El testeo puede ser de forma manual ingresando nuestra web en cada navegador, pero también hay diferentes herramientas que te permiten visualizar tu web en diferentes browser, como por ejemplo: Browershots, IE Tester y Browser Sandbox.

# ¿Sabías la importancia de testear la compatibilidad?

¡Hasta la próxima!

# Links
https://www.lawebera.es/xhtml-css/compatibilidad-web-navegadores.php