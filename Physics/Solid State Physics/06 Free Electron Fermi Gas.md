---
title: Free Electron Fermi Gas
date: 2026-05-18
tags:
  - solid-state-physics
  - free-electron-model
  - fermi-gas
  - kittel-ch6
aliases:
  - 自由电子费米气体
  - Kittel Chapter 6
cssclasses:
  - physics-note
---

# Free Electron Fermi Gas

> *"In a theory which has given results like these, there must certainly be a great deal of truth."*
> — H. A. Lorentz

[[自由电子模型]] 可以理解金属的许多物理性质（不仅是简单金属）。根据这个模型，组成原子的价电子成为**传导电子**，在金属体积内自由运动。

## 自由电子模型的基本图像

最简单的金属是**碱金属**（Li, Na, K, Cs, Rb）。以钠为例：
- 自由 Na 原子的价电子处于 3s 态
- 在金属中，这个电子成为 3s 传导带中的传导电子
- 每个 Na⁺ 离子芯包含 10 个电子（1s² 2s² 2p⁶），其空间分布在金属中与自由离子中基本相同
- 离子芯只占钠晶体体积的约 **15%**（Na⁺ 自由离子半径 0.98 Å，金属中最近邻距离之半为 1.83 Å）
- 碱金属为 bcc 结构，贵金属（Cu, Ag, Au）为 fcc 结构

一个含有 $N$ 个原子的单价晶体有 $N$ 个传导电子和 $N$ 个正离子芯。

## 经典自由电子理论的困难

自由电子的经典理论在量子力学发明之前就已发展，有几个显著的成功：
- 推导出**欧姆定律**的形式
- 建立了**电导率与热导率**之间的关系

但经典理论**无法解释**：
1. **电子气的热容**：经典预测每个电子贡献 $\frac{1}{2}k_BT$，总热容 $C = \frac{3}{2}Nk_B$，但实验值远小于此
2. **电子气的磁化率**
3. **传导电子的极长自由程**：实验表明传导电子可以在金属中沿直线自由穿行许多原子距离，极纯样品低温下平均自由程可达 $10^8$ 个原子间距（超过 1 cm）

> [!warning] 关键区分
> 这些失败**不是自由电子模型的失败**，而是**经典 Maxwell 分布函数**的失败。模型本身（电子自由运动）没问题，错的是用经典统计来描述电子。

> [!tip] 为什么凝聚态对传导电子如此"透明"？
> (a) 物质波在周期性结构中可以自由传播（下一章处理）
> (b) 传导电子很少被其他传导电子散射——这是**泡利不相容原理**的结果

**自由电子费米气体**：受泡利原理约束的自由电子气。

---

## ENERGY LEVELS IN ONE DIMENSION

Kittel 的讲法很聪明：三维问题数学复杂，但物理本质和一维一样。先在一维里把**量子化能级**、**泡利不相容原理**、**费米能**这三个核心概念讲清楚。

### 1. 物理模型与薛定谔方程

想象一个质量为 $m$ 的电子被限制在长度为 $L$ 的一维线段上，两端是**无限高势垒**（电子跑不出去）。这就是量子力学中最经典的**无限深势阱**（infinite square well）问题。

定态薛定谔方程为：

$$
\mathcal{H}\psi_n = -\frac{\hbar^2}{2m}\frac{d^2\psi_n}{dx^2} = \epsilon_n \psi_n \tag{1}
$$

其中 $\mathcal{H} = p^2/2m$ 为哈密顿量（自由电子，忽略势能），动量 $p$ 在量子力学中表示为算符 $-i\hbar\, d/dx$，$\epsilon_n$ 是电子在轨道中的能量。

> [!note] 轨道（Orbital）的概念
> "轨道"指**单电子**波动方程的解。这个术语让我们能区分：
> - $N$ 个相互作用电子系统的精确量子态
> - 近似量子态：将 $N$ 个电子分配到 $N$ 个不同的轨道，每个轨道是单电子波动方程的解
>
> 轨道模型仅在电子间**无相互作用**时才是精确的。

### 2. 边界条件与驻波解

![[imgs/standing_wave_solu.png]]

> Figure 2 First three energy levels and wavefunctions of a free electron of mass m confined to a line of length L. The energy levels are labeled according to the quantum number n which gives the number of half-wavelengths in the wavefunction. The wavelengths are indicated on the wavefunctions. The energy $\epsilon _ { n }$ of the level of quantum number n is equal to $( h ^ { 2 } / 2 m ) ( n / 2 L ) ^ { 2 }$ .

两端无限高势垒意味着波函数在边界处必须为零：

$$
\psi_n(0) = 0, \quad \psi_n(L) = 0
$$

这和电子在两端被"夹住"的驻波完全类比。满足条件的解是正弦波，且要求**整数个半波长**恰好塞进长度 $L$：

$$
\psi_n = A \sin\left(\frac{2\pi}{\lambda_n} x\right), \quad \frac{1}{2}n\lambda_n = L \tag{2}
$$

其中：
- $n$ 为正整数（量子数），表示半波长的个数
- $A$ 为归一化常数
- $n = 1$ 时塞了半个波长，$n = 2$ 时塞了一个完整波长，以此类推

**验证这是薛定谔方程的解：**

$$
\frac{d\psi_n}{dx} = A\left(\frac{n\pi}{L}\right)\cos\left(\frac{n\pi}{L}x\right)
$$

$$
\frac{d^2\psi_n}{dx^2} = -A\left(\frac{n\pi}{L}\right)^2\sin\left(\frac{n\pi}{L}x\right)
$$

代入方程 (1)，二阶导数产生一个负号与方程左边的负号抵消，等式成立。

### 3. 量子化能级

由上述推导直接得到能量本征值：

$$
\boxed{\epsilon_n = \frac{\hbar^2}{2m}\left(\frac{n\pi}{L}\right)^2} \tag{3}
$$

**能级的关键特征：**
- 能量与 $n^2$ 成正比：$\epsilon_1 : \epsilon_2 : \epsilon_3 : \epsilon_4 = 1 : 4 : 9 : 16$
- 能级间距随 $n$ 增大而增大：$\Delta\epsilon = \epsilon_{n+1} - \epsilon_n \propto 2n+1$
- 能量与 $L^2$ 成反比：盒子越大，能级越密集（宏观极限下趋于连续）
- $n = 1$ 是最低能级（**零点能** $\epsilon_1 = \frac{\hbar^2\pi^2}{2mL^2}$），不存在 $n = 0$ 的状态

### 4. 泡利不相容原理：电子怎么填？

到这里还只是单电子量子力学。固体物理的核心问题是：**$N$ 个电子怎么分配在这些能级上？**

> [!important] 泡利不相容原理
> **不能有两个电子占据完全相同的量子态**（即所有量子数完全相同）。这适用于原子、分子和固体中的电子。

