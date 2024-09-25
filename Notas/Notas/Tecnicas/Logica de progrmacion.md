#Programación #escuela

- **Definición**: La lógica de programación es el conjunto de principios y técnicas utilizados para resolver problemas y construir algoritmos en el ámbito de la programación.
- **Objetivo**: Desarrollar habilidades para descomponer problemas complejos en pasos secuenciales y lógicos que una computadora pueda ejecutar.

## Conceptos Básicos

### Algoritmos
- **Definición**: Un algoritmo es una secuencia finita de pasos bien definidos para resolver un problema o realizar una tarea específica.
- **Características**:
  - **Finito**: Debe tener un número limitado de pasos.
  - **Definido**: Cada paso debe estar claramente especificado.
  - **Efectivo**: Debe resolver el problema con precisión.
- **Ejemplo**:
  ```python
  # Algoritmo para sumar los primeros n números naturales
  def sum_first_n_numbers(n):
      total = 0
      for i in range(1, n + 1):
          total += i
      return total
  ```

### Pseudocódigo
- **Definición**: El pseudocódigo es una representación informal de un algoritmo, utilizando una mezcla de lenguaje natural y estructuras de control de programación.
- **Ejemplo**:
  ```plaintext
  INICIO
  DEFINIR n COMO ENTERO
  DEFINIR total COMO ENTERO
  total = 0
  PARA i DESDE 1 HASTA n HACER
      total = total + i
  FIN PARA
  IMPRIMIR total
  FIN
  ```

### Diagramas de flujo
- **Definición**: Un diagrama de flujo es una representación gráfica de un algoritmo, donde se utilizan diferentes símbolos para representar operaciones y el flujo de control.
- **Símbolos comunes**:
  - **Óvalo**: Inicio/Fin.
  - **Rectángulo**: Proceso.
  - **Rombo**: Decisión.
  - **Flechas**: Flujo de control.

### Estructuras de Control en Programación

#### 1. **Estructuras de Control**
- **Definición:** Las estructuras de control determinan el flujo de ejecución de un programa.
- **Tipos Principales:**
  - Estructuras de control condicionales
  - Estructuras de control iterativas
  - Estructuras de control de selección múltiple

#### 2. **Estructuras de Control Condicionales**
- **If-Else:**
  - **Sintaxis Básica:**
    ```python
    if condición:
        # Código a ejecutar si la condición es verdadera
    else:
        # Código a ejecutar si la condición es falsa
    ```
  - **Ejemplo:**
    ```python
    edad = 18
    if edad >= 18:
        print("Eres mayor de edad.")
    else:
        print("Eres menor de edad.")
    ```
- **Elif:**
  - **Sintaxis Básica:**
    ```python
    if condición1:
        # Código si condición1 es verdadera
    elif condición2:
        # Código si condición2 es verdadera
    else:
        # Código si ninguna condición es verdadera
    ```
  - **Ejemplo:**
    ```python
    nota = 85
    if nota >= 90:
        print("A")
    elif nota >= 80:
        print("B")
    elif nota >= 70:
        print("C")
    else:
        print("F")
    ```

#### 3. **Estructuras de Control Iterativas**
- **While:**
  - **Sintaxis Básica:**
    ```python
    while condición:
        # Código a ejecutar mientras la condición sea verdadera
    ```
  - **Ejemplo:**
    ```python
    i = 1
    while i <= 5:
        print(i)
        i += 1
    ```
- **For:**
  - **Sintaxis Básica:**
    ```python
    for variable in secuencia:
        # Código a ejecutar para cada elemento en la secuencia
    ```
  - **Ejemplo:**
    ```python
    for i in range(1, 6):
        print(i)
    ```

#### 4. **Estructuras de Control de Selección Múltiple**
- **Switch-Case (Disponible en algunos lenguajes como C, C++):**
  - **Sintaxis Básica:**
    ```c
    switch (variable) {
        case valor1:
            // Código a ejecutar si variable == valor1
            break;
        case valor2:
            // Código a ejecutar si variable == valor2
            break;
        default:
            // Código a ejecutar si variable no coincide con ningún caso
    }
    ```
  - **Ejemplo:**
    ```c
    int dia = 3;
    switch (dia) {
        case 1:
            printf("Lunes");
            break;
        case 2:
            printf("Martes");
            break;
        case 3:
            printf("Miércoles");
            break;
        default:
            printf("Otro día");
    }
    ```
