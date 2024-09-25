### Descripción del Programa

Este programa calcula la integral definida de una función \( f(x) \) en un intervalo \([a, b]\) utilizando el método de Simpson 3/8. Este método es una técnica de integración numérica que proporciona una aproximación más precisa que el método de Simpson 1/3 al utilizar una combinación de coeficientes para sumar las áreas bajo la curva.

### Funcionamiento del Programa

1. **Incluir Librerías:**
   - `#include <stdio.h>`: Para funciones de entrada/salida (`printf`, `scanf`).
   - `#include <math.h>`: Para funciones matemáticas (`exp`, `log`, `pow`, etc.).

2. **Definir la Función a Integrar:**
   - La función a integrar se define en una función separada llamada `function`.

3. **Implementación del Método de Simpson 3/8:**
   - El método de Simpson 3/8 se implementa en la función `simpson38`.

4. **Configuración de los Límites de Integración y Número de Subintervalos:**
   - Los límites de integración \( a \) y \( b \) y el número de subintervalos \( n \) se configuran en la función `main`.

5. **Cálculo de la Integral:**
   - El programa calcula la integral y muestra el resultado al usuario.

### Sintaxis del Programa

#### Función a Integrar

```c
double function(double x) {
    // Aquí se define la función que se va a integrar
    return 2 / (x * x - 4);  // Ejemplo: función f(x) = 2 / (x^2 - 4)
}
```

### Método de Simpson 3/8 Compuesto

Aquí está la función `simpson38_compuesto` explicada línea por línea:

```c
double simpson38_compuesto(double (*f)(double), double a, double b, int n) {
    // Verifica si el número de subintervalos es múltiplo de 3
    if (n % 3 != 0) {
        printf("El número de subintervalos debe ser múltiplo de 3.\n");
        return NAN; // Retorna NaN si n no es múltiplo de 3
    }

    // Calcula el ancho de cada subintervalo
    double h = (b - a) / n;
    
    // Inicializa la suma con los valores de la función en los límites
    double sum = f(a) + f(b);

    // Itera a través de los subintervalos
    for (int i = 1; i < n; ++i) {
        double x_i = a + i * h; // Calcula el punto x_i
        // Si i es múltiplo de 3, multiplica por 2, de lo contrario, por 3
        if (i % 3 == 0) {
            sum += 2 * f(x_i);
        } else {
            sum += 3 * f(x_i);
        }
    }

    // Calcula el valor final de la integral usando la fórmula de Simpson 3/8 compuesto
    return 3 * h * sum / 8;
}
```

**Explicación detallada:**

1. `double simpson38_compuesto(double (*f)(double), double a, double b, int n)`: Define la función `simpson38_compuesto` que toma como parámetros la función `f`, los límites de integración `a` y `b`, y el número de subintervalos `n`.

2. `if (n % 3 != 0)`: Verifica si `n` es múltiplo de 3. Si no lo es, se imprime un mensaje de error y se retorna `NAN` (Not a Number).

3. `double h = (b - a) / n;`: Calcula el ancho de cada subintervalo `h`.

4. `double sum = f(a) + f(b);`: Inicializa la suma con los valores de la función en los límites `a` y `b`.

5. `for (int i = 1; i < n; ++i)`: Inicia un bucle para iterar a través de los subintervalos.

6. `double x_i = a + i * h;`: Calcula el punto `x_i`.

7. `if (i % 3 == 0) { sum += 2 * f(x_i); } else { sum += 3 * f(x_i); }`: Verifica si `i` es múltiplo de 3. Si lo es, multiplica el valor de la función en `x_i` por 2 y lo agrega a `sum`. Si no, multiplica por 3 y lo agrega a `sum`.

8. `return 3 * h * sum / 8;`: Calcula y retorna el valor final de la integral usando la fórmula de Simpson 3/8 compuesto.

### Método de Simpson 3/8 Simple

Aquí está la función `simpson38_simple` explicada línea por línea:

```c
double simpson38_simple(double (*f)(double), double a, double b) {
    // Calcula el ancho de cada subintervalo
    double h = (b - a) / 3;
    
    // Retorna la aproximación de la integral usando la fórmula de Simpson 3/8 simple
    return (3 * h / 8) * (f(a) + 3 * f(a + h) + 3 * f(a + 2 * h) + f(b));
}
```

**Explicación detallada:**

1. `double simpson38_simple(double (*f)(double), double a, double b)`: Define la función `simpson38_simple` que toma como parámetros la función `f` y los límites de integración `a` y `b`.

2. `double h = (b - a) / 3;`: Calcula el ancho de cada subintervalo `h`, dividiendo el intervalo en 3 partes iguales.

3. `return (3 * h / 8) * (f(a) + 3 * f(a + h) + 3 * f(a + 2 * h) + f(b));`: Calcula y retorna la aproximación de la integral usando la fórmula de Simpson 3/8 simple, que involucra los valores de la función en `a`, `a + h`, `a + 2 * h` y `b`.

### Ejecución del Programa

