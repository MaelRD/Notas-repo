#Programación 
# Programación en C

C es un lenguaje de programación de propósito general, desarrollado por Dennis Ritchie en los Laboratorios Bell entre 1969 y 1973. Es conocido por su eficiencia y control sobre el hardware, y es ampliamente utilizado en sistemas operativos, software de sistemas y aplicaciones embebidas.

### Características Principales

- **Lenguaje de bajo nivel**: Permite un control detallado del hardware.
- **Portabilidad**: Código C puede ser compilado en una variedad de plataformas.
- **Eficiencia**: Alta eficiencia en términos de ejecución y uso de recursos.
- **Librerías Ricas**: Extensa colección de bibliotecas estándar y de terceros.

---
### Manual de Sintaxis Completa en C con Explicaciones Detalladas

### 1. Estructura de un Programa en C
Un programa típico en C incluye:
- Directivas de preprocesador
- Declaración de funciones
- Definición de la función `main`

```c
#include <stdio.h> // Directiva de preprocesador para incluir la librería estándar de entrada y salida

int main() {       // Declaración de la función principal
    // Código del programa
    return 0;      // Retorna 0 para indicar que el programa terminó correctamente
}
```

### 2. Comentarios
- Comentarios de una sola línea: `// Esto es un comentario de una línea`
- Comentarios de múltiples líneas: `/* Esto es un comentario de múltiples líneas */`

```c
// Comentario de una línea
/* 
   Comentario
   de múltiples
   líneas 
*/
```

### 3. Tipos de Datos Básicos
C soporta varios tipos de datos básicos:
- `int`: Enteros
- `float`: Números de punto flotante
- `double`: Números de punto flotante de doble precisión
- `char`: Carácter

```c
int edad = 25;
float altura = 1.75;
double peso = 70.5;
char inicial = 'A';
```

### 4. Variables y Constantes
- Declaración de variables: `tipo nombreVariable;`
- Inicialización de variables: `tipo nombreVariable = valor;`
- Constantes: `const tipo nombreConstante = valor;`

```c
int numero = 10;
const float PI = 3.14;
```

### 5. Operadores
- **Aritméticos**: `+`, `-`, `*`, `/`, `%`
- **Relacionales**: `==`, `!=`, `>`, `<`, `>=`, `<=`
- **Lógicos**: `&&`, `||`, `!`
- **Asignación**: `=`, `+=`, `-=`, `*=`, `/=`, `%=` 
- **Unarios**: `++`, `--`
- **Bit a bit**: `&`, `|`, `^`, `~`, `<<`, `>>`

```c
int suma = 5 + 3;  // Operador aritmético
int esIgual = (5 == 5); // Operador relacional
int yLogico = (1 && 0); // Operador lógico
int bitwiseAnd = 5 & 3; // Operador bit a bit
```

### 6. Estructuras de Control
#### Condicionales
Las estructuras condicionales permiten tomar decisiones en el código en función de condiciones evaluadas.

```c
int x = 10;

if (x > 0) { // Si x es mayor que 0
    printf("x es positivo\n");
} else if (x < 0) { // Si x es menor que 0
    printf("x es negativo\n");
} else { // Si x es igual a 0
    printf("x es cero\n");
}
```

#### Bucles
Los bucles permiten repetir un bloque de código mientras se cumple una condición.

- **Bucle for**: Se utiliza cuando se conoce el número de iteraciones de antemano.

```c
// Sintaxis del bucle for:
// for (inicialización; condición; actualización) {
//     // Código a ejecutar en cada iteración
// }

for (int i = 0; i < 10; i++) {
    printf("%d\n", i); // Imprime los números del 0 al 9
}
```

- **Bucle while**: Se utiliza cuando no se conoce el número de iteraciones de antemano y se basa en una condición.

```c
// Sintaxis del bucle while:
// while (condición) {
//     // Código a ejecutar mientras la condición sea verdadera
// }

int i = 0;
while (i < 10) {
    printf("%d\n", i); // Imprime los números del 0 al 9
    i++; // Incrementa i en cada iteración
}
```

- **Bucle do-while**: Similar al bucle while, pero la condición se evalúa después de ejecutar el bloque de código al menos una vez.

