## Sintaxis de JavaScript

### Conceptos Básicos

#### Comentarios

- **Comentarios de una sola línea:**
  ```javascript
  // Esto es un comentario de una sola línea
  ```

- **Comentarios de varias líneas:**
  ```javascript
  /* Esto es un comentario
     de varias líneas */
  ```

#### Variables

- **Declaración de variables:**
  ```javascript
  let nombre = 'Juan';  // variable que puede cambiar
  const PI = 3.1416;    // variable constante que no puede cambiar
  var edad = 25;        // variable con alcance global o de función
  ```

  **Explicación:**
  - `let` se utiliza para declarar variables que pueden cambiar.
  - `const` se utiliza para declarar constantes que no pueden cambiar.
  - `var` es una forma antigua de declarar variables que tiene un alcance de función o global.

### Tipos de Datos

- **Números:**
  ```javascript
  let numero = 42;
  ```

- **Cadenas de texto:**
  ```javascript
  let saludo = 'Hola, mundo!';
  ```

- **Booleanos:**
  ```javascript
  let esVerdadero = true;
  ```

- **Arreglos:**
  ```javascript
  let colores = ['rojo', 'verde', 'azul'];
  ```

- **Objetos:**
  ```javascript
  let persona = {
    nombre: 'Juan',
    edad: 30
  };
  ```

### Operadores

- **Operadores aritméticos:**
  ```javascript
  let suma = 5 + 3;    // 8
  let resta = 5 - 3;   // 2
  let multiplicacion = 5 * 3;  // 15
  let division = 5 / 3;  // 1.666...
  let modulo = 5 % 3;   // 2
  ```

- **Operadores de asignación:**
  ```javascript
  let x = 10;
  x += 5;  // x ahora es 15
  x -= 3;  // x ahora es 12
  x *= 2;  // x ahora es 24
  x /= 4;  // x ahora es 6
  ```

### Estructuras de Control

- **Condicionales:**
  ```javascript
  if (edad >= 18) {
    console.log('Eres mayor de edad');
  } else {
    console.log('Eres menor de edad');
  }

  // Condicional múltiple
  let calificacion = 'A';
  switch (calificacion) {
    case 'A':
      console.log('Excelente');
      break;
    case 'B':
      console.log('Bueno');
      break;
    case 'C':
      console.log('Regular');
      break;
    default:
      console.log('Desconocido');
  }
  ```

- **Bucles:**
  ```javascript
  // Bucle for
  for (let i = 0; i < 5; i++) {
    console.log(i);
  }

  // Bucle while
  let i = 0;
  while (i < 5) {
    console.log(i);
    i++;
  }

  // Bucle do-while
  let j = 0;
  do {
    console.log(j);
    j++;
  } while (j < 5);
  ```

### Funciones

- **Declaración de funciones:**
  ```javascript
  function saludar(nombre) {
    return `Hola, ${nombre}!`;
  }
  ```

- **Funciones anónimas y flecha:**
  ```javascript
  // Función anónima
  const sumar = function(a, b) {
    return a + b;
  };

  // Función flecha
  const restar = (a, b) => a - b;
  ```

### Manejo de Errores

- **Try...catch:**
  ```javascript
  try {
    let resultado = division(10, 0);
  } catch (error) {
    console.log('Ocurrió un error:', error.message);
  }

  function division(a, b) {
    if (b === 0) {
      throw new Error('División por cero');
    }
    return a / b;
  }
  ```

### Manejo del DOM

- **Selección de elementos:**
  ```javascript
  let titulo = document.getElementById('titulo');
  let parrafos = document.getElementsByClassName('parrafo');
  let enlaces = document.querySelectorAll('a');
  ```

- **Modificación de elementos:**
  ```javascript
  titulo.textContent = 'Nuevo Título';
  titulo.style.color = 'blue';
  ```

### Asincronía

- **Promesas:**
  ```javascript
  const promesa = new Promise((resolve, reject) => {
    let exito = true;
    if (exito) {
      resolve('La operación fue exitosa');
    } else {
      reject('La operación falló');
    }
  });

  promesa.then(mensaje => {
    console.log(mensaje);
  }).catch(error => {
    console.log(error);
  });
  ```

- **Async/Await:**
  ```javascript
  async function obtenerDatos() {
    try {
      let respuesta = await fetch('https://api.example.com/datos');
      let datos = await respuesta.json();
      console.log(datos);
    } catch (error) {
      console.log('Error:', error);
    }
  }
  ```
¡Claro! Aquí te dejo algunos ejemplos de programas en JavaScript con explicaciones línea por línea. 

### Ejemplo 1: Calculadora Básica

Este programa es una calculadora simple que suma, resta, multiplica o divide dos números ingresados por el usuario.

