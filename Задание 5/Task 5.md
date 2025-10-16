# Дано

## Вариант 1

$$    
A =     
 \begin{pmatrix}    
  -8 & 1 & 0 & \cdots & 0 & 0 \\    
  15 & -8 & 1 & \cdots & 0 & 0 \\    
  0 & 15 & -8 & \cdots & 0 & 0 \\    
  \vdots  & \vdots & \vdots & \ddots & \vdots & \vdots  \\    
  0 & 0 & 0 & \cdots & -8 & 1 \\    
  0 & 0 & 0 & \cdots & 15 & -8     
 \end{pmatrix}    
$$

Порядок матрицы *n* = 8

# Решение

## Вывод рекуррентного соотношения

$$    
|A| =     
  -8 *
 \begin{vmatrix}    
  -8 & 1 & \cdots & 0 & 0 \\    
  15 & -8 & \cdots & 0 & 0 \\    
  \vdots & \vdots & \ddots & \vdots & \vdots  \\    
  0 & 0 & \cdots & -8 & 1 \\    
  0 & 0 & \cdots & 15 & -8     
 \end{vmatrix} 
 -1 *
 \begin{vmatrix}    
  15 & 1 & \cdots & 0 & 0 \\    
  0 & -8 & \cdots & 0 & 0 \\    
  \vdots  & \vdots & \ddots & \vdots & \vdots  \\    
  0 & 0 & \cdots & -8 & 1 \\    
  0 & 0 & \cdots & 15 & -8     
 \end{vmatrix}  
$$

$$    
|A| =     
  -8 *
 \begin{vmatrix}    
  -8 & 1 & \cdots & 0 & 0 \\    
  15 & -8 & \cdots & 0 & 0 \\    
  \vdots & \vdots & \ddots & \vdots & \vdots  \\    
  0 & 0 & \cdots & -8 & 1 \\    
  0 & 0 & \cdots & 15 & -8     
 \end{vmatrix} 
 -1 * 15
 \begin{vmatrix}    
  -8 & \cdots & 0 & 0 \\    
  \vdots & \ddots & \vdots & \vdots  \\    
  0 & \cdots & -8 & 1 \\    
  0 & \cdots & 15 & -8     
 \end{vmatrix} 
$$

Таким образом получаем рекуррентное соотношение: |A| = -8 * |A|<sub>n-1</sub> - 15 * |A|<sub>n-2</sub>

## Составление и решение характеристического уравнения

$\lambda$<sup>n</sup> = -8 $\lambda$<sup>n-1</sup> - 15 $\lambda$<sup>n-2</sup> 

$\lambda$<sup>2</sup> + 8 $\lambda$ + 15 = 0

$\lambda$<sub>1</sub> + $\lambda$<sub>2</sub> = -8 , $\lambda$<sub>1</sub> * $\lambda$<sub>2</sub> = 15

$\lambda$<sub>1</sub> = -5 , $\lambda$<sub>2</sub> = -3

## Составление общей формулы

$\lambda$<sub>1</sub> $\neq$ $\lambda$<sub>2</sub> , следовательно:

|A|<sub>n</sub> = a * (-5)<sup>n</sup> + b * (-3)<sup>n</sup>

### Найдем константы

Так как последовательность глубиной 2, она определяется двумя последовательными элементами.

|A|<sub>1</sub> = -8 , |A|<sub>2</sub> = 49

$$
\begin{cases}
-8 = a * (-5) + b * (-3) \\
49 = a * (-5)<sup>2</sup> + b (-3)<sup>2</sup>
\end{cases}
$$

$$
+
\begin{cases}
-8 = a * (-5) + b * (-3) | -3 \\
49 = a * (-5)<sup>2</sup> + b (-3)<sup>2</sup>
\end{cases}
$$

$$
25 = 10a + 0
$$

Таким образом, a = 2,5; b = -1,5

|A|<sub>n</sub> = 2,5 * (-5)<sup>n</sup> - 1,5 * (-3)<sup>n</sup>

## Найдем определитель 8 порядка

|A|<sub>8</sub> = 2,5 * (-5)<sup>8</sup> - 1,5 * (-3)<sup>8</sup> = 966 721
