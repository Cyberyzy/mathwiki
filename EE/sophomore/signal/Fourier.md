## 若干傅里叶变换和它们之间的关系

1. 连续傅里叶变换 FT——周期性连续信号

2. 傅里叶级数 FS——非周期性连续信号

3. 离散时域傅里叶变换 DTFT——周期性离散信号 4

4. 离散周期信号的傅里叶级数 DFS

5. 离散傅里叶变换 DFT——非周期性离散信号&FFT

### FS

傅里叶级数是将连续信号与正交函数基做内积，投影到 n 维函数空间上，**周期性会导致频率离散**

变换式如下：

$$
a_n=\frac{T}{2}\int_{-\frac{T}{2}}^{\frac{T}{2}}f(t)cos\space n\omega tdt
$$

$$
b_n=\frac{T}{2}\int_{-\frac{T}{2}}^{\frac{T}{2}}f(t)sin\space n\omega tdt
$$

### FT

常规的傅里叶变换

### 同 FT 的关系：

直接对一周期信号 $f(t)$ 做傅里叶级数展开

$$
f(t)=\sum F_ne^{jn\omega t}
$$

再做傅里叶变换

$$
\mathcal{f(t)}=2\pi\sum F_n\delta(\omega-n\omega_1)
$$

即周期信号的傅里叶变换是由脉冲信号组成的，离散，而且仍然周期。

原始信号：周期性的连续信号，频域信号：非周期的离散信号

#### DFS

$$
X_d(k)=\sum_{n=0}^{N-1}x_d(n)e^{-j\frac{2\pi}{N}kn}
$$

$$
x_d(n)=\frac{1}{N}\sum_{k=0}^{N-1}X_{d}(k)e^{j\frac{2\pi}{N}kn}
$$

特点：

1. 时域周期，频域离散：各频率分量的周期之比是有理数

2. 时域离散，频域周期：离散复指数序列 $ e^{j\theta kn} $ 随 k 周期变化，则 $ x_d(n) $ 的投影也随 k 周期变化。

3. 偶实奇虚：

   $$
   \begin{align*}
   X_d(k)&=\sum_{n=0}^{N-1}x_d(n)e^{-j\frac{2\pi}{N}kn}\\
      &=\sum_{n=0}^{N-1}x_d(n)cos(\frac{2\pi}{N}kn)-j\sum_{n=0}^{N-1}x_d(n)sin(\frac{2\pi}{N}kn)
   \end{align*}
   $$

   当$ x_d(n) $ 是偶函数，则 $ X_d(k) $ 为实函数，当$ x_d(n) $ 是奇函数，则 $ X_d(k) $ 为虚函数。

4. 和 FS 的关系：

我们考虑一个连续周期信号 $ X*{continue} $
第一步：求 $ X*{continue} $ 的傅里叶级数

$$
X_{ag}(k\omega)
$$

第二步：对 $ X\_{continue} $ 抽样，求抽样信号的 DFS

$$
X_d(k)=\sum_{n=0}^{N-1}x_d(n)e^{-j\frac{2\pi}{N}kn}
$$

第三步：
求 $ X*{continue} $ 的傅里叶变换，找 $ X*{ag}$ 满足的式子

$$
X_{a}(\omega)=2\pi\sum_{k=-\infty}^{\infty}X_{ag}(k\omega_1)\delta(\omega-k\omega_1)
$$

第四步：对 $ X\_{continue} $ 冲激抽样，求其傅里叶级数，得到

$$
X_{arg}(k\omega_1)=\frac{1}{T_1}X_{dg}(k)\quad\text{FS}[x_{ax}(t)]=\frac{1}{T_1}\text{DFS}\left[x_{d}(n)\right]
$$

#### DTFT

从 z 变换引出较为容易

$$
X(e^{j\omega})=\sum_{n=-\infty}^{+\infty}x(n)e^{-jn\omega}\\
x(n)=\frac{1}{2\pi}\int_{-\pi}^{\pi}X(e^{j\omega})e^{jn\omega}d\omega
$$

## z 变换

$$
   X(z)=\sum_{n=-\infty}^{+\infty}x(n)z^{-n}\\
   x(n)=\frac{1}{2\pi i}\int X(z)z^{n-1}
$$

只消记住

$$
   \mathcal{Z}(u_d(n))=\frac{z}{z-1}
$$

逆 z 变换，三种办法，留数、长除法和部分分式展开。留数比较简单。
性质：

### 线性叠加

线性叠加之后，收敛域可能变大

$$
\begin{gathered}
{\mathscr{Z}}[ax(n)+by(n)]=aX(z)+bY(z) \\
(R_1<|z|<R_2)
\end{gathered}
$$

### 位移

双边 z 变换

$$
   \mathscr{Z}(x(n-m))=z^{-m}X(z)
$$

单边 z 变换
右侧

$$
   \mathscr{Z}\big[x\left(n-m\right)u\left(n\right)\big]=z^{-m}\Big[X\left(z\right)+\sum_{k=-m}^{-1}x\left(k\right)z^{-k}\Big]
$$

左侧

$$
   \mathscr{Z}\big[x\left(n+m\right)u\left(n\right)\big]=z^{-m}\Big[X\left(z\right)-\sum_{k=0}^{m-1}x\left(k\right)z^{-k}\Big]
$$

### 微分

$$
   \mathcal{Z}\big[nx\left(n\right)\big]=-z\frac{\text{d}}{\text{d}z}X\left(z\right)
$$

### 终值定理

$$
\begin{aligned}
& X(z)={\mathcal{L}}[x(n)]=\sum_{n=0}^{\infty}x(n)z^{-n}  \\
&\lim\limits_{n\to\infty}x(n) =\lim\limits_{z\to1}[(z-1)X(z)]
\end{aligned}
$$

条件是：当$ n\to \infty $ 时，$ x(n) $ 收敛，换句话说，$ X(z) $ 的极点在单位圆内，或者只能在$ z=\pm 1 $且为 1 阶极点。
