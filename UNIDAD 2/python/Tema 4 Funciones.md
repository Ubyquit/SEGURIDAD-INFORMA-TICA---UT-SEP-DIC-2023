
Las funciones son bloques de código organizados y reutilizables que realizan una acción específica. Ayudan a modularizar el código y a reducir la repetición.

#### **1. Definición y llamada a funciones**

**a) Definir una función:**

Usa la palabra clave `def` seguida del nombre de la función y paréntesis.

**Ejemplo:**

```python
def saludo():
    print("¡Hola!")
```

**b) Llamar a una función:**

Una vez que la función ha sido definida, puedes "llamarla" o "invocarla" desde cualquier lugar de tu código.

**Ejemplo:**

```python
saludo()  # Esto imprimirá "¡Hola!" en la pantalla.
```

#### **2. Argumentos y valores de retorno**

**a) Funciones con argumentos:**

Puedes pasar valores a una función mediante argumentos.

**Ejemplo:**

```python
def saludo_personalizado(nombre):
    print(f"¡Hola, {nombre}!")
```

Uso:

```python
saludo_personalizado("Juan")  # Esto imprimirá "¡Hola, Juan!" en la pantalla.
```

**b) Funciones que retornan valores:**

Usa la palabra clave `return` para enviar un valor de regreso al lugar donde se llamó a la función.

**Ejemplo:**

```python
def suma(a, b):
    return a + b
```

Uso:

```python
resultado = suma(3, 4)
print(resultado)  # Esto imprimirá "7" en la pantalla.
```

#### **3. Funciones lambda**

Son funciones pequeñas y anónimas que pueden tener cualquier número de argumentos, pero solo una expresión. La expresión es evaluada y retornada.

**Ejemplo:**

```python
multiplica = lambda a, b: a * b

print(multiplica(5, 3))  # Esto imprimirá "15" en la pantalla.
```

---

**Ejercicio práctico 1:** Crea una función que reciba una lista de números y retorne el mayor de ellos.

```python
def numero_mayor(lista):
    return max(lista)

numeros = [3, 1, 8, 4, 6]
print(numero_mayor(numeros))  # Esto imprimirá "8" en la pantalla.
```

**Ejercicio práctico 2:** Crea una función que convierta grados Celsius a Fahrenheit.

```python
def celsius_a_fahrenheit(celsius):
    return (celsius * 9/5) + 32

grados_c = 25
print(celsius_a_fahrenheit(grados_c))  # Esto imprimirá "77.0" en la pantalla.
```

**Ejercicio práctico 3:** Usa una función lambda para calcular el área de un rectángulo.

```python
area_rectangulo = lambda largo, ancho: largo * ancho

l = 5
a = 3
print(area_rectangulo(l, a))  # Esto imprimirá "15" en la pantalla.
```

Las funciones son una herramienta esencial en programación para organizar y reutilizar el código, y son especialmente útiles a medida que los proyectos crecen en tamaño y complejidad.