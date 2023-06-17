# 电磁场



## 边值问题

一般方程

$$
\nabla^2\varphi=-\rho/\varepsilon
$$

第一类边界条件

连续性条件

$$
\varphi_i=\varphi_j
$$

法向条件

$$
\varepsilon_j\frac{\partial\varphi_j}{\partial n}-\varepsilon_i\frac{\partial\varphi_i}{\partial n}=\rho_s
$$

第二类边界条件

法向条件

$$
\frac{\partial \varphi}{\partial n}=0
$$

此称为第二类边界。电力线组成的面为齐次第二类边界面。一般是场的对称面，只计算一半场域时作为边界面的情况

切向条件

$$
\varphi_i=U
$$

上述条件是必要的，如果 $U$ 未知，称为悬浮边界，需要加上如下条件

$$
\iint_S\boldsymbol{D}\cdot\mathrm{d}\boldsymbol{S}=\iint_S D_n\mathrm{d}S=-\iint_S\varepsilon\frac{\partial\varphi}{\partial n}\mathrm{d}S=q
$$

悬浮边界有如下三种情况：

a) 已知导体总电荷

b) 屏蔽导体球壳

c) 孤立导体

对简单结构导体，有时可以看出或近似认为电荷均匀分布，但也应加第一类边界条件.



## 镜像法和电轴法

镜像法：

1. 球形边界

边值问题为，认为球壳接地

$$
-\frac{q}{4\pi \epsilon\sqrt{d^2+R^2-2dRcos\theta}}-
-\frac{q^{\prime}}{4\pi \epsilon\sqrt{b^2+R^2+2bRcos\theta}}=0
$$



解得像电荷为 $q^{\prime}=\frac{R}{d}q$ ，距离为$d=R^2/b$

2. 无限大平面
   
   $$
   \varphi_1=\varphi_2\\ 
\varepsilon_1\frac{\partial \varphi_1}{\partial n}=\varepsilon_2\frac{\partial \varphi_2}{\partial n}
   $$

解得像电荷为

$$
q_1=\frac{\varepsilon_1-\varepsilon_2}{\varepsilon_1+\varepsilon_2},\quad q_2=\frac{2\varepsilon_2}{\varepsilon_1+\varepsilon_2}
$$

## 电轴法

$$
\begin{aligned}
a_1^2+b^2=h_1^2\\
a_2^2+b^2=h_2^2\\
h_1+h_2=d
\end{aligned}
$$



## 恒定电流场

### 1. 基本方程

$$
\nabla\cdot J=-\frac{\partial \rho}{\partial t}\\
\nabla \times E=0\\
J=\sigma E\\
\iint_S J\cdot dS=0\\
\iint E\cdot dl=0
$$

边界条件和E一致



如果满足

$$
\frac{\varepsilon_1}{\varepsilon_2}=\frac{\sigma_1}{\sigma_2}
$$

则交界面上无面电荷，否则有





(a) 磁力线即为Az的第一类边界。场中应选一参考点设Az=0。(b) 与磁力线垂直的面(铁磁材料边界的空气侧)为Az的齐次二类边界，





## 互感和自感

回路电流I产生的磁链与该电流的比值称为自感：单位 亨利

磁链：一个小面积dS上的磁链等于该面积上的磁通 $d \Psi $乘其磁力线所交链的电流的个数 $N_d$，即

$$
d\Psi=N_dBdS
$$

单位 韦伯

求法：加流求$\Psi$ 

$$
A=\frac{\mu_0}{4\pi}\oint_{l_1}\frac{Idl_1}{r}
$$

$$
\begin{aligned}
&\varphi_o =\oint_{l_2}A\cdot\text{d}\boldsymbol{l}_2=\frac{\mu_0I}{4\pi}\boldsymbol{\oint}_{l_2}\boldsymbol{\oint}_{l_1}\frac{\text{d}\boldsymbol{l}_1\cdot\text{d}\boldsymbol{l}_2}{r}  \\
&L_0 =\frac{\mu_0}{4\pi}\oint_{l_2}\oint_{l_1}\frac{\text{d}\boldsymbol{l}_1\cdot\text{d}\boldsymbol{l}_2}{r} 
\end{aligned}
$$

受力计算

1. 虚位移
   
   $$
   dW=dW_m+fdg
   $$

$$
dW=pdt=id\Psi\\
dW_m=\frac{1}{2}id\Psi
$$

则

$$
f=\frac{\partial W_m}{\partial g}
$$

若没接电源，磁场能减小则要么电流减小，要么磁链减小，或同时减小。韦伯指出是磁链守恒保持不变，系统的能量平衡关系为：磁场做功 = 磁场能减小量

