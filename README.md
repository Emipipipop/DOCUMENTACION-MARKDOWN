# 🧮 Resolución de Sistemas de Ecuaciones Lineales

En este documento se desarrollan paso a paso distintas técnicas para resolver sistemas lineales, incluyendo: **eliminación de Gauss**, **método de Gauss-Jordan**, **cálculo de la matriz inversa** y **regla de Cramer**, además de la clasificación de sistemas según el tipo de solución que presentan.

---

## 📌 Ejercicio 1. Sistema (3×3) con varios métodos

Se estudia el sistema:

$$
\begin{cases}
x + y + z = 6\\
2x - y + z = 3\\
x + 2y - z = 2
\end{cases}
$$

En su representación matricial:

$$
A =
\begin{pmatrix}
1 & 1 & 1\\
2 & -1 & 1\\
1 & 2 & -1
\end{pmatrix},
\qquad
\mathbf{x} =
\begin{pmatrix}
x\\y\\z
\end{pmatrix},
\qquad
\mathbf{b} =
\begin{pmatrix}
6\\3\\2
\end{pmatrix},
\qquad
A\mathbf{x} = \mathbf{b}.
$$

---

### 🔹 1.1 Método de Gauss (eliminación hacia adelante)

Matriz aumentada del sistema:

$$
\left[
\begin{array}{ccc|c}
1 & 1 & 1 & 6\\
2 & -1 & 1 & 3\\
1 & 2 & -1 & 2
\end{array}
\right]
$$

1. **Eliminación de \(x\) en filas 2 y 3**:

$$
R_2 \leftarrow R_2 - 2R_1,\quad
R_3 \leftarrow R_3 - R_1
$$

$$
\longrightarrow
\left[
\begin{array}{ccc|c}
1 & 1 & 1 & 6\\
0 & -3 & -1 & -9\\
0 & 1 & -2 & -4
\end{array}
\right]
$$

2. **Intercambio de filas** para facilitar pivoteo:

$$
R_2 \leftrightarrow R_3
\Longrightarrow
\left[
\begin{array}{ccc|c}
1 & 1 & 1 & 6\\
0 & 1 & -2 & -4\\
0 & -3 & -1 & -9
\end{array}
\right]
$$

3. **Eliminación de \(y\) de la fila 3**:

$$
R_3 \leftarrow R_3 + 3R_2
$$

$$
\longrightarrow
\left[
\begin{array}{ccc|c}
1 & 1 & 1 & 6\\
0 & 1 & -2 & -4\\
0 & 0 & -7 & -21
\end{array}
\right]
$$

**Sustitución regresiva**:

$$
-7z = -21 \; \Rightarrow \; z = 3,
$$

$$
y - 2z = -4 \; \Rightarrow \; y - 6 = -4 \; \Rightarrow \; y = 2,
$$

$$
x + y + z = 6 \; \Rightarrow \; x + 2 + 3 = 6 \; \Rightarrow \; x = 1.
$$

✅ **Solución obtenida**:

$$
\boxed{(x,y,z) = (1,\,2,\,3)}
$$

---

### 🔹 1.2 Método de Gauss-Jordan

Partiendo de la matriz escalonada:

$$
\left[
\begin{array}{ccc|c}
1 & 1 & 1 & 6\\
0 & 1 & -2 & -4\\
0 & 0 & -7 & -21
\end{array}
\right]
$$

1. **Normalizar el pivote de la fila 3**:

$$
R_3 \leftarrow -\frac{1}{7} R_3
\Longrightarrow
\left[
\begin{array}{ccc|c}
1 & 1 & 1 & 6\\
0 & 1 & -2 & -4\\
0 & 0 & 1 & 3
\end{array}
\right]
$$

2. **Eliminar \(z\) de las filas 1 y 2**:

$$
R_2 \leftarrow R_2 + 2R_3,\quad
R_1 \leftarrow R_1 - R_3
$$

$$
\longrightarrow
\left[
\begin{array}{ccc|c}
1 & 1 & 0 & 3\\
0 & 1 & 0 & 2\\
0 & 0 & 1 & 3
\end{array}
\right]
$$

3. **Eliminar \(y\) de la primera fila**:

$$
R_1 \leftarrow R_1 - R_2
$$

$$
\Longrightarrow
\left[
\begin{array}{ccc|c}
1 & 0 & 0 & 1\\
0 & 1 & 0 & 2\\
0 & 0 & 1 & 3
\end{array}
\right]
$$

✅ **Resultado directo**:

$$
x = 1,\quad y = 2,\quad z = 3.
$$

---

### 🔹 1.3 Método de la matriz inversa

Matriz de coeficientes:

$$
A = 
\begin{pmatrix}
1 & 1 & 1 \\
2 & -1 & 1 \\
1 & 2 & -1
\end{pmatrix}.
$$

**Determinante** (regla de Sarrus):

$$
\det(A) = 1(-1)(-1) + 1(1)(1) + 1(2)(2) - 1(-1)(1) - 1(2)(-1) - 1(1)(2) = 7 \neq 0.
$$

**Matriz inversa**:

$$
A^{-1} = \frac{1}{7} 
\begin{pmatrix}
-1 & 3 & 2 \\
3 & -2 & 1 \\
5 & -1 & -3
\end{pmatrix}.
$$

Solución mediante producto:

