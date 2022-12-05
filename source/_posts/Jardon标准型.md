---
title: Jordan标准型
tags: 矩阵论
categories: 
    - 数学
    - 矩阵论
---

## Jordan标准型

![Jordan标准型定义](/img/矩阵论/Jordan标准型定义.png)

其中 $J_1(\lambda_1),J_2(\lambda_2)$分别构成Jardon块。

即对任意矩阵 $A$，比存在n阶可逆矩阵$P$，使
$$P^{-1}AP=\begin{bmatrix}
    J_1 & & & \\ & J_2 & & \\ & & \ddots & \\ & & & J_n
\end{bmatrix} = J$$

每一个 $J$ 都是Jardon块
$$J_i=\begin{bmatrix}
    \lambda_i & 1 & & \\ & \lambda_i & \ddots & & \\ & & \ddots &1 \\ & & & \lambda_i
\end{bmatrix}$$


### Jordan标准型的结构与结论
- Jordan标准型的个数$k$是线性无关特征向量的个数
- 矩阵可对角化当且仅当$k=n$
- 相应于一个已知特征值的Jordan块的个数是该特征值的几何重数，它是相应的特征子空间的维数，相应于一个已知特征值的所有Jordan的阶数之和，是该特征值的代数重数
- 特征值的几何重数 < 代数重数
- 矩阵不同特征值对应的特征向量线性无关

![定理2](/img/矩阵论/Jordan标准型定理2.png)