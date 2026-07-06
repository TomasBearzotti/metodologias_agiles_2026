# Ejercicio Nro: 17

## Enunciado

**Objetivo:** Desarrollar una aplicación web que permita a los usuarios gestionar sus finanzas personales de manera eficiente y segura. La aplicación debe cumplir con los siguientes requisitos funcionales:

1. **Gestión de cuentas bancarias:**
   - Permitir la creación y edición de cuentas bancarias.
   - Visualizar el saldo actual y el historial de movimientos de cada cuenta.
   - Realizar transferencias entre cuentas propias.
   - Descargar el historial de movimientos en formato CSV o PDF.

2. **Gestión de ingresos y gastos:**
   - Permitir la creación y edición de ingresos y gastos.
   - Categorizar los ingresos y gastos por tipo (salario, alquiler, alimentación, etc.).
   - Visualizar gráficos y reportes sobre los ingresos y gastos por categoría y período de tiempo.
   - Establecer presupuestos para diferentes categorías de gastos.

3. **Gestión de deudas:**
   - Permitir la creación y edición de deudas.
   - Indicar el monto total de la deuda, la tasa de interés, el plazo de pago y el monto de las cuotas.
   - Visualizar un calendario de pagos y realizar simulaciones de diferentes escenarios de pago.
   - Generar informes sobre el progreso en el pago de las deudas.

**Resolver:**

- Estimación del tamaño del proyecto (X PFC).
- Cálculo del costo por punto de función (Y USD).
- Cantidad de puntos de función que se pueden hacer en un mes (Z personas, W PFC/mes).
- Duración del proyecto (A meses).
- Costo del proyecto (B USD).

## Resolución

Para resolver este ejercicio utilizando el método COSMIC y siguiendo las instrucciones (clasificando en Pequeña, Mediana y Grande), vamos a asignar una estimación de puntos basada en la cantidad de movimientos de datos esperados para cada tipo de interacción: **Pequeña (S = 3 PFC)**, **Mediana (M = 5 PFC)** y **Grande (L = 8 PFC)**.

**1. Identificación y Clasificación de Interacciones Funcionales:**

_Gestión de cuentas bancarias:_

- Creación y edición de cuentas bancarias -> **M (5 PFC)** _(Entrada, lectura, escritura, salida)._
- Visualizar saldo actual e historial -> **M (5 PFC)** _(Lecturas múltiples, salida a pantalla)._
- Realizar transferencias entre cuentas propias -> **L (8 PFC)** _(Validación, múltiples lecturas, múltiples escrituras, salida de confirmación)._
- Descargar historial de movimientos (CSV/PDF) -> **M (5 PFC)** _(Generación de reporte)._

_Gestión de ingresos y gastos:_

- Creación y edición de ingresos y gastos -> **M (5 PFC)**
- Categorizar los ingresos y gastos por tipo -> **S (3 PFC)** _(Interacción simple de guardado)._
- Visualizar gráficos y reportes -> **L (8 PFC)** _(Procesamiento de datos estadísticos y representación gráfica)._
- Establecer presupuestos para categorías -> **M (5 PFC)**

_Gestión de deudas:_

- Creación y edición de deudas -> **M (5 PFC)**
- Indicar monto, tasa, plazo y cuotas (Cálculo) -> **M (5 PFC)**
- Visualizar calendario de pagos y simular escenarios -> **L (8 PFC)** _(Proyecciones temporales y cálculos dinámicos)._
- Generar informes sobre el progreso -> **M (5 PFC)**

**2. Calcular el tamaño funcional:**
Sumando los Puntos de Función COSMIC (PFC):

- Cuentas: 5 + 5 + 8 + 5 = 23 PFC
- Ingresos/Gastos: 5 + 3 + 8 + 5 = 21 PFC
- Deudas: 5 + 5 + 8 + 5 = 23 PFC
- **Tamaño total estimado (X): 67 PFC**

**3. Obtener el costo por punto de función:**
Asumiendo un entorno de desarrollo regional promedio (como se solicita, investigando el mercado):

- **Costo por punto de función (Y): 150 USD**

**4. Determinar la cantidad de PFC por mes:**
Considerando un equipo ágil estándar:

- Tamaño del equipo (**Z**): **3 personas** (ej. 1 Frontend, 1 Backend, 1 QA/Analista).
- Capacidad de desarrollo (**W**): **30 PFC/mes** _(promedio de 10 PFC mensuales por integrante)._

**5. Calcular la duración del proyecto:**

- Duración (**A**) = Tamaño funcional (X) / Capacidad mensual (W)
- Duración = 67 / 30 = **2,23 meses** (aprox. 9 a 10 semanas de trabajo).

**6. Estimar el costo total:**

- Costo total (**B**) = Tamaño total (X) \* Costo por punto de función (Y)
- Costo total = 67 \* 150 USD = **10.050 USD**

**Resumen de Resultados Finales:**

- **X** = 67 PFC
- **Y** = 150 USD
- **Z** = 3 personas
- **W** = 30 PFC/mes
- **A** = 2,23 meses
- **B** = 10.050 USD
