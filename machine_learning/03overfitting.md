### 不同拟合程度

![image-20230427214628455](D:\Personal\AI_notes\machine_learning\assets\image-20230427214628455.png)

### 解决过拟合方法

1. 收集更多数据。
2. 去掉无关特征项，可能去掉有用特征。
3. 正则化（Regularization） 减小多项式参数，不会完全消除特征，但可以降低无用特征的影响。

### 正则化

对cost function添加系数项，来保证系数不会过大，并且通常对所有系数同时添加，此时cost function的形式为：
$$
J(\vec{w},b)=\frac{1}{2m}\sum_{i=1}^{m}(f_{\vec{w}, b}(\vec{x}^{(i)})-y^{(i)})^2+\frac{\lambda}{2m}\sum_{j=1}^{n}w_{j}^{2}
$$
进行梯度下降时，公式保持不变：
$$
repeat\{\\&
w_j=w_j-\alpha\frac{\partial}{\partial{w_j}}J(\vec{w},b)\\&
b=b-\alpha\frac{\partial}{\partial{b}}J(\vec{w},b)\\
\}
$$
其中一般不对b进行正则化，只需关注w：
$$
w_j=w_j-\alpha\{\frac{1}{m}\sum_{i=1}^m[(f_{\vec{w},b}(\vec{x}^{(i)})-y^{(i)})x_j^{(i)}]+\frac{\lambda}{m}w_j\}
$$
提出公共项w后：
$$
w_j=w_j(1-\alpha\frac{\lambda}{m})-\frac{1}{m}\sum_{i=1}^m[(f_{\vec{w},b}(\vec{x}^{(i)})-y^{(i)})x_j^{(i)}]
$$
$1-\alpha\frac{\lambda}{m}$是个略小于1的数，因此正则化会在每次递归时缩小$w_j$的值。

