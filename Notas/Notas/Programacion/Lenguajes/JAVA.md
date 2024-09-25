#Programación en java 
# Programación en Java

## Introducción

Java es un lenguaje de programación de propósito general, concurrente, orientado a objetos y basado en clases, diseñado para tener las menores dependencias de implementación posibles. Fue desarrollado por Sun Microsystems (ahora parte de Oracle Corporation) y lanzado en 1995. Java es conocido por su portabilidad, lo que significa que los programas escritos en Java pueden ejecutarse en cualquier dispositivo que tenga la Máquina Virtual Java (JVM).

### Características Principales

- **Orientado a Objetos**: Facilita la creación de programas modulares y reutilizables.
- **Portabilidad**: "Escribe una vez, ejecuta en cualquier lugar" gracias a la JVM.
- **Seguridad**: Proporciona un entorno seguro para ejecutar aplicaciones.
- **Multihilo**: Permite el desarrollo de aplicaciones con múltiples hilos de ejecución.
- **Bibliotecas Estándar Ricas**: Amplia colección de bibliotecas estándar y de terceros.

---


# Sintaxis de Java 


## 1. Estructura Básica de un Programa en Java

Un programa en Java consiste en clases y métodos. La estructura básica es la siguiente:

```java
// Definimos una clase pública llamada MiPrograma.
public class MiPrograma {
    // El método principal, punto de entrada del programa.
    public static void main(String[] args) {
        // Imprime "Hola, Mundo!" en la consola.
        System.out.println("Hola, Mundo!");
    }
}
```

### Explicación:
- `public class MiPrograma`: Declara una clase pública llamada `MiPrograma`. En Java, todo el código debe estar dentro de una clase.
- `public static void main(String[] args)`: Este es el punto de entrada del programa. `main` es un método especial que se ejecuta cuando el programa empieza.
- `System.out.println("Hola, Mundo!");`: Este comando imprime el texto "Hola, Mundo!" en la consola.

## 3. Tipos de Datos y Variables

### Tipos de Datos Primitivos

```java
// Definimos una variable entera llamada numero y le asignamos el valor 10.
int numero = 10;

// Definimos una variable de punto flotante (decimal) llamada precio y le asignamos el valor 19.99.
double precio = 19.99;

// Definimos una variable de carácter llamada letra y le asignamos el carácter 'A'.
char letra = 'A';

// Definimos una variable booleana llamada esVerdadero y le asignamos el valor true (verdadero).
boolean esVerdadero = true;
```

### Tipos de Datos Referenciados

```java
// Definimos una variable de cadena (texto) llamada saludo y le asignamos el texto "Hola".
String saludo = "Hola";

// Definimos un array (arreglo) de enteros llamado numeros y le asignamos cinco valores.
int[] numeros = {1, 2, 3, 4, 5};
```

## 4. Operadores

### Aritméticos

```java
int suma = 5 + 3;    // La variable suma contiene el valor 8 (5 + 3).
int resta = 5 - 3;   // La variable resta contiene el valor 2 (5 - 3).
int multiplicacion = 5 * 3; // La variable multiplicacion contiene el valor 15 (5 * 3).
double division = 5.0 / 3.0; // La variable division contiene el valor 1.6667 (5 / 3).
int modulo = 5 % 3;  // La variable modulo contiene el valor 2 (el resto de 5 dividido por 3).
```

### Relacionales

```java
boolean esIgual = (5 == 3);    // false, porque 5 no es igual a 3.
boolean esDiferente = (5 != 3); // true, porque 5 es diferente de 3.
boolean esMayor = (5 > 3);     // true, porque 5 es mayor que 3.
boolean esMenor = (5 < 3);     // false, porque 5 no es menor que 3.
```

### Lógicos

```java
boolean y = (true && false);  // false, porque ambos valores no son verdaderos.
boolean o = (true || false);  // true, porque al menos uno de los valores es verdadero.
boolean no = !true;           // false, porque la negación de verdadero es falso.
```

## 5. Estructuras de Control

### Condicionales

#### `if`, `else if`, `else`

