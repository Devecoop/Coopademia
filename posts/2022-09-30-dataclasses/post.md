# Placa 1 - Introducción
Hoy en coopademia: Dataclasses de Python

Desde su versión 3.7 python nos provee de Dataclasses. Las mismas nos permiten generar muchos de los métodos y atributos de una clase que son normalmente utilizados de manera automatizada. (boilerplate).

# Placa 2 - Sintaxis

Para transformar una clase en dataclass solo tenemos que usar el decordador @dataclass de la siguiente manera

dataclasses overview.jpg

Las dataclasses en python nos permiten generar automáticamente los dunder methods también llamados métodos mágicos (como __init__, __eq__, __repr__), y facilita la creación de atributos e incialización de los mismos.

Son interesante los casos de __init__ y __repr__ ya que el primero como método constructor nos permite inicializar atributos del objeto y el segundo representarlos en pantalla

# Placa 3 - Clase tradicional

```
class Persona:
    def __init__(self, nombre, apellido, edad):
        self.nombre = nombre
        self.apellido = apellido
        self.edad = edad

    def __repr__(self):
        repr = f'Persona({self.nombre}, {self.apellido}: {self.edad})'
```     

# Placa 4 - Dataclass

```
from dataclasses import dataclass, field

@dataclass
class Persona:
    nombre: str     
    apellido: str    
    edad: int = 0

```     


# Placa 5 - Parámetros de incialización

Próximamente más tips de Python

# Links


- https://itsfoss.com/linux-command-tricks/
- https://www.putorius.net/top-5-bash-tips-for-beginners.html
- https://www.bitarray.io/15-cool-bash-tricks/