```javascript
// Función para sumar dos números
function sumar(a, b) {
    return a + b;
}

// Función para restar dos números
function restar(a, b) {
    return a - b;
}

// Función para multiplicar dos números
function multiplicar(a, b) {
    return a * b;
}

// Función para dividir dos números
function dividir(a, b) {
    // Verifica que el divisor no sea cero para evitar errores
    if (b === 0) {
        throw new Error('No se puede dividir por cero');
    }
    return a / b;
}

// Solicita al usuario ingresar dos números y una operación
let numero1 = parseFloat(prompt('Ingrese el primer número:'));
let numero2 = parseFloat(prompt('Ingrese el segundo número:'));
let operacion = prompt('Ingrese la operación (sumar, restar, multiplicar, dividir):');

try {
    let resultado;
    // Realiza la operación solicitada por el usuario
    switch (operacion) {
        case 'sumar':
            resultado = sumar(numero1, numero2);
            break;
        case 'restar':
            resultado = restar(numero1, numero2);
            break;
        case 'multiplicar':
            resultado = multiplicar(numero1, numero2);
            break;
        case 'dividir':
            resultado = dividir(numero1, numero2);
            break;
        default:
            throw new Error('Operación no válida');
    }
    console.log(`El resultado de ${operacion} ${numero1} y ${numero2} es ${resultado}`);
} catch (error) {
    console.log(error.message);
}
```

#### Explicación

1. **Declaración de funciones:**
   - `sumar(a, b)`: Devuelve la suma de `a` y `b`.
   - `restar(a, b)`: Devuelve la resta de `a` y `b`.
   - `multiplicar(a, b)`: Devuelve la multiplicación de `a` y `b`.
   - `dividir(a, b)`: Devuelve la división de `a` y `b`. Verifica que `b` no sea cero para evitar errores.

2. **Solicita entrada del usuario:**
   - `prompt('Ingrese el primer número:')`: Solicita al usuario que ingrese el primer número.
   - `prompt('Ingrese el segundo número:')`: Solicita al usuario que ingrese el segundo número.
   - `prompt('Ingrese la operación (sumar, restar, multiplicar, dividir):')`: Solicita al usuario que ingrese la operación a realizar.

3. **Realiza la operación solicitada:**
   - `switch (operacion)`: Evalúa el valor de `operacion` y ejecuta el caso correspondiente.
   - `console.log(...)`: Muestra el resultado en la consola.

4. **Manejo de errores:**
   - `try...catch`: Captura y maneja cualquier error que ocurra durante la ejecución del código, mostrando un mensaje de error en la consola.

### Ejemplo 2: Contador de Palabras

Este programa cuenta el número de palabras en una cadena de texto ingresada por el usuario.

```javascript
// Función para contar palabras en una cadena
function contarPalabras(texto) {
    // Divide el texto en palabras utilizando espacios como separadores
    let palabras = texto.trim().split(/\s+/);
    // Devuelve la cantidad de palabras
    return palabras.length;
}

// Solicita al usuario ingresar una cadena de texto
let texto = prompt('Ingrese una cadena de texto:');

// Llama a la función contarPalabras y muestra el resultado
let numeroDePalabras = contarPalabras(texto);
console.log(`El número de palabras en la cadena ingresada es: ${numeroDePalabras}`);
```

#### Explicación

1. **Función para contar palabras:**
   - `contarPalabras(texto)`: Recibe una cadena de texto y devuelve la cantidad de palabras en ella.
     - `texto.trim()`: Elimina los espacios en blanco al principio y al final de la cadena.
     - `texto.split(/\s+/)`: Divide la cadena en palabras utilizando uno o más espacios como separadores.
     - `palabras.length`: Devuelve el número de elementos en el arreglo `palabras`, que corresponde al número de palabras.

2. **Solicita entrada del usuario:**
   - `prompt('Ingrese una cadena de texto:')`: Solicita al usuario que ingrese una cadena de texto.

3. **Cuenta las palabras y muestra el resultado:**
   - `contarPalabras(texto)`: Llama a la función `contarPalabras` con el texto ingresado por el usuario.
   - `console.log(...)`: Muestra el número de palabras en la consola.

### Ejemplo 3: FizzBuzz

Este programa imprime los números del 1 al 100, pero para múltiplos de 3 imprime "Fizz", para múltiplos de 5 imprime "Buzz", y para múltiplos de ambos imprime "FizzBuzz".

```javascript
// Bucle del 1 al 100
for (let i = 1; i <= 100; i++) {
    // Inicializa la variable resultado como una cadena vacía
    let resultado = '';

    // Verifica si el número es múltiplo de 3
    if (i % 3 === 0) {
        resultado += 'Fizz';
    }

    // Verifica si el número es múltiplo de 5
    if (i % 5 === 0) {
        resultado += 'Buzz';
    }

    // Si resultado sigue siendo una cadena vacía, asigna el número
    if (resultado === '') {
        resultado = i;
    }

    // Imprime el resultado
    console.log(resultado);
}
```

#### Explicación

1. **Bucle del 1 al 100:**
   - `for (let i = 1; i <= 100; i++)`: Itera desde `i = 1` hasta `i = 100`.

2. **Inicializa la variable `resultado`:**
   - `let resultado = '';`: Inicializa `resultado` como una cadena vacía para cada iteración.

3. **Verifica múltiplos de 3 y 5:**
   - `if (i % 3 === 0)`: Si `i` es múltiplo de 3, añade "Fizz" a `resultado`.
   - `if (i % 5 === 0)`: Si `i` es múltiplo de 5, añade "Buzz" a `resultado`.

4. **Asigna el número si no es múltiplo de 3 ni de 5:**
   - `if (resultado === '')`: Si `resultado` sigue siendo una cadena vacía, asigna el número `i` a `resultado`.

5. **Imprime el resultado:**
   - `console.log(resultado)`: Muestra el valor de `resultado` en la consola.