```java
int numero = 10;

if (numero > 0) {
    // Este bloque se ejecuta si la condición (numero > 0) es verdadera.
    System.out.println("El número es positivo");
} else if (numero < 0) {
    // Este bloque se ejecuta si la condición anterior es falsa y (numero < 0) es verdadera.
    System.out.println("El número es negativo");
} else {
    // Este bloque se ejecuta si todas las condiciones anteriores son falsas.
    System.out.println("El número es cero");
}
```

#### `switch`

```java
int dia = 2;

switch (dia) {
    case 1:
        // Este bloque se ejecuta si dia es 1.
        System.out.println("Lunes");
        break;
    case 2:
        // Este bloque se ejecuta si dia es 2.
        System.out.println("Martes");
        break;
    case 3:
        // Este bloque se ejecuta si dia es 3.
        System.out.println("Miércoles");
        break;
    default:
        // Este bloque se ejecuta si dia no es ninguno de los casos anteriores.
        System.out.println("Otro día");
        break;
}
```

### Bucles

#### `for`

```java
// Bucle que se ejecuta 5 veces.
for (int i = 0; i < 5; i++) {
    // En cada iteración, imprime el valor de i.
    System.out.println("i es " + i);
}
```

#### `while`

```java
int i = 0;

// Bucle que se ejecuta mientras i sea menor que 5.
while (i < 5) {
    // En cada iteración, imprime el valor de i.
    System.out.println("i es " + i);
    // Incrementa el valor de i en 1.
    i++;
}
```

#### `do-while`

```java
int i = 0;

// Bucle que se ejecuta al menos una vez, y luego mientras i sea menor que 5.
do {
    // En cada iteración, imprime el valor de i.
    System.out.println("i es " + i);
    // Incrementa el valor de i en 1.
    i++;
} while (i < 5);
```

## 6. Clases y Objetos

### Definición de una Clase

```java
// Definimos una clase llamada Persona.
public class Persona {
    // Campos de la clase (variables miembro).
    String nombre;
    int edad;

    // Constructor de la clase.
    public Persona(String nombre, int edad) {
        this.nombre = nombre;  // Asigna el valor del parámetro nombre al campo nombre.
        this.edad = edad;      // Asigna el valor del parámetro edad al campo edad.
    }

    // Método de la clase.
    public void mostrarInfo() {
        // Imprime el nombre y la edad de la persona.
        System.out.println("Nombre: " + nombre + ", Edad: " + edad);
    }
}
```

### Crear Objetos

```java
public class Main {
    public static void main(String[] args) {
        // Crear un objeto de la clase Persona.
        Persona persona1 = new Persona("Juan", 25);
        // Llamar al método mostrarInfo del objeto persona1.
        persona1.mostrarInfo();
    }
}
```

## 7. Herencia

```java
// Clase base (superclase).
public class Animal {
    // Método que hace un sonido.
    public void hacerSonido() {
        System.out.println("El animal hace un sonido");
    }
}

// Clase derivada (subclase) que extiende Animal.
public class Perro extends Animal {
    // Sobrescribe el método hacerSonido de la superclase.
    @Override
    public void hacerSonido() {
        System.out.println("El perro ladra");
    }
}
```

```java
public class Main {
    public static void main(String[] args) {
        // Crear un objeto de la clase Perro.
        Perro perro = new Perro();
        // Llamar al método hacerSonido del objeto perro.
        perro.hacerSonido();  // El perro ladra
    }
}
```

## 8. Interfaces

```java
// Definir una interfaz llamada Animal.
interface Animal {
    // Método abstracto (sin implementación) que hace un sonido.
    void hacerSonido();
}

// Clase Perro que implementa la interfaz Animal.
class Perro implements Animal {
    // Implementar el método hacerSonido de la interfaz Animal.
    @Override
    public void hacerSonido() {
        System.out.println("El perro ladra");
    }
}
```

```java
public class Main {
    public static void main(String[] args) {
        // Crear un objeto de la clase Perro y asignarlo a una variable de tipo Animal.
        Animal perro = new Perro();
        // Llamar al método hacerSonido del objeto perro.
        perro.hacerSonido();  // El perro ladra
    }
}
```

