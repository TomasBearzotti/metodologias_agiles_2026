# Ejercicio Nro: 13

## Enunciado

1. ¿Qué es Extreme Programming (XP) y cuál es su objetivo principal dentro de las metodologías ágiles?
2. ¿Cuáles son los cinco valores principales de XP? Explicá brevemente cada uno.
3. ¿Por qué XP considera que las pruebas son un elemento fundamental del desarrollo de software?
4. ¿Qué es Test Driven Development (TDD) y cómo se relaciona con XP?
5. ¿En qué consiste la práctica de Pair Programming? Mencioná dos ventajas y una posible dificultad.
6. ¿Qué son las historias de usuario en XP y por qué se prefieren frente a una especificación extensa de requisitos?
7. ¿Qué significa Continuous Integration en XP y qué beneficios aporta al equipo de desarrollo?
8. ¿Cómo se aplica el concepto de Weekly Cycle en un proyecto desarrollado con XP?
9. En XP se plantea que se fija el tiempo, el costo y la calidad, y se negocia el alcance. ¿Qué significa esta idea? Explicalo con un ejemplo.
10. Elegí tres prácticas de XP y explicá cómo podrían aplicarse en un proyecto real de desarrollo de software.

## Resolución

### 1. Concepto y objetivo de Extreme Programming (XP)

Extreme Programming (XP) es un marco de desarrollo ágil centrado fuertemente en la ingeniería de software. Su objetivo principal es producir software de altísima calidad y adaptarse a los requerimientos cambiantes del cliente, mejorando al mismo tiempo la calidad de vida del equipo de desarrollo mediante la aplicación de buenas prácticas llevadas a niveles "extremos".

### 2. Los cinco valores principales de XP

- **Comunicación:** Se prioriza el diálogo cara a cara entre todo el equipo (incluyendo al cliente) por encima de la documentación exhaustiva para evitar malentendidos.
- **Simplicidad:** Consiste en desarrollar solo lo que se necesita en el momento ("hacer la cosa más simple que pueda funcionar"), evitando la sobre-ingeniería.
- **Feedback (Retroalimentación):** Obtener respuestas constantes y rápidas a través de pruebas automatizadas, entregas cortas al cliente y comunicación diaria del equipo.
- **Coraje:** Tener la valentía para tomar decisiones difíciles, como desechar código que no funciona, refactorizar arquitecturas o ser honestos con el cliente sobre los plazos.
- **Respeto:** Valorar el trabajo de los compañeros (por ejemplo, no romper la compilación del equipo) y respetar al cliente entregando software que aporte valor real.

### 3. Las pruebas como elemento fundamental

En XP, las pruebas son la red de seguridad del proyecto. Se considera que si una funcionalidad no está probada, simplemente no existe o no funciona. Al contar con un conjunto de pruebas automatizadas, los programadores tienen la confianza para modificar y refactorizar el código continuamente sin el miedo de introducir nuevos errores ("regresiones") en el sistema.

### 4. Test Driven Development (TDD) y su relación con XP

TDD (Desarrollo Guiado por Pruebas) es una práctica técnica en la que primero se escribe una prueba automatizada que falla, luego se escribe el código mínimo necesario para que la prueba pase, y finalmente se refactoriza el código para mejorarlo. Es una de las prácticas centrales de XP porque asegura que el 100% del código esté probado desde el inicio y fomenta un diseño de software simple y modular.

### 5. Pair Programming (Programación de a pares)

Consiste en que dos desarrolladores trabajen juntos en una misma computadora. Uno actúa como "Piloto" (escribe el código) y el otro como "Copiloto" (revisa en tiempo real, piensa en casos de borde y en la arquitectura general).

- **Ventajas:** Produce código con muchos menos errores (revisión continua) y facilita la transferencia rápida de conocimiento entre los miembros del equipo.
- **Dificultad:** Puede resultar mentalmente agotador, especialmente si hay incompatibilidad de personalidades o falta de comunicación entre los programadores.

### 6. Historias de Usuario vs. Especificación extensa

Las historias de usuario son descripciones breves de una funcionalidad escritas desde la perspectiva del cliente. En XP se prefieren porque no son contratos rígidos, sino el "punto de partida para una conversación". Evitan el desperdicio de redactar documentos enormes que inevitablemente quedarán obsoletos, fomentando que el equipo hable directamente con el cliente justo antes de implementar la funcionalidad.

### 7. Continuous Integration (Integración Continua)

Significa que los desarrolladores integran su código al repositorio principal varias veces al día. Cada integración dispara automáticamente la compilación y ejecución de todas las pruebas.

- **Beneficios:** Elimina el "infierno de integración" al final del proyecto. Los conflictos de código se detectan y resuelven en cuestión de horas o minutos, asegurando que el software siempre esté en un estado funcional.

### 8. Weekly Cycle (Ciclo Semanal)

Es el ritmo de iteración en XP. Al inicio de la semana, el equipo se reúne con el cliente, quien prioriza las historias de usuario. El equipo divide esas historias en tareas técnicas y se compromete a realizar solo aquellas que entren en el plazo de una semana. El viernes, el equipo entrega software funcionando, probado y listo para ser evaluado por el cliente.

### 9. Variables del proyecto: Tiempo, Costo, Calidad y Alcance

En los proyectos tradicionales se suele fijar el alcance, lo que a menudo termina sacrificando la calidad o el tiempo. XP fija el tiempo (fechas de entrega inamovibles), el costo (equipo definido) y la calidad (cero defectos conocidos), dejando el alcance como la variable negociable.

- **Ejemplo:** Si un equipo tiene que entregar una app de delivery el 15 del mes (tiempo fijo) y a mitad del desarrollo nota que no llega, en lugar de trabajar horas extras o entregar la app llena de bugs, negocia con el cliente posponer la funcionalidad de "seguimiento GPS en vivo" (negociar alcance). La app se entrega a tiempo, funciona perfecto, pero con una función menos.

### 10. Aplicación de tres prácticas XP en un proyecto real

Tomando como ejemplo el desarrollo del sistema web de un hospital:

- **Cliente in situ:** Asignar a un empleado administrativo del hospital para que trabaje codo a codo con el equipo de desarrollo. Si hay dudas sobre cómo se factura una obra social, el equipo le pregunta directamente en lugar de adivinar.
- **Small Releases (Entregas Pequeñas):** En lugar de lanzar todo el sistema del hospital en un año, lanzar al primer mes solo el módulo de turnos online. Esto permite que los pacientes lo empiecen a usar rápido y den feedback útil.
- **Estándares de codificación:** Definir reglas claras de cómo nombrar las variables y estructurar los archivos del proyecto. Si un desarrollador se enferma, otro puede tomar su código y entenderlo inmediatamente sin perder tiempo descifrando un estilo de programación distinto.