一维情况下，传导电子轨道的量子数为 $n$ 和 $m_s$：
- $n$：任意正整数（1, 2, 3, …）
- $m_s = \pm\frac{1}{2}$：磁量子数，对应自旋向上↑或向下↓

因此**每个能级 $n$ 可以容纳 2 个电子**（一个自旋向上，一个自旋向下）。

> [!example] 6 个电子的基态填充
>
> | $n$ | $m_s$ | 占据 | | $n$ | $m_s$ | 占据 |
> |-----|-------|------|---|-----|-------|------|
> | 1   | ↑     | 1    | | 3   | ↑     | 1    |
> | 1   | ↓     | 1    | | 3   | ↓     | 1    |
> | 2   | ↑     | 1    | | 4   | ↑     | 0    |
> | 2   | ↓     | 1    | | 4   | ↓     | 0    |
>
> 从最低能级开始，每层填 2 个电子（↑和↓各一），由低到高依次填充，直到所有 $N$ 个电子都安置好。这就是系统的**基态**。

> [!note] 简并度（Degeneracy）
> 多个轨道可能具有相同能量。具有相同能量的轨道数称为**简并度**。在一维无限深势阱中，不计自旋时每个能级是非简并的；计入自旋后，每个 $n$ 有 **2 重简并**。

### 5. 费米能 $\epsilon_F$

定义 $n_F$ 为**最高被占据能级**的量子数。从 $n = 1$ 开始填充，每个能级填 2 个电子，直到所有 $N$ 个电子都安置好。设 $N$ 为偶数：

$$
2n_F = N \quad \Rightarrow \quad n_F = \frac{N}{2}
$$

> [!important] 费米能的定义
> **费米能 $\epsilon_F$** 定义为 $N$ 电子系统基态中最高被占据能级的能量。
>
> 在 $T = 0$ 时，低于 $\epsilon_F$ 的能级**全满**，高于 $\epsilon_F$ 的能级**全空**。

将 $n = n_F$ 代入能级公式 (3)，得到一维情况下的费米能：

$$
\boxed{\epsilon_F = \frac{\hbar^2}{2m}\left(\frac{n_F\pi}{L}\right)^2 = \frac{\hbar^2}{2m}\left(\frac{N\pi}{2L}\right)^2} \tag{4}
$$

### 6. 费米能的物理意义

费米能是理解金属电子性质**最核心的概念之一**：

- **$\epsilon_F$ 是 $T = 0$ 时电子占据态的能量上限**。低于 $\epsilon_F$ 的能级全满，高于 $\epsilon_F$ 的全空。
- 金属中 $N$ 是巨大的（$\sim 10^{22}$ 个/cm³），$L$ 也很大，所以 $\epsilon_F$ 对应的 $n_F$ 是一个巨大的数字。
- 代入典型数值，$\epsilon_F$ 大约在 **1–10 eV** 的量级，对应**费米温度**：

$$
T_F = \frac{\epsilon_F}{k_B} \sim 10^4\text{–}10^5 \text{ K}
$$

- 这意味着在常温（300 K）下：

$$
k_BT \ll \epsilon_F
$$

电子气是**高度简并的**（highly degenerate）。

> [!tip] 为什么经典理论会失败？
> 经典理论认为每个自由度贡献 $\frac{1}{2}k_BT$ 的热能，所有电子都能参与热激发。但量子力学告诉我们：
> - 绝大多数电子被**泡利原理"锁"**在低能态上
> - 只有费米面附近 $k_BT$ 能量范围内的电子才能被热激发
> - 这部分电子占比 $\sim k_BT/\epsilon_F \sim 10^{-2}$–$10^{-3}$
>
> 这就是电子热容远小于经典预测的根源，也是下一节要讨论的内容。

### 7. 从一维到三维的推广

三维情况下，电子被限制在边长为 $L$ 的立方体中，波函数变成三个方向正弦波的乘积，量子数变成 $(n_x, n_y, n_z)$：

$$
\epsilon = \frac{\hbar^2\pi^2}{2mL^2}(n_x^2 + n_y^2 + n_z^2)
$$

在 $(n_x, n_y, n_z)$ 空间中，等能面变成了**球面**。

用**周期性边界条件**（periodic boundary conditions）代替硬壁边界条件后（Kittel 在第 5 章声子部分已引入），允许的 $\mathbf{k}$ 点在 $k$ 空间中均匀分布，每个点占据体积 $(2\pi/L)^3$。$T = 0$ 时电子占据 $k$ 空间中的一个球（**费米球**），球的半径就是**费米波矢** $k_F$。

---

## 与经典模型的对比总结

| 方面 | 经典模型 | 量子模型（费米气体） |
|------|----------|---------------------|
| 电子统计 | Maxwell-Boltzmann 分布 | Fermi-Dirac 分布 |
| 热容 | $C = \frac{3}{2}Nk_B$（过大） | $C \propto T$（与实验一致） |
| 散射机制 | 电子频繁碰撞 | 泡利原理限制电子-电子散射 |
| 能量分布 | 所有电子参与热激发 | 仅费米面附近 $\sim k_BT$ 范围内的电子参与 |
| 自由程 | 难以解释长自由程 | 泡利原理 + 周期势 → 长自由程 |

---

## EFFECT OF TEMPERATURE ON THE FERMI-DIRAC DISTRIBUTION

### 1. 从基态到有限温度：发生了什么？

上一节建立了 $T = 0$ 时的基态图像：电子从最低能级开始填充，直到费米能 $\epsilon_F$，低于 $\epsilon_F$ 全满，高于 $\epsilon_F$ 全空。这是一个**完全有序**的状态。

当温度升高时，热激发会改变这个图像：
- 一些**原本被占据**的能级（$\epsilon < \epsilon_F$）上的电子获得热能，跃迁到**原本空着**的能级（$\epsilon > \epsilon_F$）
- 结果：低于 $\epsilon_F$ 的能级不再全满，高于 $\epsilon_F$ 的能级不再全空
- 电子气的**动能增加**

> [!tip] 关键物理图像
> 温度的效果是在费米能附近**模糊化**了占据情况。$T = 0$ 时占据函数是一个完美的阶跃函数，$T > 0$ 时这个阶跃被**软化**了。

### 2. 费米-狄拉克分布函数

热平衡时，能量为 $\epsilon$ 的轨道被占据的概率由 **Fermi-Dirac 分布函数**给出：

$$
\boxed{f(\epsilon) = \frac{1}{\exp[(\epsilon - \mu)/k_BT] + 1}} \tag{5}
$$

其中：
- $f(\epsilon)$：能量为 $\epsilon$ 的轨道被电子占据的概率（$0 \leq f \leq 1$）
- $\mu$：**化学势**（chemical potential），是温度的函数
- $k_B$：玻尔兹曼常数
- $T$：绝对温度

