
El control de flujo en programación se refiere a la decisión sobre qué instrucciones ejecutar y en qué orden. Python, como la mayoría de los lenguajes de programación, incluye sentencias condicionales y bucles.

#### **1. Condicionales: `if`, `elif`, `else`**

Permiten ejecutar bloques de código basados en condiciones específicas.

**Ejemplo:**

```python
edad = 18

if edad < 18:
    print("Eres menor de edad.")
elif edad == 18:
    print("Tienes justo 18 años.")
else:
    print("Eres mayor de edad.")
```

#### **2. Bucles**

Los bucles permiten ejecutar un bloque de código repetidamente.

**a) Bucle `for`:** 

Se utiliza para iterar sobre una secuencia (lista, tupla, cadena, etc.).

**Ejemplo:**

```python
frutas = ["manzana", "banana", "cereza"]

for fruta in frutas:
    print(fruta)
```

**b) Bucle `while`:** 

Ejecuta un bloque de código mientras una condición sea verdadera.

**Ejemplo:**

```python
numero = 1

while numero <= 5:
    print(numero)
    numero += 1
```

---

**Ejercicio práctico 1:** Programa que pide al usuario ingresar un número y muestra si es par o impar.

```python
numero = int(input("Introduce un número: "))

if numero % 2 == 0:
    print("El número es par.")
else:
    print("El número es impar.")
```

**Ejercicio práctico 2:** Programa que imprime los primeros 10 números de la serie Fibonacci.

```python
a, b = 0, 1
for i in range(10):
    print(a)
    a, b = b, a+b
```

**Ejercicio práctico 3:** Programa que pide al usuario un número `n` y muestra la suma de todos los números del 1 al `n`.

```python
n = int(input("Introduce un número: "))
suma = 0

for i in range(1, n+1):
    suma += i

print(f"La suma de los números del 1 al {n} es: {suma}")
```

Con estos conceptos, los estudiantes aprenderán a tomar decisiones en sus programas y a repetir acciones de manera eficiente. Estas estructuras de control de flujo son fundamentales para cualquier tipo de desarrollo y son ampliamente utilizadas en programación.