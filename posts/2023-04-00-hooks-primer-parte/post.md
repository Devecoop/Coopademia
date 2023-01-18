
# Placa 1 - Introducción
Hoy en coopademia: React ¿Qué son los Hooks? - Parte I


# Placa 2 - Un poco de historia

 Luego de 5 años de existencia de la biblioteca, el equipo de React había encontrado varios problemas para los cuales era necesario un componente más simple que las clases, capaz de tener estado y ciclo de vida. Estas deben utilizarse siempre en el nivel superior de los componentes.

# Placa 3 - ¿Qué viene a sumar Hooks?

La posibilidad de crear funciones que permiten unir nuestros componentes funcionales a características propias de un componente de clase. Es decir, proporcionan un estado y un ciclo de vida a estos componentes permitiendo evitar el uso de las clases.

# Placa 4 - Existen diferentes tipos de Hooks,

Los más utilizados son los de: estado, de efecto y de contexto 

Hoy veremos el useState que nos permite agregarle un estado local a un componente funcional y cambiar ese estado.


# Placa 5- Veamos un ejemplo

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


# Placa 6 - ¿Qué podemos observar en este ejemplo?

En primer lugar, declaramos dos variables utilizando desestructuración de array: la primera, showText, representa el estado del componente; la segunda, setShowText, representa la función con la que cambiaremos el valor de ese estado. Además, le asignamos un valor inicial (false).
Finalmente, utilizamos un manejador para el evento onClick del botón, setShowText, para cambiar el estado pasándole el valor true, lo que permite que se muestre el texto.

# Placa 7- Para tener en cuenta

Es importante considerar que los hooks suponen una adición a lo que ya existía y por lo tanto no implican el fin de los componentes de clase, es importante ir conociendo esta nueva función porque simplifica mucho el trabajo de desarrollo.

# Placa 6 - Imagen final con el logo de Devecoop.

¿Conocías Hooks?

¡Proximamente parte II!