> [!note] 化学势 $\mu$ 的物理意义
> $\mu$ 不是随意选取的，而是由**粒子数守恒**条件确定的：
> $$
> N = \int_0^\infty g(\epsilon) f(\epsilon)\, d\epsilon
> $$
> 其中 $g(\epsilon)$ 是态密度。对于给定的 $N$ 和 $T$，$\mu$ 必须调整到使上式成立。

### 3. 分布的极限行为

#### $T = 0$ 极限

当 $T \to 0$ 时，指数项的行为取决于 $\epsilon - \mu$ 的符号：

- 若 $\epsilon < \mu$：$(\epsilon - \mu)/k_BT \to -\infty$，$\exp(-\infty) = 0$，所以 $f = 1$（全满）
- 若 $\epsilon > \mu$：$(\epsilon - \mu)/k_BT \to +\infty$，$\exp(+\infty) = \infty$，所以 $f = 0$（全空）
- 若 $\epsilon = \mu$：函数在此处**不连续**地从 1 跳变到 0

因此：

$$
\mu(T=0) = \epsilon_F
$$

**在绝对零度，化学势等于费米能。** 费米能就是 $T = 0$ 时最高被占据轨道的能量。

#### 任意温度：$f(\mu) = 1/2$

将 $\epsilon = \mu$ 代入分布函数 (5)：

$$
f(\mu) = \frac{1}{\exp(0) + 1} = \frac{1}{1 + 1} = \frac{1}{2}
$$

> [!important] 普适性质
> **在所有温度下**，化学势 $\mu$ 处的占据概率恰好为 **1/2**。这是一个不依赖于温度的普适结果。

这意味着在图 3 中，所有不同温度下的 $f(\epsilon)$ 曲线都通过同一点：$(\mu, 1/2)$。

![[imgs/different_temp_of_fd_distrubution.png]]

> Figure 3 Fermi-Dirac distribution function (5) at the various labelled temperatures, for $T _ { F } \equiv \epsilon _ { F } / k _ { B } = 5 0 , 0 0 0 \mathrm { \ K } .$ . The results apply to a gas in three dimensions. The total number of particles is constant, independent of temperature. The chemical potential $\mu$ at each temperature may be read off the graph as the energy at which $f = 0 . 5$ .

#### 高能尾端：Boltzmann 极限

考虑高能尾端，即 $\epsilon - \mu \gg k_BT$ 的区域。此时指数项远大于 1：

$$
f(\epsilon) = \frac{1}{\exp[(\epsilon - \mu)/k_BT] + 1} \cong \frac{1}{\exp[(\epsilon - \mu)/k_BT]} = \exp[(\mu - \epsilon)/k_BT]
$$

这正是经典的 **Boltzmann（Maxwell）分布**。

> [!tip] 量子 → 经典的过渡
> 在高能尾端，量子效应（泡利不相容原理）不再重要，因为那里的轨道几乎都是空的，两个电子占据同一态的概率极小。此时量子统计自然退化为经典统计。

### 4. 化学势随温度的变化

虽然 Kittel 在这一节没有详细展开，但化学势 $\mu(T)$ 的行为值得理解：

- **$T = 0$**：$\mu = \epsilon_F$
- **$T > 0$**：$\mu$ 略微下降（对于三维自由电子气）
- 物理原因：温度升高时，分布函数在 $\epsilon_F$ 附近"软化"，为了保持总粒子数 $N$ 不变，$\mu$ 需要微调

对于金属，由于 $T_F \sim 50000$ K，在常温（300 K）下：

$$
\frac{T}{T_F} \sim \frac{300}{50000} = 0.006
$$

因此 $\mu$ 相对于 $\epsilon_F$ 的偏移非常小，通常可以近似认为 $\mu \approx \epsilon_F$。

### 5. 图 3 的解读

图 3 展示了不同温度下的 Fermi-Dirac 分布（以 $T_F = 50000$ K 为参数）：

- **$T = 0$**：完美的阶跃函数，在 $\epsilon_F$ 处从 1 跳变到 0
- **$T = 0.01\,T_F$（500 K）**：在 $\epsilon_F$ 附近出现一个窄的过渡区，宽度 $\sim k_BT$
- **$T = 0.1\,T_F$（5000 K）**：过渡区变宽，但大部分区域仍接近阶跃
- **$T = T_F$（50000 K）**：分布显著偏离阶跃，但仍与经典分布不同

> [!important] 核心结论
> 对于金属，常温 $T \ll T_F$，费米-狄拉克分布与 $T = 0$ 的阶跃函数差别极小。只有能量在 $\mu$ 附近 $\pm k_BT$ 范围内的电子才会受到温度的影响。这就是为什么：
> - 电子热容正比于 $T$（只有 $\sim T/T_F$ 的电子参与热激发）
> - 电导率受温度影响（声子散射），但电子气的总能量变化很小

### 6. 与经典分布的对比

| 特征 | Fermi-Dirac 分布 | Maxwell-Boltzmann 分布 |
|------|-------------------|----------------------|
| 适用范围 | 全能量范围 | 仅 $\epsilon - \mu \gg k_BT$ |
| 最大占据数 | $f \leq 1$（泡利原理） | 无上限 |
| $T = 0$ 行为 | 阶跃函数 | 所有粒子趋于零能量 |
| 物理效应 | 电子高度简并 | 经典理想气体 |

---

## 参见

