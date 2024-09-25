### 📖 1. Introducción

**El papel de los algoritmos en la computación**
- **Definición de un algoritmo**: Un algoritmo es un conjunto finito de instrucciones bien definidas y no ambiguas que, dadas ciertas condiciones iniciales, producen un resultado deseado y terminan en un tiempo finito.
- **Importancia en la resolución de problemas computacionales**: Los algoritmos son fundamentales para resolver problemas de manera eficiente en la computación. Son el corazón de la programación y el software.
- **Relación con hardware y software**: Los algoritmos optimizados pueden mejorar el rendimiento del hardware y hacer que el software sea más eficiente.

---

### 📖 2. Fundamentos

#### El papel de los algoritmos en la computación
- **Algoritmos y su importancia**:
  - **Fundamentales para la computación**: Los algoritmos son esenciales para realizar tareas computacionales de manera eficiente y correcta.
  - **Eficiencia y corrección son cruciales**: Un algoritmo debe ser tanto correcto (producir los resultados correctos) como eficiente (usar los recursos de manera óptima).

#### Introducción
- **Ordenamiento por inserción**:
  - **Simple e intuitivo**: Inserta cada elemento en su posición correcta dentro de una lista ordenada.
  - **Eficiente para pequeños conjuntos de datos**: Aunque tiene un tiempo de ejecución de \(O(n^2)\), puede ser rápido para listas pequeñas o casi ordenadas.
- **Análisis de algoritmos**:
  - **Notación asintótica: \(O\), \(\Omega\), \(\Theta\)**:
    - **Big-O (\(O\))**: Describe el peor caso, es una cota superior.
    - **Omega (\(\Omega\))**: Describe el mejor caso, es una cota inferior.
    - **Theta (\(\Theta\))**: Describe el caso promedio, es una cota ajustada que representa tanto el mejor como el peor caso.

#### Crecimiento de funciones
- **Notaciones asintóticas**:
  - **Big-O (\(O\))**: Proporciona una cota superior para el tiempo de ejecución de un algoritmo, asegurando que el tiempo no crezca más rápido que una función dada.
  - **Omega (\(\Omega\))**: Proporciona una cota inferior para el tiempo de ejecución de un algoritmo, asegurando que el tiempo no crezca más lentamente que una función dada.
  - **Theta (\(\Theta\))**: Proporciona una cota ajustada, lo que significa que el tiempo de ejecución está acotado tanto por arriba como por abajo por la misma función.

#### Recurrencias
- **Resolución de recurrencias**:
  - **Teorema maestro**: Proporciona una manera directa de resolver recurrencias que aparecen en algoritmos de divide y vencerás.
  - **Método de sustitución**: Involucra suponer una solución y luego probar por inducción matemática que la solución es correcta.
  - **Método del árbol de recurrencia**: Visualiza la recurrencia como un árbol para ayudar a deducir la solución.

#### Análisis probabilístico y algoritmos aleatorizados
- **Análisis probabilístico**:
  - **Tiempo de ejecución esperado**: Calcula el tiempo de ejecución promedio de un algoritmo considerando todos los posibles casos de entrada.
- **Algoritmos aleatorizados**:
  - **Ejemplo: Quicksort aleatorizado**: Utiliza números aleatorios para hacer decisiones en el algoritmo, mejorando el rendimiento promedio.

---

### 📖 3. Ordenamiento y estadísticas de orden

#### Ordenamiento por inserción
- **Algoritmo de ordenamiento por inserción**:
  - **Simple y efectivo para listas pequeñas**: Inserta cada elemento en su posición correcta dentro de una lista ordenada.
  - **Pseudocódigo y ejemplo**: Ilustraciones claras del funcionamiento paso a paso del algoritmo.

#### Merge Sort
- **Algoritmo Merge Sort**:
  - **Divide y vencerás**: Divide el problema en subproblemas más pequeños, los resuelve recursivamente y combina las soluciones.
  - **Relación de recurrencia y análisis**: Su tiempo de ejecución es \(O(n \log n)\).

