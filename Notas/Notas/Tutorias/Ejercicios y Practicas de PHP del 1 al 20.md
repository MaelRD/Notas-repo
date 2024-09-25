
# PRACTICA 1

| **PREGUNTA**                                                     | **RESPUESTA**                                                                                                                                                                                    |
| ---------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| ¿Quién inventó PHP?                                              | El canadiense-danés Rasmus Lerdorf en 1994                                                                                                                                                       |
| ¿Qué es PHP?                                                     | Un lenguaje de programación o lenguaje de secuencias de comandos (scripts) que se integra en páginas HTML y es interpretado por el servidor                                                      |
| ¿Qué significa PHP?                                              | Personal Home Page                                                                                                                                                                               |
| ¿Cuáles son las diferencias más notables entre JavaScript y PHP? | 1) A veces no es compatible con todos los navegadores 2) En JavaScript podemos llegar a ver el código fuente y en PHP no 3) JavaScript corre en el lado del cliente. PHP en el lado del servidor |
| ¿Qué tipo de licencia tiene PHP?                                 | PHP tiene una licencia Open Source o GNU                                                                                                                                                         |
| ¿Dónde podemos encontrar ayuda para PHP?                         | En el sitio oficial www.php.net/manual/es/                                                                                                                                                       |
| ¿Qué necesitamos para trabajar con PHP?                          | Un servidor web                                                                                                                                                                                  |
| ¿Cómo accedemos a nuestro servidor local?                        | Con http://localhost o http://127.0.0.1                                                                                                                                                          |
| ¿Dónde se encuentra la página de inicio de XAMPP?                | En c:\xampp\htdocs                                                                                                                                                                               |

# PRACTICA 2
Investiga sobre las diferentes versiones de PHP existentes y sus características.

# PRACTICA 3
Realiza la práctica de Instalación XAMPP de tu Cuaderno de Trabajo (Busca en internet y descarga el XAMPP. También deberás instalarlo en un USB personal).

| **PREGUNTA**                               | **RESPUESTA**             |
| ------------------------------------------ | ------------------------- |
| ¿De qué sitio obtuviste el XAMPP?          | www.apachefriends.org     |
| ¿De qué sitio obtuviste el XAMPP Portable? | www.portableapps.com      |
| ¿Qué servicios instalaste del XAMPP?       | Apache, MySQL, FTP Server |

# PRACTICA 4
Realiza la práctica de virtualización de tu Cuaderno de Ejercicios.

**Ejercicio 1 - 01_info.php**
```html
<!DOCTYPE html>
<html>
<head>
    <title>PHP-Info</title>
</head>
<body>
    <?php
    phpinfo();
    ?>
</body>
</html>
```


![[Pasted image 20240607083210.png]]

| **PREGUNTA**                              | **RESPUESTA**                                                |
| ----------------------------------------- | ------------------------------------------------------------ |
| ¿Qué es lo que hace la función phpinfo()? | Muestra la información sobre el estado de PHP y el servidor. |

**Ejercicio 2 - 02_hola.php**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Hola Mundo</title>
</head>
<body>
    <h1>El famoso script Hello World</h1>
    <p>
        <?php
        echo "Hola Mundo!";
        ?>
    </p>
</body>
</html>
```

| **PREGUNTA**                             | **RESPUESTA**                    |
| ---------------------------------------- | -------------------------------- |
| ¿Cómo comenzamos un bloque de PHP?       | utilizado los símbolos "< ? php" |
| ¿Cómo imprimimos un mensaje en pantalla? | echo                             |
|                                          |                                  |

**Ejercicio 3 - 03_hola2.php**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Hola Mundo</title>
</head>
<body>
    <h1>El famoso script Hello World</h1>
    <p>
        <?php
        echo "<b>Hola</b> Mundo!";
        ?>
    </p>
</body>
</html>
```

![[Pasted image 20240607083857.png]]

| **PREGUNTA**                               | **RESPUESTA**                                                                  |
| ------------------------------------------ | ------------------------------------------------------------------------------ |
| ¿Cuál es la diferencia con el ejercicio 2? | Que podemos usar etiquetas HTML dentro del bloque PHP para formatear el texto. |

