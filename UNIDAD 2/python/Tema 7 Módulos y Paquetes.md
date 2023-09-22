En Python, a medida que los programas crecen, es esencial organizar y modularizar el código. Los módulos y paquetes son herramientas que facilitan esta organización.

#### **1. Módulos**

Un módulo es simplemente un archivo que contiene definiciones y declaraciones de Python. El nombre del archivo es el nombre del módulo con el sufijo `.py` añadido.

**Ejemplo:**

Supongamos que tienes un archivo llamado `operaciones.py` con el siguiente contenido:

```python
def suma(a, b):
    return a + b

def resta(a, b):
    return a - b
```

Puedes usar las funciones definidas en el módulo `operaciones` de la siguiente manera:

```python
import operaciones

resultado = operaciones.suma(5, 3)
print(resultado)  # Imprimirá 8
```

#### **2. Importación de Módulos**

Existen varias maneras de importar módulos:

**a) Importación completa:**

```python
import operaciones
```

**b) Importación de funciones específicas:**

```python
from operaciones import suma, resta
```

**c) Renombrar módulos o funciones al importar:**

```python
import operaciones as ops
```

o

```python
from operaciones import suma as add
```

#### **3. Paquetes**

Un paquete es una forma de organizar módulos relacionados en un único directorio. Esencialmente, es un directorio que contiene un archivo especial llamado `__init__.py` (que puede estar vacío) y uno o más módulos.

**Ejemplo de estructura de paquete:**

```
mipaquete/
│
├─ __init__.py
├─ modulo1.py
└─ modulo2.py
```

Para importar módulos desde un paquete:

```python
from mipaquete import modulo1
```

---

**Ejercicio práctico 1:** Crea un módulo llamado `calculos` que contenga funciones para calcular el área de diferentes figuras geométricas. Luego, importa ese módulo y utiliza sus funciones.

*calculos.py:*
```python
def area_rectangulo(largo, ancho):
    return largo * ancho

def area_circulo(radio):
    import math
    return math.pi * radio * radio
```

*programa_principal.py:*
```python
from calculos import area_rectangulo, area_circulo

print(area_rectangulo(5, 3))  # Imprimirá 15
print(area_circulo(7))       # Imprimirá aproximadamente 153.93804002589985
```

**Ejercicio práctico 2:** Crea un paquete llamado `matematicas` con módulos separados para operaciones básicas y avanzadas. Luego, utiliza funciones de ambos módulos.

Con el manejo de módulos y paquetes, los desarrolladores pueden estructurar sus proyectos de Python de manera más clara, facilitando la mantenibilidad y escalabilidad del código.