#### Heapsort
- **Heaps y Heapsort**:
  - **Montículos binarios**: Estructura de datos completa y eficiente para la implementación de Heapsort.
  - **Operaciones con montículos**: Inserción, eliminación, y construcción del montículo.
  - **Algoritmo y análisis**: Heapsort tiene un tiempo de ejecución de \(O(n \log n)\) y es eficiente tanto en el mejor como en el peor caso.

#### Quicksort
- **Algoritmo Quicksort**:
  - **Particionamiento**: Divide el array en dos subarrays según un pivote y ordena recursivamente.
  - **Análisis promedio y peor caso**: Promedio \(O(n \log n)\), peor caso \(O(n^2)\).
  - **Versión aleatorizada**: Utiliza un pivote aleatorio para mejorar el rendimiento promedio.

#### Ordenamiento en tiempo lineal
- **Ordenamiento en tiempo lineal**:
  - **Ordenamiento por conteo**: Eficiente para rangos limitados de datos, tiempo \(O(n + k)\).
  - **Ordenamiento por radix**: Ordena números enteros considerando cada dígito.
  - **Ordenamiento por cubetas**: Distribuye los elementos en un número finito de cubetas, cada una de las cuales se ordena individualmente.

#### Medianas y estadísticas de orden
- **Estadísticas de orden**:
  - **Algoritmo Select**: Encuentra el \(k\)-ésimo elemento más pequeño en tiempo lineal.
  - **Mediana de medianas**: Técnica para seleccionar un pivote de manera eficiente en Quickselect.

---

### 📖 4. Estructuras de datos

#### Pilas y colas
- **Pilas**:
  - **Principio LIFO (Last In, First Out)**: Último en entrar, primero en salir.
  - **Operaciones**: `push` (insertar), `pop` (eliminar).
- **Colas**:
  - **Principio FIFO (First In, First Out)**: Primero en entrar, primero en salir.
  - **Operaciones**: `enqueue` (insertar), `dequeue` (eliminar).

#### Listas enlazadas
- **Listas enlazadas simples y dobles**:
  - **Operaciones**: Inserción, eliminación, búsqueda.
  - **Ventajas**: Eficientes en inserciones y eliminaciones.

#### Árboles
- **Estructuras básicas de árboles**:
  - **Terminología**: Raíz, hojas, altura, profundidad.
  - **Árboles binarios**: Cada nodo tiene hasta dos hijos.

#### Árboles binarios de búsqueda
- **Propiedades de los BST**:
  - **Operaciones**: Inserción, eliminación, búsqueda.
  - **Ordenados**: Todos los nodos en el subárbol izquierdo son menores que el nodo raíz, y todos los nodos en el subárbol derecho son mayores.

#### Árboles rojo-negro
- **Propiedades de los árboles rojo-negro**:
  - **Árboles binarios de búsqueda balanceados**: Mantienen el árbol balanceado mediante reglas de coloración.
  - **Inserción y eliminación**: Operaciones más complejas pero garantizan balanceo.

#### Estructuras de datos aumentadas
- **Técnicas de aumento**:
  - **Ejemplos y casos de uso**: Añadir información adicional a las estructuras de datos para mejorar la eficiencia de ciertos algoritmos.

---

### 📖 5. Técnicas avanzadas de diseño y análisis

#### Programación dinámica
- **Conceptos de programación dinámica**:
  - **Subproblemas superpuestos**: Resolver subproblemas una vez y almacenar sus soluciones.
  - **Estructura óptima**: Soluciones óptimas para subproblemas llevan a soluciones óptimas para el problema original.
  - **Ejemplos**: Serie de Fibonacci, multiplicación de cadenas de matrices.

#### Algoritmos codiciosos
- **Principios de los algoritmos codiciosos**:
  - **Toma de decisiones locales**: Elegir la mejor opción en cada paso con la esperanza de encontrar la solución global óptima.
  - **Ejemplos**: Selección de actividades, codificación de Huffman.

