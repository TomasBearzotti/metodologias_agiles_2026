# Ejercicio Nro: 14

## Enunciado
Tu tarea es desarrollar una aplicación informática utilizando la técnica TDD para gestionar una cuenta bancaria. La aplicación debe permitir a los usuarios abrir una cuenta, realizar depósitos, hacer retiros y transferir fondos entre cuentas. 

Etapa 1: Especificación y prueba inicial
1. Especifica los requisitos básicos del sistema y las funcionalidades clave, como la apertura de cuenta, depósito de fondos, retiro de fondos y transferencia de fondos.
2. Escribe una prueba inicial que verifique si el sistema puede crear una instancia de una cuenta bancaria y obtener su saldo inicial.

## Resolución

### Etapa 1: Especificación y prueba inicial

**1. Especificación de Requisitos Básicos**
* **Apertura de cuenta:** El sistema debe permitir instanciar una cuenta asociada a un titular, asignando un saldo inicial (que por defecto será 0 si no se especifica).
* **Depósito de fondos:** Se debe poder incrementar el saldo actual sumando un monto específico mayor a cero.
* **Retiro de fondos:** Se debe poder descontar un monto del saldo, validando previamente que la cuenta tenga los fondos suficientes para la operación.
* **Transferencia de fondos:** El sistema debe permitir extraer un monto de una cuenta origen y depositarlo en una cuenta destino, asegurando la integridad de ambas operaciones.

**2. Prueba Inicial (Fase Roja de TDD)**
Siguiendo la metodología TDD, escribimos la prueba antes de que exista el código real. Esta prueba define el comportamiento que esperamos de nuestro sistema al crear una cuenta.

**Archivo: `test_banco.py`**
```python
import pytest
from banco import CuentaBancaria

def test_crear_cuenta_y_obtener_saldo_inicial():
    # Arrange (Preparar el escenario)
    cuenta = CuentaBancaria(titular="Juan Perez", saldo_inicial=1000)
    
    # Act (Actuar)
    saldo = cuenta.obtener_saldo()
    titular = cuenta.obtener_titular()
    
    # Assert (Verificar los resultados)
    assert saldo == 1000
    assert titular == "Juan Perez"

def test_crear_cuenta_saldo_por_defecto():
    # Arrange & Act
    cuenta = CuentaBancaria(titular="Maria Lopez")
    
    # Assert
    assert cuenta.obtener_saldo() == 0
```
### Etapa 2: Desarrollo de las funcionalidades básicas

En esta etapa de TDD, escribimos el código de producción necesario en `banco.py` para hacer que las pruebas pasen a verde, iterando funcionalidad por funcionalidad.

**3. Implementar la apertura de cuenta (Pasar a Verde el test de la Etapa 1)**

Para que el test inicial pase, creamos la estructura básica de la clase `CuentaBancaria`.

**Archivo: `banco.py`**
```python
class CuentaBancaria:
    def __init__(self, titular, saldo_inicial=0):
        self._titular = titular
        self._saldo = saldo_inicial

    def obtener_saldo(self):
        return self._saldo

    def obtener_titular(self):
        return self._titular
```
*(Al ejecutar `pytest`, el test de la Etapa 1 ahora pasa a verde).*

---

**4. Implementar funcionalidad de depósito**

*Fase Roja:* Agregamos el test de depósito en `test_banco.py`.
```python
def test_depositar_fondos():
    # Arrange
    cuenta = CuentaBancaria(titular="Juan Perez", saldo_inicial=1000)
    
    # Act
    cuenta.depositar(500)
    
    # Assert
    assert cuenta.obtener_saldo() == 1500
```

*Fase Verde:* Implementamos el método en `banco.py` para hacer pasar el test.
```python
    # Agregar dentro de la clase CuentaBancaria en banco.py
    def depositar(self, monto):
        if monto > 0:
            self._saldo += monto
```

---

**5. Implementar funcionalidad de retiro**

*Fase Roja:* Escribimos la prueba para los retiros en `test_banco.py`.
```python
def test_retirar_fondos():
    # Arrange
    cuenta = CuentaBancaria(titular="Juan Perez", saldo_inicial=1000)
    
    # Act
    cuenta.retirar(400)
    
    # Assert
    assert cuenta.obtener_saldo() == 600
```

*Fase Verde:* Implementamos la lógica en `banco.py`.
```python
    # Agregar dentro de la clase CuentaBancaria en banco.py
    def retirar(self, monto):
        if 0 < monto <= self._saldo:
            self._saldo -= monto
```

---

**6. Implementar funcionalidad de transferencia**

*Fase Roja:* Agregamos la prueba de transferencia en `test_banco.py`.
```python
def test_transferir_fondos():
    # Arrange
    cuenta_origen = CuentaBancaria(titular="Juan Perez", saldo_inicial=1000)
    cuenta_destino = CuentaBancaria(titular="Maria Lopez", saldo_inicial=500)
    
    # Act
    cuenta_origen.transferir(cuenta_destino, 300)
    
    # Assert
    assert cuenta_origen.obtener_saldo() == 700
    assert cuenta_destino.obtener_saldo() == 800
```

