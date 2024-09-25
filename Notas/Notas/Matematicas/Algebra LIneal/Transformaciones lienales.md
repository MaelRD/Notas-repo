
#matematicas, #algebra-lineal, #transformaciones-lineales
## Definiciones

- **Transformación Lineal**: Una transformación \( T: V \to W \) entre dos espacios vectoriales \( V \) y \( W \) es lineal si para todos los vectores \( \mathbf{u}, \mathbf{v} \in V \) y todos los escalares \( c \in \mathbb{R} \) (o \( \mathbb{C} \)),
  1. \( T(\mathbf{u} + \mathbf{v}) = T(\mathbf{u}) + T(\mathbf{v}) \)
  2. \( T(c\mathbf{u}) = cT(\mathbf{u}) \)

## Teoremas y Fórmulas

- **Teorema de la Linealidad**: Si \( T: V \to W \) es una transformación lineal, entonces:
  \[
  T(a\mathbf{u} + b\mathbf{v}) = aT(\mathbf{u}) + bT(\mathbf{v})
  \]
  para todos los vectores \( \mathbf{u}, \mathbf{v} \in V \) y todos los escalares \( a, b \in \mathbb{R} \) (o \( \mathbb{C} \)).

- **Matriz de una Transformación Lineal**: Dada una base \( \{ \mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_n \} \) de \( V \) y una transformación lineal \( T: V \to W \), la matriz \( A \) de \( T \) está dada por:
  \[
  A = \begin{bmatrix} T(\mathbf{v}_1) & T(\mathbf{v}_2) & \cdots & T(\mathbf{v}_n) \end{bmatrix}
  \]

## Ejemplos

1. **Ejemplo 1: Transformación Lineal en \( \mathbb{R}^2 \)**:
    - **Transformación**: \( T: \mathbb{R}^2 \to \mathbb{R}^2 \) definida por \( T(x, y) = (2x, 3y) \)
    - **Verificación**:
      \[
      T((x_1, y_1) + (x_2, y_2)) = T(x_1 + x_2, y_1 + y_2) = (2(x_1 + x_2), 3(y_1 + y_2)) = (2x_1 + 2x_2, 3y_1 + 3y_2) = T(x_1, y_1) + T(x_2, y_2)
      \]
      \[
      T(c(x, y)) = T(cx, cy) = (2(cx), 3(cy)) = c(2x, 3y) = cT(x, y)
      \]

2. **Ejemplo 2: Matriz de una Transformación Lineal**:
    - **Base de \( \mathbb{R}^2 \)**: \( \{ \mathbf{e}_1, \mathbf{e}_2 \} \) donde \( \mathbf{e}_1 = (1, 0) \) y \( \mathbf{e}_2 = (0, 1) \)
    - **Transformación**: \( T(x, y) = (x + y, y - x) \)
    - **Cálculo de la matriz**:
      \[
      T(\mathbf{e}_1) = T(1, 0) = (1, -1)
      \]
      \[
      T(\mathbf{e}_2) = T(0, 1) = (1, 1)
      \]
      \[
      A = \begin{bmatrix} T(\mathbf{e}_1) & T(\mathbf{e}_2) \end{bmatrix} = \begin{bmatrix} 1 & 1 \\ -1 & 1 \end{bmatrix}
      \]

## Problemas

- **Problema 1**: Verificar si la transformación \( T: \mathbb{R}^3 \to \mathbb{R}^3 \) definida por \( T(x, y, z) = (x + y, y + z, z + x) \) es lineal.
- **Problema 2**: Encontrar la matriz de la transformación lineal \( T: \mathbb{R}^2 \to \mathbb{R}^2 \) definida por \( T(x, y) = (3x - y, 2y + x) \) en la base estándar.



Esta nota incluye las definiciones básicas, teoremas, ejemplos y problemas relacionados con las transformaciones lineales en álgebra lineal. Puedes ajustarla según tus necesidades específicas y agregar más detalles o secciones si lo consideras necesario.