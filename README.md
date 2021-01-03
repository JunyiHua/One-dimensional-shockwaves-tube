# One-dimensional-shockwaves-tube

thesis for applying the Bachelor Degree

[TOC]



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

对于一个一阶偏微分方程$\frac{\partial\rho}{\partial t}+c^2\frac{\partial \rho}{\partial x}=0$，即一维的对流（质量守恒）方程，其初值问题即一阶的柯西问题。为了将其转为双曲型的二阶波动方程以方便使用行波法的达朗贝尔公式，故将$\rho$表示为势函数的偏导数$\frac{\partial\psi}{\partial x}$，此时可以将$\rho$理解为速度。方程被化为
$$
\frac{\partial^2\psi}{\partial t^2}=c_0^2\frac{\partial^2\psi}{\partial x^2}
$$
直接运用达朗贝尔公式，得到解函数的形式为$\psi=F(x-c_0t)+G(x+c_0t)$，其中F，G的形式由初始条件和边界条件确定。



### 特征线的流体力学图景

数学上，二元函数的偏微分方程组沿特征线可以化为常微分方程组，使得问题的求解得以简化；

物理上，特征线是扰动的传播轨迹。因此利用特征线可以看出问题的初边值条件如何影响流场的发展，从而有效地分析流场，获得清晰的物理图像。

特征线的存在只与偏微分方程的性质有关，双曲型方程有两个特征线，抛物型方程有一个特征线，椭圆型方程没有特征线，而与小扰动的存在与否无关。存在的小扰动必然沿着特征线传播，沿着特征线传播的不只是小扰动。沿着特征线物理量可能变化也可能不变化，状态量的变化与否由特征关系（将特征线方程代回偏微分方程得到的特征方程）决定。

综合地说：小扰动沿着特征线传播；小扰动以声波传播；声波轨迹与特征线一致。

在二维流动中，特征线就是马赫线。接下来在二维流动中讨论微分方程的分类和特征线。

#### 二维流动中的特征线



#### 流体力学中的特征线总结

从特征线的一般解法可以明确特征线的特点：

1. 作为微分方程解的特征线
   偏微分方程解的积分曲面可以由无限多数目的曲线构建而成。若是这些曲线是沿着积分曲面的特征线选择，则曲线在自变量上平面上的投影就是特征线，曲线本身对应了特征方程。
2. 流体力学中的特征线
   特征线是流体状态量的导数（一阶微商）可能不连续的点的轨迹，即若间断线。弱间断是指物理量本身不间断，其微商或导数发生间断。（强间断是指物理量本身发生间断）
3. 特征线与冲击波
   一维不定常流动中特征线是扰动传播的轨迹，二维定常超声速流动中的特征线是马赫线，冲击波是强间断。在特征线上，流体状态量本身是连续的，但它们的导数可能不连续。在冲击波阵面上，流体速度、压力等状态量不连续。

特征线的性质归纳如下：

1. 在连续流动区域，同族特征线不相交；
2. 弱间断只沿特征线传播；
3. 相邻的不同类型（平衡）流动区域，其分界线是特征线。

对于一般超声速流动和非定常流动，因为存在以弱间断为特征的特征线，因此，以特征线为界划分了具有不同流动特性的流场。波传播可能造成不同的流动特性，具有不同特性的流场将有不同的解的表达式。一般难以找到能描述全流场的统一形式，这从某一角度说明了波传播过程中引起的局部化效应。

## 热力学基础

### 热力学量

### 热力学函数

## 一维流体力学基本方程

### 守恒型和非守恒型欧拉方程

### 欧拉方程的微分形式

### 欧拉方程的积分形式

### 欧拉方程组的特征方程

#### 特征方程的推导

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

将三族特征线分别记为$C_{+},C_{-},C_0$。沿着特征线$C_{\pm}$，表示一组物理量的组合是常量，其本质是牛顿第三定律；而沿着特征线$C_0$，熵值不变，但是不同的$C_0$上熵值可能不同。对于均熵的绝热流动或者等熵流动，等熵条件在各处满足，此时这一族特征线也就没有了考虑的必要，即均熵条件下考虑两族特征线，非均熵条件下考虑三族特征线。

