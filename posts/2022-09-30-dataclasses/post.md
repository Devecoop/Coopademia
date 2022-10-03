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

Los parámetros de dataclass() son:

init: Si es verdadero (valor por defecto), el método __init__() será generado.

Si la clase ya define __init__(), este parámetro es ignorado.

repr: Si es verdadero (valor por defecto), el método __repr__() es generado. La cadena de representación generada tendrá el nombre de la clase junto al nombre y la representación de cada uno de sus campos, en el mismo orden en el que están definidos en la clase. Es posible indicar que ciertos campos no sean incluidos en la representación. Por ejemplo: InventoryItem(name='widget', unit_price=3.0, quantity_on_hand=10).

Si la clase ya define __repr__(), este parámetro es ignorado.

eq: Si es verdadero (por defecto), el método __eq__() es generado. Este método compara entre instancias de la clase representando cada una de ellas mediante una tupla, siendo los elementos de la misma los campos de la clase ubicados en el mismo orden en el que fueron definidos (dos tuplas son iguales si, y sólo si, sus campos son iguales).

Si la clase ya define __eq__(), este parámetro es ignorado.

order: Si es verdadero (False es el valor por defecto), los métodos __lt__(), __le__(), __gt__() y __ge__() serán generados. Estos métodos comparan la clase como si fuera una tupla con sus campos, en orden. Ambas instancias en la comparación deben ser del mismo tipo. Si order es verdadero y eq falso, se lanza una excepción ValueError.

Si la clase ya define __lt__(), __le__(), __gt__() o __ge__(), se lanza una excepción TypeError.

unsafe_hash: Si es False (por defecto), se genera el método __hash__() de acuerdo a los valores de eq y frozen definidos.

__hash__() es utilizado por la función incorporada hash() y cuando los objetos definidos por la clase son añadidos a colecciones hash, como por ejemplo diccionarios y conjuntos. Definir el método __hash__() en una clase implica que sus instancias son inmutables. La mutabilidad es una propiedad compleja, ya que depende de cómo el programador utilice el objeto, la existencia y comportamiento de __eq__() y del valor asignado a las flags eq y frozen en el decorador dataclass().

Por defecto, dataclass() no añade de forma implícita el método __hash__() a menos que sea seguro hacerlo. Tampoco añade o cambia un método __hash__() previamente definido de forma explícita. Definir el atributo de clase __hash__ = None tiene un significado específico en Python, descrito en la documentación dedicada a __hash__().

If __hash__() is not explicitly defined, or if it is set to None, then dataclass() may add an implicit __hash__() method. Although not recommended, you can force dataclass() to create a __hash__() method with unsafe_hash=True. This might be the case if your class is logically immutable but can nonetheless be mutated. This is a specialized use case and should be considered carefully.

A continuación se explican las reglas que se aplican en la creación implícita del método __hash__(). Observar que no es compatible definir explícitamente un método __hash__() en su clase de datos y al mismo tiempo asignar unsafe_hash=True; esto lanza una excepción TypeError.

Si eq y frozen son ambos verdaderos, dataclass() genera por defecto un método hash() por ti. En el caso que eq sea verdadero y frozen falso, a __hash__() se le asigna None, en consecuencia será unhashable (lo cual es deseable, ya que es mutable). Si eq es falso, __hash__() permanece sin cambios, por lo que en este caso se hará uso del método hash() heredado de la superclase (lo que implica que si la superclase es object, se aplicará el hashing basado en el id de los objetos).

frozen: Si es verdadero (el valor por defecto es False), cualquier intento de asignación a un campo de la clase lanza una excepción. Esto emula el comportamiento de las instancias congeladas (frozen) de sólo lectura. Si __setattr__() o __delattr__() son definidos en la clase, se lanzará una excepción TypeError. Esto es ampliado más abajo.



# Placa 6 - Parámetros de incialización y valores por defecto

@dataclass
class C:
    a: int       # 'a' has no default value
    b: int = 0   # assign a default value for 'b'




Próximamente más tips de Python

# Links


- https://itsfoss.com/linux-command-tricks/
- https://www.putorius.net/top-5-bash-tips-for-beginners.html
- https://www.bitarray.io/15-cool-bash-tricks/