#### Análisis amortizado
- **Técnicas de análisis amortizado**:
  - **Método agregado**: Calcular el costo total de una secuencia de operaciones y luego dividir por el número de operaciones.
  - **Método de contabilidad**: Asignar un "crédito" a las operaciones y asegurarse de que el costo total se mantenga dentro de los límites.
  - **Método potencial**: Utilizar una función potencial para analizar el costo de las operaciones.

---

### 📖 6. Algoritmos de grafos

#### Algoritmos básicos de grafos
- **Conceptos básicos de grafos**:
  - **Representaciones de grafos**: Matriz de adyacencia y lista de adyacencia.
  - **BFS y DFS**: Búsqueda en anchura (BFS)

 y búsqueda en profundidad (DFS) para explorar grafos.

#### Árboles de expansión mínima
- **Algoritmos MST**:
  - **Algoritmo de Kruskal**: Utiliza el enfoque de conjuntos disjuntos para construir el árbol de expansión mínima.
  - **Algoritmo de Prim**: Crece el árbol de expansión mínima a partir de un nodo inicial.

#### Caminos más cortos desde una sola fuente
- **Algoritmos de caminos más cortos**:
  - **Algoritmo de Dijkstra**: Encuentra los caminos más cortos desde un nodo fuente a todos los demás nodos en un grafo con pesos no negativos.
  - **Algoritmo de Bellman-Ford**: Maneja grafos con pesos negativos y detecta ciclos negativos.

#### Caminos más cortos entre todos los pares
- **Caminos más cortos entre todos los pares**:
  - **Algoritmo de Floyd-Warshall**: Encuentra los caminos más cortos entre todos los pares de nodos en un grafo.

#### Flujo máximo
- **Redes de flujo**:
  - **Método de Ford-Fulkerson**: Encuentra el flujo máximo en una red de flujo utilizando caminos aumentantes.

---

### 📖 7. Temas seleccionados

#### Redes de ordenamiento
- **Redes de comparación**:
  - **Ordenador bitónico**: Una red de comparación específica para ordenar secuencias bitónicas (secuencias que primero aumentan y luego disminuyen).

#### Operaciones con matrices
- **Algoritmo de Strassen**:
  - **Multiplicación rápida de matrices**: Algoritmo más rápido que la multiplicación de matrices estándar para grandes matrices.

#### Programación lineal
- **Conceptos básicos de programación lineal**:
  - **Algoritmo Simplex**: Método iterativo para resolver problemas de programación lineal.

#### Polinomios y la FFT
- **Transformada rápida de Fourier (FFT)**:
  - **Multiplicación de polinomios**: Técnica eficiente para multiplicar polinomios utilizando FFT.

#### Algoritmos numéricos
- **Conceptos básicos de teoría numérica**:
  - **Algoritmo de Euclides**: Método eficiente para calcular el máximo común divisor (MCD).
  - **Cifrado RSA**: Algoritmo de cifrado basado en la factorización de números grandes.

#### Búsqueda de cadenas
- **Algoritmos de búsqueda de cadenas**:
  - **Algoritmo de Knuth-Morris-Pratt (KMP)**: Método eficiente para buscar patrones en textos.

#### Geometría computacional
- **Algoritmos geométricos**:
  - **Envolventes convexas**: Encontrar la envolvente convexa de un conjunto de puntos.
  - **Intersección de segmentos de línea**: Determinar si dos segmentos de línea se intersectan.

#### NP-completitud
- **Teoría de NP-completitud**:
  - **P vs NP**: Problema abierto sobre si cada problema cuya solución puede ser verificada en tiempo polinomial puede ser resuelto en tiempo polinomial.
  - **Reducciones en tiempo polinomial**: Técnica para demostrar que un problema es NP-completo.

#### Algoritmos de aproximación
- **Técnicas de aproximación**:
  - **Problemas y soluciones de ejemplo**: Métodos para encontrar soluciones aproximadas a problemas difíciles de resolver exactamente.
