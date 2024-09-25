### 1. **Definición de la tabla de adyacencias**
```cpp
string tabAdyacencias[100][14] = {
    //   Ini  Fin      A           B          C          D          E     Nodos  Total
    {"A","B",   " "," ",   "5","1",   " "," ",   " "," ",   " "," ",   "1",   "5"},
    {"A","B",   " "," ",   "5","2",   "6","1",   " "," ",   " "," ",   "2",   "11"},..... //las omiti pq que hueva ponerlas todas alch
};
```
- **Descripción**: `tabAdyacencias` es un array bidimensional que almacena rutas posibles entre ciudades. Cada fila representa una ruta, y cada columna almacena detalles como ciudades de inicio y fin, segmentos intermedios, número de nodos y distancia total.
- **Columnas**:
  - `Ini` y `Fin`: Ciudad inicial y final de la ruta.
  - `A`, `B`, `C`, `D`, `E`: Segmentos de la ruta, cada uno con su costo en kilómetros.
  - `Nodos`: Número total de nodos en la ruta.
  - `Total`: Distancia total de la ruta en kilómetros.

- **Array bidimensional**: Se usa para organizar datos tabulares en filas y columnas.

```cpp
// Declaración de un array bidimensional
int matriz[3][4] = {
    {1, 2, 3, 4},
    {5, 6, 7, 8},
    {9, 10, 11, 12}
};

// Acceso a elementos
int valor = matriz[1][2]; // valor será 7
```

### 2. **Entrada del usuario**
```cpp
int main() {
    string ciudadIni, ciudadFin;

    // Solicitar la ciudad inicial
    cout << "Ingresa la ciudad inicial: ";
    getline(cin, ciudadIni);

    // Solicitar la ciudad final
    cout << "Ingresa la ciudad final: ";
    getline(cin, ciudadFin);
```
- **Descripción**: Se piden al usuario las ciudades inicial (`ciudadIni`) y final (`ciudadFin`) usando `getline` para permitir nombres de ciudades con espacios.

- **Entrada del usuario**: `getline` se usa para leer una línea completa de entrada, incluyendo espacios.

```cpp
// Leer una línea completa de entrada
string nombre;
getline(cin, nombre);

// Entrada con espacios
// Ejemplo: "Ciudad de México"
```

### 3. **Contar rutas entre las ciudades**
```cpp
    int contador = 0;
    int rutasEncontradas = 0;

    // Contar el número de rutas entre las dos ciudades
    while (contador < 100 && !tabAdyacencias[contador][0].empty()) {
        if (tabAdyacencias[contador][0] == ciudadIni && tabAdyacencias[contador][1] == ciudadFin) {
            rutasEncontradas++;
        }
        contador++;
    }
```
- **Descripción**: Se recorre `tabAdyacencias` para contar cuántas rutas hay entre `ciudadIni` y `ciudadFin`. `rutasEncontradas` se incrementa cada vez que se encuentra una coincidencia.

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

### 4. **Verificar si hay rutas**
```cpp
    if (rutasEncontradas == 0) {
        cout << "No hay rutas entre " << ciudadIni << " y " << ciudadFin << ".\n";
        return 0;
    }
```
- **Descripción**: Si no se encuentran rutas (`rutasEncontradas == 0`), se informa al usuario y se termina el programa.

- **Condicional if**: Se usa para ejecutar código solo si una condición es verdadera.

```cpp
// Sintaxis de if
if (condición) {
    // Código a ejecutar si la condición es verdadera
}

int x = 5;
if (x > 0) {
    printf("x es positivo\n");
}
```

### 5. **Guardar las rutas encontradas**
```cpp
    // Crear un array para almacenar las rutas encontradas
    string rutas[rutasEncontradas][14];
    int indiceRuta = 0;
    contador = 0;

    // Guardar las rutas entre las dos ciudades
    while (contador < 100 && !tabAdyacencias[contador][0].empty()) {
        if (tabAdyacencias[contador][0] == ciudadIni && tabAdyacencias[contador][1] == ciudadFin) {
            for (int j = 0; j < 14; j++) {
                rutas[indiceRuta][j] = tabAdyacencias[contador][j];
            }
            indiceRuta++;
        }
        contador++;
    }
```
- **Descripción**: Se crea un array `rutas` para almacenar las rutas encontradas entre `ciudadIni` y `ciudadFin`. Las rutas se copian desde `tabAdyacencias` a `rutas`.

- **Bucle for**: Se usa para iterar sobre una secuencia de valores.

```cpp
// Sintaxis del bucle for
for (inicialización; condición; incremento) {
    // Código a ejecutar en cada iteración
}

for (int i = 0; i < 10; i++) {
    printf("%d\n", i); // Imprime los números del 0 al 9
}
```

### 6. **Mostrar las rutas encontradas**
```cpp
    // Mostrar las rutas encontradas
    cout << "Rutas posibles de " << ciudadIni << " a " << ciudadFin << ":\n";
    for (int i = 0; i < rutasEncontradas; i++) {
        cout << i+1 << ". ";
        for (int j = 2; j < 12; j+=2) {
            if (rutas[i][j] != " ") {
                cout << rutas[i][j] << " (" << rutas[i][j+1] << " km) ";
            }
        }
        cout << "- Total de nodos: " << rutas[i][12] << ", Total de km: " << rutas[i][13] << "\n";
    }
```
- **Descripción**: Se recorre `rutas` y se muestran todas las rutas posibles. Se imprime cada segmento de la ruta con su distancia, el número total de nodos y la distancia total.

