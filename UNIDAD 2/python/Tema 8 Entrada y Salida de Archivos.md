Python facilita la lectura y escritura de archivos. Esta capacidad es crucial para muchas aplicaciones, desde el procesamiento de datos hasta la configuración de programas.

#### **1. Apertura de archivos**

El método `open()` es la clave para manipular archivos en Python. 

**Ejemplo:**

```python
archivo = open("ejemplo.txt", "r")  # Abre el archivo en modo lectura
```

Los modos comunes son:

- `"r"`: Lectura (por defecto).
- `"w"`: Escritura (sobrescribe el archivo si ya existe).
- `"a"`: Añadir (agrega contenido al final del archivo si ya existe).
- `"b"`: Modo binario (se utiliza junto con otros modos, como `"rb"` o `"wb"`).

#### **2. Leer archivos**

**Ejemplo:**

```python
contenido = archivo.read()  # Lee todo el contenido
print(contenido)
```

También puedes leer una línea a la vez o todas las líneas como una lista:

```python
linea = archivo.readline()
lineas = archivo.readlines()
```

#### **3. Escribir en archivos**

```python
archivo = open("ejemplo.txt", "w")
archivo.write("Hola mundo!")
archivo.close()
```

#### **4. Cerrar archivos**

Es importante cerrar archivos después de usarlos para liberar recursos:

```python
archivo.close()
```

#### **5. Uso de `with`**

La declaración `with` se utiliza para simplificar el manejo de excepciones y asegurarse de que los archivos se cierren adecuadamente:

```python
with open("ejemplo.txt", "r") as archivo:
    contenido = archivo.read()
    print(contenido)
# El archivo se cierra automáticamente después del bloque 'with'
```

---

**Ejercicio práctico 1:** Crea un programa que escriba una lista de tareas en un archivo y luego lo lea y muestre en pantalla.

*escritura.py:*
```python
tareas = ["Comprar leche", "Estudiar Python", "Hacer ejercicio"]

with open("tareas.txt", "w") as archivo:
    for tarea in tareas:
        archivo.write(tarea + "\n")
```

*lectura.py:*
```python
with open("tareas.txt", "r") as archivo:
    lineas = archivo.readlines()
    for linea in lineas:
        print(linea.strip())
```

**Ejercicio práctico 2:** Modifica el programa anterior para que el usuario pueda añadir una nueva tarea al archivo.

```python
nueva_tarea = input("Introduce una nueva tarea: ")

with open("tareas.txt", "a") as archivo:
    archivo.write(nueva_tarea + "\n")
```

La capacidad de leer y escribir archivos permite a los programas interactuar con datos almacenados de manera persistente y es fundamental para muchas aplicaciones prácticas.