```c
// Sintaxis del bucle do-while:
// do {
//     // Código a ejecutar
// } while (condición);

int j = 0;
do {
    printf("%d\n", j); // Imprime los números del 0 al 9
    j++; // Incrementa j en cada iteración
} while (j < 10);
```

### 7. Funciones
Las funciones permiten organizar el código en bloques reutilizables. Una función puede tomar argumentos y retornar un valor.

```c
#include <stdio.h>

// Declaración de la función suma que toma dos enteros y retorna su suma
int suma(int a, int b) {
    return a + b;
}

int main() {
    int resultado = suma(3, 4); // Llamada a la función suma
    printf("La suma es %d\n", resultado); // Imprime el resultado de la suma
    return 0;
}
```

### 8. Arrays
Un array es una colección de elementos del mismo tipo almacenados en ubicaciones contiguas de memoria.

```c
int numeros[5] = {1, 2, 3, 4, 5}; // Declaración e inicialización de un array de 5 enteros

// Acceso a los elementos del array usando un bucle for
for (int i = 0; i < 5; i++) {
    printf("%d\n", numeros[i]); // Imprime los elementos del array
}
```

### 9. Punteros
Un puntero es una variable que almacena la dirección de memoria de otra variable.

```c
int x = 10;
int *ptr = &x; // ptr ahora apunta a x

printf("El valor de x es %d\n", x); // Imprime el valor de x
printf("La dirección de x es %p\n", (void*)ptr); // Imprime la dirección de x
printf("El valor al que apunta ptr es %d\n", *ptr); // Imprime el valor al que apunta ptr (es decir, el valor de x)
```

### 10. Entrada y Salida (I/O)
#### 10.1 Función `printf`
La función `printf` se utiliza para imprimir datos en la consola. Su sintaxis básica es:

```c
int printf(const char *format, ...);
```

- **Formatos más comunes:**
  - `%d` o `%i`: Entero
  - `%f`: Número de punto flotante
  - `%c`: Carácter
  - `%s`: Cadena de caracteres
  - `%p`: Puntero
  - `%x` o `%X`: Entero hexadecimal
  - `%o`: Entero octal

```c
int edad = 25;
float altura = 1.75;
char inicial = 'A';

printf("Tengo %d años\n", edad);
printf("Mido %.2f metros\n", altura); // .2f limita el número de decimales a 2
printf("Mi inicial es %c\n", inicial);
```

#### 10.2 Función `scanf`
La función `scanf` se utiliza para leer datos de la consola. Su sintaxis básica es:

```c
int scanf(const char *format, ...);
```

- **Formatos más comunes:**
  - `%d` o `%i`: Entero
  - `%f`: Número de punto flotante
  - `%c`: Carácter
  - `%s`: Cadena de caracteres

```c
int edad;
float altura;
char inicial;

printf("Introduce tu edad: ");
scanf("%d", &edad); // Lee un entero y lo almacena en la variable edad
printf("Introduce tu altura: ");
scanf("%f", &altura); // Lee un número de punto flotante y lo almacena en la variable altura
printf("Introduce tu inicial: ");
scanf(" %c", &inicial); // Espacio antes de %c para consumir el carácter de nueva línea

printf("Edad: %d, Altura: %.2f, Inicial: %c\n", edad, altura, inicial);
```

### 11. Estructuras
Una estructura es una colección de variables bajo un mismo nombre. Las estructuras permiten agrupar diferentes tipos de datos.

```c
struct Persona {
    char nombre[50];
    int edad;
    float altura;
};

struct Persona p1;

strcpy(p1.nombre, "Juan"); // Asigna el nombre a la estructura
p1.edad = 30; // Asigna la edad a la estructura
p1.altura = 1.75; // Asigna la altura a la estructura

printf("Nombre: %s, Edad: %d, Altura: %.2f\n", p1.nombre, p1.edad, p1.altura); // Imprime los valores de la estructura
```

### 12. Archivos
Para trabajar con archivos se utilizan las

 funciones `fopen`, `fprintf`, `fscanf`, `fclose`, entre otras.