$$
\mathbf{x} = A^{-1}\mathbf{b} 
= \frac{1}{7} 
\begin{pmatrix}
-1 & 3 & 2 \\
3 & -2 & 1 \\
5 & -1 & -3
\end{pmatrix}
\begin{pmatrix}
6 \\ 3 \\ 2
\end{pmatrix} 
= \frac{1}{7}
\begin{pmatrix}
7 \\ 14 \\ 21
\end{pmatrix}
=
\begin{pmatrix}
1 \\ 2 \\ 3
\end{pmatrix}.
$$
---

### 🔹 1.4 Regla de Cramer

Determinante principal:

$$
D = 7.
$$

Matrices para cada incógnita:

$$
A_x =
\begin{pmatrix}
6 & 1 & 1\\
3 & -1 & 1\\
2 & 2 & -1
\end{pmatrix},
\quad
A_y =
\begin{pmatrix}
1 & 6 & 1\\
2 & 3 & 1\\
1 & 2 & -1
\end{pmatrix},
\quad
A_z =
\begin{pmatrix}
1 & 1 & 6\\
2 & -1 & 3\\
1 & 2 & 2
\end{pmatrix}.
$$

Determinantes respectivos:

$$
D_x = 7,\quad D_y = 14,\quad D_z = 21.
$$

Solución:

$$
x = \frac{D_x}{D} = 1,\quad
y = \frac{D_y}{D} = 2,\quad
z = \frac{D_z}{D} = 3.
$$

✅ **Los cuatro métodos coinciden en la solución**: \((1,2,3)\).

---

## 📌 Ejercicio 2. Clasificación de sistemas

### 🔸 2.1 Sistema (a)

$$
\begin{cases}
x + y = 3\\
2x + 2y = 6
\end{cases}
$$

Matriz aumentada:

$$
\left[
\begin{array}{cc|c}
1 & 1 & 3\\
2 & 2 & 6
\end{array}
\right]
$$

Eliminación:

$$
R_2 \leftarrow R_2 - 2R_1
\Longrightarrow
\left[
\begin{array}{cc|c}
1 & 1 & 3\\
0 & 0 & 0
\end{array}
\right]
$$

✅ **Infinitas soluciones** (sistema compatible indeterminado).

---

### 🔸 2.2 Sistema (b)

$$
\begin{cases}
x + y = 3\\
2x + 2y = 7
\end{cases}
$$

$$
\left[
\begin{array}{cc|c}
1 & 1 & 3\\
2 & 2 & 7
\end{array}
\right]
$$

Eliminación:

$$
R_2 \leftarrow R_2 - 2R_1
\Longrightarrow
\left[
\begin{array}{cc|c}
1 & 1 & 3\\
0 & 0 & 1
\end{array}
\right]
$$

❌ **Sin solución** (sistema incompatible).

---

### 🔸 2.3 Sistema (c)

$$
\begin{cases}
x + y = 3\\
x - y = 1
\end{cases}
$$

$$
\left[
\begin{array}{cc|c}
1 & 1 & 3\\
1 & -1 & 1
\end{array}
\right]
$$

Proceso:

1. \( R_2 \leftarrow R_2 - R_1 \):

$$
\left[
\begin{array}{cc|c}
1 & 1 & 3\\
0 & -2 & -2
\end{array}
\right]
$$

2. Normalización: \( R_2 \leftarrow -\frac{1}{2} R_2 \):

$$
\left[
\begin{array}{cc|c}
1 & 1 & 3\\
0 & 1 & 1
\end{array}
\right]
$$

3. Eliminación: \( R_1 \leftarrow R_1 - R_2 \):

$$
\left[
\begin{array}{cc|c}
1 & 0 & 2\\
0 & 1 & 1
\end{array}
\right]
$$

✅ **Solución única**:

$$
x = 2,\quad y = 1.
$$

---

## 📌 Ejercicio 3. Sistema (4×4)

Sistema:

$$
\begin{cases}
x + y + z + w = 10\\
2x + y - z + w = 5\\
x - y + z - w = 1\\
x + y - z + 2w = 8
\end{cases}
$$

Matriz aumentada:

$$
\left[
\begin{array}{cccc|c}
1 & 1 & 1 & 1 & 10\\
2 & 1 & -1 & 1 & 5\\
1 & -1 & 1 & -1 & 1\\
1 & 1 & -1 & 2 & 8
\end{array}
\right]
$$

Tras aplicar eliminación gaussiana:

$$
\left[
\begin{array}{cccc|c}
1 & 1 & 1 & 1 & 10\\
0 & 1 & 3 & 1 & 15\\
0 & 0 & 1 & 0 & \frac{7}{2}\\
0 & 0 & 0 & 1 & 5
\end{array}
\right]
$$

**Sustitución regresiva**:

$$
w = 5,
$$

$$
z = \frac{7}{2},
$$

$$
y = -\frac{1}{2},
$$

$$
x = 2.
$$

✅ **Solución**:

$$
\boxed{(x,y,z,w) = \left(2,\;-\frac{1}{2},\;\frac{7}{2},\;5\right)}
$$

---

## 🎯 Conclusión

Se han aplicado diferentes técnicas para resolver sistemas lineales, obteniendo los mismos resultados cuando el sistema es **compatible determinado**. Cada método presenta sus ventajas en términos de claridad, eficiencia numérica o aplicación teórica, lo que permite elegir la herramienta más adecuada según el contexto del problema.
