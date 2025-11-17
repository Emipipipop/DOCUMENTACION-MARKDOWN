# Tecnológico de Software

## Materia: Fundamentos de Álgebra

### Alumno: Francisco Emilio Esquivel Torres

### Actividad #18 - Matrices doc2

---

## Identificación de matrices

**Matriz identidad**, porque la diagonal está compuesta solo por unos y los elementos fuera de la diagonal son ceros.

$$
A = \begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix}
$$

---

## Ejemplo: Suma de matrices

Calcula la suma de A y B:

$$
A = \begin{pmatrix}
1 & 2 & 3 \\
4 & 5 & 6
\end{pmatrix}
$$

$$
B = \begin{pmatrix}
9 & 10 & 11 \\
12 & 13 & 14
\end{pmatrix}
$$

$$
A + B = \begin{pmatrix}
1 + 9 & 2 + 10 & 3 + 11 \\
4 + 12 & 5 + 13 & 6 + 14
\end{pmatrix}
$$

$$
A + B = \begin{pmatrix}
10 & 12 & 14 \\
16 & 18 & 20
\end{pmatrix}
$$

---

## Ejercicio 1: Determinantes 2×2

### Matriz A
$$
A = \begin{pmatrix} 5 & 2 \\ 3 & 1 \end{pmatrix}
$$

**Cálculo:**
$$
\text{det}(A) = (5)(1) - (2)(3) = 5 - 6 = \boxed{-1}
$$

### Matriz B
$$
B = \begin{pmatrix} -1 & 4 \\ 2 & -8 \end{pmatrix}
$$

**Cálculo:**
$$
\text{det}(B) = (-1)(-8) - (4)(2) = 8 - 8 = \boxed{0}
$$

### Matriz C
$$
C = \begin{pmatrix} 6 & 9 \\ 2 & 3 \end{pmatrix}
$$

**Cálculo:**
$$
\text{det}(C) = (6)(3) - (9)(2) = 18 - 18 = \boxed{0}
$$

### Matriz D
$$
D = \begin{pmatrix} 0 & 5 \\ -5 & 0 \end{pmatrix}
$$

**Cálculo:**
$$
\text{det}(D) = (0)(0) - (5)(-5) = 0 + 25 = \boxed{25}
$$

---

## Ejercicio 2: Regla de Sarrus

### Matriz E
$$
E = \begin{pmatrix} 1 & 2 & 3 \\ 0 & 1 & 4 \\ 5 & 6 & 0 \end{pmatrix}
$$

**Cálculo:**
$$
\begin{align*}
\text{det}(E) &= 1(1\cdot0 - 4\cdot6) - 2(0\cdot0 - 4\cdot5) + 3(0\cdot6 - 1\cdot5) \\
&= 1(0-24) - 2(0-20) + 3(0-5) \\
&= -24 + 40 - 15 = \boxed{1}
\end{align*}
$$

### Matriz F
$$
F = \begin{pmatrix} 2 & -1 & 3 \\ 1 & 4 & 0 \\ 3 & 2 & -2 \end{pmatrix}
$$

**Cálculo:**
$$
\begin{align*}
\text{det}(F) &= 2(4\cdot(-2) - 0\cdot2) - (-1)(1\cdot(-2) - 0\cdot3) + 3(1\cdot2 - 4\cdot3) \\
&= 2(-8-0) + 1(-2-0) + 3(2-12) \\
&= -16 - 2 - 30 = \boxed{-48}
\end{align*}
$$

---

## Ejercicio 3: Método de cofactores

### Matriz G
$$
G = \begin{pmatrix} 1 & 0 & 2 \\ -1 & 3 & 1 \\ 2 & 0 & 1 \end{pmatrix}
$$

**Expandimos por la segunda columna (tiene dos ceros):**
$$
\begin{align*}
\text{det}(G) &= 0\cdot C_{12} + 3\cdot C_{22} + 0\cdot C_{32} \\
&= 3\cdot(-1)^{2+2}\cdot\begin{vmatrix} 1 & 2 \\ 2 & 1 \end{vmatrix} \\
&= 3\cdot(1\cdot1 - 2\cdot2) \\
&= 3\cdot(1-4) = 3\cdot(-3) = \boxed{-9}
\end{align*}
$$

---

## Ejercicio 4: Verificar propiedades

### Matrices dadas:
$$
A = \begin{pmatrix} 2 & 1 \\ 1 & 3 \end{pmatrix}, \quad B = \begin{pmatrix} 1 & 2 \\ 3 & 1 \end{pmatrix}
$$

**Determinantes individuales:**
$$
\text{det}(A) = 2\cdot3 - 1\cdot1 = 6-1 = 5
$$
$$
\text{det}(B) = 1\cdot1 - 2\cdot3 = 1-6 = -5
$$

**Producto AB:**
$$
AB = \begin{pmatrix} 2 & 1 \\ 1 & 3 \end{pmatrix}\begin{pmatrix} 1 & 2 \\ 3 & 1 \end{pmatrix} = \begin{pmatrix} 5 & 5 \\ 10 & 5 \end{pmatrix}
$$
$$
\text{det}(AB) = 5\cdot5 - 5\cdot10 = 25-50 = -25
$$

**Verificación 1:** $\text{det}(AB) = \text{det}(A)\cdot\text{det}(B)$
$$
-25 = 5\cdot(-5) = -25 \quad \checkmark
$$

**Verificación 2:** $\text{det}(A^T) = \text{det}(A)$
$$
A^T = \begin{pmatrix} 2 & 1 \\ 1 & 3 \end{pmatrix}, \quad \text{det}(A^T) = 2\cdot3 - 1\cdot1 = 5 \quad \checkmark
$$

---

## Ejercicio 5: Aplicación geométrica

**Vectores:** $\vec{u} = (3, 2)$, $\vec{v} = (1, 4)$

**a) Área del paralelogramo:**
$$
\text{Área} = |\text{det}(\vec{u}, \vec{v})| = \left|\begin{vmatrix} 3 & 2 \\ 1 & 4 \end{vmatrix}\right| = |3\cdot4 - 2\cdot1| = |12-2| = \boxed{10}
$$

**b) ¿Cambia el área si intercambiamos?**
No, porque $|\text{det}(\vec{u}, \vec{v})| = |\text{det}(\vec{v}, \vec{u})|$

**c) Significado del signo del determinante:**
El signo indica la orientación de los vectores. Positivo = orientación antihoraria, Negativo = orientación horaria.

---

## Resumen final

| Ejercicio | Resultados |
|-----------|------------|
| 1A | -1 |
| 1B | 0 |
| 1C | 0 |
| 1D | 25 |
| 2E | 1 |
| 2F | -48 |
| 3G | -9 |
| 4 | Propiedades verificadas ✓ |
| 5 | Área = 10 u² |
