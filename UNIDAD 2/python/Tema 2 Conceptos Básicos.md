#### **1. Variables y tipos de datos**

En Python, una variable se utiliza para almacenar un valor. No es necesario declarar explícitamente el tipo de dato de una variable, ya que Python es un lenguaje de tipado dinámico.

**Ejemplo:**

```python
nombre = "Juan"
edad = 20
altura = 1.80
es_estudiante = True
```

- `nombre` es una variable de tipo `str` (cadena de texto).
- `edad` es una variable de tipo `int` (entero).
- `altura` es una variable de tipo `float` (decimal).
- `es_estudiante` es una variable de tipo `bool` (booleano).

#### **2. Operadores**

**a) Aritméticos:** Se usan para realizar operaciones matemáticas.

```python
a = 10
b = 3

suma = a + b
resta = a - b
multiplicacion = a * b
division = a / b
modulo = a % b  # Retorna el residuo de la división
```

**b) De comparación:** Se usan para comparar valores.

```python
a == b  # Igual a
a != b  # Diferente de
a > b   # Mayor que
a < b   # Menor que
a >= b  # Mayor o igual que
a <= b  # Menor o igual que
```

**c) Lógicos:** Se usan para combinar condiciones.

```python
x = True
y = False

resultado_and = x and y  # True si x e y son verdaderos
resultado_or = x or y   # True si al menos uno es verdadero
resultado_not = not x   # True si x es falso, y viceversa
```

#### **3. Entrada y salida estándar**

**a) Entrada (`input()`):** 

```python
nombre = input("¿Cuál es tu nombre? ")
print(f"Hola, {nombre}!")
```

**b) Salida (`print()`):**

```python
edad = 20
print(f"Tengo {edad} años.")  # Uso de f-strings para formatear salida
```

---

**Ejercicio práctico 1:** Solicita al usuario ingresar su nombre, edad y ciudad de origen y luego muestra un mensaje personalizado con esos datos.

```python
nombre = input("Introduce tu nombre: ")
edad = input("Introduce tu edad: ")
ciudad = input("Introduce tu ciudad de origen: ")

print(f"¡Hola {nombre}! Veo que tienes {edad} años y eres de {ciudad}.")
```

**Ejercicio práctico 2:** Solicita dos números al usuario y muestra la suma, resta, multiplicación y división de esos números.

```python
num1 = float(input("Introduce el primer número: "))
num2 = float(input("Introduce el segundo número: "))

print(f"Suma: {num1 + num2}")
print(f"Resta: {num1 - num2}")
print(f"Multiplicación: {num1 * num2}")
print(f"División: {num1 / num2}")
```

Estos son los conceptos básicos para comenzar a programar en Python. Una vez que los estudiantes estén familiarizados con estas nociones, podrán construir programas más complejos y comprender mejor los temas avanzados.