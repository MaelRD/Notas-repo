#Programación en python
# Programación en Python

## Introducción

Python es un lenguaje de programación de alto nivel, interpretado y de propósito general, conocido por su sintaxis clara y concisa. Fue creado por Guido van Rossum y lanzado por primera vez en 1991. Python se utiliza en una variedad de aplicaciones, desde desarrollo web hasta análisis de datos y aprendizaje automático.

### Características Principales

- **Fácil de Leer y Escribir**: Sintaxis sencilla y clara.
- **Interpretado**: No requiere compilación.
- **Portabilidad**: Funciona en múltiples plataformas como Windows, macOS y Linux.
- **Gran Ecosistema de Bibliotecas**: Amplio soporte de bibliotecas y frameworks.
- **Multiparadigma**: Soporta programación orientada a objetos, imperativa y funcional.

---

### Sintaxis Básica en Python

## Introducción

Python es un lenguaje de programación de alto nivel, interpretado y de propósito general, conocido por su sintaxis sencilla y su legibilidad. Estas notas cubren los aspectos básicos de la sintaxis de Python.

---

### Variables y Tipos de Datos en Python

#### Variables

En Python, no es necesario declarar el tipo de una variable, ya que Python es un lenguaje de tipado dinámico.

```python
x = 5          # entero
y = 3.14       # flotante
nombre = "Ana" # cadena
es_mayor = True # booleano
```

#### Tipos de Datos Comunes

- **int**: Enteros
- **float**: Números de punto flotante
- **str**: Cadenas de texto
- **bool**: Booleanos (`True` o `False`)

#### Conversión de Tipos

```python
x = 5
y = float(x)  # convierte entero a flotante
z = str(x)    # convierte entero a cadena
```

---

### Operadores en Python

#### Operadores Aritméticos

```python
a = 10
b = 3
print(a + b)  # suma
print(a - b)  # resta
print(a * b)  # multiplicación
print(a / b)  # división
print(a // b) # división entera
print(a % b)  # módulo
print(a ** b) # potencia
```

#### Operadores de Comparación

```python
print(a == b)  # igual
print(a != b)  # distinto
print(a > b)   # mayor que
print(a < b)   # menor que
print(a >= b)  # mayor o igual que
print(a <= b)  # menor o igual que
```

#### Operadores Lógicos

```python
print(True and False) # y lógico
print(True or False)  # o lógico
print(not True)       # negación lógica
```

---

### Estructuras de Control en Python

#### Condicionales If...Else

```python
edad = 18

if edad >= 18:
    print("Eres mayor de edad.")
else:
    print("Eres menor de edad.")
```

#### Bucles For

```python
for i in range(5):
    print(i)
```

#### Bucles While

```python
i = 0
while i < 5:
    print(i)
    i += 1
```

---

### Funciones en Python

#### Definición y Llamado de Funciones

```python
def saludar(nombre):
    return f"Hola, {nombre}"

print(saludar("Ana"))
```

#### Funciones con Múltiples Parámetros

```python
def sumar(a, b):
    return a + b

print(sumar(3, 4))
```

#### Parámetros por Defecto

```python
def saludar(nombre="Mundo"):
    return f"Hola, {nombre}"

print(saludar())
print(saludar("Ana"))
```

---

### Listas y Otros Contenedores en Python

#### Listas

```python
frutas = ["manzana", "banana", "cereza"]
print(frutas[0])  # acceso por índice
frutas.append("naranja")  # agregar elemento
print(frutas)
```

#### Tuplas

```python
punto = (1, 2)
print(punto[0])  # acceso por índice
```

#### Diccionarios

```python
persona = {"nombre": "Ana", "edad": 30}
print(persona["nombre"])  # acceso por clave
persona["edad"] = 31  # modificar valor
print(persona)
```

---

### Manejo de Excepciones en Python

#### Bloques Try...Except

```python
try:
    x = 1 / 0
except ZeroDivisionError:
    print("No se puede dividir por cero.")
```

#### Bloque Finally

```python
try:
    x = 1 / 0
except ZeroDivisionError:
    print("No se puede dividir por cero.")
finally:
    print("Este bloque se ejecuta siempre.")
```

---

### Entrada/Salida (I/O) en Python

#### Entrada de Datos

```python
nombre = input("¿Cuál es tu nombre? ")
print(f"Hola, {nombre}")
```