- **Bucle anidado**: Se utiliza para iterar sobre estructuras de datos multidimensionales.

```cpp
// Bucle for anidado
for (int i = 0; i < 3; i++) {
    for (int j = 0; j < 4; j++) {
        printf("%d ", matriz[i][j]); // Imprime elementos de la matriz
    }
    printf("\n");
}
```

### 7. **Encontrar y mostrar la ruta más corta**
```cpp
    // Encontrar la ruta más corta en términos de distancia
    int menorDistancia = stoi(rutas[0][13]);
    int indiceMenorDistancia = 0;
    for (int i = 1; i < rutasEncontradas; i++) {
        if (stoi(rutas[i][13]) < menorDistancia) {
            menorDistancia = stoi(rutas[i][13]);
            indiceMenorDistancia = i;
        }
    }

    // Mostrar la ruta más corta
    cout << "\nLa ruta más corta es:\n";
    for (int j = 2; j < 12; j+=2) {
        if (rutas[indiceMenorDistancia][j] != " ") {
            cout << rutas[indiceMenorDistancia][j] << " (" << rutas[indiceMenorDistancia][j+1] << " km) ";
        }
    }
    cout << "- Total de nodos: " << rutas[indiceMenorDistancia][12] << ", Total de km: " << rutas[indiceMenorDistancia][13] << "\n";
```
- **Descripción**: Se busca la ruta con la menor distancia total (`menorDistancia`) y se imprime.

- **Conversión de cadena a entero**: `stoi` se usa para convertir una cadena a un número entero.

```cpp
// Convertir cadena a entero
string str = "123";
int num = stoi(str); // num será 123
```
### 8. **Encontrar y mostrar la ruta con menos nodos** (continuación)
```cpp
    // Encontrar la ruta con menos nodos
    int menorNodos = stoi(rutas[0][12]);
    int indiceMenorNodos = 0;
    for (int i = 1; i < rutasEncontradas; i++) {
        if (stoi(rutas[i][12]) < menorNodos) {
            menorNodos = stoi(rutas[i][12]);
            indiceMenorNodos = i;
        }
    }

    // Mostrar la ruta con menos nodos
    cout << "\nLa ruta con menos nodos es:\n";
    for (int j = 2; j < 12; j+=2) {
        if (rutas[indiceMenorNodos][j] != " ") {
            cout << rutas[indiceMenorNodos][j] << " (" << rutas[indiceMenorNodos][j+1] << " km) ";
        }
    }
    cout << "- Total de nodos: " << rutas[indiceMenorNodos][12] << ", Total de km: " << rutas[indiceMenorNodos][13] << "\n";

    return 0;
}
```
- **Descripción**: Se busca la ruta con el menor número de nodos (`menorNodos`) y se imprime.
- **Conversión de cadena a entero**: `stoi` se usa para convertir una cadena a un número entero, permitiendo la comparación de distancias y nodos.

### Resumen de funciones y su uso

#### 1. **Definición de la tabla de adyacencias**
```cpp
string tabAdyacencias[100][14] = { /* ... datos ... */ };
```
- **Uso**: Almacena las rutas posibles entre ciudades con sus detalles (ciudades, segmentos, nodos, distancia total).
- **Beneficio**: Permite estructurar y acceder fácilmente a las rutas durante el procesamiento del programa.

#### 2. **Entrada del usuario**
```cpp
getline(cin, ciudadIni);
getline(cin, ciudadFin);
```
- **Uso**: Captura la ciudad inicial y final del usuario.
- **Beneficio**: Permite al usuario especificar las ciudades entre las cuales desea encontrar rutas.

#### 3. **Contar rutas entre las ciudades**
```cpp
while (contador < 100 && !tabAdyacencias[contador][0].empty()) { /* ... */ }
```
- **Uso**: Recorre la tabla para contar y almacenar las rutas que coinciden con las ciudades especificadas.
- **Beneficio**: Determina cuántas rutas existen y las guarda para análisis posterior.

#### 4. **Verificar si hay rutas**
```cpp
if (rutasEncontradas == 0) { /* ... */ }
```
- **Uso**: Verifica si se encontraron rutas y, si no, informa al usuario.
- **Beneficio**: Evita procesamiento adicional si no hay rutas disponibles.

#### 5. **Guardar las rutas encontradas**
```cpp
while (contador < 100 && !tabAdyacencias[contador][0].empty()) { /* ... */ }
```
- **Uso**: Copia las rutas encontradas en un array separado para análisis detallado.
- **Beneficio**: Facilita el procesamiento y la comparación de rutas específicas.

#### 6. **Mostrar las rutas encontradas**
```cpp
for (int i = 0; i < rutasEncontradas; i++) { /* ... */ }
```
- **Uso**: Imprime todas las rutas encontradas con detalles de cada segmento.
- **Beneficio**: Proporciona al usuario una lista completa de opciones de ruta.

#### 7. **Encontrar y mostrar la ruta más corta**
```cpp
for (int i = 1; i < rutasEncontradas; i++) { /* ... */ }
```
- **Uso**: Compara las distancias totales para encontrar y mostrar la ruta más corta.
- **Beneficio**: Permite al usuario identificar la ruta más eficiente en términos de distancia.

#### 8. **Encontrar y mostrar la ruta con menos nodos**
```cpp
for (int i = 1; i < rutasEncontradas; i++) { /* ... */ }
```
- **Uso**: Compara el número de nodos para encontrar y mostrar la ruta con menos nodos.
- **Beneficio**: Permite al usuario identificar la ruta más eficiente en términos de cantidad de nodos.