```c
FILE *file;
file = fopen("datos.txt", "w"); // Abre un archivo para escritura

if (file != NULL) {
    fprintf(file, "Hola, archivo!\n"); // Escribe en el archivo
    fclose(file); // Cierra el archivo
}

file = fopen("datos.txt", "r"); // Abre un archivo para lectura

if (file != NULL) {
    char linea[100];
    while (fgets(linea, sizeof(linea), file) != NULL) { // Lee una línea del archivo
        printf("%s", linea); // Imprime la línea leída
    }
    fclose(file); // Cierra el archivo
}
```
Para que tus notas sean más completas y útiles, te recomiendo agregar las siguientes secciones:

### 13. Funciones y Paso de Parámetros
Explicación detallada sobre cómo funcionan las funciones en C, incluyendo el paso de parámetros por valor y por referencia.

```c
#include <stdio.h>

// Función que suma dos números (paso por valor)
int suma(int a, int b) {
    return a + b;
}

// Función que intercambia dos números (paso por referencia)
void intercambiar(int *a, int *b) {
    int temp = *a;
    *a = *b;
    *b = temp;
}

int main() {
    int x = 10, y = 20;
    printf("Suma: %d\n", suma(x, y));

    printf("Antes del intercambio: x = %d, y = %d\n", x, y);
    intercambiar(&x, &y);
    printf("Después del intercambio: x = %d, y = %d\n", x, y);
    return 0;
}
```

### 14. Manejo de Cadenas
Cómo trabajar con cadenas de caracteres en C, incluyendo funciones estándar como `strcpy`, `strlen`, `strcmp`, etc.

```c
#include <stdio.h>
#include <string.h>

int main() {
    char str1[20] = "Hola";
    char str2[20];

    // Copiar una cadena
    strcpy(str2, str1);
    printf("str2: %s\n", str2);

    // Concatenar cadenas
    strcat(str1, " Mundo");
    printf("str1: %s\n", str1);

    // Longitud de una cadena
    int len = strlen(str1);
    printf("Longitud de str1: %d\n", len);

    // Comparar cadenas
    int cmp = strcmp(str1, str2);
    printf("Comparación de str1 y str2: %d\n", cmp);

    return 0;
}
```

### 15. Memoria Dinámica
Uso de funciones para manejar memoria dinámica (`malloc`, `calloc`, `realloc`, `free`).

```c
#include <stdio.h>
#include <stdlib.h>

int main() {
    int *ptr;
    int n, i;

    n = 5;
    printf("Número de elementos: %d\n", n);

    // Asignación de memoria usando malloc
    ptr = (int*)malloc(n * sizeof(int));

    if (ptr == NULL) {
        printf("Error de memoria.\n");
        exit(0);
    }

    // Inicializar el array
    for (i = 0; i < n; ++i) {
        ptr[i] = i + 1;
    }

    // Imprimir los elementos del array
    printf("Los elementos del array son: ");
    for (i = 0; i < n; ++i) {
        printf("%d ", ptr[i]);
    }

    // Liberar la memoria asignada
    free(ptr);

    return 0;
}
```

### 16. Estructuras y Uniones
Explicación sobre estructuras avanzadas y el uso de uniones.

```c
#include <stdio.h>

struct Persona {
    char nombre[50];
    int edad;
    float altura;
};

union Data {
    int i;
    float f;
    char str[20];
};

int main() {
    struct Persona p1;
    union Data data;

    // Uso de estructuras
    strcpy(p1.nombre, "Juan");
    p1.edad = 30;
    p1.altura = 1.75;
    printf("Nombre: %s, Edad: %d, Altura: %.2f\n", p1.nombre, p1.edad, p1.altura);

    // Uso de uniones
    data.i = 10;
    printf("data.i: %d\n", data.i);
    data.f = 220.5;
    printf("data.f: %.2f\n", data.f);
    strcpy(data.str, "C Programming");
    printf("data.str: %s\n", data.str);

    return 0;
}
```

### 17. Manejo de Errores
Cómo manejar errores en C, incluyendo el uso de `errno`, `perror`, y `strerror`.

```c
#include <stdio.h>
#include <errno.h>
#include <string.h>

int main() {
    FILE *file;

    file = fopen("no_existe.txt", "r");

    if (file == NULL) {
        printf("Error al abrir el archivo: %s\n", strerror(errno));
    } else {
        fclose(file);
    }

    return 0;
}
```