> 特征线的另外一个定义是：对于双曲型方程组，在$(x,t)$平面上有这样一组曲线，在这些曲线上，给定任意物理参数的值作为柯西问题的初始值（柯西问题的初始值是一阶微商），这样柯西问题的解一般是不存在的，这些曲线就称为方程组的特征曲线。
>
> 现在考虑另外一个思路，通过构造线性方程组去解欧拉方程组
> $$
> \left\{
> \begin{array}{rcl}
> \frac{\partial\rho}{\partial t}+u\frac{\partial\rho}{\partial x}+\rho\frac{\partial u}{\partial x}=0\\
> \frac{\partial u}{\partial t}+u\frac{\partial u}{\partial x}+\frac{1}{\rho}\frac{\partial p}{\partial x}=0\\
> \frac{\partial S}{\partial t}+u\frac{\partial S}{\partial x}=0
> \end{array}
> \right.
> $$
> 设特征曲线$x=x(t)$，要在特征线上求出各个物理量的一级微商的解，做如下操作。
>
> 引入热力学状态函数$p=f(\rho,S)$，将状态量$p$用$\rho,S$替代表示，有$\frac{\partial p}{\partial x}=\frac{\partial p}{\partial\rho}\frac{\partial\rho}{\partial x}+\frac{\partial p}{\partial S}\frac{\partial S}{\partial x}$。
>
> 再引入以下一组全微分
> $$
> \left\{
> \begin{array}{rcl}
> d\rho=\frac{\partial \rho}{\partial t}dt+\frac{\partial \rho}{\partial x}dx\\
> du=\frac{\partial u}{\partial t}dt+\frac{\partial u}{\partial x}dx\\
> dS=\frac{\partial S}{\partial t}dt+\frac{\partial S}{\partial x}dx
> \end{array}
> \right.
> $$
> 将以上关系式相互代入、联立得到线性方程组
> $$
> \left(\begin{array}{cc}
> 1 & 0 & 0 & u & \rho & 0\\
> 0 & \rho & 0 & p_{\rho} & \rho u & p_S\\
> 0 & 0 & 1 & 0 & 0 & u\\
> dt & 0 & 0 & dx & 0 & 0\\
> 0 & dt & 0 & 0 & dx & 0\\
> 0 & 0 & dt & 0 & 0 & dx
> \end{array}\right)
> \left(\begin{array}{c}
> \frac{\partial \rho}{\partial t}\\
> \frac{\partial u}{\partial t}\\
> \frac{\partial \rho}{\partial x}\\
> \frac{\partial u}{\partial x}\\
> \frac{\partial S}{\partial t}\\
> \frac{\partial S}{\partial x}\\
> \end{array}\right)
> =
> \left(\begin{array}{c}
> 0\\
> 0\\
> 0\\
> d\rho\\
> du\\
> dS\\
> \end{array}\right)
> $$
> 因为是在特征曲线上，一级微商不存在（特征曲线上有弱间断，即一级微商间断不连续，具体见后文间断部分），所以以上线性方程组无解，系数矩阵的行列式为零。
> $$
> \left|\begin{array}{cc}
> 1 & 0 & 0 & u & \rho & 0\\
> 0 & \rho & 0 & p_{\rho} & \rho u & p_S\\
> 0 & 0 & 1 & 0 & 0 & u\\
> dt & 0 & 0 & dx & 0 & 0\\
> 0 & dt & 0 & 0 & dx & 0\\
> 0 & 0 & dt & 0 & 0 & dx
> \end{array}\right|
> =0
> $$
> 即$\rho(udt-dx)^3-\rho p_\rho(udt-dx)dt^2=0$，其中$p_\rho=c^2$，故可以得到特征线族
> $$
> \frac{dx}{dt}=u,u+c,u-c
> $$
> 在特征关系下，原方程组有解（我的理解是，特征线上物理量的一阶微商无解，但是其组合也就是特征关系本身有解，这也就解释了所谓的特征曲线上物理参数之间一定满足相应的特征关系，而所谓的解也就是特征关系等式右侧的那个常数），运用克莱默法则，将等式右侧的矩阵分别带入系数矩阵的第五、六列，令其为零，即得到特征关系式
> $$
> \frac{dx}{dt}=u:dS=0\\
> \frac{dx}{dt}=u\pm t:du\pm\frac{dp}{\rho c}=0
> $$
> 见前文，$\rho c$是空气阻尼，特征关系的本质仍然是等熵绝热和牛顿第三定律。

#### 黎曼不变量

考虑等熵绝热流动，忽略特征线$C_0$，只考虑特征线$C_\pm$，其上有特征关系$\frac{du}{dt}\pm\frac{1}{\rho c}\frac{dp}{dt}=0$，进行如下变换
$$
\frac{du}{dt}\pm\frac{1}{\rho c}\frac{dp}{dt}=0\\
{du}\pm\frac{1}{\rho c}{dp}=0\\
\Rightarrow \int({du}\pm\frac{1}{\rho c}{dp})=Const\\
\Rightarrow u \pm \int(\frac{1}{\rho c}{dp})=Const\\
\Rightarrow^{dp=c^2d\rho} 
\Rightarrow u \pm \int\frac{c}{\rho}{d\rho}=Const
$$
称$\alpha=u + \int\frac{c}{\rho}{d\rho},\beta=u - \int\frac{c}{\rho}{d\rho}$为黎曼不变量，黎曼不变量在特征线上为以常量，其实就是特征关系。

对于$(x,t)$相空间上的每一点，其必然是两条异族特征线的交点。在给定介质与其状态方程的情况下，黎曼不变量可以通过积分解出，从而求出流场中各个物理量的分布，即通过联立两个黎曼不变量并求解来求得$p,\rho,c,s$等物理量。

#### 依赖关系与合适的初边值条件

在$(x,t)$相空间上，当给定一个初始条件后，不妨假设可以得到$t=0$时的两点$A(x_1),B(x_2)$的物理参量，其中$x_1<x_2$，进而得到两组黎曼不变量，分别是$\alpha_0(x_1),\beta_0(x_1);\alpha_0(x_2),\beta_0(x_2)$。那么$A$的$C_+$特征线和$B$的$C_-$特征线必然交于一点$P(x_3,t_3)$，有
$$
\alpha(x_3,t_3)=\alpha_0(x_1)\\
\beta(x_3,t_3)=\beta_0(x_2)
$$
借此可以进一步得到$P$点的所有物理信息。

但是$P$点的黎曼不变量不仅是依靠$A,B$两点的信息，而是线段$\overline{AB}$上所有的信息。或者说，需要$\overline{AB}$的所有信息来确切描述特征线的形象，进而确定点$P$的确切相位。这样，称线段$\overline{AB}$为点$P$的依赖区。

所有能受到线段$\overline{AB}$上点的物理信息的影响的点的集合就是对应的影响区，即在过点$A$的$C_-$特征线和过点$B$的$C_-$特征线之间的区域。考虑到特征线就是小扰动的传播轨迹，由于这一段线段之间的初始扰动始终传不到影响区之外，故影响区两边的特征线被视为扰动波的“波头”轨迹，波头的运动速度分别是$u-c$和$u+c$，即波相对于流体以声速运动。

对于多方气体，即$\gamma=3$，此时$(x,t)$平面上的特征线为直线。

当我们想要得到$(x,t)$空间上一个区域的物理量，就需要给定合适的初始条件和边界条件，使得其影响区能够覆盖所要获取的区域。首先引出“空向线”和“时向线”的概念：若所给曲线上的特征线都在同一侧，这个曲线是空向线；若所给曲线上的两族特征线分布在两边，这个曲线是时向线。如$(x,t)$平面上的$x$轴是空向线，$t$轴是时向线。

对于空向线，边界上必须给定两个量的值（比如$\alpha$和$\beta$）；对于时相线，边界上只需要给定一个量的值，另外一个量将由空向线上相应的特征线带过来。将边界表示在$(x,t)$平面上，分析边界曲线的类别，就知道应当怎样给出合适的边界条件。

## 间断

### 简单波



### 间断问题

### 黎曼问题

## 黎曼问题的迭代法

## 参考文献

- 数学物理方法——顾樵
- 一维不定常流体动力学教程——卢芳云
- 一维非定常流体力学——周毓麟
- 一维流体力学差分方法——水鸿寿
- 超声速流与冲击波——R.柯朗，K.O.弗里德里克斯