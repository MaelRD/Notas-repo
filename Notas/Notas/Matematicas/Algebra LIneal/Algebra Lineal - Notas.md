
# Álgebra Lineal

## Definición y Aplicaciones
- **Definición**: El álgebra lineal es una rama de las matemáticas que estudia los espacios vectoriales y las transformaciones lineales entre ellos.
- **Aplicaciones**: Se utiliza en diversas áreas como física, informática, economía, estadística e ingeniería.

## Conceptos Básicos

### Vectores
- **Definición**: Un vector es un objeto que tiene magnitud y dirección.
- **Notación**: Se representa usualmente como $$ \mathbf{v} = (v_1, v_2, \ldots, v_n) .$$
- **Ejemplo**:
  
  $$ \mathbf{v} = (3, 4)$$


### Operaciones con Vectores
- **Suma de Vectores**:
  $$\mathbf{u} + \mathbf{v} = (u_1 + v_1, u_2 + v_2, \ldots, u_n + v_n)$$
  - **Ejemplo**:
    
    $$\mathbf{u} = (1, 2), \mathbf{v} = (3, 4)
    \mathbf{u} + \mathbf{v} = (4, 6)$$
    
- **Multiplicación por un Escalar**:

  $$c \mathbf{v} = (c v_1, c v_2, \ldots, c v_n)
  $$
  - **Ejemplo**:
$$c = 2, \mathbf{v} = (3, 4)
2 \mathbf{v} = (6, 8)$$
  
### Producto Punto
- **Definición**: El producto punto de dos vectores $$\mathbf{u} \, y \, \mathbf{v}$$ es un escalar.
 $$ \[
  \mathbf{u} \cdot \mathbf{v} = u_1 v_1 + u_2 v_2 + \ldots + u_n v_n
  \]$$
  - **Ejemplo**:
$$\mathbf{u} = (1, 2, 3), \mathbf{v} = (4, 5, 6)$$
$$\mathbf{u} \cdot \mathbf{v} = 1 \cdot 4 + 2 \cdot 5 + 3 \cdot 6 = 32$$


### Producto Cruz
- **Definición**: El producto cruz de dos vectores en $$\mathbb{R}^3$$ es un vector perpendicular a ambos.
 $$ \[
  \mathbf{u} \times \mathbf{v} = (u_2 v_3 - u_3 v_2, u_3 v_1 - u_1 v_3, u_1 v_2 - u_2 v_1)
  \]$$
  - **Ejemplo**:
  
    $$\mathbf{u} = (1, 2, 3), \mathbf{v} = (4, 5, 6)
    \mathbf{u} \times \mathbf{v} = (-3, 6, -3)$$
    

## Matrices

### Definición
- **Definición**: Una matriz es un arreglo bidimensional de números.
- **Notación**: Se denota como: $$\( A = [a_{ij}] \)$$ donde \( a_{ij} \) es el elemento en la fila \( i \) y la columna \( j \).
- **Ejemplo**:
  
  $$ A = \begin{pmatrix}
  1 & 2 & 3 \\
  4 & 5 & 6 \\
  7 & 8 & 9
  \end{pmatrix} $$
  

### Operaciones con Matrices
- **Suma de Matrices**:
$$  \
  A + B = [a_{ij} + b_{ij}]
  $$
  - **Ejemplo**:
    ```plaintext
    A = \begin{pmatrix}
    1 & 2 \\
    3 & 4
    \end{pmatrix},
    B = \begin{pmatrix}
    5 & 6 \\
    7 & 8
    \end{pmatrix}
    A + B = \begin{pmatrix}
    6 & 8 \\
    10 & 12
    \end{pmatrix}
    ```

- **Multiplicación por un Escalar**:
$$C\cdot A=CA_{ij}$$
  - **Ejemplo**:
    
    $$c = 2, A = \begin{pmatrix}
    1 & 2 \\
    3 & 4
    \end{pmatrix}
    2A = \begin{pmatrix}
    2 & 4 \\
    6 & 8
    \end{pmatrix} $$
