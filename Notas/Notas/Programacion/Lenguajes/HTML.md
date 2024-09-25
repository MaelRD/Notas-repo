#Programación 
HTML (HyperText Markup Language) es el lenguaje estándar utilizado para crear páginas web. Consiste en una serie de elementos que describen la estructura y el contenido de un documento web.

---

### Estructura Básica de un Documento HTML

Un documento HTML básico tiene la siguiente estructura:

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Documento HTML Básico</title>
</head>
<body>
    <h1>¡Hola, mundo!</h1>
    <p>Este es un documento HTML básico.</p>
</body>
</html>
```

- `<!DOCTYPE html>`: Declara el tipo de documento y la versión de HTML.
- `<html>`: Elemento raíz que contiene todo el contenido de la página.
- `<head>`: Contiene metadatos y enlaces a recursos externos.
- `<title>`: Define el título del documento.
- `<body>`: Contiene el contenido visible de la página web.

---

### Elementos y Etiquetas Comunes en HTML

HTML utiliza una serie de etiquetas para definir diferentes partes del contenido.

#### Encabezados

```html
<h1>Título de Nivel 1</h1>
<h2>Título de Nivel 2</h2>
<h3>Título de Nivel 3</h3>
```

#### Párrafos

```html
<p>Este es un párrafo.</p>
<p>Este es otro párrafo.</p>
```

#### Enfatizar Texto

```html
<strong>Texto en negrita</strong>
<em>Texto en cursiva</em>
```

#### Citas

```html
<blockquote>
    Esta es una cita larga.
</blockquote>
```

---

### Atributos HTML

Los atributos proporcionan información adicional sobre los elementos HTML.

#### Ejemplos de Atributos

```html
<a href="https://www.ejemplo.com" target="_blank">Enlace a Ejemplo</a>
<img src="imagen.jpg" alt="Descripción de la imagen">
```

- `href`: Define la URL de un enlace.
- `target`: Define dónde abrir el enlace.
- `src`: Especifica la ruta de una imagen.
- `alt`: Proporciona texto alternativo para una imagen.

---

### Listas en HTML

HTML soporta varios tipos de listas para organizar contenido.

#### Listas Ordenadas

```html
<ol>
    <li>Primer elemento</li>
    <li>Segundo elemento</li>
    <li>Tercer elemento</li>
</ol>
```

#### Listas Desordenadas

```html
<ul>
    <li>Primer elemento</li>
    <li>Segundo elemento</li>
    <li>Tercer elemento</li>
</ul>
```

#### Listas de Definiciones

```html
<dl>
    <dt>Término 1</dt>
    <dd>Definición del término 1</dd>
    <dt>Término 2</dt>
    <dd>Definición del término 2</dd>
</dl>
```

---

### Enlaces en HTML

Los enlaces permiten a los usuarios navegar entre páginas y recursos.

```html
<a href="https://www.ejemplo.com">Visitar Ejemplo</a>
<a href="#seccion2">Ir a la Sección 2</a>
```

- `href`: Define la URL o el destino del enlace.
- `#`: Navega a una parte específica del documento.

---

### Imágenes en HTML

Las imágenes se insertan en las páginas web utilizando la etiqueta `<img>`.

```html
<img src="imagen.jpg" alt="Descripción de la imagen">
```

- `src`: Especifica la ruta de la imagen.
- `alt`: Proporciona texto alternativo.

---

### Formularios en HTML

Los formularios permiten a los usuarios enviar datos a un servidor.

#### Ejemplo de Formulario

```html
<form action="/submit" method="post">
    <label for="nombre">Nombre:</label>
    <input type="text" id="nombre" name="nombre">
    
    <label for="email">Email:</label>
    <input type="email" id="email" name="email">
    
    <input type="submit" value="Enviar">
</form>
```

- `action`: Define la URL a la que se enviarán los datos del formulario.
- `method`: Especifica el método HTTP para enviar los datos (`get` o `post`).
- `input`: Define un campo de entrada de datos.
- `label`: Proporciona una etiqueta para un campo de entrada.

---

### Tablas en HTML

Las tablas organizan datos en filas y columnas.

#### Ejemplo de Tabla

```html
<table>
    <thead>
        <tr>
            <th>Encabezado 1</th>
            <th>Encabezado 2</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Dato 1</td>
            <td>Dato 2</td>
        </tr>
        <tr>
            <td>Dato 3</td>
            <td>Dato 4</td>
        </tr>
    </tbody>
</table>
```

- `<table>`: Define la tabla.
- `<thead>`: Agrupa el contenido del encabezado.
- `<tbody>`: Agrupa el contenido del cuerpo.
- `<tr>`: Define una fila de la tabla.
- `<th>`: Define una celda de encabezado.
- `<td>`: Define una celda de datos.

---

### Multimedia en HTML

HTML permite la integración de multimedia como audio y video.

#### Insertar Video

```html
<video width="320" height="240" controls>
    <source src="video.mp4" type="video/mp4">
    Tu navegador no soporta el elemento de video.
</video>
```

#### Insertar Audio

```html
<audio controls>
    <source src="audio.mp3" type="audio/mp3">
    Tu navegador no soporta el elemento de audio.
</audio>
```

---

### Introducción a HTML5

HTML5 introduce nuevos elementos y atributos para mejorar la funcionalidad de las páginas web.

#### Elementos Nuevos

- `<article>`: Contenido independiente y auto-contenido.
- `<section>`: Sección temática de un documento.
- `<header>`: Encabezado de una sección o página.
- `<footer>`: Pie de página de una sección o página.
- `<nav>`: Conjunto de enlaces de navegación.
- `<figure>` y `<figcaption>`: Contenido multimedia y su leyenda.

#### Ejemplo de HTML5

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Documento HTML5</title>
</head>
<body>
    <header>
        <h1>Título Principal</h1>
    </header>
    <nav>
        <ul>
            <li><a href="#inicio">Inicio</a></li>
            <li><a href="#acerca">Acerca de</a></li>
        </ul>
    </nav>
    <section id="inicio">
        <h2>Sección de Inicio</h2>
        <p>Contenido de la sección de inicio.</p>
    </section>
    <section id="acerca">
        <h2>Sección Acerca de</h2>
        <p>Contenido de la sección acerca de.</p>
    </section>
    <footer>
        <p>Pie de página</p>
    </footer>
</body>
</html>
```

---

### Buenas Prácticas y Accesibilidad en HTML

Para crear sitios web efectivos y accesibles, considera las siguientes prácticas:

- Usa etiquetas semánticas para describir el contenido.
- Asegúrate de que todos los elementos interactivos sean accesibles mediante teclado.
- Proporciona texto alternativo para las imágenes (`alt`).
- Usa `aria-*` atributos para mejorar la accesibilidad cuando sea necesario.
- Mantén el HTML limpio y bien estructurado para facilitar el mantenimiento y la lectura.

---

