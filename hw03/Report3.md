# hw3

### 1 Question

​	在球坐标系(𝜌，𝜃，𝜑)下，产生上半球面上均匀分布的随机坐标点，给出其直接抽样方法。

### 2 Method

​	设 $p(\theta,\varphi)$是球面上均匀的概率密度分布函数，**以球坐标为系**，半径r=1，那么有上
$$
\int pds=\int^{2\pi}_{0}\int^{\pi/2}_0 p(\theta,\varphi)\sin\theta d\theta d\varphi=1
$$
解出 $p(\theta,\varphi )=1/2\pi$

​	那么对于 $(\theta,\varphi)$来说，符合的概率密度函数为
$$
g(\theta,\varphi)=\frac{sin\theta}{2\pi}=\sin\theta\times\frac{1}{2\pi}=f(\theta)\times h(\varphi)
$$
​	对 $(\theta,\varphi)$进行直接抽样法抽样：

​	$\theta$的累积函数 $F(\theta)$为
$$
F(\theta)=\int^{\theta}_0{\sin t}dt={1-\cos\theta}
$$
​	故为了得到 $\theta$的抽样值，需要先得到(0，1）上均匀分布的 $\xi_1$，然后根据直接抽样法

$$
\theta = \arccos(1-\xi_1)
$$
​	而 $\varphi $的分布可由（0，1）上均匀分布 $\xi_2$得到
$$
\varphi = 2\pi \xi_2
$$

### 3 Experiment

​	根据以上方法，抽样出 $(\theta,\varphi)$ ，根据坐标公式转化
$$
x=\sin\theta\cos\varphi\\
y=\sin\theta\sin\varphi\\
z=\cos \theta
$$
​	可得绘制出上半球面的均匀分布图像

![](F:\MyDocuments\Physics\Computational Physics\Homework\hw03\球面均匀分布.png)

### 4 Summary

​	通过把球面上的均匀分布转换为以$𝑓(\theta) = \sin\theta~ (\theta \in (0, \pi)$为概率密度的 $\theta $，以及在$(0, 2\pi)$上均匀分布的 $\varphi $ 的联合分布得到了球面上均匀分布点的生成方式。最后根据直接抽样法，通过 $\theta = \arccos(1-\xi_1)$和 $\varphi = 2\pi \xi_2$的方式，抽样得到分布。