### 18. Bibliotecas Estándar
Breve descripción de las bibliotecas estándar más comunes y sus usos (`<math.h>`, `<stdlib.h>`, `<string.h>`, `<time.h>`, etc.).

```c
#include <stdio.h>
#include <math.h>
#include <stdlib.h>
#include <string.h>
#include <time.h>

int main() {
    // Ejemplo de <math.h>
    double num = 9.0;
    printf("Raíz cuadrada de %.2f es %.2f\n", num, sqrt(num));

    // Ejemplo de <stdlib.h>
    int val = atoi("123");
    printf("Valor convertido: %d\n", val);

    // Ejemplo de <string.h>
    char str[20] = "Hola";
    printf("Longitud de la cadena '%s': %zu\n", str, strlen(str));

    // Ejemplo de <time.h>
    time_t t;
    time(&t);
    printf("Hora y fecha actual: %s", ctime(&t));

    return 0;
}
```

### 19. Macros y Preprocesador
Uso de macros y directivas del preprocesador.

```c
#include <stdio.h>

#define PI 3.14
#define AREA_CIRCULO(r) (PI * (r) * (r))

int main() {
    int radio = 5;
    double area = AREA_CIRCULO(radio);
    printf("Área del círculo con radio %d es %.2f\n", radio, area);
    return 0;
}
```

### 20. Ejemplos Prácticos
Incluir ejemplos de programas completos que aborden problemas comunes, como manejo de archivos, estructuras de datos, algoritmos de ordenación, etc.

#### Ejemplo: Ordenación de un Array

```c
#include <stdio.h>

void ordenacionBurbuja(int arr[], int n) {
    for (int i = 0; i < n-1; i++) {
        for (int j = 0; j < n-i-1; j++) {
            if (arr[j] > arr[j+1]) {
                int temp = arr[j];
                arr[j] = arr[j+1];
                arr[j+1] = temp;
            }
        }
    }
}

int main() {
    int arr[] = {64, 34, 25, 12, 22, 11, 90};
    int n = sizeof(arr)/sizeof(arr[0]);
    ordenacionBurbuja(arr, n);
    printf("Array ordenado: ");
    for (int i = 0; i < n; i++) {
        printf("%d ", arr[i]);
    }
    return 0;
}
```

Tus notas ahora cubren una amplia gama de temas importantes en el lenguaje de programación C. Sin embargo, siempre hay algunas áreas adicionales que pueden ser útiles agregar para tener una cobertura aún más completa y detallada. Aquí hay algunas sugerencias adicionales para asegurar que tus notas sean aún más útiles y exhaustivas:

### 21. Tipos Definidos por el Usuario
Uso de `typedef` para crear nuevos tipos de datos.

```c
#include <stdio.h>

typedef unsigned int uint;
typedef struct {
    int dia;
    int mes;
    int anio;
} Fecha;

int main() {
    uint edad = 25;
    Fecha hoy = {6, 6, 2024};
    printf("Edad: %u\n", edad);
    printf("Fecha: %02d/%02d/%04d\n", hoy.dia, hoy.mes, hoy.anio);
    return 0;
}
```

### 22. Enumeraciones
Uso de `enum` para definir conjuntos de constantes.

```c
#include <stdio.h>

enum Dia {DOMINGO, LUNES, MARTES, MIERCOLES, JUEVES, VIERNES, SABADO};

int main() {
    enum Dia hoy = MIERCOLES;
    printf("El valor de hoy es: %d\n", hoy);
    return 0;
}
```

### 23. Estructuras de Datos Básicas
Implementación de listas enlazadas, pilas y colas.

#### Lista Enlazada Simple

```c
#include <stdio.h>
#include <stdlib.h>

struct Nodo {
    int dato;
    struct Nodo *siguiente;
};

void imprimirLista(struct Nodo *n) {
    while (n != NULL) {
        printf("%d ", n->dato);
        n = n->siguiente;
    }
}

int main() {
    struct Nodo *cabeza = NULL;
    struct Nodo *segundo = NULL;
    struct Nodo *tercero = NULL;

    cabeza = (struct Nodo*)malloc(sizeof(struct Nodo));
    segundo = (struct Nodo*)malloc(sizeof(struct Nodo));
    tercero = (struct Nodo*)malloc(sizeof(struct Nodo));

    cabeza->dato = 1;
    cabeza->siguiente = segundo;

    segundo->dato = 2;
    segundo->siguiente = tercero;

    tercero->dato = 3;
    tercero->siguiente = NULL;

    imprimirLista(cabeza);

    free(cabeza);
    free(segundo);
    free(tercero);

    return 0;
}
```

