---
layout: post
title: Tipos de tests
subheading: 
author: Ska
image: assets/images/posts/coopademia/0.png
categories: testing
tags: testing
sidebar: []
---
# Introducción
Hoy en coopademia: Tipos de testing

A la hora de desarrollar software, en muchas ocasiones es poco valorado el proceso de prueba del mismo o "testing", siendo este cada vez mas importante a medida que nuestro proyecto crece. Hoy vamos a explorar los diferentes tipos de tests que existen así como el propósito de cada uno.

# ¿Qué tipo de testing existen?

Si bien existen variedad de tipos de tests, a grandes rasgos podemos identificar las siguientes:

- Unit Tests
- Integration Tests
- Functional Tests
- End-To-End Tests
- Regression Testing
- Smoke Testing
- Acceptance Testing

Veamos en detalle algunos de ellos

# Unit Tests

Son los tests de más bajo nivel. Mediante los tests de unidad lo que se prueba es funcionalidad lo más atómica y específica posible. Buscamos aislar el comportamiento de una función o método, abstrayendo cualquier interacción con otros módulos, funciones o agentes externos como bases de datos o conexiones de red.

# Integration/Functional Tests

Las pruebas de integración y funcionales, son tests de alto nivel donde se verifican que las distintas partes del sistema funcionen correctamente al estar en conjunto. En el caso de los tests funcionales además de verificar el funcionamiento, se comprueba que las salidas de una acción, se correspondan con el procesamiento de los datos que fueron ingresados, sin importar los estados intermedios.


# End 2 End Tests

Las pruebas de punta a punta (End to end) sirven para replicar el comportamiento de les usuaries del sistema de manera completa. Se verifican cosas como:

- Inicios de sesión
- Recupero de contraseñas
- Uso de filtros
...

Estas pruebas son muy costosas para mantener de manera automatizada, por lo que se suele apelar más a los tests unitarios y mantener unos pocos tests de punta a punta.

# Acceptance Tests

Son pruebas manuales que se realizan una vez que el software se encuentra en funcionamiento para constatar que el sistema satisfaga los requerimientos del negocio.

Es importante que los criterios de aceptación estén definidos antes de comenzar a trabajar en el proyecto y ser actualizados ante cualquier cambio que pueda surgir.

# Conclusión

Los distintos tipos de Tests nos permiten asegurar el comportamiento en las diversas partes e instancias del desarrollo de nuestro software. Nos ayudan a entregar un producto mejor, más seguro, estable y mantenible en el tiempo.

¿Ya le agregaste Tests a tu proyecto?

¡Hasta la próxima!

