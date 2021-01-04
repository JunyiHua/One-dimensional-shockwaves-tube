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

### 可约双曲型方程组

考虑关于两个因变量$u,v$和两个自变量$x,y$的一阶双曲型方程组
$$
L_1=A_1\frac{\partial u}{\partial x}+B_1\frac{\partial u}{\partial y}+C_1\frac{\partial v}{\partial x}+D_1\frac{\partial v}{\partial y}+E_1=0\\
L_1=A_2\frac{\partial u}{\partial x}+B_2\frac{\partial u}{\partial y}+C_2\frac{\partial v}{\partial x}+D_2\frac{\partial v}{\partial y}+E_2=0
$$
其中的系数都是$(u,v,x,y)$的函数。当$E_1=E_2=0$，方程组就是一阶双曲型齐次方程组，在此基础上当系数$A,B,C,D$都只是依赖于$(u,v)$时，这个方程组就称为可约方程组。

当雅各比矩阵的行列式
$$
||J||=||\frac{\partial(u,v)}{\partial(x,y)}||=
\left|\begin{array}{rcl}
\frac{\partial u}{\partial x} & \frac{\partial u}{\partial y}\\
\frac{\partial v}{\partial x} & \frac{\partial v}{\partial y}
\end{array}\right|
$$
非零时，方程组就是一个线性方程组，能够通过变换实现$(u,v)$和$(x,y)$的位置对调，此时函数图像就能实现从$(u,v)$平面向$(x,y)$平面的映射。