- **Equivalente en Python (Usando Diccionarios y Funciones):**
  - **Ejemplo:**
    ```python
    def lunes():
        return "Lunes"
    
    def martes():
        return "Martes"
    
    def miercoles():
        return "Miércoles"
    
    def otro_dia():
        return "Otro día"
    
    switch = {
        1: lunes,
        2: martes,
        3: miercoles
    }
    
    dia = 3
    print(switch.get(dia, otro_dia)())
    ```

#### 5. **Bucles Anidados**
- **Descripción:** Bucles dentro de otros bucles.
- **Ejemplo:**
  ```python
  for i in range(1, 4):
      for j in range(1, 4):
          print(f"i={i}, j={j}")
  ```

Las funciones y procedimientos son bloques de código reutilizables en programación que permiten estructurar y organizar mejor el código. A continuación, te proporcionaré una guía detallada para comprender y utilizar funciones y procedimientos.

### Funciones y Procedimientos en Programación

#### 1. **Funciones y Procedimientos**
- **Definición:**
  - **Funciones:** Bloques de código que realizan una tarea específica y pueden devolver un valor.
  - **Procedimientos:** Bloques de código que realizan una tarea específica pero no devuelven un valor (también llamados subrutinas o métodos en algunos lenguajes).

- **Ventajas:**
  - Reutilización de código.
  - Mejora de la legibilidad y mantenimiento del código.
  - Modularización del programa.

#### 2. **Definición y Llamada de Funciones**
- **Sintaxis Básica (Python):**
  ```python
  def nombre_funcion(parámetros):
      # Cuerpo de la función
      return valor_de_retorno
  ```

- **Ejemplo:**
  ```python
  def suma(a, b):
      return a + b

  resultado = suma(5, 3)
  print(resultado)  # Salida: 8
  ```

- **Notas:**
  - **Parámetros:** Variables que se pasan a la función.
  - **Valor de Retorno:** El resultado que la función devuelve.

#### 3. **Definición y Llamada de Procedimientos**
- **Sintaxis Básica (Python):**
  ```python
  def nombre_procedimiento(parámetros):
      # Cuerpo del procedimiento
      # No hay valor de retorno
  ```

- **Ejemplo:**
  ```python
  def imprimir_suma(a, b):
      print(a + b)

  imprimir_suma(5, 3)  # Salida: 8
  ```

- **Notas:**
  - No devuelven valores explícitamente, aunque pueden modificar variables globales o realizar acciones como imprimir en pantalla.

#### 4. **Parámetros y Argumentos**
- **Parámetros Posicionales:**
  - Se pasan en el orden en que se definen.
  - **Ejemplo:**
    ```python
    def saludo(nombre, edad):
        print(f"Hola {nombre}, tienes {edad} años.")

    saludo("Juan", 25)  # Salida: Hola Juan, tienes 25 años.
    ```

- **Parámetros Nombrados:**
  - Se pasan especificando el nombre del parámetro.
  - **Ejemplo:**
    ```python
    saludo(nombre="Juan", edad=25)  # Salida: Hola Juan, tienes 25 años.
    ```

- **Valores por Defecto:**
  - Se pueden asignar valores por defecto a los parámetros.
  - **Ejemplo:**
    ```python
    def saludo(nombre, edad=18):
        print(f"Hola {nombre}, tienes {edad} años.")

    saludo("Juan")  # Salida: Hola Juan, tienes 18 años.
    saludo("Pedro", 22)  # Salida: Hola Pedro, tienes 22 años.
    ```

