# Ejercicio Nro: 18

## Enunciado
Crear un documento .md donde se describa:
- Cada uno de los 5 prompts desarrollados.
- Resultados de la aplicación de cada prompt.
- Técnicas utilizadas en cada prompt.

---

## Resolución

### Agente 1: Definición del Product Backlog
**1. Prompt Desarrollado**
- **Contexto:** Actúas como un Product Owner experimentado trabajando en una empresa de desarrollo de software. Tu objetivo es transformar las necesidades del negocio en historias de usuario claras y priorizadas.
- **Instrucción:** Analiza los requerimientos proporcionados por el cliente para la aplicación web de gestión de envíos logísticos y redacta el Product Backlog inicial.
- **Input:** Requerimientos iniciales del cliente: Registro y autenticación de usuarios; Creación y seguimiento de envíos; Generación de reportes de estado de envíos; Integración con sistemas de terceros para rastreo de envíos.

**2. Resultados de la Aplicación**
- **Output:** Product Backlog inicial con las siguientes historias de usuario prioritarias:
    - Como usuario, puedo registrarme e iniciar sesión en la aplicación.
    - Como usuario, puedo crear un nuevo envío y seguir su estado.
    - Como usuario, puedo generar reportes de estado de mis envíos.

**3. Técnicas Utilizadas**
- **Role-playing (Asignación de Rol):** Se le asigna a la IA la personalidad de un "Product Owner experimentado" para condicionar el tono y el enfoque hacia el negocio.
- **Formateo Específico (Historias de Usuario):** Se induce a la IA a redactar los requerimientos utilizando la estructura ágil estándar ("Como [rol], quiero/puedo [acción]...").
- **Clasificación y Priorización:** Se le pide transformar requerimientos crudos en elementos de valor priorizados.

**4. Razonamiento Scrum**
En Scrum, el Product Owner (Dueño del Producto) es el responsable exclusivo de analizar, definir y priorizar qué es lo más urgente para armar primero. Forzamos a la IA a usar el formato de "Historias de Usuario" porque las metodologías ágiles priorizan centrarse en lo que necesita el cliente y el valor que aportan, sustituyendo a los densos documentos de requerimientos técnicos.

---

### Agente 2: Planificación del Sprint
**1. Prompt Desarrollado**
- **Contexto:** Actúas como Scrum Master y facilitador técnico. Tu rol es ayudar al equipo de desarrolladores a tomar los ítems del Product Backlog y desglosarlos en tareas asignables para el ciclo de trabajo.
- **Instrucción:** Toma las historias de usuario prioritarias del backlog y crea un Plan del Sprint, definiendo tareas técnicas específicas y asignando a los desarrolladores responsables.
- **Input:** Product Backlog (Salida del Agente 1).

**2. Resultados de la Aplicación**
- **Output:** Plan del Sprint con las siguientes tareas y responsables:
    - Tarea 1: Desarrollar la funcionalidad de registro e inicio de sesión. (Desarrollador A).
    - Tarea 2: Implementar la funcionalidad de creación y seguimiento de envíos. (Desarrollador B).
    - Tarea 3: Diseñar e implementar la generación de reportes de estado de envíos. (Desarrollador C).
    - Tarea 4: Integrar la aplicación con los sistemas de terceros para rastreo de envíos. (Desarrollador D).

**3. Técnicas Utilizadas**
- **Encadenamiento de Prompts (Prompt Chaining):** Utiliza la salida del Agente 1 como entrada directa para mantener el contexto del proyecto.
- **Role-playing:** Adopta la figura dual de Scrum Master y facilitador técnico.
- **Desglose de Tareas (Task Breakdown):** Convierte historias de usuario (centradas en el negocio) en tareas técnicas accionables (centradas en el desarrollo).

**4. Razonamiento Scrum**
Al principio de cada ciclo se hace una Reunión de Planificación (Sprint Planning) donde el equipo elige qué porción de historias puede comprometerse a terminar. Como Scrum fomenta los equipos auto-organizados y multifuncionales, los integrantes tienen la autonomía para tomar los requerimientos y decidir en conjunto cuál es la mejor forma técnica de resolverlos. El prompt simula este desglose técnico que los desarrolladores hacen guiados por el Scrum Master.

---

### Agente 3: Ejecución del Sprint
**1. Prompt Desarrollado**
- **Contexto:** Actúas como el Development Team. Tu objetivo es programar, testear e integrar el código de las tareas asignadas para generar valor real.
- **Instrucción:** Simula la ejecución técnica de las tareas planificadas e informa qué características de software están terminadas y listas para usar.
- **Input:** Plan del Sprint (Salida del Agente 2).

