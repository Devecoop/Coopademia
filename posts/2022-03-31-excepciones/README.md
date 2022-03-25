# Placa 1 - Introducción
Hoy en coopademia: Manejo de excepciones

# Placa 2 - Qué son las excepciones?

Una excepción es un evento inesperado que ocurre mientras ejecutamos nuestro programa: Se interrumpe el flujo normal del mismo.


# Placa 3 - Qué tipo de eventos generan una excepción? (mediatypes)

En algunos lenguajes o sus librerías, estos eventos generan excepciones:

- Intentar hacer un request a una web que no existe (o está caída)
- Intentar abrir un archivo que no existe
- Intentar dividir por cero!
- intentar acceder a una key de un diccionario que no existe
- Intentar acceder a una propiedad de objeto inexistente: `null.blah`


# Placa 4 - Qué pasa si no manejamos nuestras excepciones?

Supongamos que nuestro programa es una calculadora.

Vamos a necesitar definir qué hacer en algunos casos en donde el usuario pueda introducir datos que lleven a algún tipo de error, en este caso matemático.

Por ejemplo, si nuestro programa recibe dos números y una operación, y el usuario ingresa 1/0 en muchos lenguajes el programa lanzará una excepción.

¿Qué significa esto?

El flujo del programa se interrumpirá, y salvo que hagamos algo al respecto (“manejarlo”) el error se propagará hacia arriba en el stacktrace hasta el final lo cual causará  que se detenga el programa.

En muchos casos también obtendremos el mensaje de error en la consola y el lugar dónde se generó “ZeroDivisionError”

<img src="images/excepciones-1.png" width="700">

# Placa 5 - Manejo de excepciones
Lo que debemos hacer es adelantarnos a esta situación. Cómo? Manejando esa excepción.

Esto consiste en utilizar una estructura que posee (en principio) dos partes
- ## Try:
    Para delimitar el scope de manejo de nuestra excepción usamos el bloque try.
- ## Except (o catch):
    Bloque que captura la excepción que buscamos y que nos permite actuar en función de ese error:
    - mostrarle al usuario un mensaje
    - loggear el error y enviarlo a algún servicio como Sentry para luego poder corregirlo
    - devolver un valor por defecto

<img src="images/excepciones-2.png" width="700">



# Placa 6 - Excepciones propias:
Además de las excepciones que existen en las librerías y lenguajes, podemos crear nuestras para
tener un mejor manejo de errores en nuestro código y aplicación.

Para esto, creamos una clase que extienda de la clase Exception:

<img src="images/excepciones-3.png" width="700">


Utilizando `raise` en nuestro código podemos forzar el lanzamiento de una excepción.




# Links
