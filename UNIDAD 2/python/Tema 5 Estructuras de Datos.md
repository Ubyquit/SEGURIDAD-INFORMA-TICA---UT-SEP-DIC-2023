
Las estructuras de datos en Python son colecciones que permiten organizar y almacenar múltiples elementos, facilitando su manipulación y consulta.

#### **1. Listas**

Son estructuras de datos ordenadas y modificables, que pueden contener múltiples valores, incluso de diferentes tipos.

**Ejemplo:**

```python
frutas = ["manzana", "banana", "cereza"]
numeros = [1, 2, 3, 4, 5]
mixto = ["texto", 123, True, 3.14]
```

Acceso y modificación:

```python
print(frutas[0])       # Imprime "manzana"
frutas[1] = "uva"      # Cambia "banana" por "uva"
```

Métodos comunes:

```python
frutas.append("naranja")    # Agrega un elemento al final
frutas.remove("manzana")    # Elimina un elemento específico
frutas.pop()                # Elimina el último elemento
```

#### **2. Tuplas**

Son similares a las listas, pero son inmutables, es decir, no puedes modificar su contenido una vez creado.

**Ejemplo:**

```python
colores = ("rojo", "verde", "azul")
```

Acceso:

```python
print(colores[1])    # Imprime "verde"
```

#### **3. Conjuntos (Sets)**

Son colecciones no ordenadas y sin elementos duplicados.

**Ejemplo:**

```python
animales = {"gato", "perro", "pez"}
```

Métodos comunes:

```python
animales.add("pájaro")     # Agrega un elemento
animales.remove("pez")     # Elimina un elemento
```

#### **4. Diccionarios**

Son colecciones no ordenadas de pares clave-valor.

**Ejemplo:**

```python
persona = {
    "nombre": "Juan",
    "edad": 25,
    "ciudad": "Madrid"
}
```

Acceso y modificación:

```python
print(persona["nombre"])    # Imprime "Juan"
persona["edad"] = 26        # Modifica el valor de "edad"
```

---

**Ejercicio práctico 1:** Crea una lista con tus películas favoritas y muestra la tercera película en la lista.

```python
peliculas = ["El Padrino", "Matrix", "Forrest Gump"]
print(peliculas[2])  # Imprime "Forrest Gump"
```

**Ejercicio práctico 2:** Dado un diccionario que guarda las calificaciones de un estudiante, calcula el promedio.

```python
calificaciones = {
    "matemáticas": 90,
    "historia": 85,
    "física": 78,
    "química": 93
}

promedio = sum(calificaciones.values()) / len(calificaciones)
print(f"El promedio es: {promedio}")
```

**Ejercicio práctico 3:** Crea un conjunto con tus hobbies y agrega uno nuevo.

```python
hobbies = {"leer", "correr", "cocinar"}
hobbies.add("bailar")
print(hobbies)
```

Las estructuras de datos son esenciales en programación para organizar la información de manera efectiva, permitiendo operaciones más rápidas y eficientes sobre ella.

---

#### Manipulación de Cadenas**

#### **1. Acceso a caracteres y slicing**
Las cadenas en Python son secuencias de caracteres y se pueden acceder a ellos usando índices.

**Ejemplo:**

```python
texto = "criptografia"
print(texto[0])  # c
print(texto[-1])  # a
print(texto[2:5])  # ipt
```

#### **2. Métodos comunes**

Python ofrece una variedad de métodos para trabajar con cadenas:

- **split()**: Divide una cadena en una lista de subcadenas basándose en un delimitador.
  
  ```python
  frase = "Hola Mundo"
  palabras = frase.split()
  print(palabras)  # ['Hola', 'Mundo']
  ```

- **join()**: Une una lista de cadenas en una única cadena.

  ```python
  palabras = ['Hola', 'Mundo']
  frase = ' '.join(palabras)
  print(frase)  # Hola Mundo
  ```

- **replace()**: Reemplaza una subcadena con otra.

  ```python
  saludo = "Hola Mundo"
  saludo_modificado = saludo.replace("Mundo", "Python")
  print(saludo_modificado)  # Hola Python
  ```

- **upper(), lower()**: Convierten la cadena a mayúsculas o minúsculas.

  ```python
  texto = "Python"
  print(texto.upper())  # PYTHON
  print(texto.lower())  # python
  ```

#### **3. Codificación de caracteres y bytes**

Dado que estamos hablando de criptografía, es crucial comprender cómo funcionan las codificaciones y cómo convertir cadenas a bytes y viceversa.

- **str.encode()**: Convierte una cadena a bytes.
  
  ```python
  texto = "Python"
  bytes_texto = texto.encode('utf-8')
  print(bytes_texto)  # b'Python'
  ```

- **bytes.decode()**: Convierte bytes a una cadena.

  ```python
  bytes_texto = b'Python'
  texto = bytes_texto.decode('utf-8')
  print(texto)  # Python
  ```

---

**Ejercicio práctico 1:** Dada una cadena que contiene palabras separadas por comas (ej. "manzana,banana,cereza"), conviértela en una lista y luego únela nuevamente en una cadena separada por espacios.

**Ejercicio práctico 2:** Convierte el mensaje "¡Hola Mundo!" a bytes y luego decodifícalo de nuevo a una cadena.

La manipulación de cadenas es un aspecto esencial de la programación en Python, especialmente en aplicaciones relacionadas con la criptografía, donde a menudo se necesita procesar y transformar texto. ¡Espero que encuentres útil este contenido para tu curso!