
La Programación Orientada a Objetos (OOP) es un paradigma de diseño y programación que se basa en la idea de organizar el código en "clases" que representan objetos del mundo real o conceptos abstractos, y "objetos", que son instancias de estas clases.

#### **1. Definición de Clases**

Una clase es como un blueprint o plantilla para crear objetos. Define atributos (variables) y comportamientos (métodos) que sus objetos tendrán.

**Ejemplo:**

```python
class Coche:
    marca = ""
    modelo = ""
    color = ""

    def describir(self):
        return f"Un coche {self.color} de marca {self.marca} y modelo {self.modelo}"
```

#### **2. Creación de Objetos**

Un objeto es una instancia de una clase.

```python
mi_coche = Coche()
mi_coche.marca = "Toyota"
mi_coche.modelo = "Corolla"
mi_coche.color = "rojo"

print(mi_coche.describir())  # Salida: Un coche rojo de marca Toyota y modelo Corolla
```

#### **3. Constructor `__init__`**

Se usa para inicializar los atributos de un objeto al momento de su creación.

```python
class Coche:
    def __init__(self, marca, modelo, color):
        self.marca = marca
        self.modelo = modelo
        self.color = color
```

Al crear un objeto, puedes pasar argumentos al constructor:

```python
mi_coche = Coche("Toyota", "Corolla", "rojo")
```

#### **4. Encapsulamiento**

Es la práctica de ocultar detalles de implementación y exponer solo características esenciales. Se puede lograr utilizando variables y métodos privados (prefix `_` o `__`).

#### **5. Herencia**

Permite que una clase herede atributos y métodos de otra clase.

```python
class Vehiculo:
    def __init__(self, marca, color):
        self.marca = marca
        self.color = color

class Coche(Vehiculo):
    def __init__(self, marca, color, modelo):
        super().__init__(marca, color)
        self.modelo = modelo
```

---

**Ejercicio práctico 1:** Crea una clase `Persona` con atributos para nombre y edad, y un método para presentarse.

```python
class Persona:
    def __init__(self, nombre, edad):
        self.nombre = nombre
        self.edad = edad

    def presentarse(self):
        return f"Hola, mi nombre es {self.nombre} y tengo {self.edad} años."

juan = Persona("Juan", 25)
print(juan.presentarse())
```

**Ejercicio práctico 2:** Extiende la clase `Persona` con una subclase `Estudiante` que añade el atributo `carrera`.

```python
class Estudiante(Persona):
    def __init__(self, nombre, edad, carrera):
        super().__init__(nombre, edad)
        self.carrera = carrera

    def presentarse(self):
        return f"Hola, mi nombre es {self.nombre}, tengo {self.edad} años y estudio {self.carrera}."

ana = Estudiante("Ana", 20, "Ingeniería")
print(ana.presentarse())
```

La Programación Orientada a Objetos es una herramienta esencial en el arsenal de un programador, ya que facilita la organización, reutilización y escalabilidad del código.