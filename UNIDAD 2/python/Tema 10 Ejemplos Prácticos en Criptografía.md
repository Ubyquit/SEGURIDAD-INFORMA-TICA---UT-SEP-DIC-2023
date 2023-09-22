#### **1. Implementación del cifrado César**

El cifrado César es un tipo de cifrado por sustitución en el que cada letra en el texto original es reemplazada por una letra situada a un número fijo de posiciones en el alfabeto.

**Ejemplo en Python:**

```python
def cifrado_cesar(texto, desplazamiento):
    cifrado = ""

    for char in texto:
        if char.isalpha(): # Comprobamos si el carácter es una letra
            shifted = ord(char) + desplazamiento

            if char.islower():
                if shifted > ord('z'):
                    cifrado += chr(ord('a') + (shifted - ord('z') - 1))
                else:
                    cifrado += chr(shifted)
            elif char.isupper():
                if shifted > ord('Z'):
                    cifrado += chr(ord('A') + (shifted - ord('Z') - 1))
                else:
                    cifrado += chr(shifted)
        else:
            cifrado += char

    return cifrado

print(cifrado_cesar("Hola Mundo", 3))  # "Krud Pxqgr"
```

#### **2. Generación de números primos**

Generar números primos es fundamental para muchos algoritmos criptográficos, como RSA.

**Ejemplo de generación de números primos usando el "Criba de Eratóstenes":**

```python
def criba_eratostenes(n):
    primos = [True] * (n+1)
    p = 2
    while p**2 <= n:
        if primos[p]:
            for i in range(p**2, n+1, p):
                primos[i] = False
        p += 1

    return [i for i in range(2, n+1) if primos[i]]

print(criba_eratostenes(100))  # Lista de primos hasta 100
```

#### **3. Uso de bibliotecas de criptografía para ejemplos más avanzados**

Python cuenta con diversas bibliotecas para trabajar con criptografía, como `cryptography`.

**Ejemplo de cifrado y descifrado con Fernet (de la biblioteca `cryptography`):**

```python
from cryptography.fernet import Fernet

# Generar una clave
clave = Fernet.generate_key()
cipher = Fernet(clave)

# Cifrar un mensaje
texto = "Mensaje secreto"
texto_cifrado = cipher.encrypt(texto.encode())
print(texto_cifrado)

# Descifrar el mensaje
texto_descifrado = cipher.decrypt(texto_cifrado).decode()
print(texto_descifrado)  # "Mensaje secreto"
```

**Nota:** Si decides utilizar la biblioteca `cryptography`, asegúrate de instalarla previamente con `pip install cryptography`.

---

**Ejercicio práctico 1:** Crea una función que permita descifrar un mensaje cifrado con el cifrado César, dada la clave de desplazamiento.

**Ejercicio práctico 2:** Utiliza la función de la "Criba de Eratóstenes" para encontrar los primeros 100 números primos.

**Ejercicio práctico 3:** Utiliza la biblioteca `cryptography` para cifrar y descifrar un mensaje usando un algoritmo de tu elección distinto de Fernet.