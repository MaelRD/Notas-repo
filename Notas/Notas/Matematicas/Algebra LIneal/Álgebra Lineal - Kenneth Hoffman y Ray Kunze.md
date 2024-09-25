
- **Contenido**: Espacios vectoriales, transformaciones lineales, determinantes, valores propios y vectores propios, entre otros.

## Capítulo 1: Sistemas de Ecuaciones Lineales

### Definiciones Básicas
- **Ecuación Lineal**: Una ecuación de la forma $$\(a_1x_1 + a_2x_2 + \ldots + a_nx_n = b\), donde \(a_i\) y \(b\) $$son constantes.
- **Sistema de Ecuaciones Lineales**: Conjunto de ecuaciones lineales que se resuelven simultáneamente.
- **Solución**: Un conjunto de valores para las variables que satisface todas las ecuaciones.

### Métodos de Solución
- **Eliminación de Gauss**: Proceso de transformar un sistema de ecuaciones en una forma escalonada.
- **Eliminación de Gauss-Jordan**: Proceso de transformar un sistema en la forma escalonada reducida.

### Ejemplo

$$
Sistema:
2x + 3y = 5
4x + 6y = 10

Forma escalonada:
1 2 2.5
0 0 0
$$
```

## Capítulo 2: Espacios Vectoriales

### Definición
- **Espacio Vectorial**: Un conjunto de vectores donde se pueden realizar las operaciones de suma de vectores y multiplicación por escalares que satisfacen ciertos axiomas.

### Subespacios
- **Definición**: Un subespacio de un espacio vectorial es un subconjunto que es en sí mismo un espacio vectorial bajo las mismas operaciones.

### Combinaciones Lineales y Bases
- **Combinación Lineal**: Una expresión de la forma \(c_1\mathbf{v}_1 + c_2\mathbf{v}_2 + \ldots + c_n\mathbf{v}_n\).
- **Base**: Un conjunto de vectores linealmente independientes que generan el espacio vectorial.
- **Dimensión**: El número de vectores en una base.

### Ejemplo
```plaintext
En \(\mathbb{R}^3\), los vectores \(\mathbf{i} = (1, 0, 0)\), \(\mathbf{j} = (0, 1, 0)\) y \(\mathbf{k} = (0, 0, 1)\) forman una base.
```

## Capítulo 3: Transformaciones Lineales

### Definición
- **Transformación Lineal**: Una función \(T: V \rightarrow W\) que cumple con:
  - \(T(\mathbf{u} + \mathbf{v}) = T(\mathbf{u}) + T(\mathbf{v})\)
  - \(T(c\mathbf{u}) = cT(\mathbf{u})\)

### Núcleo e Imagen
- **Núcleo (Ker(T))**: El conjunto de vectores en \(V\) que se transforman en el vector cero en \(W\).
- **Imagen (Im(T))**: El conjunto de todos los vectores que se pueden obtener como \(T(\mathbf{v})\) para algún \(\mathbf{v}\) en \(V\).

### Ejemplo
```plaintext
Si \(T(\mathbf{v}) = A\mathbf{v}\), donde \(A\) es una matriz, entonces \(\text{Ker}(T) = \{\mathbf{v} \mid A\mathbf{v} = \mathbf{0}\}\) y \(\text{Im}(T)\) es el conjunto de todos los productos \(A\mathbf{v}\).
```

## Capítulo 4: Determinantes

### Definición
- **Determinante**: Un escalar asociado a una matriz cuadrada que proporciona información sobre la invertibilidad de la matriz.

### Propiedades
- \(\det(AB) = \det(A) \det(B)\)
- \(\det(A^T) = \det(A)\)
- Si \(A\) es invertible, \(\det(A^{-1}) = \frac{1}{\det(A)}\)

### Cálculo de Determinantes
- Para una matriz $\(2 \times 2\):$
  $$\[
  A = \begin{pmatrix}
  a & b \\
  c & d
  \end{pmatrix}, \quad \det(A) = ad - bc
  \]
$$
### Ejemplo
$$A = \begin{pmatrix}
1 & 2 \\
3 & 4
\end{pmatrix}, \quad \det(A) = 1 \cdot 4 - 2 \cdot 3 = -2$$

## Capítulo 5: Valores Propios y Vectores Propios

### Definición
- **Valor Propio**: Un escalar \(\lambda\) tal que existe un vector no nulo \(\mathbf{v}\) que cumple \(A\mathbf{v} = \lambda\mathbf{v}\).
- **Vector Propio**: Un vector \(\mathbf{v}\) no nulo que cumple \(A\mathbf{v} = \lambda\mathbf{v}\).

### Polinomio Característico
- Definición: El polinomio \(p(\lambda) = \det(A - \lambda I)\) cuyas raíces son los valores propios de \(A\).

### Ejemplo
```plaintext
A = \begin{pmatrix}
2 & 1 \\
1 & 2
\end{pmatrix}

Polinomio característico:
\det(A - \lambda I) = \det\begin{pmatrix}
2-\lambda & 1 \\
1 & 2-\lambda
\end{pmatrix} = (2-\lambda)^2 - 1 = \lambda^2 - 4\lambda + 3

Valores propios: \lambda_1 = 1, \lambda_2 = 3
```

## Capítulo 6: Espacios de Inner Product

### Definición
- **Inner Product**: Una función \(\langle \mathbf{u}, \mathbf{v} \rangle\) que asigna un número real a cada par de vectores de un espacio vectorial y cumple ciertos axiomas (linealidad, simetría, positividad).

### Norma e Inducida
- **Norma**: \(\| \mathbf{v} \| = \sqrt{\langle \mathbf{v}, \mathbf{v} \rangle}\)
- **Ortogonalidad**: Dos vectores \(\mathbf{u}\) y \(\mathbf{v}\) son ortogonales si \(\langle \mathbf{u}, \mathbf{v} \rangle = 0\).

### Ejemplo
```plaintext
En \(\mathbb{R}^2\), el inner product usual es \(\langle \mathbf{u}, \mathbf{v} \rangle = u_1v_1 + u_2v_2\).

Para \(\mathbf{u} = (1, 2)\) y \(\mathbf{v} = (3, 4)\):
\(\langle \mathbf{u}, \mathbf{v} \rangle = 1 \cdot 3 + 2 \cdot 4 = 11\)

Norma de \(\mathbf{u}\):
\(\| \mathbf{u} \| = \sqrt{1^2 + 2^2} = \sqrt{5}\)
```