*Fase Verde:* Escribimos el método de transferencia en `banco.py`. Aplicamos el principio DRY reutilizando los métodos de retiro y depósito que ya funcionan.
```python
    # Agregar dentro de la clase CuentaBancaria en banco.py
    def transferir(self, cuenta_destino, monto):
        if 0 < monto <= self._saldo:
            self.retirar(monto)
            cuenta_destino.depositar(monto)
```

### Etapa 3: Pruebas adicionales y mejoras

En esta etapa, nos enfocamos en los casos de borde y posibles errores del usuario. Siguiendo el ciclo TDD, primero escribimos la prueba de cómo debería reaccionar el sistema ante un error (ej. lanzando una excepción) y luego modificamos el código.

**7. Pruebas adicionales (Casos límite)**

*Fase Roja:* Agregamos en `test_banco.py` las pruebas para los retiros sin fondos y transferencias fallidas.

```python
import pytest

def test_retirar_mas_del_saldo_lanza_error():
    # Arrange
    cuenta = CuentaBancaria(titular="Juan Perez", saldo_inicial=100)
    
    # Act & Assert
    with pytest.raises(ValueError, match="Fondos insuficientes"):
        cuenta.retirar(500)

def test_transferir_sin_fondos_lanza_error():
    # Arrange
    cuenta_origen = CuentaBancaria(titular="Juan Perez", saldo_inicial=100)
    cuenta_destino = CuentaBancaria(titular="Maria Lopez", saldo_inicial=0)
    
    # Act & Assert
    with pytest.raises(ValueError, match="Fondos insuficientes"):
        cuenta_origen.transferir(cuenta_destino, 200)
    
    # Verificamos que los saldos no se alteraron tras el error
    assert cuenta_origen.obtener_saldo() == 100
    assert cuenta_destino.obtener_saldo() == 0
```

**8. y 9. Ejecutar pruebas y Refactorizar**

*Fase Verde y Refactorización:* Ahora ajustamos `banco.py` para que lance (`raise`) los errores correspondientes en lugar de simplemente ignorar las operaciones. Esto mejora la solidez del sistema.

**Archivo: `banco.py` (Versión refactorizada)**
```python
class CuentaBancaria:
    def __init__(self, titular, saldo_inicial=0):
        self._titular = titular
        self._saldo = saldo_inicial

    def obtener_saldo(self):
        return self._saldo

    def obtener_titular(self):
        return self._titular

    def depositar(self, monto):
        if monto <= 0:
            raise ValueError("El monto a depositar debe ser mayor a cero")
        self._saldo += monto

    def retirar(self, monto):
        if monto <= 0:
            raise ValueError("El monto a retirar debe ser mayor a cero")
        if monto > self._saldo:
            raise ValueError("Fondos insuficientes")
        self._saldo -= monto

    def transferir(self, cuenta_destino, monto):
        # Al usar el método retirar, ya aprovechamos sus validaciones (DRY)
        self.retirar(monto)
        cuenta_destino.depositar(monto)
```

**10. Ejecutar pruebas nuevamente**
Ejecutamos `pytest`. Al refactorizar y reutilizar `self.retirar(monto)` dentro de `transferir`, la validación de fondos insuficientes se aplica automáticamente a las transferencias. ¡Todo en verde!

---

### Etapa 4: Cobertura completa de pruebas

**11. Asegurar cobertura y 12. Casos límite y situaciones excepcionales**

*Fase Roja:* Faltaba probar qué pasa si un usuario intenta depositar o retirar un monto negativo (por ejemplo, `-500`). 

Agregamos los últimos tests en `test_banco.py`:
```python
def test_depositar_monto_negativo_lanza_error():
    cuenta = CuentaBancaria(titular="Juan Perez")
    with pytest.raises(ValueError, match="El monto a depositar debe ser mayor a cero"):
        cuenta.depositar(-50)

def test_retirar_monto_negativo_lanza_error():
    cuenta = CuentaBancaria(titular="Juan Perez", saldo_inicial=100)
    with pytest.raises(ValueError, match="El monto a retirar debe ser mayor a cero"):
        cuenta.retirar(-20)
```

**13. Ejecutar todas las pruebas y verificar**
*Fase Verde Final:* Como en la refactorización anterior ya agregamos la validación `if monto <= 0`, estas nuevas pruebas pasan instantáneamente. 

**Resumen del ejercicio TDD:**
Hemos completado el ciclo **Red -> Green -> Refactor**. 
Comenzamos especificando el comportamiento deseado mediante pruebas unitarias que fallaban, escribimos el código mínimo necesario para superarlas y luego mejoramos la estructura del código añadiendo validaciones (excepciones). Esto nos garantiza un sistema confiable, 100% testeado y listo para adaptarse a nuevos requerimientos en el futuro.