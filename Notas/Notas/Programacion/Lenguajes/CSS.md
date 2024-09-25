#Programación en css

# Diseño con CSS (Cascading Style Sheets)

CSS (Cascading Style Sheets) es un lenguaje utilizado para describir la presentación de un documento escrito en HTML o XML. CSS permite separar el contenido de la estructura de presentación, facilitando la gestión y el mantenimiento de los sitios web.

### Características Principales

- **Separación de Contenido y Diseño**: Mantiene el HTML limpio y enfocado en la estructura del contenido.
- **Reutilización de Estilos**: Aplicación de estilos en múltiples páginas desde un único archivo CSS.
- **Control Preciso del Diseño**: Permite un control detallado sobre la apariencia de los elementos en una página web.
- **Compatibilidad con Dispositivos**: Facilita la creación de diseños responsivos y adaptativos.


---

### Sintaxis Básica en CSS

Un archivo CSS consiste en una serie de reglas. Cada regla tiene un selector y un bloque de declaraciones.

#### Ejemplo de Regla CSS:

```css
selector {
    propiedad: valor;
}
```

#### Ejemplo:

```css
body {
    background-color: #f0f0f0;
    font-family: Arial, sans-serif;
}
```

[[Diseño con CSS]]

---

### Selectores en CSS

Los selectores indican a qué elementos HTML se aplican las reglas de estilo.

#### Tipos de Selectores:

- **Selectores de Tipo**: Se aplican a todos los elementos de un tipo específico.

  ```css
  p {
      color: blue;
  }
  ```

- **Selectores de Clase**: Se aplican a elementos con un atributo de clase específico.

  ```css
  .mi-clase {
      font-size: 14px;
  }
  ```

- **Selectores de ID**: Se aplican a un único elemento con un atributo de ID específico.

  ```css
  #mi-id {
      background-color: yellow;
  }
  ```

- **Selectores de Atributo**: Se aplican a elementos con un atributo específico.

  ```css
  input[type="text"] {
      border: 1px solid #ccc;
  }
  ```

- **Selectores Combinados**: Se combinan selectores para aplicar estilos a elementos bajo ciertas condiciones.

  ```css
  div p {
      margin: 10px;
  }
  ```

[[Diseño con CSS]]

---

### Propiedades de Texto y Fuentes en CSS

CSS ofrece varias propiedades para controlar la apariencia del texto y las fuentes.

#### Propiedades Comunes:

- **color**: Define el color del texto.

  ```css
  p {
      color: red;
  }
  ```

- **font-family**: Define la familia de fuentes.

  ```css
  body {
      font-family: 'Arial', sans-serif;
  }
  ```

- **font-size**: Define el tamaño de la fuente.

  ```css
  h1 {
      font-size: 2em;
  }
  ```

- **font-weight**: Define el grosor de la fuente.

  ```css
  strong {
      font-weight: bold;
  }
  ```

- **line-height**: Define la altura de la línea.

  ```css
  p {
      line-height: 1.5;
  }
  ```

[[Diseño con CSS]]

---

### Modelo de Caja en CSS

El modelo de caja es un concepto fundamental en CSS que describe cómo se diseña y estructura el espacio alrededor de los elementos.

#### Componentes del Modelo de Caja:

- **Contenido**: El área donde se muestra el contenido.
- **Padding**: El espacio entre el contenido y el borde.
- **Border**: El borde que rodea el padding y el contenido.
- **Margin**: El espacio fuera del borde que separa el elemento de otros elementos.

#### Ejemplo:

```css
div {
    width: 300px;
    padding: 20px;
    border: 5px solid black;
    margin: 10px;
}
```

[[Diseño con CSS]]

---

### Diseño de Layouts con CSS

CSS proporciona diversas técnicas para diseñar la disposición de los elementos en la página.

#### Diseño con Flexbox:

Flexbox es un modelo de diseño unidimensional que permite alinear y distribuir espacio entre elementos en un contenedor.

```css
.container {
    display: flex;
    justify-content: space-between;
}
```

#### Diseño con Grid:

Grid Layout es un sistema de diseño bidimensional para crear diseños complejos.

```css
.container {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 10px;
}
```

[[Diseño con CSS]]

---

### Diseño Responsivo en CSS

El diseño responsivo permite que una página web se adapte a diferentes tamaños de pantalla y dispositivos.

#### Media Queries:

```css
@media (max-width: 600px) {
    body {
        background-color: lightblue;
    }
}
```

#### Unidades Relativas:

- **em**: Relativa al tamaño de la fuente del elemento.
- **rem**: Relativa al tamaño de la fuente del elemento raíz (html).
- **%**: Relativa al contenedor del elemento.

[[Diseño con CSS]]

---

### Animaciones y Transiciones en CSS

CSS permite agregar animaciones y transiciones para mejorar la experiencia del usuario.

#### Transiciones:

```css
div {
    transition: background-color 0.5s;
}

div:hover {
    background-color: yellow;
}
```

#### Animaciones:

```css
@keyframes ejemplo {
    from {background-color: red;}
    to {background-color: yellow;}
}

div {
    animation: ejemplo 2s infinite;
}
```

[[Diseño con CSS]]

---

### Prácticas Avanzadas en CSS

CSS tiene muchas características avanzadas para mejorar el diseño y la funcionalidad.

#### Pseudoelementos y Pseudoclases:

- **Pseudoelementos**: Estilizan partes específicas de un elemento.

  ```css
  p::first-line {
      font-weight: bold;
  }
  ```

- **Pseudoclases**: Estilizan elementos en un estado específico.

  ```css
  a:hover {
      color: green;
  }
  ```

#### Variables CSS:

```css
:root {
    --main-color: #3498db;
}

body {
    color: var(--main-color);
}
```

#### Preprocesadores CSS:

Los preprocesadores como Sass o Less añaden funcionalidades avanzadas como variables, anidamiento de reglas y mixins.

```scss
$main-color: #3498db;

body {
    color: $main-color;
}
```

[[Diseño con CSS]]

---
