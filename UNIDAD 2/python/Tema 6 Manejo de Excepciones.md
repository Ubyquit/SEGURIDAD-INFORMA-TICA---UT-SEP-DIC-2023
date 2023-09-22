En la programación, es común encontrar errores inesperados durante la ejecución. El manejo de excepciones permite que el programa se recupere de estos errores y continúe su ejecución en lugar de detenerse por completo.

#### **1. ¿Qué es una excepción?**

Una excepción es un evento que ocurre durante la ejecución de un programa y que interrumpe el flujo normal del programa. Las excepciones en Python son objetos que representan errores.

#### **2. Bloque `try` y `except`**

Si sabes que un bloque de código puede causar un error, puedes colocarlo en un bloque `try` y manejar el error en el bloque `except`.

**Ejemplo:**

```python
try:
    numero = int(input("Introduce un número: "))
    resultado = 10 / numero
    print(resultado)
except ZeroDivisionError:
    print("No puedes dividir por cero.")
except ValueError:
    print("Debes ingresar un número válido.")
```

En el ejemplo anterior, si el usuario introduce `0` se lanzará una `ZeroDivisionError` y si introduce una letra o palabra se lanzará una `ValueError`.

#### **3. Bloque `else`**

Se puede usar un bloque `else` después del `except`. Este bloque se ejecutará si no se lanzó ninguna excepción en el bloque `try`.

```python
try:
    numero = int(input("Introduce un número: "))
except ValueError:
    print("Debes ingresar un número válido.")
else:
    print(f"Has introducido el número {numero}.")
```

#### **4. Bloque `finally`**

Este bloque se ejecuta siempre, independientemente de si se lanza o no una excepción. Es útil para la limpieza, como cerrar archivos o liberar recursos.

```python
try:
    f = open("archivo.txt")
    # procesar el archivo
except FileNotFoundError:
    print("El archivo no se encuentra.")
finally:
    f.close()
```

---

**Ejercicio práctico 1:** Escribe un programa que solicite al usuario dos números y muestre la división de ambos, manejando posibles errores.

```python
try:
    num1 = float(input("Introduce el primer número: "))
    num2 = float(input("Introduce el segundo número: "))
    resultado = num1 / num2
    print(f"El resultado es: {resultado}")
except ZeroDivisionError:
    print("No puedes dividir por cero.")
except ValueError:
    print("Debes ingresar números válidos.")
```

**Ejercicio práctico 2:** Escribe un programa que intente abrir un archivo que no existe y maneje el error mostrando un mensaje personalizado al usuario.

```python
try:
    f = open("archivo_inexistente.txt", "r")
except FileNotFoundError:
    print("Error: No se pudo abrir el archivo porque no existe.")
```

El manejo adecuado de excepciones es esencial para desarrollar aplicaciones robustas y resistentes a errores. A través de este mecanismo, los programas pueden reaccionar adecuadamente a situaciones inesperadas y garantizar una experiencia más fluida para el usuario.