Claro, aquí tienes una explicación detallada del manejo de excepciones en Java, incluyendo el uso de `try`, `catch` y `finally`.

---

## 9. Manejo de Excepciones en Java

### `try`, `catch`, `finally`

El manejo de excepciones en Java permite capturar y manejar errores en tiempo de ejecución de manera controlada. Esto se realiza mediante los bloques `try`, `catch` y `finally`.

#### Ejemplo:

```java
public class EjemploExcepcion {
    public static void main(String[] args) {
        try {
            // Intentar dividir por cero (lo que causará una excepción).
            int resultado = 10 / 0;
        } catch (ArithmeticException e) {
            // Capturar la excepción y mostrar un mensaje.
            System.out.println("Error: División por cero.");
        } finally {
            // Este bloque se ejecuta siempre, haya o no excepción.
            System.out.println("Bloque finally ejecutado.");
        }
    }
}
```

### Explicación del Código:

1. **Bloque `try`**:
    - El código dentro del bloque `try` se ejecuta normalmente.
    - En este caso, intenta realizar una división por cero (`int resultado = 10 / 0;`), lo que causa una `ArithmeticException`.

2. **Bloque `catch`**:
    - Si ocurre una excepción en el bloque `try`, se captura en el bloque `catch`.
    - El parámetro `e` es una instancia de la excepción capturada (`ArithmeticException` en este caso).
    - Dentro del bloque `catch`, puedes manejar la excepción, por ejemplo, mostrando un mensaje de error.

3. **Bloque `finally`**:
    - Este bloque se ejecuta siempre, independientemente de si se lanzó o no una excepción.
    - Es útil para liberar recursos o realizar limpiezas necesarias, como cerrar archivos o conexiones a bases de datos.
    - En este ejemplo, imprime "Bloque finally ejecutado.".

### Importancia del Manejo de Excepciones:

- **Robustez**: Ayuda a que la aplicación no se detenga abruptamente ante un error no controlado.
- **Mantenibilidad**: Proporciona un mecanismo claro para gestionar y responder a errores.
- **Control de Recursos**: Permite garantizar que los recursos se liberen correctamente, evitando fugas de recursos.

### Otros Aspectos del Manejo de Excepciones:

#### Declaración de Excepciones

Algunos métodos pueden lanzar excepciones que no desean manejar directamente. En estos casos, se utiliza la palabra clave `throws` en la declaración del método.

```java
public void leerArchivo(String nombreArchivo) throws IOException {
    // Código que puede lanzar IOException.
}
```

#### Excepciones Personalizadas

Puedes definir tus propias excepciones heredando de la clase `Exception`.

```java
public class MiExcepcion extends Exception {
    public MiExcepcion(String mensaje) {
        super(mensaje);
    }
}
```

#### Uso de Múltiples `catch`

Puedes manejar diferentes tipos de excepciones con múltiples bloques `catch`.

```java
try {
    // Código que puede lanzar diferentes excepciones.
} catch (IOException e) {
    // Manejar IOException.
} catch (SQLException e) {
    // Manejar SQLException.
}
```

### Ejemplo Completo con Excepciones Personalizadas y Múltiples `catch`:

```java
public class EjemploCompleto {
    public static void main(String[] args) {
        try {
            metodoQuePuedeLanzarExcepciones(true);
        } catch (MiExcepcion e) {
            System.out.println("Capturada MiExcepcion: " + e.getMessage());
        } catch (IOException e) {
            System.out.println("Capturada IOException: " + e.getMessage());
        } finally {
            System.out.println("Bloque finally ejecutado.");
        }
    }

    public static void metodoQuePuedeLanzarExcepciones(boolean lanzaMiExcepcion) throws MiExcepcion, IOException {
        if (lanzaMiExcepcion) {
            throw new MiExcepcion("Esto es una excepción personalizada.");
        } else {
            throw new IOException("Esto es una IOException.");
        }
    }
}
```

---
