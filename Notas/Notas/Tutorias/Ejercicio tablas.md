### Realizar una tabla con html y javascript donde:
- Generemos una tabla con id y nombre
- Un botón para agregar nuevos datos a la tabla y un botón para cancelar esa función 
- Funcionalidad para al dar clic derecho en  la fila podamos editarla o eliminarla
- UN mensaje donde nos diga que se ha borrado exitosamente. 

#### Tabla id y nombre:
Para generar la tabla id nombre, ocuparemos:
```html
- **`<tr>`**: Define una fila en la tabla.
    
- **`<th>` y `<td>`**: Definen celdas de encabezado y celdas de datos, respectivamente. `<th>` se usa para encabezados de columna en `<thead>`, y `<td>` para datos en `<tbody>`.
```

#### Botón con funcionalidades:
Para crear un botón utilizaremos java script:

```javascript
    function agregarFila() {
        var nuevaFila = '<tr><td></td><td><input type="text" placeholder="Ingrese nombre"></td></tr>';
        var tbody = document.querySelector('#tablaIdNombre tbody');
        tbody.insertAdjacentHTML('beforeend', nuevaFila);
    }

    function cancelarAgregar() {
        var tbody = document.querySelector('#tablaIdNombre tbody');
        tbody.lastElementChild.remove(); // Elimina la última fila agregada (fila de entrada)
    }


    function agregarFila() {
        var nuevaFila = '<tr><td></td><td><input type="text" placeholder="Ingrese nombre"></td></tr>';
        var tbody = document.querySelector('#tablaIdNombre tbody');
        tbody.insertAdjacentHTML('beforeend', nuevaFila);
    }

    function cancelarAgregar() {
        var tbody = document.querySelector('#tablaIdNombre tbody');
        tbody.lastElementChild.remove(); // Elimina la última fila agregada (fila de entrada)
    }```
```    var contadorFilas = 3; // Contador inicial con el numero de filas existentes

    function agregarFila() {
        contadorFilas++; // Incrementa el contador de filas
        var nuevaFila = '<tr><td>' + contadorFilas + '</td><td><input type="text" placeholder="Ingrese nombre"></td></tr>';
        var tbody = document.querySelector('#tablaIdNombre tbody');
        tbody.insertAdjacentHTML('beforeend', nuevaFila);
    }

    function cancelarAgregar() {
        var tbody = document.querySelector('#tablaIdNombre tbody');
        tbody.lastElementChild.remove(); // Elimina la última fila agregada (fila de entrada)
        contadorFilas--; // Decrementa el contador de filas
    }
```


query selector:
condicon = class