#### Lectura de Archivos

```python
with open("archivo.txt", "r") as archivo:
    contenido = archivo.read()
    print(contenido)
```

#### Escritura de Archivos

```python
with open("archivo.txt", "w") as archivo:
    archivo.write("Hola, mundo")
```

---

### Módulos y Paquetes en Python

#### Importar Módulos

```python
import math
print(math.sqrt(16))
```

#### Importar Funciones Específicas

```python
from math import sqrt
print(sqrt(16))
```

#### Creación de Módulos Propios

Crea un archivo `mimodulo.py`:

```python
def saludar(nombre):
    return f"Hola, {nombre}"
```

Importa y usa el módulo:

```python
import mimodulo
print(mimodulo.saludar("Ana"))
```

---

### Estructuras de Control en Python

Python soporta estructuras de control como condicionales y bucles.

#### Condicional If...Else:

```python
edad = 20

if edad >= 18:
    print("Eres mayor de edad.")
else:
    print("Eres menor de edad.")
```

#### Bucles For:

```python
for i in range(10):
    print(i)
```

#### Bucles While:

```python
i = 0

while i < 10:
    print(i)
    i += 1
```

[[Programación en Python]]

---

### Funciones en Python

Las funciones en Python se definen con la palabra clave `def`.

#### Ejemplo de Función:

```python
def saludar(nombre):
    return f"¡Hola, {nombre}!"

print(saludar("Juan"))
```

#### Funciones Lambda:

```python
suma = lambda a, b: a + b
print(suma(5, 3))
```

[[Programación en Python]]

---

### Manejo de Listas y Diccionarios en Python

#### Listas

Las listas son colecciones ordenadas y mutables.

```python
numeros = [1, 2, 3, 4, 5]

# Acceso a elementos
print(numeros[0])  # Imprime 1

# Añadir elementos
numeros.append(6)

# Eliminar elementos
numeros.remove(3)

# Recorrer lista
for num in numeros:
    print(num)
```

#### Diccionarios

Los diccionarios son colecciones desordenadas de pares clave-valor.

```python
persona = {"nombre": "Juan", "edad": 25}

# Acceso a elementos
print(persona["nombre"])  # Imprime "Juan"

# Añadir elementos
persona["altura"] = 1.75

# Eliminar elementos
del persona["edad"]

# Recorrer diccionario
for clave, valor in persona.items():
    print(f"{clave}: {valor}")
```

[[Programación en Python]]

---

### Manejo de Archivos en Python

Python proporciona varias funciones para manejar archivos a través del módulo `open`.

#### Leer un Archivo:

```python
with open('archivo.txt', 'r') as archivo:
    contenido = archivo.read()
    print(contenido)
```

#### Escribir en un Archivo:

```python
with open('archivo.txt', 'w') as archivo:
    archivo.write("¡Hola, mundo!")
```

[[Programación en Python]]

---

### Programación Orientada a Objetos en Python

Python soporta programación orientada a objetos (POO), permitiendo la definición de clases y objetos.

#### Definición de Clases y Objetos:

```python
class Persona:
    def __init__(self, nombre, edad):
        self.nombre = nombre
        self.edad = edad

    def saludar(self):
        return f"Hola, me llamo {self.nombre} y tengo {self.edad} años."

# Crear objeto
juan = Persona("Juan", 25)
print(juan.saludar())
```

#### Herencia:

```python
class Animal:
    def __init__(self, nombre):
        self.nombre = nombre

    def hacer_sonido(self):
        return "El animal hace un sonido."

class Perro(Animal):
    def hacer_sonido(self):
        return "El perro ladra."

perro = Perro("Firulais")
print(perro.hacer_sonido())
```

[[Programación en Python]]

---

### Bibliotecas Comunes en Python

Python tiene un ecosistema rico de bibliotecas para diversas aplicaciones.

#### Numpy

Para computación numérica y manipulación de arrays.

```python
import numpy as np

a = np.array([1, 2, 3])
print(a * 2)
```

#### Pandas

Para manipulación y análisis de datos.

```python
import pandas as pd

data = {'Nombre': ['Juan', 'Ana'], 'Edad': [25, 30]}
df = pd.DataFrame(data)
print(df)
```

#### Matplotlib

Para visualización de datos.

```python
import matplotlib.pyplot as plt

plt.plot([1, 2, 3], [4, 5, 6])
plt.show()
```