### 24. Manipulación de Bits
Operaciones bit a bit, máscaras y desplazamiento de bits.

```c
#include <stdio.h>

int main() {
    unsigned char a = 5; // 00000101
    unsigned char b = a << 1; // 00001010
    unsigned char c = a & b; // 00000000
    unsigned char d = a | b; // 00001111
    unsigned char e = a ^ b; // 00001111
    unsigned char f = ~a; // 11111010

    printf("a = %d\n", a);
    printf("b = %d\n", b);
    printf("c = %d\n", c);
    printf("d = %d\n", d);
    printf("e = %d\n", e);
    printf("f = %d\n", f);

    return 0;
}
```

### 25. Trabajando con Bibliotecas
Creación y uso de bibliotecas estáticas y dinámicas.

#### Creación de una Biblioteca Estática

1. Crear el archivo de cabecera (`milib.h`):

```c
#ifndef MILIB_H
#define MILIB_H

void hola();

#endif
```

2. Crear el archivo de implementación (`milib.c`):

```c
#include <stdio.h>
#include "milib.h"

void hola() {
    printf("Hola, mundo!\n");
}
```

3. Compilar la biblioteca:

```bash
gcc -c milib.c -o milib.o
ar rcs libmilib.a milib.o
```

4. Usar la biblioteca en un programa (`main.c`):

```c
#include "milib.h"

int main() {
    hola();
    return 0;
}
```

5. Compilar y enlazar:

```bash
gcc main.c -L. -lmilib -o main
```

### 26. Programación con Hilos
Uso de la biblioteca `pthread` para la programación concurrente.

```c
#include <stdio.h>
#include <stdlib.h>
#include <pthread.h>

void *imprimirMensaje(void *vargp) {
    printf("Hola desde el hilo!\n");
    return NULL;
}

int main() {
    pthread_t hilo;
    pthread_create(&hilo, NULL, imprimirMensaje, NULL);
    pthread_join(hilo, NULL);
    printf("Hola desde el main!\n");
    return 0;
}
```

### 27. Gestión Avanzada de Archivos
Lectura y escritura en archivos binarios.

```c
#include <stdio.h>

int main() {
    FILE *archivo;
    int num = 1234;
    archivo = fopen("binario.dat", "wb");
    fwrite(&num, sizeof(int), 1, archivo);
    fclose(archivo);

    int leido;
    archivo = fopen("binario.dat", "rb");
    fread(&leido, sizeof(int), 1, archivo);
    fclose(archivo);

    printf("Número leído: %d\n", leido);
    return 0;
}
```

### 28. Depuración y Herramientas de Desarrollo
Uso de herramientas como `gdb` para la depuración de programas.

GNU Debugger Es un depurador para varios lenguajes, incluyendo C y C++. Permite inspeccionar qué hace un programa en punto determinado de la ejecución. Errores como segmentation faults son más fáciles de encontrar con la ayuda de gdb

#### Ejemplo Básico con `gdb`

1. Compilar el programa con información de depuración:

```bash
gcc -g main.c -o main
```

2. Ejecutar `gdb`:

```bash
gdb main
```

3. Dentro de `gdb`:

```gdb
break main
run
next
print variable
continue
```

### 29. [[Buenas Prácticas de Programación]] en C
Consejos y recomendaciones para escribir código limpio, eficiente y mantenible.

- **Comentarios claros y concisos:** Explicar el propósito de las funciones y las partes complejas del código.
- **Uso de nombres significativos:** Nombres de variables y funciones que reflejen su propósito.
- **Estructuración del código:** Organizar el código en funciones y módulos.
- **Gestión adecuada de la memoria:** Siempre liberar la memoria dinámica con `free`.
- **Pruebas exhaustivas:** Verificar el correcto funcionamiento del código con diferentes casos de prueba.
- **Manejo de errores:** Implementar verificaciones de errores en todas las operaciones críticas.

---