- **Multiplicación de Matrices**:
  $$\
  C = AB, \text{ donde } c_{ij} = \sum_{k=1}^n a_{ik} b_{kj}
  $$
  - **Ejemplo**:
    $$
    A = \begin{pmatrix}
    1 & 2 \\
    3 & 4
    \end{pmatrix},
    B = \begin{pmatrix}
    2 & 0 \\
    1 & 2
    \end{pmatrix}
    AB = \begin{pmatrix}
    4 & 4 \\
    10 & 8
    \end{pmatrix}
    $$

### Determinante
- **Definición**: El determinante es un escalar que se puede calcular a partir de una matriz cuadrada.
- **Propiedades**:
$$
  - \( \det(AB) = \det(A) \det(B) \)
  - \( \det(A^T) = \det(A) \)
  - Si \( A \) es invertible, \( \det(A^{-1}) = \frac{1}{\det(A)} \)

  $$
- Ejemplo**:
  
$$A = \begin{pmatrix}
  1 & 2 \\
  3 & 4
  \end{pmatrix}
  \det(A) = 1 \cdot 4 - 2 \cdot 3 = -2
  
$$
### Matriz Inversa
- **Definición**: $$La\, matriz\, inversa\, de\, \,( A )\, es\, ( A^{-1} )\, tal\, que\, ( AA^{-1} = A^{-1}A = I $$.
- **Cálculo**: Para una matriz \( 2 \times 2 \),
$$  \[
  A^{-1} = \frac{1}{\det(A)} \begin{pmatrix}
  d & -b \\
  -c & a
  \end{pmatrix}
  \]
  donde \( A = \begin{pmatrix}
  a & b \\
  c & d
  \end{pmatrix} \).$$
- **Ejemplo**:
  ```plaintext
  A = \begin{pmatrix}
  1 & 2 \\
  3 & 4
  \end{pmatrix}
  \det(A) = -2
  A^{-1} = \frac{1}{-2} \begin{pmatrix}
  4 & -2 \\
  -3 & 1
  \end{pmatrix} = \begin{pmatrix}
  -2 & 1 \\
  1.5 & -0.5
  \end{pmatrix}
  ```

## Espacios Vectoriales

### Definición
- **Espacio Vectorial**: Un conjunto \( V \) de vectores donde se pueden realizar las operaciones de suma de vectores y multiplicación por escalares y que satisface ciertos axiomas (cerradura, asociatividad, conmutatividad, etc.).

### Subespacios
- **Definición**: Un subespacio de \( V \) es un subconjunto de \( V \) que es en sí mismo un espacio vectorial bajo las mismas operaciones.
- **Ejemplo**:
  ```plaintext
  El conjunto de vectores \(\mathbf{v} = (v_1, v_2, 0)\) en \(\mathbb{R}^3\) es un subespacio de \(\mathbb{R}^3\).
  ```

### Base y Dimensión
- **Base**: Un conjunto de vectores linealmente independientes que generan el espacio vectorial.
- **Dimensión**: El número de vectores en una base del espacio vectorial.
- **Ejemplo**:
  ```plaintext
  En \(\mathbb{R}^2\), los vectores \(\mathbf{i} = (1, 0)\) y \(\mathbf{j} = (0, 1)\) forman una base.
  ```

## Transformaciones Lineales

### Definición
- **Transformación Lineal**: Una función \( T: V \rightarrow W \) que cumple con:
  -

 \( T(\mathbf{u} + \mathbf{v}) = T(\mathbf{u}) + T(\mathbf{v}) \)
  - \( T(c\mathbf{u}) = cT(\mathbf{u}) \)
- **Ejemplo**:
  ```plaintext
  T(\mathbf{v}) = A \mathbf{v}, donde A es una matriz.
  ```

### Núcleo e Imagen
- **Núcleo (Kernel)**: El conjunto de vectores en \( V \) que se transforman en el vector cero en \( W \).
- **Imagen**: El conjunto de todos los vectores que se pueden obtener como \( T(\mathbf{v}) \) para algún \( \mathbf{v} \) en \( V \).
- **Ejemplo**:
  ```plaintext
  Si \( T(\mathbf{v}) = A \mathbf{v} \), entonces \(\text{Ker}(T) = \{\mathbf{v} \mid A\mathbf{v} = \mathbf{0}\}\).
  ```
```