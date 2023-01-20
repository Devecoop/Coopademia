# Placa 1 - Introducción
Hoy en coopademia: CReact Hooks parte II

# Placa 2 -
En la primera parte vimos las ventajas de usar Hooks para prescindir de clases, luego vimos uno de los más utilizados el useState. hoy es el turno de useEffects

# Placa 3 - useEffects: el Hook del efecto
Este hook es el que utilizaremos para reemplazar los métodos del ciclo de vida de los componentes de clase: ComponentDidMount, ComponentDidUpdate, ComponentWillUnmount. El hook useEffect es el equivalente a estos tres métodos combinados. Este hook se ejecuta siempre después del primer renderizado y después de cada actualización y, por lo tanto, se utiliza para ejecutar funciones después de hacer render.


# Placa 4 - ¿Qué hace useEffects?
useEffect recibe una función que puede realizar todo tipo de operación incluyendo efectos secundarios. Un ejemplo típico de una operación que podemos querer realizar es una llamada a un servicio.


# Placa 5 - ¿Cómo controlamos las llamadas?
Para controlar las llamadas para asegurarnos de que no se haga la petición innecesariamente si, por ejemplo, un valor se mantuvo equivalente entre renderizados,  con useEffect lo logramos pasándole a la función, un array como segundo parámetro. El valor de este array será el que React comparará para saber si tiene que volver a ejecutar el hook. En caso de no variar este valor, el hook no se ejecutará. 

# Placa 6 -Veamos un ejemplo:

import React, { useState, useEffect } from 'react';
 
function FormExample() {
 const [name, setName] = useState('');
 const [lastName, setLastName] = useState('');
 useEffect(() => {
   console.log('se ha ejecutado el hook');
 }, [name]);
 
 return (
   <div>
     <input value={name} onChange={(event) => setName(event.target.value)} />
     <input value={lastName} onChange={(event) => setLastName(event.target.value)} />
   </div>
 );
}


# Placa 7 - ¿Qué podemos observar en él?

El hook useEffect simplemente realiza un console.log() en cada ocasión en que se ejecuta. Si no le pasaremos el segundo parámetro [name], veríamos el resultado de console.log() cada vez que el usuario introduce un valor en cualquiera de los dos inputs. En cambio, al pasarle la variable name como dependencia, el hook se ejecuta solamente cuando el usuario introduce un valor en el input correspondiente a name.

# Placa 8 - Reflexiones finales
Al usar este hook de efecto es importante pasarle este segundo parámetro, si no puede ejecutarse innecesariamente y hasta generar un loop infinito.

# Placa 9 - Placa final de Devecoop. 
Te esperamos para seguir adentrándonos en el mundo Hooks de React.


¡Hasta la próxima!