# PRACTICA 5
Confecciona un programa que muestre una serie de mensajes en la página empleando el comando ECHO. Ten en cuenta que cuando utilizas el comando ECHO el mensaje se debe encerrar entre comillas dobles.

![[Pasted image 20240607084131.png]]

**Ejercicio 4 - 04_variable1.php**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Primer ejemplo de Variables</title>
</head>
<body>
    <h1>Primer ejemplo de Variables</h1>
    <p>
        <?php
        $Name = "Miguel";
        echo "Hola <b>$Name</b>, encantado de conocerte";
        ?>
    </p>
</body>
</html>
```


![[Pasted image 20240607084242.png]]

| **PREGUNTA**                                                              | **RESPUESTA**                    |
| ------------------------------------------------------------------------- | -------------------------------- |
| ¿Cómo declaramos una variable?                                            | Con el signo $. Ejemplo $Nombre. |
| ¿Importan las mayúsculas y minúsculas en la declaración de las variables? | No.                              |

**Ejercicio 5 - 05_variable2.php**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Segundo ejemplo de Variables</title>
</head>
<body>
    <h1>Segundo ejemplo de Variables usando el operador concatenación .</h1>
    <p>
        <?php
        $Name = "Miguel";
        echo "Hola <b>" . $Name . "</b>, encantado de conocerte";
        ?>
    </p>
</body>
</html>
```

![[Pasted image 20240607084333.png]]

**PREGUNTA** | **RESPUESTA**
--- | ---
¿Qué es la concatenación? | La suma de cadenas.
¿Cómo hacemos la concatenación en PHP? | Con el punto (.).

**Ejercicio 6 - 06_break.php**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Break en la ventana del navegador</title>
</head>
<body>
    <h1>Break en la ventana del navegador</h1>
    <p>
        <?php
        $Name = "Miguel";
        echo "Hola <b>$Name</b>, encantado de conocerte<br>";
        echo "Gracias por venir!";
        ?>
    </p>
</body>
</html>
```



**PREGUNTA** | **RESPUESTA**
--- | ---
¿Qué es lo que hace el script? | Saluda al usuario y utiliza la etiqueta `<br>` para salto de línea.

**Ejercicio 7 - 07_break2.php**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Break en la ventana del navegador con signo \</title>
</head>
<body>
    <h1>Break en la ventana del navegador con signo \</h1>
    <p>
        <?php
        $Name = "Miguel";
        echo "Hola <b>$Name</b>, encantado de conocerte<br>\n";
        echo "Gracias por venir!\n";
        ?>
    </p>
</body>
</html>
```

![[Pasted image 20240607084528.png]]

**PREGUNTA** | **RESPUESTA**
--- | ---
¿Cuál es la diferencia con el ejercicio 6? | Se realiza el salto de línea con la instrucción `\n` dentro del script pero no afecta a lo que el usuario ve en el navegador.

**Ejercicio 8 - 08_weekdays1.php**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Introducción a los arrays, método largo</title>
</head>
<body>
    <h1>Introducción a los arrays, método largo</h1>
    <p>A continuación, escribiremos los arrays de acuerdo al método largo.</p>
    <p>
        <?php
        /*
        Este es el método largo para la creación de arrays, donde cada uno de los
        arreglos está en una línea diferente, junto con su valor índice correspondiente
        */
        $dia[0] = "domingo";
        $dia[1] = "lunes";
        $dia[2] = "martes";
        $dia[3] = "miércoles";
        $dia[4] = "jueves";
        $dia[5] = "viernes";
        $dia[6] = "sábado";
        //mostrar el miércoles
        echo $dia[3];
        ?>
    </p>