**2. Resultados de la Aplicación**
- **Output:** Incremento de software funcional con las siguientes funcionalidades implementadas:
    - Registro e inicio de sesión de usuarios.
    - Creación y seguimiento de envíos.
    - Generación de reportes de estado de envíos.
    - Integración con sistemas de terceros para rastreo de envíos.

**3. Técnicas Utilizadas**
- **Encadenamiento de Prompts:** Mantiene la secuencia lógica ingresando el Plan del Sprint.
- **Simulación de Escenarios:** Obliga a la IA a saltar la codificación real y simular el resultado de un proceso completado (Incremento).
- **Role-playing:** Asume la identidad colectiva del Development Team.

**4. Razonamiento Scrum**
La regla de oro de esta metodología es que al final de cada Sprint (iteración) se debe entregar un incremento de software funcionando. Obligamos a la IA a generar este "Output" porque el Incremento es vital: demuestra que al final del ciclo hay algo "terminado" y funcional que el cliente realmente puede ver.

---

### Agente 4: Revisión del Sprint
**1. Prompt Desarrollado**
- **Contexto:** Actúas simulando la dinámica entre el Cliente y el equipo Scrum durante la reunión de Sprint Review.
- **Instrucción:** Revisa el software entregado, genera feedback desde la perspectiva del negocio e identifica las lecciones aprendidas por el equipo técnico durante la construcción.
- **Input:** Incremento de software funcional (Salida del Agente 3).

**2. Resultados de la Aplicación**
- **Output:**
    - *Retroalimentación del cliente:* El cliente está satisfecho con las funcionalidades implementadas y sugiere agregar la opción de enviar notificaciones a los clientes sobre el estado de sus envíos.
    - *Lecciones aprendidas:* Mejorar la comunicación con el equipo de desarrollo para tener una mejor comprensión de los requerimientos del cliente. Implementar pruebas más exhaustivas antes de la entrega.

**3. Técnicas Utilizadas**
- **Role-playing Múltiple/Dinámico:** La IA simula a dos partes distintas (el Cliente dando feedback y el Equipo reflexionando) en un solo prompt.
- **Generación de Feedback Sintético:** Se fuerza a la IA a crear nuevos requerimientos (la opción de notificaciones) para simular cambios del mundo real.
- **Encadenamiento de Prompts:** Utiliza el Incremento del paso anterior como base de evaluación.

**4. Razonamiento Scrum**
Este agente simula la Sprint Review, el evento donde se le muestra el incremento al cliente para recibir feedback inmediato. La técnica de generar nuevos requerimientos en el prompt refleja el valor ágil de la "Colaboración con el cliente". Además, demuestra el principio mental de aceptar los cambios en los requisitos como una ventaja competitiva en lugar de aferrarnos a un plan rígido.

---

### Agente 5: Retrospectiva del Sprint
**1. Prompt Desarrollado**
- **Contexto:** Actúas como el Scrum Master guiando al equipo en un proceso de mejora continua (inspección y adaptación).
- **Instrucción:** Toma los comentarios y errores detectados en la revisión para redactar un plan de acción concreto que se aplicará en el próximo ciclo de trabajo.
- **Input:** Retroalimentación del cliente y lecciones aprendidas (Salida del Agente 4).

**2. Resultados de la Aplicación**
- **Output:** Plan de mejora para el siguiente Sprint:
    - Mejorar la coordinación entre los miembros del equipo de desarrollo.
    - Implementar un proceso más eficiente para la estimación y asignación de tareas.
    - Incorporar la funcionalidad de envío de notificaciones a los clientes sobre el estado de sus envíos en el próximo Sprint.

**3. Técnicas Utilizadas**
- **Cierre de Ciclo (Loop Methodology):** Toma las lecciones aprendidas y los nuevos requerimientos y los transforma en action items concretos, demostrando el principio empírico de Scrum.
- **Role-playing:** Adopta el rol de Scrum Master enfocado en procesos y mejora de equipos.
- **Encadenamiento de Prompts:** Cierra la secuencia lógica utilizando los hallazgos de la revisión.

**4. Razonamiento Scrum**
La Retrospectiva es, quizás, el evento más importante de la agilidad. El razonamiento de encadenar el feedback del cliente y los errores del equipo hacia este último agente responde al principio de "Reflexión y ajuste": el equipo debe analizar sus fallos a intervalos regulares y proponer mejoras para ser más efectivos en el siguiente ciclo.