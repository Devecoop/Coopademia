# Placa 1 - Introducción
Hoy en coopademia: Dataclasses de Python

Desde su versión 3.7 python nos provee de Dataclasses. Las mismas nos permiten generar muchos de los métodos y atributos de una clase que son normalmente utilizados de manera automatizada. (boilerplate).

# Placa 2 - Sintaxis

Para transformar una clase en dataclass solo tenemos que usar el decordador @dataclass de la siguiente manera

dataclasses overview.jpg

Las dataclasses en python nos permiten generar automáticamente los dunder methods también llamados métodos mágicos (como __init__, __eq__, __repr__), y facilita la creación de atributos e incialización de los mismos.

Son interesante los casos de __init__ y __repr__ ya que el primero como método constructor nos permite inicializar atributos del objeto y el segundo representarlos en pantalla

en lugar de escribir:

```
class Persona:
    def __init__(self, nombre, apellido, edad):
        self.nombre = nombre
        self.apellido = apellido
        self.edad = edad

    def __repr__(self):
        repr = f'Persona({self.nombre}, {self.apellido}: {self.edad})'
```     

Uso:
	- Apretá `ctrl + r` y comenzá a escribir.
	- Se te va a mostrar el último comando que matchee
	- Si querés buscar comandos anteriores otra vez apretá `ctrl + r` todas las veces necesarias hasta que encuentres el comando deseado.
	- Si lo encontrás, con `Enter` lo ejecutas
	- Si no lo encontrás, con `ctrl + c` cerrás la búsqueda
	
Extra tip: si ejecutás un comando que sabés que te va a ser útil en el futuro podés taggearlo, simplemente agregando un comentario (#) luego del mismo: 
		`docker-compose exec container /bin/bash #bash-en-container`

# Placa 3 - Búsqueda en archivos

* El buscador por excelencia, súper útil y versátil: `grep`

Lo que hace es buscar patrones en cada archivo y mostrarlos por pantalla si coinciden. 
El uso habitual es búsqueda de patrones en un archivo:
	`grep patron archivo`

Pero también podemos hacer búsquedas recursivas (-r) y case-insensitive (-i), lo que nos permite buscar patrones en directorios:

`grep -ri patron /ruta/a/directorio`


# Placa 4 - Bloqueos

Te pasó alguna vez que se te bloqueó la terminal y no entendiste por qué? Podés haber presionado sin querer el comando `ctrl + s` (que frena el output a la pantalla)
Para solucionar esto simplemente presionamos `ctrl + q` (continúa el output a la pantalla)

Otra que te puede haber pasado es estar corriendo un comando y haber presionado `ctrl + z`. Esto no frena el comando, pero si lo manda al background (o sea, no ves la salida).
Para recuperarlo podemos usar el comando `fg` en la terminal.


# Placa 5

Próximamente más tips de BASH

# Links


- https://itsfoss.com/linux-command-tricks/
- https://www.putorius.net/top-5-bash-tips-for-beginners.html
- https://www.bitarray.io/15-cool-bash-tricks/
