# Дано 

## Вариант 9

$$    
A =     
 \begin{pmatrix}    
  4 & 3 & 0 & \cdots & 0 & 0 \\    
  -4 & 4 & 3 & \cdots & 0 & 0 \\    
  0 & -4 & 4 & \cdots & 0 & 0 \\    
  \vdots  & \vdots & \vdots & \ddots & \vdots & \vdots  \\    
  0 & 0 & 0 & \cdots & 4 & 3 \\    
  0 & 0 & 0 & \cdots & -4 & 4     
 \end{pmatrix}    
$$

Порядок матрицы *n* = 9

# Решение

## Вывод рекуррентного соотношения

$$    
|A| =     
  4 *
 \begin{vmatrix}    
  4 & 3 & \cdots & 0 & 0 \\    
  -4 & 4 & \cdots & 0 & 0 \\    
  \vdots & \vdots & \ddots & \vdots & \vdots  \\    
  0 & 0 & \cdots & 4 & 3 \\    
  0 & 0 & \cdots & -4 & 4     
 \end{vmatrix} 
 -3 *
 \begin{vmatrix}    
  -4 & 3 & \cdots & 0 & 0 \\    
  0 & 4 & \cdots & 0 & 0 \\    
  \vdots  & \vdots & \ddots & \vdots & \vdots  \\    
  0 & 0 & \cdots & 4 & 3 \\    
  0 & 0 & \cdots & -4 & 4     
 \end{vmatrix}  
$$

$$    
|A| =     
  4 *
 \begin{vmatrix}    
  4 & 3 & \cdots & 0 & 0 \\    
  -4 & 4 & \cdots & 0 & 0 \\    
  \vdots & \vdots & \ddots & \vdots & \vdots  \\    
  0 & 0 & \cdots & 4 & 3 \\    
  0 & 0 & \cdots & -4 & 4     
 \end{vmatrix} 
 -3 * (-4)
 \begin{vmatrix}    
  4 & \cdots & 0 & 0 \\    
  \vdots & \ddots & \vdots & \vdots  \\    
  0 & \cdots & 4 & 3 \\    
  0 & \cdots & -4 & 4     
 \end{vmatrix} 
$$

Таким образом получаем рекуррентное соотношение: 
$$|A| = 4 * |A|_{n-1} + 12 * |A|_{n-2}$$

## Составление и решение характеристического уравнения

$$
\lambda^n = 4 \lambda^{n-1} + 12 \lambda^{n-2}
$$

$$
\lambda^2 - 4\lambda - 12 = 0
$$

$$
\lambda_1 + \lambda_2 = 4 , \quad \lambda_1 \lambda_2 = -12
$$

$$
\lambda_1 = 6 , \quad \lambda_2 = -2
$$

## Составление общей формулы

Так как $\lambda_1 \neq \lambda_2$, следовательно:

$$
|A|_n = a \cdot 6^n + b \cdot (-2)^n
$$

### Найдём константы

Так как последовательность глубиной 2, она определяется двумя последовательными элементами.

$$
|A|_1 = 4 , \quad |A|_2 = 28
$$

$$
\begin{cases}
4 = a \cdot 6 + b \cdot (-2) \\
28 = a \cdot 6^2 + b \cdot (-2)^2
\end{cases}
$$

$$
\begin{cases}
4 = 6a - 2b \\
28 = 36a + 4b
\end{cases}
$$

Умножим первое уравнение на 2:

$$
\begin{cases}
8 = 12a - 4b \\
28 = 36a + 4b
\end{cases}
$$

Сложим уравнения:

$$
36 = 48a \Rightarrow a = 0.75
$$

Подставим во второе:

$$
4 = 6(0.75) - 2b \Rightarrow 4 = 4.5 - 2b \Rightarrow b = 0.25
$$

Таким образом:

$$
|A|_n = 0.75 \cdot 6^n + 0.25 \cdot (-2)^n
$$

## Найдём определитель 9 порядка

$$
|A|_9 = 0.75 \cdot 6^9 + 0.25 \cdot (-2)^9
$$

$$
6^9 = 10\,077\,696 , \quad (-2)^9 = -512
$$

$$
|A|_9 = 0.75 \cdot 10\,077\,696 + 0.25 \cdot (-512) = 7\,558\,272 - 128 = 7\,558\,144
$$

**Ответ:**  
$$|A|_9 = 7\,558\,144$$
