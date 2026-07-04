# Ejercicio Nro: 15

## Enunciado

Generar un plan de trabajo basado en SCRUM para resolver la siguiente tarea.
Objetivo: El objetivo de este ejercicio es que los alumnos universitarios practiquen la creación de historias de usuarios para un sistema informático de presupuesto de construcción de galpones, utilizando la metodología ágil.
Descripción del ejercicio:

1. Los alumnos deberán formar equipos de trabajo, de preferencia de 3 a 5 personas por equipo.
2. Cada equipo deberá seleccionar la temática de construcción de galpones para su sistema informático de presupuesto.
3. Los equipos deberán generar al menos tres historias de usuario para su sistema, basadas en la temática seleccionada. Cada historia de usuario debe incluir un título y una descripción que contenga los criterios de aceptación.
4. Las historias de usuario deben estar enfocadas en las funcionalidades y características del sistema informático, considerando aspectos como la creación de presupuestos detallados, seguimiento del presupuesto durante la construcción, inclusión de etapas, generación de informes, entre otros.
5. Los equipos deben asegurarse de que las historias de usuario sean claras, concisas y comprensibles, siguiendo las buenas prácticas de redacción de historias ágiles.
6. Al finalizar, cada equipo deberá presentar sus historias de usuario al resto de la clase, explicando el contexto de su sistema y los criterios de aceptación de cada historia.
7. Se fomenta el intercambio de ideas y la retroalimentación constructiva entre los equipos durante las presentaciones.

## Resolución

### Parte 1: Plan de Trabajo Basado en SCRUM

Para abordar la creación de este sistema informático de presupuestos, el equipo de 4 personas se organizará mediante el framework Scrum de la siguiente manera:

**Roles del Equipo**

- **Product Owner:** Encargado de definir la temática (Galpones Avícolas) y priorizar qué funcionalidades del presupuesto aportan más valor al negocio.
- **Scrum Master:** Facilita el entorno de trabajo, asegurándose de que el equipo aplique buenas prácticas ágiles al redactar las historias.
- **Developers (2 personas):** Encargados del análisis técnico, la estimación y la redacción detallada de los criterios de aceptación.

**Eventos Scrum para el Ejercicio**

- **Sprint Planning:** Reunión inicial para definir el objetivo (Ej: "Tener el módulo base de presupuestos definido") y seleccionar qué historias de usuario se van a redactar.
- **Daily Scrum:** Sincronización rápida para comentar qué historias ya se redactaron y si hay bloqueos técnicos.
- **Sprint Review:** Coincide con el punto 6 de la consigna; el equipo presentará las historias de usuario terminadas al resto de la clase para recibir feedback de los stakeholders (profesor y compañeros).
- **Sprint Retrospective:** Reunión interna final para analizar cómo fue la dinámica del grupo y mejorar la comunicación para futuros TPs.

---

### Parte 2: Historias de Usuario (Temática: Galpones Avícolas)

### HU 1: Crear presupuesto base del galpón

**Como** Analista de Proyectos  
**Quiero** generar un presupuesto inicial ingresando las dimensiones del galpón  
**Para** brindarle al cliente una estimación rápida de los costos estructurales básicos.

**Criterios de Aceptación:**

- **Dado** que el analista se encuentra en el dashboard principal, **Cuando** hace clic en "Nuevo Presupuesto" e ingresa los metros cuadrados válidos, **Entonces** el sistema debe generar un borrador con el cálculo de materiales base (chapa, perfilería, cemento).
- **Dado** que el analista ingresa medidas negativas o nulas, **Cuando** intenta guardar, **Entonces** el sistema debe arrojar un error indicando "Las dimensiones deben ser mayores a 0".

### HU 2: Agregar sistema de ventilación al presupuesto

**Como** Técnico en Climatización  
**Quiero** agregar módulos de ventilación automatizada al presupuesto existente  
**Para** contemplar los costos del control de temperatura exigido para la cría de aves.

**Criterios de Aceptación:**

- **Dado** un presupuesto en estado "Borrador", **Cuando** el técnico selecciona la opción "Agregar Ventilación" y elige la potencia de los extractores, **Entonces** el sistema debe sumar el costo del equipamiento al total general en tiempo real.
- **Dado** que se agregó un módulo de ventilación, **Cuando** se visualiza el desglose, **Entonces** el ítem debe mostrar costo de equipo y costo estimado de mano de obra por separado.

### HU 3: Generar informe final en formato PDF

**Como** Administrador del sistema  
**Quiero** exportar el presupuesto detallado a un documento PDF  
**Para** poder enviárselo al cliente final de manera formal y profesional.

**Criterios de Aceptación:**

- **Dado** un presupuesto en estado "Aprobado", **Cuando** el administrador presiona el botón "Exportar PDF", **Entonces** el sistema debe descargar un archivo que incluya el logo de la empresa constructora, el detalle de etapas y el costo total con impuestos.
- **Dado** un presupuesto al que le faltan cargar costos obligatorios, **Cuando** se intenta exportar, **Entonces** el botón de "Exportar PDF" debe estar deshabilitado.

# Ejercicio Nro: 15.2

- **Resolucion de la actividad** [Bearzotti-Tomás.pdf](Bearzotti-Tomás.pdf)