</body>
</html>
```

![[Pasted image 20240607084645.png]]

**PREGUNTA** | **RESPUESTA**
--- | ---
¿Qué es un array? | Un arreglo o conjunto de valores que comparten un mismo nombre de variable.
¿Cómo declaramos un array? | `$dia[numElemento]`. Ej. `$dia[0]`, `$dia[1]`.

**Ejercicio 9 - 09_weekdays2.php**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Introducción a los arrays, método corto</title>
</head>
<body>
    <h1>Introducción a los arrays, método corto</h1>
    <p>A continuación, escribiremos los arrays de acuerdo al método corto.</p>
    <p>
        <?php
        /*
        Este es el método corto para la creación de arrays, donde todo el array
        puede estar en una sola línea de código.
        */
        $dia = array("domingo", "lunes", "martes", "miércoles", "jueves", "viernes", "sábado");
        //mostrar el miércoles
        echo $dia[3];
        ?>
    </p>
</body>
</html>
```

![[Pasted image 20240607084805.png]]

**PREGUNTA** | **RESPUESTA**
--- | ---
¿Qué diferencia hay con el script 8? | Este es el método corto que permite declarar un array en una sola línea.
¿Cómo se ponen los comentarios? | Con los símbolos `//` y `/* .. */`.

**Ejercicio 10 - 10_Operaciones.php**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Ejemplo de operaciones</title>
</head>
<body>
    <h1>Ejemplo de operaciones aritméticas en PHP</h1>
    <?php
    $a = 

10;
    $b = 5;
    echo "Suma: " . ($a + $b) . "<br>";
    echo "Resta: " . ($a - $b) . "<br>";
    echo "Multiplicación: " . ($a * $b) . "<br>";
    echo "División: " . ($a / $b) . "<br>";
    ?>
</body>
</html>
```

| **PREGUNTA**                                       | **RESPUESTA**                                                                                       |
| -------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| ¿Cómo se hacen las operaciones aritméticas en PHP? | Utilizando los operadores: `+` para sumar, `-` para restar, `*` para multiplicar, `/` para dividir. |
```


```html
# PRACTICA 6
En esta práctica se trabajará con condiciones y estructuras de control en PHP.

**Ejercicio 11 - 11_condicional.php**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Ejemplo de condiciones</title>
</head>
<body>
    <h1>Ejemplo de condiciones en PHP</h1>
    <?php
    $hora = date("H");
    if ($hora < "20") {
        echo "Que tengas un buen día!";
    } else {
        echo "Que tengas una buena noche!";
    }
    ?>
</body>
</html>
```

**PREGUNTA** | **RESPUESTA**
--- | ---
¿Qué es lo que hace el script? | Muestra un mensaje de buenos días o buenas noches dependiendo de la hora actual.
¿Cómo se usa una condición en PHP? | Con la estructura `if`, `else`.

**Ejercicio 12 - 12_condicional2.php**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Ejemplo de condiciones y elseif</title>
</head>
<body>
    <h1>Ejemplo de condiciones con elseif en PHP</h1>
    <?php
    $hora = date("H");
    if ($hora < "10") {
        echo "Buenos días!";
    } elseif ($hora < "20") {
        echo "Buenas tardes!";
    } else {
        echo "Buenas noches!";
    }
    ?>
</body>
</html>
```

**PREGUNTA** | **RESPUESTA**
--- | ---
¿Cuál es la diferencia con el ejercicio 11? | Se agregan más condiciones con `elseif` para mostrar diferentes mensajes según el rango de horas.

**Ejercicio 13 - 13_switch.php**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Ejemplo de switch</title>
</head>
<body>
    <h1>Ejemplo de estructura switch en PHP</h1>
    <?php
    $dia = date("D");
    switch ($dia) {
        case "Mon":
            echo "Hoy es Lunes!";
            break;
        case "Tue":
            echo "Hoy es Martes!";
            break;
        case "Wed":
            echo "Hoy es Miércoles!";
            break;
        case "Thu":
            echo "Hoy es Jueves!";
            break;
        case "Fri":
            echo "Hoy es Viernes!";
            break;
        case "Sat":
            echo "Hoy es Sábado!";
            break;
        case "Sun":
            echo "Hoy es Domingo!";
            break;
        default:
            echo "No sé qué día es!";
    }
    ?>
</body>
</html>
```

**PREGUNTA** | **RESPUESTA**
--- | ---
¿Qué hace la estructura `switch` en PHP? | Evalúa una expresión y ejecuta el código correspondiente al primer `case` que coincida.

