# 答案

同步电机用到的几个公式

1. 功率计算
   
   $$
   P=\sqrt{3}V_{\phi}Icos\theta\\
P=\frac{3VE}{X_s}\sin\delta
   $$

2. 判断电动机还是发电机，看功角，$ \delta>0 $ 为发电机

## SM1. Hint

(a)

$$
I=\frac{P}{V\cdot cos\theta}=\frac{10000}{230\cdot 0.8}\angle -cos^{-1}(0.8)=54.347\angle -36.87.\\
E_{af}=I(X_s+R)+V\\
VR=\frac{|E|-|V|}{|E|}
$$

(i)answer:0.256
(ii)同理

(b)

$$
\dot{I}(\dot{X_s}+\dot{R})=0
$$

## SM2. Hint

(a)

$$
Z_{base}=\frac{13.8^2}{10}=19.044\\
   X_s=\frac{V_{air}}{I_a}=\frac{15500}{418\sqrt{3}}=21.41
$$

(b)

$$
X_s^{'}=\frac{V_{OC}}{I_a}=\frac{13800}{460\sqrt{3}}=17.32
$$

(c)

$$
K=\frac{1}{\underline{X_s}}=\frac{1}{0.91}=1.1
$$

(d)

$$
I_a=\frac{10^7}{\sqrt{3}\times 13.8k}=418.37\angle(-36.89)\\
   E_{af}=V_a+I_a\cdot jX_s=13611.27\\
   V_{T}=\sqrt{3}E_{af}=23575.41
$$

Since

$$
E_{af}\propto I_f
$$

, now you do the calculation.

Answer: 324A

## SM3 Hint

Same as SM2

## SM4 Hint

(a)

$$
f=\frac{poles}{120}n
$$

answer: 1800rpm

(b)

看图说话

(c)

Pay attention to the type of connection, it's $ \Delta $.

$$
I=\frac{1200}{\sqrt{3}}\angle -36.89
$$

$$
\begin{align*}
V_t&=I(X_s+R)+V\\
&=\frac{1200}{\sqrt{3}}\angle -36.89\times (0.1i+0.015)+480\\
&=532.16\angle 5.3V
\end{align*}
$$

(d)

$$
P_{out}=\frac{1200}{\sqrt 3}\times 480\times 0.8\times 3=798129W\\
   P_{Cu}=3I^2R=21600W\\
   P_{in}=P_{Cu}+P_{core}+P_{f\&w}+P_{out}=889729W
$$

(e)
No load condition:532.16V
(f)
看图说话

## SM5

同上，不再赘述

## IM1 Hint

(a)

$$
poles=\frac{120f}{n}\approx 10.07
$$

考虑到有转差，取为 10.
(b)

$$
s=\frac{\frac{120f}{poles}-670}{\frac{120f}{poles}}=6.94\%
$$

(c)

$$
s_{new}=\frac{1}{4}s=1.735\%
$$

(d)

$$
f_e=s_{new}f=1.04Hz
$$

## IM2 Hint

(a)

$$
\omega_n=s\cdot \frac{120f}{poles}=2820rpm
$$

(b)
P=50kVA
(c)

$$
\tau=\frac{P_{out}}{\omega_n}=\frac{50000}{94\pi}=169.3N/m
$$

(d)

$$
P_{convert}=50000+520=50520W\\
   \tau_{ind}=\frac{50520}{94\pi}=171.1N/m
$$

(e)
f=sf

## IM3 Hint

(a) Equivalent Circuit

$$
V=\frac{V}{\sqrt 3}=120.1V\\
   Z_{eq}=(R_2/s+jX_2)//X_m+(R_1+jX_1)=0.34+0.85i\\
   I=V/Z_{eq}
$$

(b)

$$
P_{SCL}=3I_1^2R_1=1180.9W
$$

(c)

$$
P_{ag}=\sqrt{3}VIcos\theta-P_{scl}=12550.8W
$$

(d)

$$
P_{convert}=(1-s)P_{ag}=11.91kW
$$

(e)

$$
\omega_r=\frac{120\times60}{4}\times 2\pi\cdot s=57\pi\\
   \tau=\frac{P_{convert}}{\omega_r}
$$

(f), (g), (h) 都可以直接做了.

## IM4 Hint

## IM5 Hint.

(a)

考虑通过计算转矩来计算 $R_2$, 这题还挺麻烦，一开始想直接用功率求$ R_2 $，不过那样误差还蛮大的，这个做法比较直接

$$
\begin{gathered}
Z_\text{TH} =\frac{j X_{M t}\left(R_{t}+j X_{1}\right)}{R_{1}+j\left(X_{1}+X_{M}\right)}=\frac{\left(j16\Omega\right)\left(0.33\Omega+j0.42\Omega\right)}{0.33\Omega+j\left(0.42\Omega+16\Omega\right)}=0.313+j0.416\Omega=0.520\angle53^{\circ}\Omega \\
V_{\mathrm{TH}} =\frac{jX_{M}}{R_{i}+j\left(X_{i}+X_{M}\right)}v_{\phi}=\frac{\left(j16\Omega\right)}{0.33\Omega+j\left(0.42\Omega+16\Omega\right)}\left(120\angle0^{\circ}v\right)=116.9\angle1.2^{\circ}V
\end{gathered}
$$

$$
\begin{aligned}
&n_m =(1-0.038)(1800\text{r/min})=1732\text{r/min}  \\
& \\
&\tau_{_\text{ind}}=\tau_{_\text{load}}=\frac{(10~\text{hp})(746~\text{Whp})}{(1732~\text{r}/\text{min})\bigg(\frac{2\pi~\text{rad}}{1~\text{r}}\bigg)\bigg(\frac{60~\text{s}}{1~\text{min}}\bigg)}=41.1~\text{N}\cdot\text{m}
\end{aligned}
$$

$$
\tau_{\text{ind}}=\frac{3V_{\text{TH}}^2R_2/s}{\omega_{\text{smc}}\left[\left(R_{\text{TH}}+R_2/s\right)^2+\left(X_{\text{TH}}+X_2\right)^2\right]}
$$

最后解方程即可。





无线电能传输

基本都是利用电磁效应进行远距离能量传输，

超导电机

 超导电缆可以承载大电流而不产生热量，有效地提高了电机的气隙磁通密度，从而减少了相应的铜铁消耗。此外，由于较高的磁通密度，它可以在很小的体积内制造

感应子电机

在转子转动时，因气隙磁导变化引起定子绕组中的磁链发生周期性的变化而感生电动势。