- [[Kittel Chapter 7 - Energy Bands]] — 电子在周期势中的行为，解释为什么电子不被离子芯散射
- [[Kittel Chapter 5 - Phonons]] — 晶格振动，周期性边界条件的引入
- [[#FREE ELECTRON GAS IN THREE DIMENSIONS]] — 三维自由电子气的完整处理（本文）
- [[Heat Capacity of Electron Gas]] — 电子热容的量子理论

---

## FREE ELECTRON GAS IN THREE DIMENSIONS

### 1. 从一维到三维的过渡

一维问题让我们建立了基本概念（量子化能级、泡利填充、费米能），但真实金属是三维的。三维情况下数学更复杂，但物理本质相同。

### 2. 三维薛定谔方程

自由电子的三维薛定谔方程为：

$$
-\frac{\hbar^2}{2m}\left(\frac{\partial^2}{\partial x^2} + \frac{\partial^2}{\partial y^2} + \frac{\partial^2}{\partial z^2}\right)\psi_{\mathbf{k}}(\mathbf{r}) = \epsilon_{\mathbf{k}}\psi_{\mathbf{k}}(\mathbf{r}) \tag{6}
$$

### 3. 硬壁边界条件 vs 周期性边界条件

#### 硬壁边界条件（初步尝试）

如果电子被限制在边长为 $L$ 的立方体中（原点在角落），驻波解为：

$$
\psi_n(\mathbf{r}) = A \sin\left(\frac{\pi n_x x}{L}\right)\sin\left(\frac{\pi n_y y}{L}\right)\sin\left(\frac{\pi n_z z}{L}\right) \tag{7}
$$

其中 $n_x, n_y, n_z$ 为正整数。这个解可行，但后续处理（计数态、取热力学极限）不够方便。

#### 周期性边界条件（更好的选择）

更便利的是采用**周期性边界条件**（periodic boundary conditions），在第 5 章声子部分已经引入过：

$$
\psi(x+L, y, z) = \psi(x, y, z) \tag{8}
$$

对 $y$ 和 $z$ 方向同样要求周期性。这意味着波函数在盒子边界处"首尾相接"，消除了表面效应。

> [!note] 为什么选周期性边界条件？
> - 消除了硬壁边界带来的表面效应，更聚焦材料的体性质
> - 允许使用行波解（平面波），比驻波更方便
> - $k$ 空间中态的计数变得简洁
> - 热力学极限（$L \to \infty$）下，结果与边界条件的选择无关

### 4. 平面波解与量子数

满足薛定谔方程 (6) 和周期性条件 (8) 的解是**行波平面波**：

$$
\boxed{\psi_{\mathbf{k}}(\mathbf{r}) = \exp(i\mathbf{k} \cdot \mathbf{r})} \tag{9}
$$

但波矢 $\mathbf{k}$ 的分量不是任意的，必须满足周期性条件。代入 (8)：

$$
\exp[ik_x(x+L)] = \exp(i 2n\pi (x+L)/L) = \exp(i 2n\pi x/L) \cdot \exp(i 2n\pi) = \exp(i 2n\pi x/L) \tag{11}
$$

其中用到了 $\exp(i2n\pi) = 1$。因此允许的波矢分量为：

$$
k_x = 0, \quad \pm\frac{2\pi}{L}, \quad \pm\frac{4\pi}{L}, \quad \dots \tag{10}
$$

$k_y$ 和 $k_z$ 同理。每个分量形如 $2n\pi/L$，其中 $n$ 为整数（正、负或零）。

> [!important] 量子数
> 波矢 $\mathbf{k}$ 的三个分量 $(k_x, k_y, k_z)$ 是此问题的**量子数**（加上自旋量子数 $m_s$）。每个允许的 $\mathbf{k}$ 值对应一个单电子轨道。

### 5. 能量、动量和速度

将平面波 (9) 代入薛定谔方程 (6)，得到能量：

$$
\boxed{\epsilon_{\mathbf{k}} = \frac{\hbar^2}{2m}k^2 = \frac{\hbar^2}{2m}(k_x^2 + k_y^2 + k_z^2)} \tag{12}
$$

动量算符 $\mathbf{p} = -i\hbar\nabla$ 作用在平面波上：

$$
\mathbf{p}\psi_{\mathbf{k}}(\mathbf{r}) = -i\hbar\nabla\exp(i\mathbf{k}\cdot\mathbf{r}) = \hbar\mathbf{k}\,\psi_{\mathbf{k}}(\mathbf{r}) \tag{13}
$$

所以平面波是动量的本征函数，本征值为 $\hbar\mathbf{k}$。电子速度为：

$$
\mathbf{v} = \frac{\hbar\mathbf{k}}{m}
$$

> [!tip] 色散关系
> $\epsilon \propto k^2$ 是自由粒子的**色散关系**（dispersion relation）。等能面在 $k$ 空间中是**球面**——这是三维各向同性自由粒子最重要的几何特征。

### 6. 费米球（Fermi Sphere）

$T = 0$ 时，$N$ 个电子从最低能量的 $\mathbf{k}$ 态开始填充。由于 $\epsilon \propto k^2$，等能面是球面，所以被占据的态在 $k$ 空间中形成一个**球**——这就是**费米球**。

![[imgs/fermi_ball.png]]

费米球的表面称为**费米面**（Fermi surface），其半径定义为**费米波矢** $k_F$：

$$
\epsilon_F = \frac{\hbar^2}{2m}k_F^2 \tag{14}
$$

### 7. 费米波矢 $k_F$ 的推导

关键问题：$k_F$ 与电子浓度 $N/V$ 的关系是什么？

**计数 $k$ 空间中的态：**

- 由 (10)，$k_x$ 相邻允许值的间距为 $2\pi/L$，$k_y, k_z$ 同理
- 因此 $k$ 空间中每个允许的 $\mathbf{k}$ 点占据体积 $(2\pi/L)^3$
- 即：**单位 $k$ 空间体积中的态密度为 $V/(2\pi)^3$**（$V = L^3$ 是实空间体积）

**费米球内的总态数：**

费米球体积为 $\frac{4}{3}\pi k_F^3$，乘以每个态占据的 $k$ 空间体积的倒数，再乘以自旋因子 2：

$$
\underbrace{2}_{\text{自旋}} \times \underbrace{\frac{4\pi k_F^3/3}{(2\pi/L)^3}}_{\text{轨道数}} = \frac{V}{3\pi^2}k_F^3 = N \tag{15}
$$

解出 $k_F$：

$$
\boxed{k_F = \left(\frac{3\pi^2 N}{V}\right)^{1/3}} \tag{16}
$$

> [!important] 核心结果
> $k_F$ **只依赖于电子浓度 $N/V$**，与盒子尺寸 $L$ 无关。这是一个纯粹的密度效应。

### 8. 费米能 $\epsilon_F$ 和费米速度 $v_F$

将 (16) 代入 (14)：

$$
\boxed{\epsilon_F = \frac{\hbar^2}{2m}\left(\frac{3\pi^2 N}{V}\right)^{2/3}} \tag{17}
$$

费米速度（费米面上电子的速度）：

$$
\boxed{v_F = \frac{\hbar k_F}{m} = \frac{\hbar}{m}\left(\frac{3\pi^2 N}{V}\right)^{1/3}} \tag{18}
$$

### 9. Table 1 的解读

Kittel 的 Table 1 [[chapters/kittel-chapter6#^798a84|kittel-chapter6]] 计算了多种金属的费米参数。几个值得注意的要点：

- **单价金属**（Li, Na, K, Rb, Cs, Cu, Ag, Au）：电子浓度 $\sim 10^{22}$–$10^{23}$ cm⁻³，$\epsilon_F \sim 1.5$–$7$ eV，$v_F \sim 10^8$ cm/s
- **双价金属**（Be, Mg, Ca等）：电子浓度更高，$\epsilon_F$ 更大（Be 高达 14.14 eV）
- **三价/四价**（Al, Ga, In, Pb, Sn）：介于两者之间
- **费米温度** $T_F = \epsilon_F/k_B \sim 10^4$–$10^5$ K，远高于室温

> [!tip] 费米速度有多大？
> $v_F \sim 10^8$ cm/s = $10^6$ m/s，大约是光速的 0.3%。在室温下，金属中传导电子的典型速度就是这个量级，远大于经典热运动速度（$\sim 10^5$ m/s）。这就是为什么电子传导如此高效。

### 10. 态密度 $D(\epsilon)$

**态密度**（density of states）$D(\epsilon)$ 定义为单位能量间隔内的轨道数，是连接微观量子态和宏观热力学量的核心桥梁。

#### 推导

由 (17) 反过来写：能量 $\leq \epsilon$ 的总轨道数（计入自旋）为：

$$
N(\epsilon) = \frac{V}{3\pi^2}\left(\frac{2m\epsilon}{\hbar^2}\right)^{3/2} \tag{19}
$$

对 $\epsilon$ 求导即得态密度：

$$
\boxed{D(\epsilon) \equiv \frac{dN}{d\epsilon} = \frac{V}{2\pi^2}\left(\frac{2m}{\hbar^2}\right)^{3/2}\epsilon^{1/2}} \tag{20}
$$

#### 简化形式

比较 (19) 和 (20)，可以写出更简洁的关系：

$$
\boxed{D(\epsilon) = \frac{3N}{2\epsilon}} \tag{21}
$$

> [!important] 态密度的物理意义
> - $D(\epsilon) \propto \epsilon^{1/2}$：能量越高，可用的态越密集
> - 在费米能处，$D(\epsilon_F) \approx \frac{3}{2}\frac{N}{\epsilon_F}$：单位能量间隔内的态数正比于总电子数除以费米能
> - 这个关系**不依赖于具体材料参数**，是自由电子气的普适结果

![[imgs/dos.png]]

> Figure 5. Density of single-particle states as a function of energy, for a free electron gas in three dimensions. The dashed curve represents the density $f ( \epsilon , T ) D ( \epsilon )$ of filled orbitals at a finite temperature, but such that $k _ { B } T$ is small in comparison with $\epsilon _ { F } .$ The shaded area represents the filled orbitals at absolute zero. The average energy is increased when the temperature is increased from 0 to T, for electrons are thermally excited from region 1 to region 2.

#### 图 5 的解读

图 5 展示了：
- **$D(\epsilon)$ 曲线**：从原点出发按 $\epsilon^{1/2}$ 增长
- **$T = 0$**：占据函数是阶跃函数，乘积 $f(\epsilon)D(\epsilon)$ 在 $\epsilon_F$ 处截断（阴影面积 = 总电子数）
- **$T > 0$**：$f(\epsilon)$ 在 $\epsilon_F$ 附近软化，占据曲线从区域 1（略低于 $\epsilon_F$）转移到区域 2（略高于 $\epsilon_F$），总电子数不变

### 11. 逻辑总结

> 三维薛定谔方程 → 周期性边界条件 → 平面波解 $\psi_{\mathbf{k}} = e^{i\mathbf{k}\cdot\mathbf{r}}$ → 色散关系 $\epsilon \propto k^2$ → $k$ 空间态计数 → 费米球 → $k_F = (3\pi^2 N/V)^{1/3}$ → $\epsilon_F = \frac{\hbar^2}{2m}(3\pi^2 N/V)^{2/3}$ → 态密度 $D(\epsilon) \propto \epsilon^{1/2}$

这些结果是下一节计算电子热容的基础：只有费米面附近 $\sim k_BT$ 能量范围内的电子（占比 $\sim T/T_F$）才能参与热激发，所以电子热容 $\propto T$，远小于经典预测。

---

## HEAT CAPACITY OF THE ELECTRON GAS

### 1. 问题的历史背景

这是早期金属电子理论发展中**最困难的问题**。

经典统计力学预测自由粒子的热容为 $\frac{3}{2}k_B$（每个自由度 $\frac{1}{2}k_B$，三个方向）。如果 $N$ 个原子各贡献一个价电子，电子气的热容应为：

$$
C_{el}^{\text{classical}} = \frac{3}{2}Nk_B
$$

这与单原子理想气体的热容完全相同。但实验发现，室温下电子贡献的热容远小于此值，通常不到经典预测的 **1%**。

> [!warning] 核心矛盾
> 电子表现得像是**高度自由**的（参与电导），却又不贡献热容。Lorenz 等早期物理学家对此困惑不解。这个矛盾只有在泡利不相容原理和费米分布函数被发现后才得以解决。

Fermi 本人认识到："比热在绝对零度消失，在低温下与绝对温度成正比。"

### 2. 定性理解：为什么热容如此之小？

关键物理图像来自图 5。当从 $T = 0$ 加热到温度 $T$ 时：

- 只有费米能附近 $\sim k_BT$ 能量范围内的电子才能被热激发
- 这部分电子占总数的比例 $\sim k_BT/\epsilon_F = T/T_F$
- 每个被激发的电子获得能量 $\sim k_BT$

因此热激发涉及的总能量：

$$
U_{el} \approx \left(\frac{NT}{T_F}\right) \cdot k_BT \tag{22}
$$

热容为：

$$
C_{el} = \frac{\partial U}{\partial T} \approx Nk_B\left(\frac{T}{T_F}\right) \tag{23}
$$

由于 $T_F \sim 5 \times 10^4$ K，在室温下：

$$
\frac{T}{T_F} \sim \frac{300}{50000} = 0.006
$$

所以电子热容比经典值小约两个数量级。

> [!tip] 物理本质
> 绝大多数电子被泡利不相容原理"冻结"在低能态。它们想被激发，但低能态已经满了，无处可去。只有费米面附近 $\sim k_BT$ 范围内的电子才有"空位"可供跃迁。这就是量子统计对经典统计的根本修正。

### 3. 定量推导

#### 3.1 能量增量的表达式

将系统从 $T = 0$ 加热到温度 $T$ 时，总能量的增加为：

$$
\Delta U = \int_0^{\infty} d\epsilon\, \epsilon\, D(\epsilon)\, f(\epsilon) - \int_0^{\epsilon_F} d\epsilon\, \epsilon\, D(\epsilon) \tag{24}
$$

- 第一项：温度 $T$ 时的总能量（$f$ 是费米-狄拉克分布）
- 第二项：$T = 0$ 时的总能量

> [!note] 为什么对 $\Delta U$ 求导等于对 $U(T)$ 求导？
> 因为 $U(T) = \Delta U + U(0)$，而 $U(0)$ 是一个与温度无关的常数（由 $N$、$V$、$m$ 决定）。常数的导数为零，所以：
> $$
> C_{el} = \frac{\partial U(T)}{\partial T} = \frac{\partial (\Delta U)}{\partial T}
> $$
> 使用 $\Delta U$ 而非 $U(T)$ 是因为它直接对应"加热注入的能量"，物理意义更清晰。

#### 3.2 巧妙的恒等变换

直接对 (24) 求导不方便，因为两项之差看不出激发过程的物理图像。Kittel 的做法是先做恒等变换，把 $\Delta U$ 改写成两个物理意义明确的积分之和。

**第一步：粒子数守恒。** 无论温度怎么变，总电子数不变：

$$
N = \int_0^{\infty} d\epsilon\, D(\epsilon)\, f(\epsilon) = \int_0^{\epsilon_F} d\epsilon\, D(\epsilon) \tag{25}
$$

左边是温度 $T$ 时的总电子数（每个态按占据概率 $f$ 加权），右边是 $T = 0$ 时的总电子数（费米能以下全满）。

**第二步：乘以 $\epsilon_F$ 构造恒等式。** 注意 $\epsilon_F$ 是常数，可以放进积分号：

$$
\int_0^{\infty} \epsilon_F\, D(\epsilon)\, f(\epsilon)\, d\epsilon = \int_0^{\epsilon_F} \epsilon_F\, D(\epsilon)\, d\epsilon \tag{26}
$$

**第三步：改写 (24)。** 将 (24) 的第一项拆成两段：

$$
\Delta U = \underbrace{\int_0^{\epsilon_F} \epsilon\, D f\, d\epsilon}_{\text{(A)}} + \underbrace{\int_{\epsilon_F}^{\infty} \epsilon\, D f\, d\epsilon}_{\text{(B)}} - \underbrace{\int_0^{\epsilon_F} \epsilon\, D\, d\epsilon}_{\text{(C)}}
$$

对 (A) 段，把 $\epsilon$ 写成 $\epsilon = \epsilon_F - (\epsilon_F - \epsilon)$：

$$
\text{(A)} = \int_0^{\epsilon_F} \epsilon_F\, D f\, d\epsilon - \int_0^{\epsilon_F} (\epsilon_F - \epsilon)\, D f\, d\epsilon
$$

对 (A) 的第一部分，利用 (26) 的左半边拆成两段：

$$
\int_0^{\epsilon_F} \epsilon_F\, D f\, d\epsilon = \int_0^{\epsilon_F} \epsilon_F\, D\, d\epsilon - \int_{\epsilon_F}^{\infty} \epsilon_F\, D f\, d\epsilon
$$

代入并整理。$(A) + (B) - (C)$ 中，$\int_0^{\epsilon_F} \epsilon_F D d\epsilon$ 与 $-(C)$ 合并为 $\int_0^{\epsilon_F} (\epsilon_F - \epsilon) D d\epsilon$，$(B)$ 与 $-\int_{\epsilon_F}^{\infty} \epsilon_F D f d\epsilon$ 合并为 $\int_{\epsilon_F}^{\infty} (\epsilon - \epsilon_F) D f d\epsilon$，最后利用 $D - Df = D(1-f)$，最终得到：

$$
\boxed{\Delta U = \int_{\epsilon_F}^{\infty} d\epsilon\, (\epsilon - \epsilon_F)\, f(\epsilon)\, D(\epsilon) + \int_0^{\epsilon_F} d\epsilon\, (\epsilon_F - \epsilon)\, [1 - f(\epsilon)]\, D(\epsilon)} \tag{27}
$$

> [!important] 公式 (27) 的物理诠释
> - **第一项**：将电子从费米面激发到 $\epsilon > \epsilon_F$ 的空轨道所需的能量。$f(\epsilon)D(\epsilon)d\epsilon$ 是被激发的电子数，$(\epsilon - \epsilon_F)$ 是每个电子获得的能量
> - **第二项**：从 $\epsilon < \epsilon_F$ 的轨道上移走电子所对应的能量。$[1-f(\epsilon)]$ 是该轨道被腾空的概率，$(\epsilon_F - \epsilon)$ 是把电子从 $\epsilon$ 提升到费米面所需的能量
> - **两项都是正的**，分别对应图 5 中区域 2（电子激发）和区域 1（空穴产生）的贡献
>
> 加热电子气的过程可以理解为在费米面两侧同时产生**电子-空穴对**。

#### 3.3 热容的积分表达式

对 $\Delta U$ 关于 $T$ 求导。注意只有 $f(\epsilon)$ 依赖于温度：

$$
C_{el} = \frac{dU}{dT} = \int_0^{\infty} d\epsilon\, (\epsilon - \epsilon_F)\, \frac{df}{dT}\, D(\epsilon) \tag{28}
$$

#### 3.4 关键近似：在费米面处取值

对于金属中感兴趣的温度（$k_BT/\epsilon_F < 0.01$），$(\epsilon - \varepsilon_{F})df/dT$ 在 $\epsilon_F$ 附近有尖锐的正峰。因此 $D(\epsilon)$ 在积分区间内变化缓慢，可以近似为常数：

$$
C_{el} \cong D(\epsilon_F) \int_0^{\infty} d\epsilon\, (\epsilon - \epsilon_F)\, \frac{df}{dT} \tag{29}
$$

#### 3.5 化学势的近似

![[imgs/u_ef.png]]

> Figure 8 Variation with temperature of the chemical potential $\mu ,$ for free electron Fermi gases in one and three dimensions. In common metals $\tau / \epsilon _ { F } \simeq 0 . 0 1$ at room temperature, so that $\mu$ is closely equal to $\epsilon _ { F } .$ These curves were calculated from series expansions of the integral for the number of particles in the system.

在 $k_BT \ll \epsilon_F$ 的条件下（图 7 和图 8 显示 $\mu$ 偏离 $\epsilon_F$ 极小），可以将费米-狄拉克分布中的 $\mu$ 替换为常数 $\epsilon_F$。

令 $\tau \equiv k_BT$，计算导数：

$$
\frac{df}{dT} = \frac{\epsilon - \epsilon_F}{\tau^2} \cdot \frac{\exp[(\epsilon - \epsilon_F)/\tau]}{\left\{\exp[(\epsilon - \epsilon_F)/\tau] + 1\right\}^2} \tag{30}
$$

#### 3.6 换元积分

令 $x \equiv (\epsilon - \epsilon_F)/\tau$，则 $d\epsilon = \tau\, dx$。代入 (29) 和 (30)：

$$
C_{el} = k_B^2 T\, D(\epsilon_F) \int_{-\epsilon_F/\tau}^{\infty} dx\, x^2 \frac{e^x}{(e^x + 1)^2} \tag{32}
$$

由于 $\epsilon_F/\tau \sim 100$ 或更大，被积函数在 $x = -\epsilon_F/\tau$ 处已经小到可以忽略（$e^x$ 因子使然），因此可以安全地将下界扩展到 $-\infty$：

$$
\int_{-\infty}^{\infty} dx\, x^2 \frac{e^x}{(e^x + 1)^2} = \frac{\pi^2}{3} \tag{33}
$$

> [!tip] 这个积分
> 这个积分是 Sommerfeld 展开的核心结果。被积函数 $e^x/(e^x+1)^2$ 是一个偶函数形状的峰（在 $x=0$ 处最大），$x^2$ 加权后给出 $\pi^2/3$。这个结果与材料细节无关，是纯数学的。

#### 3.7 最终结果

代入 (33)：

$$
\boxed{C_{el} = \frac{1}{3}\pi^2 D(\epsilon_F)\, k_B^2 T} \tag{34}
$$

利用 $D(\epsilon_F) = 3N/(2\epsilon_F) = 3N/(2k_BT_F)$（来自公式 21）：

$$
\boxed{C_{el} = \frac{1}{2}\pi^2 N k_B \frac{T}{T_F}} \tag{36}
$$

> [!important] 核心结论
> - $C_{el} \propto T$：与实验一致
> - 数值系数 $\frac{1}{2}\pi^2 \approx 4.93$
> - 与经典值 $\frac{3}{2}Nk_B$ 相比，量子结果多了一个因子 $\pi^2 T/T_F$（室温下 $\sim 0.06$）
> - $T_F$ 是费米温度，**不是**电子的实际温度，只是为了方便而引入的参考量

### 4. 实验验证

#### 4.1 $C/T$ vs $T^2$ 作图法

在温度远低于 Debye 温度 $\Theta_D$ 和费米温度 $T_F$ 的条件下，金属的热容可以写成电子和声子贡献之和：

$$
C = \gamma T + AT^3
$$

其中：
- $\gamma T$：电子贡献（$\propto T$）
- $AT^3$：声子（晶格振动）贡献（Debye 模型，$\propto T^3$）

两边除以 $T$：

$$
\frac{C}{T} = \gamma + AT^2 \tag{37}
$$

以 $C/T$ 为纵轴、$T^2$ 为横轴作图，应得到一条直线：
- **截距** = $\gamma$（电子热容系数，Sommerfeld 参数）
- **斜率** = $A$（声子贡献系数）

图 9 展示了钾的实验数据，确实呈线性关系。

#### 4.2 Table 2 的解读

Table 2 列出了多种金属的实验 $\gamma$ 值和自由电子模型计算值的对比。几个关键观察：

- 碱金属（Li, Na, K, Rb, Cs）的 $m_{th}/m$ 在 1.2–1.45 之间，与自由电子模型相当接近
- Cu, Ag, Au（贵金属）的值也较接近 1
- 有些金属偏离较大（Ca: 1.9, Pb: 1.97）
- Bi 的 $\gamma$ 极小（0.008），说明自由电子模型对其极不适用

#### 4.3 有效质量比 $m_{th}/m$ 偏离 1 的三种物理机制

> [!note] 定义
> 定义**热有效质量** $m_{th}$：
> $$
> \frac{m_{th}}{m} \equiv \frac{\gamma_{\text{observed}}}{\gamma_{\text{free}}} \tag{38}
> $$
> 由于 $\epsilon_F \propto 1/m$，所以 $\gamma \propto m$，这个比值自然出现。

三种机制：

**（a）电子-晶格周期势相互作用**
- 电子在晶格周期势中的运动不同于自由电子
- 用**能带有效质量** $m^*$ 描述：$(m^*)^{-1} = \frac{1}{\hbar^2}\frac{d^2\epsilon}{dk^2}$
- 这是下一章（能带理论）的核心内容

**（b）电子-声子相互作用**
- 运动电子会极化/扭曲周围晶格
- 电子试图"拖拽"附近离子一起运动
- 这增加了电子的惯性 → 有效质量增大
- 这种效应在重元素中更显著

**（c）电子-电子相互作用**
- 运动电子在周围电子气中引起惯性反应
- 相当于电子拖拽着其他电子一起运动
- 也导致有效质量增大

### 5. 重费米子化合物（Heavy Fermions）

> [!tip] 极端现象
> 某些金属化合物的电子热容系数 $\gamma$ 比常规金属**大 2–3 个数量级**！
>
> 包括：$\text{UBe}_{13}$、$\text{CeAl}_3$、$\text{CeCu}_2\text{Si}_2$ 等
>
> 这些化合物中的 f 电子由于波函数重叠极弱（第 9 章紧束缚模型），惯性质量可达 $\sim 1000\, m$。

这意味着在重费米子化合物中，电子被晶格周期势"束缚"得如此之紧，以至于它们表现得像是质量巨大的准粒子。这是强关联电子体系中最引人注目的现象之一。

---

## ELECTRICAL CONDUCTIVITY AND OHM'S LAW

### 1. 核心图像：费米球在 k 空间中的平移

**无外场时：** 费米球中心在原点。对于每个被占据的 $\mathbf{k}$ 态，$-\mathbf{k}$ 态也被占据。总动量为零，没有净电流。

**施加电场 $\mathbf{E}$ 后：** 每个电子受到力 $\mathbf{F} = -e\mathbf{E}$。量子版本的牛顿第二定律：

$$
\mathbf{F} = m\frac{d\mathbf{v}}{dt} = \hbar\frac{d\mathbf{k}}{dt} = -e\left(\mathbf{E} + \frac{1}{c}\mathbf{v} \times \mathbf{B}\right) \tag{39}
$$

当 $\mathbf{B} = 0$ 时，积分得：

$$
\mathbf{k}(t) - \mathbf{k}(0) = -e\mathbf{E}t/\hbar \tag{40}
$$

**关键：所有电子的 $\mathbf{k}$ 都增加相同的量。** 整个费米球在 k 空间中刚性平移了：

$$
\delta\mathbf{k} = -e\mathbf{E}t/\hbar \tag{41}
$$

> [!important] 费米球的刚性平移
> 费米球作为一个刚体在 k 空间中移动。球内所有电子态一起移动，球的形状不变。这是因为每个电子受到相同的力，获得相同的 $\Delta\mathbf{k}$。

### 2. 欧姆定律的推导

如果没有碰撞，费米球会不断加速。实际上电子会与杂质、晶格缺陷、声子碰撞，使费米球回到平衡位置。

设碰撞时间为 $\tau$，稳态下费米球的位移为 $\delta\mathbf{k} = -e\mathbf{E}\tau/\hbar$。增量速度：

$$
\mathbf{v} = \frac{\hbar\delta\mathbf{k}}{m} = -\frac{e\mathbf{E}\tau}{m}
$$

电流密度 $\mathbf{j} = nq\mathbf{v}$，其中 $q = -e$：

$$
\mathbf{j} = \frac{ne^2\tau}{m}\mathbf{E}
$$

这就是**欧姆定律** $\mathbf{j} = \sigma\mathbf{E}$，其中：

$$
\boxed{\sigma = \frac{ne^2\tau}{m}} \tag{43}
$$

$$
\rho = \frac{1}{\sigma} = \frac{m}{ne^2\tau} \tag{44}
$$

### 3. 实验电阻率与 Matthiessen 定则

金属中的电阻率来源于两种独立的散射：

- **声子散射** $\rho_L$：电子与热振动的晶格碰撞，依赖于温度
- **杂质/缺陷散射** $\rho_i$：电子与静态缺陷碰撞，与温度无关

当两种散射机制独立时，总散射率为各自散射率之和：

$$
\frac{1}{\tau} = \frac{1}{\tau_L} + \frac{1}{\tau_i}
$$

因此：

$$
\boxed{\rho = \rho_L + \rho_i} \tag{46}
$$

这就是 **Matthiessen 定则**。$\rho_i(0)$（残余电阻率）是外推到 $T = 0$ K 时的电阻率，$\rho_L(T) = \rho - \rho_i(0)$ 对同一金属的不同样品相同。

> [!tip] 电阻率比与样品纯度
> 电阻率比 = 室温电阻率 / 残余电阻率，是样品纯度的指标。每原子百分比的杂质约产生 $1\,\mu\Omega\cdot\text{cm}$ 的残余电阻率。极纯样品电阻率比可达 $10^6$。

### 4. 平均自由程

$$
\boxed{\ell = v_F\tau} \tag{47}
$$

> [!important] 为什么用 $v_F$？
> 只有**费米面附近的电子参与输导**。深处的电子被泡利原理束缚，无法改变状态。输运过程只涉及费米面附近 $\sim k_BT$ 能量范围内的电子，它们的速度就是 $v_F$。

以铜为例：$v_F = 1.57 \times 10^8$ cm/s，在 4 K 时 $\tau \approx 2 \times 10^{-9}$ s，所以 $\ell(4\text{ K}) \approx 0.3$ cm。极纯金属在液氦温度下平均自由程可达 10 cm 以上。

### 5. 电阻率的温度依赖与 Umklapp 散射

**高温极限（$T > \Theta_D$）：** 声子浓度 $\propto T$，碰撞率 $\propto T$，所以 $\rho \propto T$。

**Umklapp 散射（倒逆散射）：** 散射过程涉及一个倒格矢 $\mathbf{G}$：

$$
\mathbf{k}' = \mathbf{k} + \mathbf{q} + \mathbf{G}
$$

这可以将电子的波矢"翻转"到布里渊区的另一侧。Umklapp 散射可以产生大角度偏转，是低温下电阻率的主要贡献者。

当费米面不与布里渊区边界相交时，存在最小声子波矢 $q_0$ 才能发生 Umklapp 散射。低温下：

$$
\text{Umklapp 散射率} \propto \exp(-\theta_U/T)
$$

对于钾（bcc，球形费米面），几何计算给出 $q_0 = 0.267 k_F$，实验测得 $\theta_U = 23$ K（远低于 Debye 温度 91 K）。在极低温下（钾中 $T < 2$ K），Umklapp 散射几乎消失。

### 6. 磁场中的运动

在电场和磁场中，考虑碰撞（弛豫时间 $\tau$），运动方程为：

$$
\hbar\left(\frac{d}{dt} + \frac{1}{\tau}\right)\delta\mathbf{k} = \mathbf{F} \tag{48}
$$

其中 $\mathbf{F} = -e\left(\mathbf{E} + \frac{1}{c}\mathbf{v} \times \mathbf{B}\right)$。

稳恒条件下（$\mathbf{B}$ 沿 $z$ 轴），漂移速度为：

$$
v_x = -\frac{e\tau}{m}E_x - \omega_c\tau v_y, \quad v_y = -\frac{e\tau}{m}E_y + \omega_c\tau v_x, \quad v_z = -\frac{e\tau}{m}E_z
$$

其中 $\omega_c = eB/mc$ 是**回旋频率**。

### 7. 霍尔效应

在纵向电场 $E_x$ 和横向磁场 $B_z$ 中，电子在 $-y$ 方向偏转并积累，产生横向霍尔电场 $E_y$。平衡时 $v_y = 0$：

$$
E_y = -\omega_c\tau E_x = -\frac{eB\tau}{mc}E_x \tag{53}
$$

定义**霍尔系数**：

$$
\boxed{R_H = \frac{E_y}{j_x B}} \tag{54}
$$

利用 $j_x = ne^2\tau E_x/m$：

$$
\boxed{R_H = -\frac{1}{nec}} \tag{55}
$$

> [!important] 霍尔系数的意义
> - **负号**：自由电子（负电荷）的 $R_H < 0$
> - **反比于 $n$**：载流子浓度越低，霍尔效应越显著
> - **与 $\tau$ 无关**：只依赖于载流子浓度

### 8. 霍尔效应的符号异常

实验发现 Al 和 In 的霍尔系数为**正**，意味着载流子表现为正电荷。自由电子模型完全无法解释。

> [!warning] 空穴（Holes）
> Peierls（1928）和 Heisenberg 解释了这种异常：在某些金属中，参与输运的不是电子，而是**空穴**——能带中未被电子占据的态，表现为正电荷载流子。这需要**能带理论**（第 7-9 章）才能解释。当费米面接近布里渊区边界时，电子的有效质量可以为负，等价于正电荷的空穴。

### 9. 热导率

利用 $K = \frac{1}{3}Cv\ell$，代入电子气的结果：

$$
\boxed{K_{el} = \frac{\pi^2 nk_B^2 T\tau}{3m}} \tag{56}
$$

纯金属中电子热导在所有温度下都占主导。

### 10. Wiedemann-Franz 定律

将 $K_{el}$（公式 56）除以 $\sigma$（公式 43）：

$$
\frac{K}{\sigma} = \frac{\pi^2 k_B^2}{3e^2}T
$$

定义 **Lorenz 数** $L = K/\sigma T$：

$$
\boxed{L = \frac{\pi^2}{3}\left(\frac{k_B}{e}\right)^2 = 2.45 \times 10^{-8}\text{ W}\cdot\Omega/\text{K}^2} \tag{59}
$$

> [!important] Wiedemann-Franz 定律的深刻之处
> - $L$ **与 $n$ 无关**：不依赖于载流子浓度
> - $L$ **与 $m$ 无关**：不依赖于电子质量
> - $L$ **与 $\tau$ 无关**：不依赖于散射机制
> - $L$ **对所有金属都是同一个常数**！
>
> Table 5 的实验数据验证了这一点。所有金属的 Lorenz 数都在 $2.3$–$3.2 \times 10^{-8}$ W·Ω/K² 范围内，与理论值符合得很好。这证明了同一种载流子（电子）同时负责电荷输运和能量输导。

---

## 参见

- [[Kittel Chapter 7 - Energy Bands]] — 电子在周期势中的行为，能带有效质量与空穴的来源
- [[Kittel Chapter 5 - Phonons]] — 晶格振动，电子-声子散射与 Umklapp 过程
- [[Hall Effect]] — 霍尔效应的更深入讨论
- [[Wiedemann-Franz Law]] — Wiedemann-Franz 定律