$$
f=-\frac{\partial W_m}{\partial g}=\frac{1}{2}I^2\frac{\partial L}{\partial g}
$$

即磁场力沿电感增加的方向。

## 时变电磁场

> 证明电容器（或导体的断口处）中的位移电流等于其导线中的传导电流。

$$
i=\oint_S J\cdot dS=\frac{dq}{dt}=\frac{d\rho_S}{dt}=\oint\frac{\partial D_n}{\partial t}dS=\oiint_SJ\cdot dS=id

$$

> 例2: 一半径为a的圆形平行板电容器，极板间距为d，分别对电容加电压源u(t)与电流源i(t)，求电容器内和电容器外附近区域距轴线r处的感应磁场强度。

先求电容内的位移电流

$$
J_D=\frac{\varepsilon \partial E}{\partial t}=\varepsilon U/d\\
H=\frac{J_D r}{2}
$$

maxwell Equation

$$
\begin{aligned}
&\nabla\times H=J_D+\frac{\partial D}{\partial t}\\

&\nabla \times E=-\frac{\partial B}{\partial t}\\
&\nabla \cdot E=\frac{\rho}{\varepsilon}\\
&\nabla \cdot B=0
\end{aligned}

$$

边界条件

$$
\begin{aligned}&\oint_{_l}\boldsymbol{H}\cdot\text{d}\boldsymbol{I}=i+\frac{\partial}{\partial t}\iint_{S}\boldsymbol{D}\cdot\text{d}\boldsymbol{S} \\&\oint_i\boldsymbol{E}_i\cdot\text{d}\boldsymbol{I}=-\frac{\partial}{\partial t}\iint_s\boldsymbol{B}\cdot\text{d}\boldsymbol{S}\end{aligned}
$$

全电流的法向连续

$$
J_{D2}+\frac{\partial D_2}{\partial t}=J_{2}+\frac{\partial D_2}{\partial t}

$$

电准静态场

$\nabla\times E=0$

（a）理想介质中的电场：已知电荷或电压，求D与E

只有在电准静态场下，对平行板电容才有E=U/d，即忽略了感应电场。

（b)完纯导体中的电流场：已知导体总电流或电压，求J与E

$$
\nabla\cdot J=0\quad\nabla\times E=0\quad\textbf{J=}\sigma E
$$

(c)非理想电介质中的电场，已知电流或电压，求J、E 、D与非均匀媒质空间点上可能有净电荷及其变化，其与电流密度的关系由电荷守恒定律约束，基本方程

$$
\begin{aligned}
&\nabla\cdot J=-\frac{\text{d}\rho}{\text{d}t}\\
&\nabla\cdot D=\rho\\
&\nabla\times\boldsymbol{E}=0\\
&\textit{J}=\sigma E\\
& D=\varepsilon E
\end{aligned}
$$

非理想电介质中的电场比较特殊

磁准静态场

$\nabla \times H=J$

a) 若电流J已知，即没有涡流导体磁场被解耦出来，可先求得磁场，再由式(2)和(4)分别求电场。求已知电流的磁场时，解法与恒定磁场相同：安培环路定律、毕奥-萨伐尔定律、矢量磁位A及其边值问题都适用。由式(2)求感应电场与感应电动势为第1节的计算内容，后面讲。库仑场的求法与静电场相同。

b)

$$
\begin{aligned}
&\nabla\times\textbf{H}=\textbf{J} \\
&\nabla\times\textbf{E}=-\frac{\partial\textbf{B}}{\partial t} \\
&\nabla\cdot\textbf{D}=\rho \\
&\nabla\cdot\textbf{J}=0
\end{aligned}
$$

若外部磁场跳变，从零跳变到H0，则环内磁场Hin不会跳变 。因为若跳变意味着磁通跳变，感应电动势会无限大，这是不可能的。因此，环内磁场会有一个上升的过程，此过程好像是环外磁场向内部扩散，称为磁扩散过程。

若H0是正弦函数，不跳变，则导体内也会产生电流起到去磁作用，使得Hin小于H0,导体环起到磁屏蔽作用。这就是导体涡流产生附加场，抵消原场的磁屏蔽现象。

导线通有交流电时，导线中间的电流较小，导线表面的电流较大，这现象称为集肤效应

若施加的为正弦电流，则各点电流密度在一个周期内的最大值呈现两导体内侧的电流密度大于外侧的现象，这种现象称为邻近效应



## 坡印廷矢量

$$
S=E\times H \quad W/m^2
$$