La función `main` coordina la ejecución del programa, solicitando los parámetros al usuario y llamando a ambas funciones para calcular las integrales.

```c
int main() {
    double a, b;
    int n;

    // Leer los límites y el número de subintervalos
    printf("Ingrese el límite inferior (a): ");
    scanf("%lf", &a);
    printf("Ingrese el límite superior (b): ");
    scanf("%lf", &b);
    printf("Ingrese el número de subintervalos (múltiplo de 3) para el método compuesto: ");
    scanf("%d", &n);

    // Calcular la integral usando Simpson 3/8 compuesto
    double result_compuesto = simpson38_compuesto(function, a, b, n);
    if (!isnan(result_compuesto)) {
        printf("El valor aproximado de la integral usando Simpson 3/8 compuesto es: %.6f\n", result_compuesto);
    }

    // Calcular la integral usando Simpson 3/8 simple
    double result_simple = simpson38_simple(function, a, b);
    printf("El valor aproximado de la integral usando Simpson 3/8 simple es: %.6f\n", result_simple);

    return 0;
}
```

**Explicación detallada:**

1. `double a, b; int n;`: Declara las variables `a` (límite inferior), `b` (límite superior) y `n` (número de subintervalos).

2. `printf` y `scanf`: Solicita al usuario que ingrese los límites de integración `a` y `b`, y el número de subintervalos `n`.

3. `double result_compuesto = simpson38_compuesto(function, a, b, n);`: Calcula la integral usando Simpson 3/8 compuesto.

4. `if (!isnan(result_compuesto)) { printf("El valor aproximado de la integral usando Simpson 3/8 compuesto es: %.6f\n", result_compuesto); }`: Verifica si el resultado no es `NAN` y muestra el resultado.

5. `double result_simple = simpson38_simple(function, a, b); printf("El valor aproximado de la integral usando Simpson 3/8 simple es: %.6f\n", result_simple);`: Calcula la integral usando Simpson 3/8 simple y muestra el resultado.

6. `return 0;`: Termina la ejecución del programa.

#### Función Principal

```c
int main() {
    double a = 0.0, b = 35.0 / 100.0;  // Límites de integración: a = 0, b = 0.35
    int n = 3;  // Número de subintervalos, debe ser múltiplo de 3

    double result = simpson38(function, a, b, n);
    if (!isnan(result)) {
        printf("El valor aproximado de la integral es: %.6f\n", result);
    }

    return 0;
}
```

### Manual de Usuario

#### Ingresar una Función Matemática

Para cambiar la función que se va a integrar, modifica la función `function`. Aquí algunos ejemplos:

1. **Función Exponencial: $$f(x) = e^{-x} $$

   ```c
   double function(double x) {
       return x*exp(-x);  // Función exponencial
   }
   ```

2. **Función Logarítmica: $$ f(x) = \log(x) $$

   ```c
   double function(double x) {
       return log(x);  // Función logarítmica
   }
   ```

3. **Función Potencia:  $$f(x) = x^3$$
   ```c
   double function(double x) {
       return pow(x, 3);  // Función potencia
   }
   ```

4. **Función Trigonométrica:  $$f(x) = \sin(x) $$

   ```c
   double function(double x) {
       return sin(x);  // Función trigonométrica
   }
   ```
5. **Función Algebraica:** $$f(x)=\frac{3x}{4-2x}$$
```c
double function(double x){
	return 3*x/(4-x*x)
}
```
7. 
#### Configurar Límites de Integración y Subintervalos

En la función `main`, configura los límites de integración \( a \) y \( b \), así como el número de subintervalos \( n \).

```c
int main() {
    double a = 0.0;          // Límite inferior de integración
    double b = 1.0;          // Límite superior de integración
    int n = 3;               // Número de subintervalos (debe ser múltiplo de 3)

    double result = simpson38(function, a, b, n);
    if (!isnan(result)) {
        printf("El valor aproximado de la integral es: %.6f\n", result);
    }

    return 0;
}
```

### Ejemplo de Ejecución

Si deseas integrar la función $$ e^{-x} $$ en el intervalo $$[0, 1]$$ con 6 subintervalos (múltiplo de 3):

1. Modifica la función `function`:

   ```c
   double function(double x) {
       return exp(-x);
   }
   ```

2. Configura los límites de integración y subintervalos:

   ```c
   int main() {
       double a = 0.0;
       double b = 1.0;
       int n = 6;

       double result = simpson38(function, a, b, n);
       if (!isnan(result)) {
           printf("El valor aproximado de la integral es: %.6f\n", result);
       }

       return 0;
   }
   ```

Al ejecutar el programa, deberías obtener la salida:

```plaintext
El valor aproximado de la integral es: 0.632121
```

Este resultado es una aproximación de la integral $$\int_{0}^{1} e^{-x} \, dx$$, que es aproximadamente 0.632121.

### Conclusión

Este programa es una herramienta útil para calcular integrales definidas utilizando el método de Simpson 3/8. La flexibilidad para definir diferentes funciones y configurar los límites de integración lo hace versátil para diversas aplicaciones matemáticas y científicas.