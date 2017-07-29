# Deep Learning 学习笔记（一）——线性代数

##　一、标量、向量、矩阵和张量

1. **标量** (scalar):标量就是单独的一个书，通常用斜体小写字母表示，比如$s\in \mathbb{R}$

2. **向量**(vector): 一个向量就是有序排列的一列数，通常用一个小写黑体表示一个列向量，向量的第一个元素是$x_1$ ，通常采用如下形式标明类型，比如，向量$x$,有$n$个元素，每个元素都属于$\mathbb{R}$，可记为$\textbf{x}\in\mathbb{R}^n$,用下标表示集合中的元素，用－表示相应元素的补集，通常书写成一个列向量：
   $$
   \textbf{x}=
   \begin{bmatrix}
   x_1 \\
   x_2\\
   \vdots\\
   x_n
   \end{bmatrix}
   $$
   ​

3. **矩阵**(matix):矩阵是一个二二维数组，通常用大写黑体表示，如$\textbf{A}$ ,如果矩阵的高度为$m$, 宽为$n$,则$\textbf{A} \in \mathbb{R}^{m×n}$,用$A_{i,j}$表示第$i$行$j$列的元素，用$:$表示一整行或一整列。

4. **张量**(tensor)：超过两维的数组。

5. **转置**(transpose)：矩阵的转置是以对角线为轴的镜像，将矩阵$\textbf{A}$的转置表示为$\textbf{A}^\mathrm{T}$ ,定义如下:
   $$
   (A^{\mathrm{T}})_{i,j}=A_{j,i}
   $$

6. 两个形状一样的矩阵，可以相加，即将对应位置的元素相加，比如$C=A+B,其中Ｃ_{i,j}=A_{i,j}+B_{i,j}$ 

7. 标量和矩阵相乘或相加，只需将标量与矩阵的每个元素相乘或相加，比如$D=a*B +C$,其中$D_{i,j}=a*B_{i,j}+c$

8. 还有一种成为**广播**的的方式，即隐式的复制向量的元素为一个矩阵，比如$\textbf{C}=\textbf{A}+\textbf{b}$,其中$C_{i,j}=A_{i,j}+b_j$

## 二、矩阵和向量相乘

1. 两个矩阵$\textbf{A}和\textbf{B}$ 的**矩阵乘积**(matrix product)是第三个矩阵，他们要满足，矩阵$\textbf{A}$的列数必须和$\textbf{B}$的行数相等，如果　$\textbf{A}\in \mathbb{R}^{m×ｎ}，\textbf{B}\in \mathbb{R}^{n×ｐ}则\textbf{C}\in\mathbb{R}^{m×ｐ}$，记为:
   $$
   \textbf{C}=\textbf{A}\textbf{B}
   $$
   其中:
   $$
   \textbf{C}_{i,j}=\sum_{k}\textbf{A}_{i,k}\textbf{B}_{k,j}
   $$

2. 如果将两个形状相同的矩阵对应位置的元素相乘，这种方式称为**元素对应乘积**（ｅｌｅｍｅｎｔ-wise product)或者**Hadamard　乘积**(Hadamard product),记为$\textbf{A}\odot\textbf{B}$

3. 两个维数相同的向量$\textbf{x}和\textbf{y}$的点积是一个数，可看做矩阵乘积$\textbf{x}^\mathrm{T}\textbf{y}$

4. 矩阵成绩常见性质

   * 分配律:$\textbf{A}(\textbf{B}+\textbf{C})=\textbf{A}\textbf{B}+\textbf{A}\textbf{C}$
   * 结合律:$\textbf{A}(\textbf{B}\textbf{C})=(\textbf{A}\textbf{B})\textbf{C}$
   * 点乘的交换律:$x^\mathrm{T}y=y^\mathrm{T}x$
   * $(\textbf{A}\textbf{B})^{\mathrm{T}}=\textbf{B}^\mathrm{T}\textbf{A}^\mathrm{T}$

5. 线性方程组表示为:
   $$
   \textbf{A}\textbf{x}=\textbf{b}
   $$


## 三、 单位矩阵和逆矩阵