#### 5. **Ámbito de las Variables**
- **Variables Locales:**
  - Declaradas dentro de una función o procedimiento.
  - Sólo accesibles dentro de esa función o procedimiento.
  - **Ejemplo:**
    ```python
    def funcion():
        variable_local = 10
        print(variable_local)

    funcion()  # Salida: 10
    print(variable_local)  # Error: variable_local no está definida
    ```

- **Variables Globales:**
  - Declaradas fuera de cualquier función o procedimiento.
  - Accesibles desde cualquier parte del programa.
  - **Ejemplo:**
    ```python
    variable_global = 20

    def funcion():
        print(variable_global)

    funcion()  # Salida: 20
    ```

#### 6. **Funciones y Procedimientos Recursivos**
- **Definición:** Una función o procedimiento que se llama a sí mismo.
- **Ejemplo de Función Recursiva:**
  ```python
  def factorial(n):
      if n == 0:
          return 1
      else:
          return n * factorial(n - 1)

  print(factorial(5))  # Salida: 120
  ```

- **Ejemplo de Procedimiento Recursivo:**
  ```python
  def cuenta_regresiva(n):
      if n > 0:
          print(n)
          cuenta_regresiva(n - 1)
      else:
          print("¡Despegue!")

  cuenta_regresiva(5)
  ```

#### 7. **Ejercicios Prácticos**
- **Ejercicio 1:** Escribir una función que calcule el área de un círculo dado su radio.
- **Ejercicio 2:** Escribir un procedimiento que imprima todos los elementos de una lista.
- **Ejercicio 3:** Crear una función recursiva para calcular el n-ésimo número de Fibonacci.



### Ejemplo de Documentación de Función

```python
def calcular_area_circulo(radio):
    """
    Calcula el área de un círculo dado su radio.

    Parámetros:
    radio (float): El radio del círculo.

    Retorna:
    float: El área del círculo.
    """
    from math import pi
    return pi * radio ** 2

# Llamada a la función
print(calcular_area_circulo(5))  # Salida: 78.53981633974483
```

### Listas y Arrays
- **Definición**: Una lista es una colección ordenada de elementos.
- **Ejemplo**:
  ```python
  lista = [1, 2, 3, 4, 5]
  print(lista[2])  # Salida: 3
  ```

### Tuplas
- **Definición**: Una tupla es una colección ordenada de elementos inmutables.
- **Ejemplo**:
  ```python
  tupla = (1, 2, 3, 4, 5)
  print(tupla[2])  # Salida: 3
  ```

### Diccionarios
- **Definición**: Un diccionario es una colección de pares clave-valor.
- **Ejemplo**:
  ```python
  diccionario = {"nombre": "Juan", "edad": 30}
  print(diccionario["nombre"])  # Salida: Juan
  ```

## Ejemplos Prácticos

### Búsqueda Lineal
- **Descripción**: Busca un elemento en una lista recorriéndola secuencialmente.
- **Ejemplo**:
  ```python
  def busqueda_lineal(lista, objetivo):
      for i in range(len(lista)):
          if lista[i] == objetivo:
              return i
      return -1

  lista = [1, 2, 3, 4, 5]
  print(busqueda_lineal(lista, 3))  # Salida: 2
  ```

### Ordenamiento Burbuja
- **Descripción**: Algoritmo de ordenamiento simple que intercambia elementos adyacentes si están en el orden incorrecto.
- **Ejemplo**:
  ```python
  def ordenamiento_burbuja(lista):
      n = len(lista)
      for i in range(n):
          for j in range(0, n-i-1):
              if lista[j] > lista[j+1]:
                  lista[j], lista[j+1] = lista[j+1], lista[j]
      return lista

  lista = [64, 34, 25, 12, 22, 11, 90]
  print(ordenamiento_burbuja(lista))  # Salida: [11, 12, 22, 25, 34, 64, 90]
  ```

## Prácticas Recomendadas
- **Dividir y Vencer**: Dividir el problema en subproblemas más pequeños.
- **Refactorización**: Mejorar continuamente el código para hacerlo más limpio y eficiente.
- **Pruebas**: Escribir pruebas para asegurar que el código funciona correctamente.
- **Documentación**: Documentar el código para facilitar su comprensión y mantenimiento.
