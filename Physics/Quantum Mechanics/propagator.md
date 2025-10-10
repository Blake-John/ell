要推导自由粒子的传播子  $G(\boxed{r}, t; \boxed{r}^\prime, 0)$ ，我们可以按照以下步骤进行：
 
步骤1：明确传播子的定义
 
传播子  $G(\boxed{r}, t; \boxed{r}^\prime, 0)$  描述自由粒子从初始位置  \boxed{r}^\prime （ t=0  时刻）传播到位置  $\boxed{r}$ （ $t$  时刻）的概率幅，其傅里叶积分形式由动量空间的叠加给出：
 

$$G(\boxed{r}, t; \boxed{r}^\prime, 0) = \frac{1}{(2\pi\hbar)^3} \int_{-\infty}^{+\infty} \mathrm{d}^3 p \exp\left[ \mathrm{i} \frac{\boxed{p} \cdot (\boxed{r} - \boxed{r}^\prime)}{\hbar} - \mathrm{i} \frac{p^2 t}{2m\hbar} \right]$$

 
其中， $\boxed{p}$  是粒子的动量，积分遍历所有动量空间；指数项的第一项是动量在空间位移上的相位，第二项是自由粒子的动能（ $E = \frac{p^2}{2m}$ ）对应的时间相位（ $\exp(-\mathrm{i}Et/\hbar)$ ）。
 
步骤2：分离三维积分（利用各向同性）
 
由于被积函数可分离为三个一维动量分量（ $p_x, p_y, p_z$ ）的乘积，三维积分可分解为三个一维积分的乘积。以  x  分量为例，令  $\boxed{\rho} = \boxed{r} - \boxed{r}^\prime$ ，则  $\boxed{p} \cdot \boxed{\rho} = p_x \rho_x + p_y \rho_y + p_z \rho_z$ ，且  $p^2 = p_x^2 + p_y^2 + p_z^2$ 。因此：
 

$$G = \left( \frac{1}{2\pi\hbar} \int_{-\infty}^{+\infty} \mathrm{d}p_x \exp\left[ \mathrm{i} \frac{p_x \rho_x}{\hbar} - \mathrm{i} \frac{p_x^2 t}{2m\hbar} \right] \right) \times \text{同理的 } y, z \text{ 分量}$$

 
步骤3：计算一维高斯型积分
 
对于单个分量（如  $x$  分量），积分形式为：
 

$$I = \int_{-\infty}^{+\infty} \mathrm{d}p \exp\left( \mathrm{i} \frac{p \rho}{\hbar} - \mathrm{i} \frac{p^2 t}{2m\hbar} \right)$$

 
这是复高斯积分，可通过配方法化简。令  $a = \frac{\mathrm{i} t}{2m\hbar} ， b = \frac{\mathrm{i} \rho}{\hbar}$ ，则被积函数为  $\exp(-a p^2 + b p)$ 。
 
配方法：
 

$$-a p^2 + b p = -a \left( p^2 - \frac{b}{a} p \right) = -a \left( p - \frac{b}{2a} \right)^2 + \frac{b^2}{4a}$$

 
代入  a, b  的表达式：
 

$$\frac{b}{2a} = \frac{\frac{\mathrm{i} \rho}{\hbar}}{2 \cdot \frac{\mathrm{i} t}{2m\hbar}} = \frac{m \rho}{t}, \quad \frac{b^2}{4a} = \frac{\left( \frac{\mathrm{i} \rho}{\hbar} \right)^2}{4 \cdot \frac{\mathrm{i} t}{2m\hbar}} = \frac{-\rho^2 / \hbar^2}{2 \mathrm{i} t / m\hbar} = \frac{\mathrm{i} m \rho^2}{2 \hbar t}$$

 
因此，积分变为：
 

$$I = \exp\left( \frac{\mathrm{i} m \rho^2}{2 \hbar t} \right) \int_{-\infty}^{+\infty} \mathrm{d}p \exp\left( -a \left( p - \frac{m \rho}{t} \right)^2 \right)$$

 
复高斯积分的公式为  $\int_{-\infty}^{+\infty} \exp(-a p^2) \mathrm{d}p = \sqrt{\frac{\pi}{a}}$ （当  $\mathrm{Re}(a) > 0$  时，此处  $a = \frac{\mathrm{i} t}{2m\hbar}$ ，需验证收敛性：由于  $t \geq 0$ ，可通过解析延拓保证积分收敛）。代入  $a$ ：
 

$$\int_{-\infty}^{+\infty} \exp\left( - \frac{\mathrm{i} t}{2m\hbar} \left( p - \frac{m \rho}{t} \right)^2 \right) \mathrm{d}p = \sqrt{\frac{2\pi m\hbar}{\mathrm{i} t}}$$

 
因此，单个分量的积分  $I$  为：
 

$$I = \exp\left( \frac{\mathrm{i} m \rho^2}{2 \hbar t} \right) \sqrt{\frac{2\pi m\hbar}{\mathrm{i} t}}$$

 
步骤4：组合三个分量的结果
 
由于  $x, y, z$  分量的积分形式完全相同，三维传播子是三个一维积分的乘积：
 

$$G = \left( \frac{1}{2\pi\hbar} \right)^3 \cdot I_x \cdot I_y \cdot I_z$$

 
代入  $I_x, I_y, I_z$  的表达式：
 

$$I_x \cdot I_y \cdot I_z = \exp\left( \frac{\mathrm{i} m (\rho_x^2 + \rho_y^2 + \rho_z^2)}{2 \hbar t} \right) \cdot \left( \sqrt{\frac{2\pi m\hbar}{\mathrm{i} t}} \right)^3$$

 
其中  $\rho_x^2 + \rho_y^2 + \rho_z^2 = |\boxed{r} - \boxed{r}^\prime|^2$ ，且  $\left( \frac{1}{2\pi\hbar} \right)^3 \cdot \left( \frac{2\pi m\hbar}{\mathrm{i} t} \right)^{3/2} = \left( \frac{m}{2\pi \mathrm{i} \hbar t} \right)^{3/2}$。
 
步骤5：整理得到最终形式
 
将上述结果组合，最终得到自由粒子传播子：
 

$$G(\boxed{r}, t; \boxed{r}^\prime, 0) = \left( \frac{m}{2\pi \mathrm{i} \hbar t} \right)^{3/2} \exp\left( \mathrm{i} \frac{m |\boxed{r} - \boxed{r}^\prime|^2}{2 \hbar t} \right) \quad (t \geq 0)$$

 
说明：上述推导利用了复高斯积分的技巧，通过配方法将动量空间的积分转化为已知的高斯型积分，最终得到了传播子的坐标空间表达式。这一结果也被称为自由粒子的格林函数，是量子力学中描述粒子传播的核心工具之一。