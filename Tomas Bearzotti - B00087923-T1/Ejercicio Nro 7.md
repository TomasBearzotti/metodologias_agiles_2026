# Ejercicio Nro: 7

## Enunciado
Dar un ejemplo de cada uno de los cuellos de botellas analizados anteriormente en el paper de Brooks

## Resolución

Basándome en las dificultades esenciales que plantea Brooks en su texto, dejo un ejemplo de la vida real para cada una:

* Complejidad: desarrollar un sistema de sueldos donde hay cientos de reglas distintas según el convenio, horas extras y descuentos que se mezclan entre sí.
* Conformidad: tener que adaptar nuestro sistema nuevo para que funcione obligado con una base de datos viejísima que el cliente se niega a actualizar.
* Mutabilidad: cuando el software ya está funcionando perfecto, pero sale una nueva ley del gobierno y hay que cambiar urgente la forma en que se calculan los impuestos en el código.
* Invisibilidad: lo difícil que es explicarle al cliente cómo está armada la arquitectura del sistema por detrás. Al no ser algo físico que se pueda ver, cuesta mucho que entiendan el esfuerzo y tiempo que lleva armarlo.