对于方程组
$$
A_1\frac{\partial u}{\partial x}+B_1\frac{\partial u}{\partial y}+C_1\frac{\partial v}{\partial x}+D_1\frac{\partial v}{\partial y}=0\\
A_2\frac{\partial u}{\partial x}+B_2\frac{\partial u}{\partial y}+C_2\frac{\partial v}{\partial x}+D_2\frac{\partial v}{\partial y}=0
$$
有
$$
\left\{\begin{array}{cc}
1=\frac{du}{du}=\frac{\partial u}{\partial x}\frac{\partial x}{\partial u}+\frac{\partial u}{\partial y}\frac{\partial y}{\partial u}\\
0=\frac{dv}{du}=\frac{\partial v}{\partial x}\frac{\partial x}{\partial u}+\frac{\partial v}{\partial y}\frac{\partial y}{\partial u}
\end{array}\right.
\Rightarrow
\left\{\begin{array}{cc}
\frac{\partial v}{\partial x}=-J\frac{\partial y}{\partial u} & \frac{\partial v}{\partial y}= J\frac{\partial x}{\partial u} \\
\frac{\partial u}{\partial x}= J\frac{\partial y}{\partial v} & \frac{\partial u}{\partial y}= J\frac{\partial x}{\partial v}
\end{array}\right.\\
$$
即
$$
\left|\begin{array}{rcl}
\frac{\partial u}{\partial x} & \frac{\partial u}{\partial y}\\
\frac{\partial v}{\partial x} & \frac{\partial v}{\partial y}
\end{array}\right|=
J\left|\begin{array}{rcl}
\frac{\partial y}{\partial v} & -\frac{\partial x}{\partial v}\\
-\frac{\partial y}{\partial u} & \frac{\partial x}{\partial u}
\end{array}\right|
$$
故而
$$
A_1\frac{\partial y}{\partial v}-B_1\frac{\partial x}{\partial v}-C_1\frac{\partial y}{\partial u}+D_1\frac{\partial x}{\partial u}=0\\
A_2\frac{\partial y}{\partial v}-B_2\frac{\partial x}{\partial v}-C_2\frac{\partial y}{\partial u}+D_2\frac{\partial x}{\partial u}=0
$$
以上变换都是建立在雅各比行列式非零的前提上。

从以上内容出发，有关于特征线与特征关系的推论：在$(x,y)$平面上，有两组特征曲线，这两组曲线是依赖于解$u(x,y),v(x,y)$的，在每一条特征线上有一个特征关系式；在$(u,v)$平面上，也有两组特征曲线，这两组曲线不依赖于$x(u,v),y(u,v)$，而且这两组曲线恰好是$(x,y)$平面上的相应特征线的特征关系。

下面考虑一维的平面等熵运动方程组
$$
\frac{\partial\rho}{\partial t}+u\frac{\partial \rho}{\partial x}+\rho\frac{\partial u}{\partial x}=0\\
\rho\frac{\partial u}{\partial t}+\rho u\frac{\partial u}{\partial x}+\frac{\partial p}{\partial x}=0\\
p=f(\rho)
$$
记$l(\rho)=\int\frac{\sqrt{f'(\rho)}}{\rho}d\rho$。此时在$(x,t)$平面上，特征线方程为$\frac{dx}{dt}=u\pm c$，特征关系式为$u\pm l(\rho(c))=Const$；在$(u,c)$平面上，特征线方程为$u\pm l(\rho(c))=Const$与$x(u,c),y(u,c)$无关，特征关系为$\frac{dx}{dt}=u\pm c$。

约定两个祥平面上的特征线的变换关系$(C_+,C_-)\rightarrow(\Gamma_+,\Gamma_-)$。

### 简单波

> 考虑问题：用特征线法求解绝热流动问题。
>
> 解析解：
>
> 理想气体情况，状态方程形式为$p=(\gamma-1)\rho e$，或$e=\frac{pv}{\gamma -1},\gamma>1$。
>
> 利用热力学关系式$Tds=de+pdv=\frac{1}{\gamma-1}(vdp+\gamma pdv)$，在等熵线情况下，压力和密度$\rho=\frac1v$的函数关系满足
> $$
> vdp+\gamma pdv=0\\
> \frac{dp}{p}+\frac{\gamma dv}{v}=0
> $$
> 积分后，有$p=Av^{-\gamma}=A\rho^{\gamma}$，其中$A(s)=Be^{\frac{S-S_0}{c_V}},B$为积分常数。
>
> 此时声速满足$c^2=\gamma A\rho^{\gamma-1}=\frac{\gamma p}{\rho}=\gamma pv=\gamma(\gamma-1)e$。对两端同时求导有
> $$
> 2cdc=\gamma pdv+\gamma vdp=(\gamma-1)vdp\\
> \Rightarrow \frac{dp}{\rho c}=\frac{2}{\gamma-1}dc
> $$
> 进而有关于黎曼不变量
> $$
> \alpha=u+l(p)=u+\int\frac{dp}{\rho c}=u+\frac{2}{\gamma-1}c\\
> \beta=u-l(p)=u-\int\frac{dp}{\rho c}=u-\frac{2}{\gamma-1}c
> $$
> 将黎曼不变量进行简单的变换得到
> $$
> u=\frac{\alpha+\beta}2\\
> c=\frac{\gamma-1}{4}(\alpha-\beta)
> $$
> 那么，对于多方气体，沿着特征线$C_+$，有$\frac{dx}{dt}=u+c=\frac{\alpha+\beta}{2}+\frac{\gamma-1}{4}(\alpha-\beta)$；沿着$C_-$特征线，有$\frac{dx}{dt}=u-c=\frac{\alpha+\beta}{2}-\frac{\gamma-1}{4}(\alpha-\beta)$。且$C_+$上$\alpha=Const,\beta\neq Const$，$C_-$反之。
>
> 将$u,c$和两条特征线联立就可以得到$u(x,t)$和$c(x,t)$，但是当特征线非直线时无法得到形式简单的解析解。
>
> 数值解：
>
> 借用解析解中最后的特征线表达式，有
> $$
> C_+:x-x_k=[\frac{\alpha_k + \beta_k}{2}+\frac{\gamma-1}{4}(\alpha_k - \beta_k)](t-t_k)\\
> C_-:x-x_{k+1}=[\frac{\alpha_{k+1}+\beta_{k+1}}{2}-\frac{\gamma-1}{4}(\alpha_{k+1}-\beta_{k+1})](t-t_{k+1})
> $$
> 且在$P$点处$u=\frac{\alpha_k+\beta_{k+1}}{2},c=\frac{\gamma-1}{4}(\alpha_k-\beta_{k+1})$。
>
> 对于这类可约双曲型方程组，写出关系式$x(c,u),t(c,u)$比得到结果$u(x,t),c(x,t)$更加容易。因此对于这样的方程组，常常适用反函数求解的方法，即先在$(u,c)$平面上解得$x,t$，再反解出结果$u,c$。详细见等熵流动通解部分。

考虑理想气体状态方程$p=(\gamma -1)\rho e,\gamma>1$，黎曼不变量表示为
$$
\alpha=u+l(p)=u+\int\frac{dp}{\rho c}=u+\frac{2}{\gamma-1}c\\
\beta=u-l(p)=u-\int\frac{dp}{\rho c}=u-\frac{2}{\gamma-1}c
$$
参见特征线部分内容，解的各级微商的间断线都在特征线上，并且不同解析性质区域（如常数区域，非常数区域）的分界线也应该是特征线。

在$(x,t)$区域上若是存在这样一个区域，此区域上的特征线经过变换到$(u,v)$平面上后得到新的特征线，即$(C_+,C_-)\rightarrow(\Gamma_+,\Gamma_-)$，而且有且只有一条$\Gamma_\pm$（或关系），那么这个区域就被称为是简单波区。换言之，在简单波区至少有一个特征关系（$(x,y)$平面）是常数。

特征关系正是黎曼不变量的表达式！

将两个黎曼不变量作为判据，可以将$(x,t)$区域划分为几个区域：

#### 常数状态区

在此区域内，两个黎曼不变量均保持不变，即$\alpha\equiv \alpha_0,\beta\equiv\beta_0$。

此时包括$u,c$在内的所有物理量都是常数。
$$
u=\frac12 (\alpha_0+\beta_0);c=\frac{\gamma-1}4 (\alpha_0-\beta_0)
$$

#### 简单波区

在此区域内，有且只有一个黎曼不变量保持常数。

1. $\alpha\equiv\alpha_0$
2. $\beta\equiv\beta_0$

通过简单分析，可以知道

1. 简单波中有一族特征线是直线
2. 与常流区域相邻区域中的等熵流动必定是简单波；反之只有简单波区才会与常流区域相邻
3. 简单波是单向行波
4. 简单波的传播速度随着流体质点的速度增加而增加

常流区与简单波区的分界线是特征线，若流体进入简单波区时穿过它，则该特征线是波头；反之若流体离开简单波区时穿过它，则该特征线是波尾。波头和波尾均沿着特征线传播。

简单波可以分为向前（右行）简单波和向后（左行）简单波，分别以速度$u+c,u-c$传播。对于向前波，$C_+$特征线是直线；对于向后波，$C_-$波是直线。

简单波是单向波，根据波前后状态的变化将其分为稀疏波（压力和密度减小）和压缩波（压力和密度增加）。在压缩波区，特征线沿着时向收聚，在稀疏波区则是特征线沿着时向发散，至于沿着空向的特征线变化趋势，则要看流体是穿过了向前的还是向后的压缩波或稀疏波。

压缩波的发展会导致间断的发生（多值点出现），稀疏波的发展不会出现间断。

#### 中心稀疏波区

这是特殊的简单波区，在这个区域中有一族特征线是一族中心直线族，该族特征线都是从同一点发出的射线。中心稀疏波包括向左稀疏波和向右稀疏波。

1. 向左中心稀疏波
   $C_-$特征线族是中心直线族。若取原点为中心，则$C_-$特征线为$\frac xt  = u-c$。
2. 向右中心稀疏波
   $C_+$特征线族是中心直线族。若取原点为中心，则$C_+$特征线为$\frac xt=u+c$。

作为特殊的简单波的中心稀疏波的出现，其实质在于$u$。$u=u(x,t)$本是一个变量，当$u=at$，即变速运动时，特征线可能不是直线，简单波区和常数区的分离点不一定是中心点；而当$u$是匀速时，简单波区和常数区的分离点就是中心点，简单波区的特征线是直线且都从中心出发，此区域也就是中心稀疏波区。但是不可能存在中心压缩波区，因为间断早在中心处就出现，此后根本不会再出现简单波。

> 考虑一维的活塞运动问题

### 间断问题

在讨论简单波时，已经指出，简单波区中有一族特征直线族，物理状态沿着这些特征直线传播。在稀疏情况，这些特征直线是发散的，随着时间推移，不同特征直线之间间隔边随之增大。在压缩波情况，这些特征直线是收敛的，不同特征直线之间的空间间距随着时间的发展而不断缩小，发展下去很可能发生同族特征直线相交的现象。在同族特征直线的交点处，物理状态已经不可能单一确定，连续可微的物理量分布已经不可能再继续存在。因此需要考虑含有间断的解。

流体力学方程组是质量、动量、能量守恒的表现形式。既然在间断处微商不存在，那么就不适合用微分方程描述此守恒律，反之可以借助积分方程对间断进行分析。
$$
[\rho]D-[\rho u]=0\\
[\rho u]D-[\rho u^2+p]=0\\
[\rho E]D-[\rho Eu+pu]=0
$$
其中$D=\frac{dx}{dt}$表示间断的运动速度，$[f]=f_2-f_1$表示两侧差值。以上方程组就是间断线两侧的物理量满足的间断关系式。

进一步地，可以将间断关系式改写为
$$
m[v]=-[u]\\
m[u]=[p]\\
m[E]=[pu]
$$
借助间断关系式讨论间断的分类

1. 接触间断
   当$m=0$时，间断两侧没有物质交换，这种间断称为接触间断，关系式退化为
   $$
   \left\{\begin{array}{rcl}
   [u]=0\\
   [p]=0
   \end{array}\right.
   \Rightarrow
   \left\{\begin{array}{rcl}
   u_1=u_2=D\\
   p_1=p_2
   \end{array}\right.
   $$
   即间断两侧速度连续且与间断速度一致，间断两侧压力连续。

2. 激波
   当$m\neq 0$时，间断两侧有物质交换，随之带来的也有动量和能量交换。当$m>0$时物质由激波右侧进入左侧，即右侧是激波前，左侧是激波后，激波向右推进，称为向右激波；反之是向左激波。

## 黎曼问题

### 黎曼问题

黎曼问题又称初始间断的分解问题，所谓初始间断是指，介质中原本存在力学的或运动的不平衡，即强间断，间断两边$u_左\neq u_右,p_左\neq p_右$，造成新的波系传播。这种不平衡一旦被打破就将产生一系列新的波系，初始间断被分解，系统开始趋于一个新的平衡。新生成的平衡状态可以由问题的初始条件确定，就是所谓的黎曼问题。激波管问题是一个典型的黎曼问题。

描述一维激波管黎曼问题：在一维管道中，原点的左边是高压气体，右边是低压气体，高压气体和低压气体在初始时刻处于静止状态，两者之间由厚度不计的薄膜分隔。$t=0$时薄膜撤出，界面处高压气体和低压气体开始相对运动，相当于是在高压气体中传入稀疏波，在低压气体中传入冲击波（冲击波在宏观上表现为一个运动着的曲面，它经过之处物质的各项物理参数发生急剧变化，冲击波可以看作是绝热不可逆的等熵过程）。

对黎曼问题进行符号表述：
$$
l+r \longrightarrow \overleftarrow{R}+m^*+\overrightarrow{S}
$$
在数值方法研究中，经常用黎曼问题的精确解检查数值方法的精确程度。

### 黎曼问题解分析

由于初值的不同，黎曼问题的解可以是以下五种情况：

1. 在接触间断的左右两侧各有一个激波间断。这些间断都从初始间断点出发，各自以常速运动。在接触间断与激波之间的区域，以及激波到达前的未受扰动的区域，都是常数状态区；
2. 在接触间断的左边有一个向左的中心稀疏波，在接触间断的右边有一个向右激波。中心稀疏波的中心同样是初始间断点，区域内的物理量是$\frac xt$的函数，并且其波前未受扰动的常数状态连续地过度到其波尾与接触间断之间的波后常数状态；
3. 接触间断的左边有一个向左激波，右边有一个向右中心稀疏区；
4. 接触间断的左右两侧各有一个中心稀疏波；
5. 在向左和向右中心稀疏波之间出现真空区域；

接下来开始推导在接触间断附近关于速度$U$和压力$P$的算法：

分别考虑左波（向左激波和向左中心稀疏波），右波（向右激波和向右中心稀疏波），需要参考Hugoniot曲线部分的内容作为先提推导。

在向左激波情况，激波的波后与波前状态之间有关系式
$$
U-u_L+\frac{P-p_L}{a_L}=0\\
a_L=\rho_L c_L\sqrt{\frac{\gamma+1}{2\gamma}(\frac{P}{p_L})+\frac{\gamma+1}{2\gamma}},P>p_L
$$
在向左中心稀疏波情况，黎曼不变量有$\alpha\equiv\alpha_0$，由关系式（见中心稀疏波部分）
$$
u+\frac{2}{\gamma-1}c\equiv u_L+\frac{2}{\gamma-1}c_L
$$
借助等熵关系$c=c_0(\frac{p}{p_0})^{\frac{\gamma-1}{2\gamma}}$进行改写得到波后与波前状态的关系
$$
U+\frac{2}{\gamma-1}c_L(\frac{P}{p_L})^{\frac{\gamma-1}{2\gamma}}=u_L+\frac{2}{\gamma-1}c_L
$$
进一步改写为与左激波情况类似的形式
$$
U-u_L+\frac{P-p_L}{a_L}=0\\
a_L=\rho_L c_L\frac{1-(\frac{P}{p_L})}
{\frac{2\gamma}{\gamma-1}[1-(\frac{P}{p_L})^{\frac{\gamma-1}{2\gamma}}]},P<p_L
$$
右波与左波同理，最终得到统一形式
$$
左波：U-u_L+\frac{P-p_L}{a_L}=0\\
右波：U-u_R-\frac{P-p_L}{a_R}=0
$$
其中
$$
a_K=
\left\{\begin{array}{rcl}

\rho_K c_K\frac{1-(\frac{P}{p_K})}
{\frac{2\gamma}{\gamma-1}[1-(\frac{P}{p_K})^{\frac{\gamma-1}{2\gamma}}]},P<p_K\\

\rho_K c_K\sqrt{\frac{\gamma+1}{2\gamma}(\frac{P}{p_K})+\frac{\gamma+1}{2\gamma}},P>p_K

\end{array}\right.
(K=L,R)
$$

### 激波管黎曼问题的迭代法

由以下关系式
$$
左波：U-u_L+\frac{P-p_L}{a_L}=0\\
右波：U-u_R-\frac{P-p_L}{a_R}=0
$$

$$
a_K=
\left\{\begin{array}{rcl}

\rho_K c_K\frac{1-(\frac{P}{p_K})}
{\frac{2\gamma}{\gamma-1}[1-(\frac{P}{p_K})^{\frac{\gamma-1}{2\gamma}}]},P<p_K\\

\rho_K c_K\sqrt{\frac{\gamma+1}{2\gamma}(\frac{P}{p_K})+\frac{\gamma+1}{2\gamma}},P>p_K

\end{array}\right.
(K=L,R)
$$

可以得到$U,P$的解
$$
U=\frac{a_L u_L+a_R u_R - (p_R-p_L)}{a_L+a_R}\\
P=\frac{a_Lp_R +a_Rp_L - a_La_R(u_R-u_L)}{a_L+a_R}
$$
对于$a_K$，其中只有一个未知量$P$，所以要围绕$P$构造差分，收敛后得到$a_K$，再进一步计算得到$U$。差分式为
$$
P^{s+1}=\frac
{a_L^sp_R +a_R^sp_L - a_L^sa_R^s(u_R-u_L)}
{a_L^s+a_R^s}\\
a_K^s=a_K(P^s;\rho_K,p_k)
$$
差分的初始值依照如下关系式给出
$$
a_L^0=\rho_L c_L;a_R^0=\rho_R c_R\\
P^1=\frac{\rho_L c_L p_R + \rho_R c_R p_L - \rho_L c_L \rho_R c_R(u_R-u_L)}{\rho_Lc_L + \rho_R c_R}
$$
存在特别强的中心稀疏波以及出现真空的情况下，迭代过程中可能出现$P^s<0$，此时计算不能正常进行，可以这样处理$P^s=\max(P^s,\epsilon),\epsilon\rightarrow 0$。

> Python实现一维激波管的简单迭代法：
>
> 

## 双曲型守恒律组



## 参考文献

- 数学物理方法——顾樵
- 一维不定常流体动力学教程——卢芳云
- 一维非定常流体力学——周毓麟
- 一维流体力学差分方法——水鸿寿
- 超声速流与冲击波——R.柯朗，K.O.弗里德里克斯