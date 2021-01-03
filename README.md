# One-dimensional-shockwaves-tube

thesis for applying the Bachelor Degree

## 张量基础

各类物理量在数学上可以用不同阶的张量来表示。简单的如标量是零阶张量，矢量是一阶张量。

### 张量表示法

零阶张量$x$；

一阶张量$\vec{u}=u_j \vec{i}_j$，其中$\vec{u}=(u,v,w)$；

二阶张量$\sigma _{ij}$，如
$$
\delta_{ij}=\left\{ 
\begin{array}{rcl}
1&i=j\\
0&i\neq j
\end{array}
\right.
$$
三阶张量$\epsilon_{ijk}$，如
$$
e_{ijk}=\left\{ 
\begin{array}{rcl}
1&i,j,k为1,2,3的偶置换\\
0&i,j,k中至少有两者相同\\
-1&i,j,k为1,2,3的奇置换
\end{array}
\right.
$$
用张量表示点乘和叉乘为
$$
\vec{u}\cdot\vec{v}=u_i v_i\\
\vec{h}=\vec{u}\times\vec{v},h_i=e_{ijk}u_j v_k
$$

### 张量表示算子

矢量微分算子$\vec{\bigtriangledown}=\vec{i}_j\frac{\partial}{\partial x_j}$；

梯度$\vec{grad}f=\vec{\bigtriangledown}f$;

散度$div\vec{u}=\vec{\bigtriangledown}\cdot\vec{u}$;

梯度$\vec{rot}\vec{u}=\vec{\bigtriangledown}\times\vec{u}$;

## 特征理论初步

### 偏微分方程分类

双曲型

椭圆型

抛物型

###  特征线法

特征线法是求解非定常连续流动问题的重要方法，参考数学物理方程的行波法。

对于一个一阶偏微分方程$\frac{\partial\rho}{\partial t}+c^2\frac{\partial \rho}{\partial x}=0$，即一维的对流（质量守恒）方程，为了将其转为双曲型的二阶波动方程以方便使用行波法的达朗贝尔公式，故将$\rho$表示为势函数的偏导数$\frac{\partial\psi}{\partial x}$，此时可以将$\rho$理解为速度。方程被化为
$$
\frac{\partial^2\psi}{\partial t^2}=c_0^2\frac{\partial^2\psi}{\partial x^2}
$$
直接运用达朗贝尔公式，得到解函数的形式为$\psi=F(x-c_0t)+G(x+c_0t)$，其中F，G的形式由初始条件和边界条件确定。



### 特征线的流体力学图景

数学上，二元函数的偏微分方程组沿特征线可以化为常微分方程组，使得问题的求解得以简化；

物理上，特征线是扰动的传播轨迹。因此利用特征线可以看出问题的初边值条件如何影响流场的发展，从而有效地分析流场，获得清晰的物理图像。

特征线的存在只与偏微分方程的性质有关，双曲型方程有两个特征线，抛物型方程有一个特征线，椭圆型方程没有特征线，而与小扰动的存在与否无关。存在的小扰动必然沿着特征线传播，沿着特征线传播的不只是小扰动。沿着特征线物理量可能变化也可能不变化，状态量的变化与否由特征关系（将特征线方程代回偏微分方程得到的特征方程）决定。

综合地说：小扰动沿着特征线传播；小扰动以声波传播；声波轨迹与特征线一致。

## 热力学基础

### 热力学量

### 热力学函数

## 一维流体力学基本方程

### 守恒型和非守恒型欧拉方程

### 欧拉方程的微分形式

### 欧拉方程的积分形式

### 欧拉方程组的特征方程

理想流体一维绝热运动的原始方程组欧拉形式为
$$
\left\{
\begin{array}{rcl}
\frac{\partial\rho}{\partial t}+u\frac{\partial\rho}{\partial x}+\rho\frac{\partial u}{\partial x}=0\\
\frac{\partial u}{\partial t}+u\frac{\partial u}{\partial x}+\frac{1}{\rho}\frac{\partial p}{\partial x}=0\\
\frac{\partial S}{\partial t}+u\frac{\partial S}{\partial x}=0
\end{array}
\right.
$$
现在从这一组方程出发，去构造它们的特征方程。

在这一欧拉方程组中涉及到四个热力学量$(p,\rho,u,S)$，但是只有三个方程（质量、动量、能量守恒），所以需要再引入一个状态方程。由于最终研究的问题是黎曼问题，即无黏可压缩的激波管问题，无黏条件下流体动力学过程属于是绝热过程，即等熵过程，考虑热力学关系式$d\rho=(\frac{\partial \rho}{\partial p})_Sdp=\frac{dp}{c^2}$，即小扰动传播（声速）公式$c^2=\frac{\partial p}{\partial \rho}$。分别对对流方程中的$\frac{\partial \rho}{\partial t}$和$\frac{\partial \rho}{\partial x}$变换，有：
$$
\frac{\partial \rho}{\partial t}=\frac{d\rho}{dp}\frac{\partial p}{\partial t}=\frac{1}{c^2}\frac{\partial p}{\partial t}\\
\frac{\partial \rho}{\partial x}=\frac{d\rho}{dp}\frac{\partial p}{\partial x}=\frac{1}{c^2}\frac{\partial p}{\partial x}
$$
带回对流方程中，有
$$
\frac{1}{c^2}\frac{\partial p}{\partial t}+\frac{u}{c^2}\frac{\partial p}{\partial x}+\rho\frac{\partial u}{\partial x}=0
\Rightarrow
\frac{1}{\rho c}\frac{\partial p}{\partial t}+\frac{u}{\rho c}\frac{\partial p}{\partial x}+c\frac{\partial u}{\partial x}=0
$$
此时得到新的欧拉方程组
$$
\left\{
\begin{array}{rcl}
\frac{1}{\rho c}\frac{\partial p}{\partial t}+\frac{u}{\rho c}\frac{\partial p}{\partial x}+c\frac{\partial u}{\partial x}=0\\
\frac{\partial u}{\partial t}+u\frac{\partial u}{\partial x}+\frac{1}{\rho}\frac{\partial p}{\partial x}=0\\
\frac{\partial S}{\partial t}+u\frac{\partial S}{\partial x}=0
\end{array}
\right.
$$
质量守恒式和动量守恒式分别相加减，得到
$$
(\frac{\partial u}{\partial t}+(u\pm c)\frac{\partial u}{\partial x})\pm
\frac{1}{\rho c}(\frac{\partial p}{\partial t}+(u\pm c)\frac{\partial p}{\partial x})=0
$$
这恰是两个一阶振动偏微分方程的线性组合，不难得到其特征线方程$\frac{dx}{dt}=u\pm c$，对应的特征线的关系式为$\frac{du}{dt}\pm\frac{1}{\rho c}\frac{dp}{dt}=0$。

至于第三个能量守恒式，很显然就能得到其特征线$\frac{dx}{dt}=u$和特征关系$\frac{dS}{dt}=0$，即等熵绝热。

将三族特征线分别记为$C_{+},C_{-},C_0$。沿着特征线$C_{\pm}$，表示一组物理量的组合是常量，其本质是牛顿第三定律；而沿着特征线$C_0$，熵值不变，但是不同的$C_0$上熵值可能不同。对于均熵的绝热流动或者等熵流动，等熵条件在各处满足，此时这一族特征线也就没有了考虑的必要。

## 间断

### 简单波

### 间断问题

### 黎曼问题

## 黎曼问题的迭代法

