## 1. ¿Qué es Javadoc?

Javadoc es una herramienta utilizada para generar documentación API en formato HTML a partir del código fuente Java. La documentación se extrae de comentarios especiales dentro del código, conocidos como comentarios Javadoc.

## 2. Cómo escribir comentarios Javadoc

Los comentarios Javadoc se colocan justo antes de la declaración de clases, interfaces, métodos, y campos. Utilizan la sintaxis especial `/** ... */`.

### 2.1. Comentarios básicos

```java
/**
 * Esta clase representa un vehículo.
 */
public class Vehiculo {
    /**
     * El modelo del vehículo.
     */
    private String modelo;

    /**
     * Establece el modelo del vehículo.
     * 
     * @param modelo El modelo a establecer.
     */
    public void setModelo(String modelo) {
        this.modelo = modelo;
    }

    /**
     * Obtiene el modelo del vehículo.
     * 
     * @return El modelo del vehículo.
     */
    public String getModelo() {
        return modelo;
    }
}
```

### 2.2. Etiquetas Javadoc

- `@author` - Para indicar el autor del código.
- `@version` - Para indicar la versión del código.
- `@param` - Para describir un parámetro de un método.
- `@return` - Para describir el valor de retorno de un método.
- `@throws` o `@exception` - Para describir las excepciones que un método puede lanzar.
- `@see` - Para referencias adicionales.
- `@deprecated` - Para marcar un elemento que está obsoleto.

Ejemplo:

```java
/**
 * Esta clase realiza operaciones matemáticas.
 * 
 * @author Juan Pérez
 * @version 1.0
 */
public class Matematicas {
    /**
     * Suma dos números.
     * 
     * @param a El primer número.
     * @param b El segundo número.
     * @return La suma de a y b.
     */
    public int sumar(int a, int b) {
        return a + b;
    }

    /**
     * Resta dos números.
     * 
     * @param a El primer número.
     * @param b El segundo número.
     * @return La resta de b de a.
     * @throws IllegalArgumentException si b es mayor que a.
     */
    public int restar(int a, int b) {
        if (b > a) {
            throw new IllegalArgumentException("b no puede ser mayor que a");
        }
        return a - b;
    }
}
```

## 3. Generar la documentación con Javadoc

### 3.1. Usar el comando `javadoc`

Para generar la documentación Javadoc, usa el comando `javadoc` seguido de las opciones y los archivos de origen.

```bash
javadoc -d doc -sourcepath src com.miempresa.miapp
```

- `-d` especifica el directorio donde se generará la documentación.
- `-sourcepath` especifica la ruta al código fuente.
- `com.miempresa.miapp` especifica el paquete para documentar.

### 3.2. Ejemplo práctico

Supongamos que tienes el siguiente árbol de directorios:

```
miapp/
├── src/
│   └── com/
│       └── miempresa/
│           └── miapp/
│               ├── Matematicas.java
│               └── Vehiculo.java
└── doc/
```

Para generar la documentación, navega hasta el directorio `miapp` y ejecuta:

```bash
javadoc -d doc -sourcepath src com.miempresa.miapp
```

Esto generará la documentación HTML en el directorio `doc`.

### 3.3. Opciones útiles de Javadoc

- `-author` - Incluye las etiquetas `@author` en la salida.
- `-version` - Incluye las etiquetas `@version` en la salida.
- `-private` - Documenta también los miembros privados.
- `-noindex` - No genera el índice de todas las clases y paquetes.

## 4. Navegar la documentación generada

Después de generar la documentación, abre el archivo `index.html` en el directorio `doc` con un navegador web para ver la documentación generada.

## 5. Buenas prácticas

- Escribe comentarios claros y concisos.
- Usa etiquetas adecuadas para mejorar la claridad de la documentación.
- Documenta todos los elementos públicos y protegidos.
- Mantén la documentación actualizada con los cambios en el código.

¡Y eso es todo! Ahora deberías tener una buena comprensión de cómo utilizar Javadoc para documentar tu código Java.
# Ejemplo de manual de la Clase `Calculadora`

La clase `Calculadora` proporciona métodos para realizar operaciones aritméticas básicas como suma, resta, multiplicación y división. Este manual detalla la funcionalidad de cada método, sus parámetros, valores de retorno y ejemplos de uso.

## Índice

1. [Descripción de la Clase](#descripción-de-la-clase)
2. [Métodos](#métodos)
    - [sumar](#sumarint-a-int-b)
    - [restar](#restarint-a-int-b)
    - [multiplicar](#multiplicarint-a-int-b)
    - [dividir](#dividirint-a-int-b)

## Descripción de la Clase

La clase `Calculadora` es una utilidad para realizar operaciones aritméticas básicas. Cada método de la clase toma dos números enteros como parámetros y devuelve el resultado de la operación aritmética correspondiente.

## Métodos

### `int sumar(int a, int b)`

Suma dos números enteros y devuelve el resultado.

**Parámetros:**
- `int a`: El primer número a sumar.
- `int b`: El segundo número a sumar.

**Retorna:**
- `int`: La suma de `a` y `b`.

**Ejemplo:**
```java
Calculadora calc = new Calculadora();
int resultado = calc.sumar(5, 3); // resultado es 8
```

### `int restar(int a, int b)`

Resta el segundo número del primero y devuelve el resultado.

**Parámetros:**
- `int a`: El número del que se va a restar.
- `int b`: El número que se va a restar.

**Retorna:**
- `int`: La resta de `b` a `a`.

**Ejemplo:**
```java
Calculadora calc = new Calculadora();
int resultado = calc.restar(5, 3); // resultado es 2
```

### `int multiplicar(int a, int b)`

Multiplica dos números enteros y devuelve el resultado.

**Parámetros:**
- `int a`: El primer número a multiplicar.
- `int b`: El segundo número a multiplicar.

**Retorna:**
- `int`: El producto de `a` y `b`.

**Ejemplo:**
```java
Calculadora calc = new Calculadora();
int resultado = calc.multiplicar(5, 3); // resultado es 15
```

### `int dividir(int a, int b)`

Divide el primer número por el segundo y devuelve el resultado. Si el divisor es cero, lanza una excepción.

**Parámetros:**
- `int a`: El numerador.
- `int b`: El denominador.

**Retorna:**
- `int`: El cociente de la división de `a` entre `b`.

**Excepciones:**
- `ArithmeticException`: Si `b` es 0.

**Ejemplo:**
```java
Calculadora calc = new Calculadora();
int resultado = calc.dividir(6, 3); // resultado es 2
```

**Nota:** Lanza `ArithmeticException` si `b` es 0.

---

Este manual proporciona una visión general de los métodos disponibles en la clase `Calculadora`, detallando su uso y proporcionando ejemplos claros. Esto debería ser útil para cualquier persona que necesite entender o utilizar esta clase en sus proyectos.
```

Este manual sigue una estructura clara y organizada, proporcionando toda la información necesaria para entender y utilizar la clase `Calculadora` de manera efectiva.