#### Requests

Para hacer peticiones HTTP.

```python
import requests

response = requests.get('https://api.example.com/data')
print(response.json())
```

Claro, aquí tienes una visión general de algunos métodos comunes de cadenas (strings) en Python:

### Métodos Básicos de Cadenas

1. **`capitalize()`**: Convierte el primer carácter de la cadena a mayúsculas y el resto a minúsculas.
   ```python
   texto = "hola mundo"
   print(texto.capitalize())  # "Hola mundo"
   ```

2. **`lower()`**: Convierte todos los caracteres de la cadena a minúsculas.
   ```python
   texto = "HELLO WORLD"
   print(texto.lower())  # "hello world"
   ```

3. **`upper()`**: Convierte todos los caracteres de la cadena a mayúsculas.
   ```python
   texto = "hello world"
   print(texto.upper())  # "HELLO WORLD"
   ```

4. **`title()`**: Convierte el primer carácter de cada palabra a mayúsculas.
   ```python
   texto = "hola mundo"
   print(texto.title())  # "Hola Mundo"
   ```

5. **`strip()`**: Elimina los espacios en blanco al principio y al final de la cadena.
   ```python
   texto = "   hola mundo   "
   print(texto.strip())  # "hola mundo"
   ```

6. **`lstrip()`**: Elimina los espacios en blanco al principio de la cadena.
   ```python
   texto = "   hola mundo"
   print(texto.lstrip())  # "hola mundo"
   ```

7. **`rstrip()`**: Elimina los espacios en blanco al final de la cadena.
   ```python
   texto = "hola mundo   "
   print(texto.rstrip())  # "hola mundo"
   ```

8. **`replace(old, new)`**: Reemplaza todas las ocurrencias de `old` con `new`.
   ```python
   texto = "hola mundo"
   print(texto.replace("mundo", "universo"))  # "hola universo"
   ```

9. **`find(sub)`**: Devuelve el índice de la primera aparición de la subcadena `sub`. Devuelve `-1` si no se encuentra.
   ```python
   texto = "hola mundo"
   print(texto.find("mundo"))  # 5
   ```

10. **`rfind(sub)`**: Devuelve el índice de la última aparición de la subcadena `sub`. Devuelve `-1` si no se encuentra.
    ```python
    texto = "hola mundo mundo"
    print(texto.rfind("mundo"))  # 10
    ```

11. **`split(sep)`**: Divide la cadena en una lista de subcadenas utilizando el separador `sep`.
    ```python
    texto = "hola mundo"
    print(texto.split(" "))  # ['hola', 'mundo']
    ```

12. **`join(iterable)`**: Une los elementos de un iterable en una cadena, separados por la cadena que llama al método.
    ```python
    lista = ["hola", "mundo"]
    print(" ".join(lista))  # "hola mundo"
    ```

13. **`isdigit()`**: Devuelve `True` si todos los caracteres en la cadena son dígitos.
    ```python
    texto = "12345"
    print(texto.isdigit())  # True
    ```

14. **`isalpha()`**: Devuelve `True` si todos los caracteres en la cadena son letras.
    ```python
    texto = "hello"
    print(texto.isalpha())  # True
    ```

15. **`startswith(prefix)`**: Devuelve `True` si la cadena comienza con el prefijo `prefix`.
    ```python
    texto = "hola mundo"
    print(texto.startswith("hola"))  # True
    ```

16. **`endswith(suffix)`**: Devuelve `True` si la cadena termina con el sufijo `suffix`.
    ```python
    texto = "hola mundo"
    print(texto.endswith("mundo"))  # True
    ```

### Ejemplo de Uso

```python
texto = "  Hola, Mundo!  "

# Convertir a mayúsculas
print(texto.upper())  # "  HOLA, MUNDO!  "

# Quitar espacios
print(texto.strip())  # "Hola, Mundo!"

# Reemplazar palabras
print(texto.replace("Mundo", "Python"))  # "  Hola, Python!  "

# Dividir en palabras
print(texto.split(", "))  # ['  Hola', 'Mundo!  ']

# Unir con separador
print(" - ".join(["Hola", "Mundo!"]))  # "Hola - Mundo!"
```

Estos métodos son útiles para manipular y trabajar con cadenas de texto en Python.

Ejercicios:
https://aprendeconalf.es/docencia/python/ejercicios/tipos-datos/