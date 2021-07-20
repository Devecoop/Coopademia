# Etapa 1 - Introducción
Hoy en coopademia: Flexbox layout en CSS y sus propiedades principales

# Etapa 2 - Definición de flexbox
El módulo **flexbox** busca proveer una forma eficiente de presentar, alinear y distribuir el espacio entre los items de un *container*, incluso cuando el tamaño es desconocido y/o dinámico.
La idea principal es darle al *container* la habilidad de alterar la altura y/o ancho de sus items para llenar de la mejor manera el espacio disponible.
Para definir un *container* como flex seteamos el atributo *display* con el valor *flex*

(aca pondría de imagen una captura de código con un

    .container {
      display: flex;
    }

)

# Etapa 3 - Atributos de dirección y alineación

**flex-direction**: Define el eje principal, es decir, la dirección (*column*: vertical o *row*: horizontal) en al que se presentarán los items. La dirección que no fue seleccionada pasará a ser el eje secundario. También se puede definir que los items se presenten en el orden inverso al que están en el HTML (*column-reverse* y *row-reverse*).

**justify-content**: Define cómo se alinean los items sobre el eje principal.

* flex-start: Los items se presentan al comienzo del eje principal.
* flex-end: Los items se presentan al final del eje principal.
* center: Los items son centrados sobre el eje principal.
* space-between: Los items son distribuidos uniformemente sobre el eje principal.
* space-around:  Los items son distribuidos uniformemente sobre el eje principal con el mismo espacio alrededor de ellos pero el espacio del primer y último item con el borde es distinto. 
* space-evenly: Los items son distribuidos uniformemente sobre el eje principal con el mismo espacio alrededor de ellos y el mismo espacio es utilizado entre el primer y último item con los bordes.

**align-items**: Define cómo se alinean los items sobre el eje secundario.

* stretch: Los items se estiran para llenar el container (respetando el *min-width*/*max-width*).
* flex-start: Los items se presentan al comienzo del eje secundario.
* flex-end: Los items se presentan al final del eje secundario.
* center: Los items son centrados sobre el eje secundario.
* baseline: Los items son alineados de tal manera que sus baselines individuales queden alineadas.

(aca pondría de imagen una captura de código con un

    .container {
      flex-direction: row | row-reverse | column | column-reverse; /*default row*/
      justify-content: flex-start | flex-end | center | space-between | space-around | space-evenly; /*default flex-start*/
      align-items: stretch | flex-start | flex-end | center | baseline; /*default stretch*/
    }

)

# Etapa 4 - Atributos de ajuste

**flex-wrap**: Define si el container intenta ajustar los items en una sola línea (*no-wrap*), en varias líneas yendo de arriba hacia abajo (*wrap*) o en el orden inverso (*wrap-reverse*).

**flex-grow**: Es una propiedad del item que define la proporción en la cual un item puede crecer en el caso que sea necesario. Por ejemplo si todos los items tienen un *flex-grow* de 1 el espacio será distribuido equitativamente entre los items. Si uno de los items tiene un *flex-grow* de 2 va a ocupar el doble de espacio que el resto de los items (o al menos va a intentar ocupar).

**flex-shrink**: Es una propiedad del item que define la proporción en la cual un item puede achicarse en el caso que sea necesario. Utiliza la misma lógica que el *flex-grow*.

**flex-basis**: Es una propiedad del item que define el tamaño por default antes que se distribuya el espacio disponible. Puede ser una medida (20%, 10px, 7remetc) o una keyword. La keyword por default es auto que utiliza el width y height para determinar el tamaño. Según el browser existen otras keywords soportadas.

**flex**: Es un atajo para definir **flex-grow**, **flex-shrink** y **flex-basis** juntas. El segundo y tercer parámetro son opcionales.

(aca pondría de imagen una captura de código con un

    .container {
	  flex-wrap: nowrap | wrap | wrap-reverse; /*default no-wrap*/
    }
    .item {
      flex: 1 3 20%
	  flex-grow: 1; /*default 0*/
	  flex-shrink: 3; /*default 1*/
	  flex-basis: 20% | auto /*default auto*/
    }

)

# Etapa 5

Próximamente más tips de CSS

# Links
https://www.w3.org/TR/css-flexbox/
https://css-tricks.com/snippets/css/a-guide-to-flexbox/
