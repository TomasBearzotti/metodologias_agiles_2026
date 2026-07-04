# Ejercicio Nro: 16

## Enunciado

**Objetivo:**
Utilizar el método Delphi para llegar a un consenso sobre la tecnología y la arquitectura más adecuadas para el desarrollo de una billetera virtual segura, escalable y confiable.

**Descripción:**
El método Delphi es una técnica de consulta estructurada que se utiliza para obtener opiniones expertas sobre un tema complejo. En este caso, el método Delphi se utilizará para recopilar información y opiniones de expertos en blockchain, seguridad, desarrollo de software y arquitectura de sistemas sobre la mejor tecnología y arquitectura para una billetera virtual.

1. **Definición del problema:** Describir objetivos, requisitos y factores clave.
2. **Selección del panel de expertos:** Identificar y reclutar a un grupo de expertos.
3. **Elaboración del cuestionario:** Diseñar preguntas sobre tecnología y arquitectura.
4. **Aplicación del método Delphi:** Rondas de consultas, análisis y retroalimentación.
5. **Selección de la tecnología y la arquitectura:** Selección final y justificación.
6. **Documentación y comunicación:** Registro del proceso y comunicación a stakeholders.

---

## Resolución

### 1. Definición del problema

El objetivo principal es definir la hoja de ruta técnica para una billetera virtual.

- **Requisitos críticos:**
  - **Seguridad:** Implementación de encriptación AES-256, autenticación biométrica y protocolos para evitar ataques de Man-in-the-Middle (MitM).
  - **Escalabilidad:** Arquitectura preparada para el crecimiento horizontal bajo demanda.
  - **Confiabilidad:** Alta disponibilidad garantizada mediante despliegues multi-región.
  - **Facilidad de uso:** Interfaz intuitiva (UX) orientada a la adopción masiva.
  - **Optimización de Costos:** Evaluación de TCO (Total Cost of Ownership) para elegir entre servicios gestionados y auto-hospedados.

- **Factores Clave de evaluación:** \* Stack de Blockchain (pública vs. privada).
  - Protocolos de seguridad (HSM, TLS 1.3).
  - Estilos arquitectónicos (Microservicios vs. Event-Driven).

### 2. Selección del panel de expertos

Se requiere un grupo heterogéneo para evitar sesgos de confirmación:

- **Perfiles buscados:** Arquitectos de nube, especialistas en seguridad (CISO), desarrolladores expertos en DLT (Distributed Ledger Technology) y analistas financieros.
- **Proceso de reclutamiento:** Se seleccionarán 12 expertos de diversos sectores (universidades, fintechs y consultoras).
- **Criterios de independencia:** Cada experto deberá firmar una declaración de ausencia de conflicto de intereses respecto a los proveedores tecnológicos evaluados.

### 3. Elaboración del cuestionario

El cuestionario se estructura para medir tanto aspectos cualitativos como cuantitativos:

- **Escala Likert:** Para valorar la eficacia de tecnologías propuestas respecto a la seguridad y escalabilidad.
- **Secciones temáticas:**
  - Comparativa de lenguajes (ej. Rust/Go vs. Node.js).
  - Estrategias de persistencia (SQL vs. NoSQL).
  - Protocolos de comunicación (gRPC vs. REST).
- **Preguntas abiertas:** Espacios para que los expertos sugieran tecnologías emergentes no contempladas inicialmente.

### 4. Aplicación del método Delphi

1. **Ronda 1:** Envío anónimo de cuestionarios. Se recopilan datos iniciales.
2. **Análisis:** Procesamiento estadístico (mediana y desviación estándar) de las respuestas para identificar los temas con mayor consenso.
3. **Ronda 2:** Los expertos reciben un informe anónimo con los resultados de la primera ronda. Se les pide reconsiderar sus respuestas frente a las opiniones de sus pares (especialmente en aquellos puntos donde hubo alta dispersión).
4. **Consenso:** Se alcanzan niveles de acuerdo superiores al 80% en los pilares tecnológicos fundamentales.

### 5. Selección de la tecnología y la arquitectura

- **Decisión:** Se opta por una arquitectura de **Microservicios basados en eventos** utilizando **Kubernetes** para orquestación, **Go** para servicios de alta concurrencia y una base de datos distribuida con soporte ACID.
- **Justificación:** La selección responde al alto consenso del panel sobre la necesidad de desacoplar los servicios de pago de los servicios de usuario para mejorar la seguridad (aislamiento) y facilitar la escalabilidad individual de los componentes.

### 6. Documentación y comunicación

- **Documentación técnica:** Se entrega el "Libro Blanco" del sistema que detalla el porqué de cada elección técnica, las restricciones superadas y los riesgos mitigados durante el proceso Delphi.
- **Comunicación:** Se presentará el roadmap técnico a los inversores enfocado en el valor de negocio (Time-to-Market y seguridad) y se coordinará una sesión de transferencia de conocimiento para el equipo de desarrollo encargado de la implementación.
