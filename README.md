# Tecnológico de Software

## Materia: Fundamentos de Álgebra

### Alumno: Francisco Emilio Esquivel Torres

### Actividad #16 - Matrices

---

## Identificación de matrices

**Matriz identidad**, porque la diagonal está compuesta solo por unos y los elementos fuera de la diagonal son ceros.

$$
A =
\begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix}
$$

---

## Ejemplo

Calcula la suma de A y B:

$$
A =
\begin{pmatrix}
1 & 2 & 3 \\
4 & 5 & 6
\end{pmatrix}
$$

$$
B =
\begin{pmatrix}
9 & 10 & 11 \\
12 & 13 & 14
\end{pmatrix}
$$

La suma de matrices del mismo tamaño se realiza **sumando cada elemento correspondiente**:

$$
A + B =
\begin{pmatrix}
1 + 9 & 2 + 10 & 3 + 11 \\
4 + 12 & 5 + 13 & 6 + 14
\end{pmatrix}
$$

$$
A + B =
\begin{pmatrix}
10 & 12 & 14 \\
16 & 18 & 20
\end{pmatrix}
$$

---
## Ejercicio 1 clasificar matrices
$$
A =
\begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix},
\quad
B =
\begin{pmatrix}
3 & 0 & 0 \\
0 & -2 & 0 \\
0 & 0 & 5
\end{pmatrix}
$$

$$
C =
\begin{pmatrix}
2 & 1 & 4 \\
1 & 3 & 5 \\
4 & 5 & 6
\end{pmatrix},
\quad
D =
\begin{pmatrix}
1 & 2 & 3 \\
0 & 4 & 5 \\
0 & 0 & 6
\end{pmatrix}
$$

A = Matriz identidad  
B = Matriz diagonal  
C = Matriz cuadrada  
D = Matriz triangular superior


## Ejercicio 2 Operaciones básicas
$$
A =
\begin{pmatrix}
2 & -1 \\
3 & 4
\end{pmatrix},
\quad
B =
\begin{pmatrix}
5 & 2 \\
-1 & 3
\end{pmatrix}
$$

a) \( A + B \)          

$$
A + B = \begin{pmatrix} 2 & -1 \\ 3 & 4 \end{pmatrix} + \begin{pmatrix} 5 & 2 \\ -1 & 3 \end{pmatrix} = \begin{pmatrix} 7 & 1 \\ 2 & 7 \end{pmatrix}
$$                               

b) \( 2A - B \)
$$
2A = 2 \times \begin{pmatrix} 2 & -1 \\ 3 & 4 \end{pmatrix} = \begin{pmatrix} 4 & -2 \\ 6 & 8 \end{pmatrix}
$$

$$
2A - B = \begin{pmatrix} 4 & -2 \\ 6 & 8 \end{pmatrix} - \begin{pmatrix} 5 & 2 \\ -1 & 3 \end{pmatrix} = \begin{pmatrix} -1 & -4 \\ 7 & 5 \end{pmatrix}
$$
c) \( AB \)
$$
AB = \begin{pmatrix} 2 & -1 \\ 3 & 4 \end{pmatrix} \begin{pmatrix} 5 & 2 \\ -1 & 3 \end{pmatrix} = \begin{pmatrix} 11 & 1 \\ 11 & 18 \end{pmatrix}
$$
d) \( BA \)
$$
BA = \begin{pmatrix} 5 & 2 \\ -1 & 3 \end{pmatrix} \begin{pmatrix} 2 & -1 \\ 3 & 4 \end{pmatrix} = \begin{pmatrix} 16 & 3 \\ 7 & 13 \end{pmatrix}
$$
e) \( A^T \)
$$
A^T = \begin{pmatrix} 2 & 3 \\ -1 & 4 \end{pmatrix}
$$

## Ejercicio 3
## Datos
$$
A = \begin{pmatrix} 1 & 2 \\ 3 & 4 \end{pmatrix}, \quad 
B = \begin{pmatrix} 2 & 0 \\ 1 & 3 \end{pmatrix}, \quad 
C = \begin{pmatrix} 1 & 1 \\ 0 & 2 \end{pmatrix}
$$

Verificar que:
$$
(AB)C = A(BC)
$$

---

## a) $AB$
$$
AB = \begin{pmatrix} 1 & 2 \\ 3 & 4 \end{pmatrix} \begin{pmatrix} 2 & 0 \\ 1 & 3 \end{pmatrix} = \begin{pmatrix} 4 & 6 \\ 10 & 12 \end{pmatrix}
$$

---

## b) $(AB)C$
$$
(AB)C = \begin{pmatrix} 4 & 6 \\ 10 & 12 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 0 & 2 \end{pmatrix} = \begin{pmatrix} 4 & 16 \\ 10 & 34 \end{pmatrix}
$$

---

## c) $BC$
$$
BC = \begin{pmatrix} 2 & 0 \\ 1 & 3 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 0 & 2 \end{pmatrix} = \begin{pmatrix} 2 & 2 \\ 1 & 7 \end{pmatrix}
$$

---

## d) $A(BC)$
$$
A(BC) = \begin{pmatrix} 1 & 2 \\ 3 & 4 \end{pmatrix} \begin{pmatrix} 2 & 2 \\ 1 & 7 \end{pmatrix} = \begin{pmatrix} 4 & 16 \\ 10 & 34 \end{pmatrix}
$$

---

## e) Comparación
$$
(AB)C = \begin{pmatrix} 4 & 16 \\ 10 & 34 \end{pmatrix}, \quad 
A(BC) = \begin{pmatrix} 4 & 16 \\ 10 & 34 \end{pmatrix}
$$

**Conclusión:** Se verifica que $(AB)C = A(BC)$

---

## Respuesta final
$$
\boxed{\begin{pmatrix} 4 & 16 \\ 10 & 34 \end{pmatrix}}
$$
## Si cumple la igualdad