# PRACTICA 7
Trabajaremos con bucles y la generación de estructuras repetitivas.

**Ejercicio 14 - 14_for.php**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Ejemplo de bucle for</title>
</head>
<body>
    <h1>Ejemplo de bucle for en PHP</h1>
    <ul>
        <?php
        for ($i = 1; $i <= 10; $i++) {
            echo "<li>Número: $i</li>";
        }
        ?>
    </ul>
</body>
</html>
```

**PREGUNTA** | **RESPUESTA**
--- | ---
¿Cómo funciona un bucle `for` en PHP? | Repite un bloque de código un número determinado de veces.

**Ejercicio 15 - 15_while.php**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Ejemplo de bucle while</title>
</head>
<body>
    <h1>Ejemplo de bucle while en PHP</h1>
    <ul>
        <?php
        $i = 1;
        while ($i <= 10) {
            echo "<li>Número: $i</li>";
            $i++;
        }
        ?>
    </ul>
</body>
</html>
```

**PREGUNTA** | **RESPUESTA**
--- | ---
¿Qué es un bucle `while` en PHP? | Ejecuta un bloque de código mientras se cumpla una condición.

**Ejercicio 16 - 16_dowhile.php**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Ejemplo de bucle do-while</title>
</head>
<body>
    <h1>Ejemplo de bucle do-while en PHP</h1>
    <ul>
        <?php
        $i = 1;
        do {
            echo "<li>Número: $i</li>";
            $i++;
        } while ($i <= 10);
        ?>
    </ul>
</body>
</html>
```

**PREGUNTA** | **RESPUESTA**
--- | ---
¿Cuál es la diferencia entre `while` y `do-while`? | `do-while` ejecuta el bloque de código al menos una vez, incluso si la condición es falsa desde el principio.

# PRACTICA 8
En esta práctica vamos a trabajar con funciones en PHP.

**Ejercicio 17 - 17_funciones.php**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Ejemplo de funciones</title>
</head>
<body>
    <h1>Ejemplo de funciones en PHP</h1>
    <?php
    function saludo($nombre) {
        return "Hola, $nombre!";
    }

    echo saludo("Miguel");
    ?>
</body>
</html>
```

**PREGUNTA** | **RESPUESTA**
--- | ---
¿Qué es una función en PHP? | Un bloque de código que se puede reutilizar, recibe parámetros y devuelve un valor.
¿Cómo se define una función en PHP? | Con la palabra clave `function` seguida del nombre de la función, paréntesis y llaves.

**Ejercicio 18 - 18_funciones2.php**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Ejemplo de funciones con parámetros y valores por defecto</title>
</head>
<body>
    <h1>Ejemplo de funciones con parámetros y valores por defecto en PHP</h1>
    <?php
    function saludo($nombre = "invitado") {
        return "Hola, $nombre!";
    }

    echo saludo("Miguel");
    echo "<br>";
    echo saludo();
    ?>
</body>
</html>
```

**PREGUNTA** | **RESPUESTA**
--- | ---
¿Cómo se definen parámetros con valores por defecto en una función? | Asignando un valor al parámetro en la definición de la función, ejemplo: `$nombre = "invitado"`.

# PRACTICA 9
Finalmente, trabajaremos con formularios y cómo manejar la entrada del usuario en PHP.

**Ejercicio 19 - 19_formulario.php**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Ejemplo de formulario</title>
</head>
<body>
    <h1>Ejemplo de formulario en PHP</h1>
    <form method="post" action="19_formulario.php">
        Nombre: <input type="text" name="nombre">
        <input type="submit">
    </form>
    <?php
    if ($_SERVER["REQUEST_METHOD"] == "POST") {
        $nombre = htmlspecialchars($_POST['nombre']);
        echo "Hola, $nombre!";
    }
    ?>
</body>
</html>
```

**PREGUNTA** | **RESPUESTA**
--- | ---
¿Qué método utiliza el formulario para enviar datos? | El método POST.
¿Qué hace `htmlspecialchars()`? | Convierte caracteres especiales en entidades HTML, evitando inyecciones de código.
