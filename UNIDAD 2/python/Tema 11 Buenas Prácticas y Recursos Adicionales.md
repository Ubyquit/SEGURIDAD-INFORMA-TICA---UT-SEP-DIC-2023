#### **1. Estilo de código y PEP 8**

El PEP 8 es la guía de estilo para escribir código en Python. Adherirse a esta guía ayuda a los programadores a escribir código que sea legible y fácil de entender.

**Puntos clave:**

- Utiliza 4 espacios por nivel de indentación.
- Limita las líneas a 79 caracteres para el código y 72 para los comentarios.
- Utiliza líneas en blanco para separar funciones y definiciones de clases.
- No uses espacios alrededor de los paréntesis, corchetes o llaves.
- Usa espacios alrededor de operadores y después de las comas.

#### **2. Herramientas útiles:**

- **IDEs**: Herramientas como PyCharm, Visual Studio Code o Atom ofrecen funciones avanzadas para escribir y depurar código Python.

- **Entornos Virtuales**: Las herramientas como `virtualenv` permiten crear entornos aislados para gestionar dependencias. Esto es especialmente útil para proyectos con requerimientos específicos.

  ```bash
  pip install virtualenv
  virtualenv mi_entorno
  source mi_entorno/bin/activate  # En sistemas basados en Unix
  mi_entorno\Scripts\activate  # En Windows
  ```

- **pip**: Es el sistema de gestión de paquetes de Python. Con `pip` puedes instalar y gestionar bibliotecas adicionales.

  ```bash
  pip install paquete_deseado
  ```

#### **3. Recursos para aprender más sobre Python y criptografía**

- **Documentación oficial de Python**: Aquí puedes encontrar toda la información sobre las funciones, módulos y características del lenguaje.
  
- **Real Python**: Ofrece tutoriales, artículos y recursos para aprender Python en profundidad.

- **Cryptography.io**: Documentación de la biblioteca `cryptography` para Python. Es una fuente esencial para entender y utilizar las funciones de criptografía de alto nivel en Python.

- **Project Euler**: Serie de problemas matemáticos y computacionales que requieren soluciones creativas usando programación. Es un recurso excelente para practicar habilidades de programación y criptografía.

---

**Ejercicio práctico 1:** Configura un entorno virtual y dentro de él instala la biblioteca `cryptography`. Comprueba que la biblioteca funciona correctamente dentro del entorno.

**Ejercicio práctico 2:** Elije un script o programa Python que hayas escrito anteriormente (o uno nuevo) y revísalo para asegurarte de que sigue las directrices del PEP 8. Puedes usar herramientas en línea como "PEP 8 online" para verificarlo.

**Ejercicio práctico 3:** Explora la documentación de `cryptography.io` y familiarízate con al menos tres funciones o módulos que aún no hayas estudiado.