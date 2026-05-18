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
- [[Free Electron Gas in 3D]] — 三维自由电子气的完整处理
- [[Heat Capacity of Electron Gas]] — 电子热容的量子理论
