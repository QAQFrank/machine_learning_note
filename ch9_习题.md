9.1

对于闵可夫斯基距离 $(\sum_{u=1}^n|x_{iu}-x_{ju}|^p)^{\frac1p}$，显然满足非负性，同一性和对称性。

设 $x_i$,，$x_j$，$x_k$：
$dist_{mk}(x_i, x_j)=(\sum_{u=1}^n|x_{iu}-x_{ju}|^p)^{\frac1p}$

$dist_{mk}(x_i, x_k)=(\sum_{u=1}^n|x_{iu}-x_{ku}|^p)^{\frac1p}$

$dist_{mk}(x_j, x_k)=(\sum_{u=1}^n|x_{ju}-x_{ku}|^p)^{\frac1p}$

$p\geq1$时，$(\sum|x_iu-x_ku|^p)^{\frac1p}+(\sum|x_ju-x_ku|^p)^{\frac1p} \geq (\sum|x_iu-x_ju|^p)^{\frac1p}$，直递性成立；

$p\leq1$时，$(\sum|x_iu-x_ku|^p)^{\frac1p}+(\sum|x_ju-x_ku|^p)^{\frac1p} \leq (\sum|x_iu-x_ju|^p)^{\frac1p}$，直递性不成立；

当$p\to\infty$, $\sum_{u=1}^n(\frac{|x_iu-x_ju|}{\max_u|x_iu-x_ju|})^p=1$
$\lim_{p\to\infty}(\sum_{u=1}^n|x_iu-x_ju|^p)^{\frac1p}=(\max_u|x_iu-x_ju|)\lim_{p\to\infty}(\sum_{u=1}^n(\frac{|x_iu-x_ju|}{\max_u|x_iu-x_ju|})^p)^{\frac1p}=\max_u|x_iu-x_ju|$;

9.6

最小距离是扩大半径直到遇到第一个其他类的点时合并这两个类；最大距离是扩大半径直到包含另一个其他类的全部样本时合并这两个类.

10.5

投影矩阵正交说明投影的各个属性之间线性无关，互不影响，降维和重构变换计算方便，但是降维时丢弃的维度无法通过其他维度基的线性组合来表示。

10.9

首先对新样本在训练集中确定其k近邻, 由于LLE假设了局部性, 所以只要利用这k+1个数据来做接下来的LLE算法运算而不用重新计算整个数据集.

11.8

$x_{k+1}=argmin_x \frac{L}{2}(x-z)^2+\lambda|x|$
 
令等式右边的目标函数为g(x)，对其求导有：

$g^\prime(x)=L(x-z)+\lambda \text{sign}(x)$

分情况讨论可得结果。

11.9

字典学习使样本转化为稀疏表示的形式，是为了利用稀疏性来使学习任务得到简化，使模型的复杂度得到降低，从而可以学习到一个对于当前的学习任务比较好的一个学习器。
而压缩感知主要是想利用信号本身所具有的稀疏性，从而实现从部分观测样本中恢复出原始信号的目的。 
