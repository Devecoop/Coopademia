# Placa 1 - Introducción
Hoy en coopademia: CSS Grid Parte II: propiedades del padre y propiedades del hije

# Placa 2 -¿Cómo acomodamos los elementos hijos desde el elemento padre?
Es posible distribuir los elementos de una forma muy sencilla y cómoda: justify-items y align-items, que ya conocemos del módulo CSS Flexbox aplicándolo al elemento padre:

.padre {
   justify-content: start;
}


# Placa 3 - Recordemos que...
justify-items
start | end | center | stretch
Distribuye los elementos en el eje horizontal.


align-items
start | end | center | stretch
Distribuye los elementos en el eje vertical.


# Placa 4 - 
(imagen de referencia 1)

Es importante tener en cuenta que mueve a todo el contenido de la grilla si queremos mover alguno en particular lo veremos en las siguientes slides


# Placa 5 - Llegó el turno de los hijes
Ahora vamos a ver ciertas propiedades que se aplican a cada ítem hijo de la cuadrícula:

.hijo {
   justify-self: start;
}

justify-self
Altera la justificación del ítem hijo en el eje horizontal.
align-self
Altera la alineación del ítem hijo en el eje vertical.

(Imagen de referencia 2)

# Placa 6 - (Imagen de referencia 3)

# Placa 7 - Imagen final con el logo de Devecoop.

¡te esperamos para la parte 3 de grid!

¡Hasta la próxima!
