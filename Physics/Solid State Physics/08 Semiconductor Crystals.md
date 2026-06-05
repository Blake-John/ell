---
title: 08 Semiconductor Crystals
tags:
  - solid-state-physics
  - semiconductor
  - kittel
  - band-gap
  - effective-mass
  - holes
  - equations-of-motion
aliases:
  - 半导体晶体
  - Kittel Chapter 8
cssclasses:
  - physics-note
---

# 08 Semiconductor Crystals

> *对应 Kittel《固态物理学》第8章*

## 引言

### 电阻率分类

| 材料 | 电阻率范围 (ohm·cm) |
|------|---------------------|
| 导体 | $< 10^{-2}$ |
| **半导体** | $10^{-2}$ ~ $10^{9}$ |
| 绝缘体 | $> 10^{14}$ |

半导体的电阻率**强烈依赖温度**。绝对零度时，纯净完美的半导体晶体是绝缘体。

### 化合物半导体命名

| 类型 | 组成 | 示例 |
|------|------|------|
| III-V | A为三价，B为五价 | InSb, GaAs |
| II-VI | A为二价，B为六价 | ZnS, CdS |
| IV-IV | A、B均为四价 | SiC |
| 金刚石型 | 与金刚石同结构 | Si, Ge |

> [!note] 本征导电 vs. 杂质导电
> 高纯度半导体表现**本征导电**，杂质半导体表现**杂质导电**。在本征温区，电学性质由带隙 $E_g$ 决定。

### 图1：载流子浓度的分类

![Fig. 1](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/cb2b8880-de0d-46c9-86bc-a8ed5d76e463/e7dee2a803e28e0f0e852b73dfb6e9530e3fd6c2029f02f22479ba36b51cc9d5.jpg)

> Figure 1 Carrier concentrations for metals, semimetals, and semiconductors.

金属 $\sim 10^{22}$ cm$^{-3}$，半金属 $\sim 10^{17}$~$10^{20}$ cm$^{-3}$，半导体 $\sim 10^{6}$~$10^{19}$ cm$^{-3}$。半导体的范围可通过掺杂向上扩展。

---

## 1 BAND GAP（带隙）

> **带隙是半导体物理的核心参数。**

### 1.1 带隙的定义

**带隙 $E_g$**：导带底与价带顶之间的能量差。

$$\boxed{E_g = E_c - E_v}$$

本征电导率和本征载流子浓度由无量纲比值 $E_g / k_B T$ 控制。室温下 $k_B T \approx 0.026$ eV，Si 的 $E_g/k_BT \approx 43$，Ge 的 $\approx 25$。

> [!important] 与第6章自由电子气的类比
> 第6章：$k_BT \ll \epsilon_F$，电子气高度简并，只有费米面附近电子参与热激发。
> 半导体：$E_g \gg k_BT$，绝大多数价带电子被带隙锁住，无法热激发。

### 1.2 图2：本征导电的能带图像

![Fig. 2](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/cb2b8880-de0d-46c9-86bc-a8ed5d76e463/ecea33d957b0305e4fd60e7761ef1de86e458a7249aeea0a5abe3ee64db976cd.jpg)

> Figure 2 Band scheme for intrinsic conductivity in a semiconductor.

**$T = 0$ K**：价带全满，导带全空，电导率为零。

**$T > 0$ K**：电子从价带热激发到导带，导带出现自由电子，价带留下空穴，两者都参与导电。

### 1.3 图3：本征载流子浓度

![Fig. 3a](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/cb2b8880-de0d-46c9-86bc-a8ed5d76e463/1597ebd2373d5ccbcd8168af47f88ca762c75d188713898ddf791406718c6178.jpg)

![Fig. 3b](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/cb2b8880-de0d-46c9-86bc-a8ed5d76e463/76fb9114eeab55e490b8649858e6eca509f8b212ba2f1109b9a29a1ce5cb1d9b.jpg)

> Figure 3 Intrinsic electron concentration for (a) Ge and (b) Si.

$\ln n_i$ ~ $1/T$ 呈直线，斜率 $-E_g/2k_B$。相同温度下 Ge 的 $n_i$ 高于 Si，因为 Ge 带隙更窄。本征条件：$n = p = n_i$。

### 1.4 直接吸收过程（Direct Absorption Process）

**条件**：导带底和价带顶在 k 空间**同一位置**（如都在 $\Gamma$ 点）。典型材料：GaAs、InSb、CdS。

**物理过程**：光子被吸收，直接将电子从价带顶激发到导带底：

$$\text{光子} \to \text{电子（导带）} + \text{空穴（价带）}$$

**为什么光子可以单独完成？** 光子波矢极小：

$$k_{photon} = \frac{\omega}{c} \sim \frac{E_g}{\hbar c} \sim 5 \times 10^{4} \text{ cm}^{-1}$$

而布里渊区尺度 $k_{BZ} \sim 2\pi/a \sim 10^{8}$ cm$^{-1}$，光子波矢小了约 3~4 个数量级。跃迁在 k 空间几乎**竖直**。

**守恒律**：

$$\hbar\omega = E_g, \qquad \mathbf{k}_f = \mathbf{k}_i + \mathbf{k}_{photon} \approx \mathbf{k}_i$$

**特征**：吸收阈值 = 带隙 $E_g = \hbar\omega_g$；吸收强，阈值陡峭；二体过程，概率高；发光效率高。

#### 图5(a)：直接带隙 k 空间图像

![Fig. 5a](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/cb2b8880-de0d-46c9-86bc-a8ed5d76e463/104eee46a58ad3170e9422c84155f4d527936bde319dbbafeb3ea5f9c7373ba7.jpg)

> Figure 5(a) 导带底和价带顶在同一 $\mathbf{k}$ 值，光跃迁为竖直箭头。

#### 图4(a)：直接带隙光吸收谱

![Fig. 4a](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/cb2b8880-de0d-46c9-86bc-a8ed5d76e463/987350f6eb16b29f971f9d82556f7aba92ce512a8acd56be970f9a88252e5c00.jpg)

> Figure 4(a) 直接带隙的光吸收。阈值确定 $E_g = \hbar\omega_g$。

### 1.5 间接吸收过程（Indirect Absorption Process）

**条件**：导带底和价带顶在 k 空间**相距很远**。典型材料：Si、Ge、GaP。

**为什么光子单独无法完成？** 电子从价带顶跃迁到导带底需要改变波矢 $\Delta\mathbf{k} = \mathbf{k}_c$，但光子波矢 $\sim 0$，无法满足波矢守恒。

**声子登场**：声子能量很小（$\hbar\Omega \sim 0.01$~$0.03$ eV），但波矢可以很大（覆盖整个布里渊区）。声子充当"**动量搬运工**"。

**守恒律**：

$$\mathbf{k}_f = \mathbf{k}_i + \mathbf{K}_{phonon}$$

$$\hbar\omega = E_g + \hbar\Omega \quad (\text{产生声子，低温})$$
$$\hbar\omega = E_g - \hbar\Omega \quad (\text{吸收声子，高温})$$

**特征**：吸收阈值 $\neq$ 真实带隙；吸收弱，阈值平缓；三体过程，概率低；发光效率低。

#### 图5(b)：间接带隙 k 空间图像

![Fig. 5b](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/cb2b8880-de0d-46c9-86bc-a8ed5d76e463/5dec13c72b65ef81ab97d26c9f1cf974d90b11e9a8bd329d16e6fb04ac5b827b.jpg)

> Figure 5(b) 间接跃迁需要光子和声子共同参与。

#### 图4(b)：间接带隙光吸收谱

![Fig. 4b](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/cb2b8880-de0d-46c9-86bc-a8ed5d76e463/0e59b0f6add11f792e2fabbc9fb7cdd4a8b36be63c74df2e07d9047005a525a0.jpg)

> Figure 4(b) 间接带隙的光吸收。阈值在 $\hbar\omega = E_g + \hbar\Omega$，大于真实带隙。$E_{vert}$ 标记不需要声子的竖直跃迁阈值。

### 1.6 间接带隙中的竖直跃迁 $E_{vert}$

在间接带隙材料中，价带中某个 $\mathbf{k}_i$ 处的电子可被竖直激发到导带中相同 $\mathbf{k}_i$ 的态，不需要声子。但导带中该 $\mathbf{k}_i$ 态能量远高于导带底，所需能量 $E_{vert} > E_g$。

间接带隙材料有两个特征能量：$E_g$（真实带隙，需声子辅助）和 $E_{vert}$（竖直跃迁阈值，不需声子但能量更高）。

### 1.7 激子（Exciton）

图4注释：吸收阈值以下有时会出现吸收线，对应**激子**——电子和空穴通过库仑吸引形成的束缚态，类似氢原子。

- 激子能量 = $E_g - E_b$（$E_b$ 为束缚能，通常几到几十 meV）
- 激子整体电中性，不直接贡献电导
- 可在晶体中移动

### 1.8 带隙的测量方法

1. **光学吸收法**（最佳）：直接带隙材料给出尖锐吸收边；间接带隙分析 $\alpha$ 与 $\hbar\omega$ 关系，$(\alpha\hbar\omega)^{1/2}$ ~ $\hbar\omega$ 外推得 $E_g$
2. **电学法**：本征温区测霍尔电压得 $n_i$，$\ln n_i$ ~ $1/T$ 斜率给出 $E_g/2$
3. **电导率**：本征区 $\rho \propto \exp(E_g/2k_BT)$

### 1.9 带隙的温度依赖性

温度升高，带隙**减小**：

| 材料 | $E_g$ (0 K) | $E_g$ (300 K) |
|------|-------------|---------------|
| Si | 1.17 eV | 1.11 eV |
| Ge | 0.744 eV | 0.66 eV |
| GaAs | 1.52 eV | 1.43 eV |

**来源**：(1) 晶格热膨胀；(2) 电子-声子相互作用。

**Varshni 公式**：$E_g(T) = E_g(0) - \alpha T^2/(T+\beta)$

### 1.10 图6：InSb 直接吸收实验

![Fig. 6](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/cb2b8880-de0d-46c9-86bc-a8ed5d76e463/f46130f5eb5298709d7f2cbf1957115a885512d5f0d0f2a173711717817cfdb2.jpg)

> Figure 6 Optical absorption in InSb. 导带底和价带顶都在 $\mathbf{k}=0$，吸收阈值尖锐。

### 1.11 带隙数据表

| 晶体 | 类型 | $E_g$(0K) | $E_g$(300K) | 晶体 | 类型 | $E_g$(0K) | $E_g$(300K) |
|------|------|-----------|-------------|------|------|-----------|-------------|
| Diamond | i | 5.4 | — | SiC(hex) | i | 3.0 | — |
| Si | i | 1.17 | 1.11 | InSb | d | 0.23 | 0.17 |
| Ge | i | 0.744 | 0.66 | InAs | d | 0.43 | 0.36 |
| αSn | d | 0.00 | 0.00 | InP | d | 1.42 | 1.27 |
| GaP | i | 2.32 | 2.25 | GaAs | d | 1.52 | 1.43 |
| GaSb | d | 0.81 | 0.68 | AlSb | i | 1.65 | 1.6 |
| CdS | d | 2.582 | 2.42 | CdSe | d | 1.840 | 1.74 |
| CdTe | d | 1.607 | 1.44 | PbS | d | 0.286 | 0.34–0.37 |
| PbSe | i | 0.165 | 0.27 | PbTe | i | 0.190 | 0.29 |
| SnTe | d | 0.3 | 0.18 | Cu₂O | d | 2.172 | — |
| **HgTe** | **d** | **−0.30** | — | | | | |

> [!warning] HgTe 带隙为**负值**（−0.30 eV），导带和价带交叠，为**半金属**。α-Sn 带隙恰好为零，处于临界点。

### 1.12 直接/间接带隙对比

| 特征 | 直接带隙 | 间接带隙 |
|------|---------|---------|
| 带边位置 | 同一 $\mathbf{k}$ | 不同 $\mathbf{k}$ |
| 跃迁粒子 | 仅光子 | 光子 + 声子 |
| 吸收阈值 | $\hbar\omega_g = E_g$ | $E_g \pm \hbar\Omega$ |
| 吸收强度 | 强，陡峭 | 弱，平缓 |
| 过程阶数 | 二体，概率高 | 三体，概率低 |
| 发光效率 | 高（LED、激光器） | 低（Si 几乎不发光） |
| 代表材料 | GaAs, InSb, CdS | Si, Ge, GaP |

---

## 2 EQUATIONS OF MOTION（运动方程）

> 推导电子在能带中的运动方程。

### 2.1 推导

#### 2.1.1 群速度

考虑由特定 $\mathbf{k}$ 附近波函数组成的波包。群速度定义为 $v_g = d\omega/dk$。量子理论中 $\omega = \epsilon/\hbar$，因此：

$$\boxed{\mathbf{v} = \hbar^{-1} \nabla_{\mathbf{k}} \epsilon(\mathbf{k})} \tag{1}$$

晶格对电子运动的影响全部包含在色散关系 $\epsilon(\mathbf{k})$ 中。

#### 2.1.2 电场中的运动方程

电场 $\mathbf{E}$ 对电子做功，在 $\delta t$ 时间内能量变化：

$$\delta\epsilon = -e E v_g \, \delta t \tag{2}$$

另一方面，由 (1) 有 $d\epsilon/dk = \hbar v_g$，所以：

$$\delta\epsilon = \frac{d\epsilon}{dk}\delta k = \hbar v_g \, \delta k \tag{3}$$

比较 (2) 与 (3)，消去 $v_g$：

$$\delta k = -\frac{eE}{\hbar}\delta t \tag{4}$$

推广到一般外力 $\mathbf{F}$：

$$\boxed{\hbar\frac{d\mathbf{k}}{dt} = \mathbf{F}} \tag{5}$$

> [!important]
> 这是晶体中电子运动的**基本方程**。形式上类似牛顿第二定律，但"动量"是**晶体动量** $\hbar\mathbf{k}$，不是真实动量。晶格周期势的影响被藏进了 $\epsilon(\mathbf{k})$。Kittel 强调："We have not overthrown Newton's second law"。

#### 2.1.3 磁场中的运动方程

加入磁场，洛伦兹力也进入右端（SI 单位制）：

$$\hbar\frac{d\mathbf{k}}{dt} = -e\mathbf{v} \times \mathbf{B} \tag{6}$$

代入群速度 $\mathbf{v} = \hbar^{-1}\nabla_{\mathbf{k}}\epsilon$，得到纯 k 空间的运动方程：

$$\boxed{\frac{d\mathbf{k}}{dt} = -\frac{e}{\hbar^2}\nabla_{\mathbf{k}}\epsilon \times \mathbf{B}} \tag{7}$$

#### 2.1.4 磁场中运动的物理图像

由 (7) 中的叉积，$d\mathbf{k}/dt \perp \nabla_{\mathbf{k}}\epsilon$，即电子在 k 空间中沿**垂直于等能面法线**的方向运动。

> [!keypoint]
> 1. 电子在**等能面**上运动（磁场不做功，能量守恒）
> 2. $k_B$（$\mathbf{k}$ 在 $\mathbf{B}$ 方向的投影）**守恒**
> 3. 轨道 = 等能面 $\cap$ 垂直于 $\mathbf{B}$ 的平面

实空间中电子做螺旋运动：垂直于 $\mathbf{B}$ 平面内为圆周运动（回旋），沿 $\mathbf{B}$ 方向为匀速直线运动。

---

### 2.2 Physical Derivation of $\hbar\dot{\mathbf{k}} = \mathbf{F}$

> 用动量守恒论证 $\hbar\dot{\mathbf{k}} = \mathbf{F}$ 的物理基础。

#### 2.2.1 布洛赫波函数

$$\psi_{\mathbf{k}} = \sum_{\mathbf{G}} C(\mathbf{k}+\mathbf{G})\exp[i(\mathbf{k}+\mathbf{G})\cdot\mathbf{r}] \tag{8}$$

布洛赫波函数是多个平面波的叠加，每个分量 $\mathbf{k}+\mathbf{G}$ 携带动量 $\hbar(\mathbf{k}+\mathbf{G})$。

#### 2.2.2 动量期望值

$$\mathbf{P}_{\mathrm{el}} = \langle\psi_{\mathbf{k}}|-i\hbar\nabla|\psi_{\mathbf{k}}\rangle = \sum_{\mathbf{G}}\hbar(\mathbf{k}+\mathbf{G})|C(\mathbf{k}+\mathbf{G})|^2$$

$$= \hbar\mathbf{k} + \hbar\sum_{\mathbf{G}}\mathbf{G}|C(\mathbf{k}+\mathbf{G})|^2 \tag{9}$$

其中用了归一化 $\sum_{\mathbf{G}}|C(\mathbf{k}+\mathbf{G})|^2 = 1$。

> [!note]
> 电子的真实动量期望值 $\mathbf{P}_{\mathrm{el}} \neq \hbar\mathbf{k}$。$\hbar\mathbf{k}$ 是**晶体动量**（量子数），不是真实力学动量。修正项 $\hbar\sum_{\mathbf{G}}\mathbf{G}|C|^2$ 来自周期势引起的布拉格反射。

#### 2.2.3 动量守恒论证

考虑电中性绝缘晶体，仅一个电子在某能带中。施加外力冲量 $\mathbf{J} = \int\mathbf{F}\,dt$。

**自由电子**：$\mathbf{J} = \hbar\Delta\mathbf{k}$

**晶体中的电子**：总动量变化 = 电子动量变化 + 晶格动量变化：

$$\mathbf{J} = \Delta\mathbf{p}_{\mathrm{el}} + \Delta\mathbf{p}_{\mathrm{lat}} \tag{11}$$

当 $\mathbf{k} \to \mathbf{k}+\Delta\mathbf{k}$ 时，由 (9)：

$$\Delta\mathbf{p}_{\mathrm{el}} = \hbar\Delta\mathbf{k} + \sum_{\mathbf{G}}\hbar\mathbf{G}\left[(\nabla_{\mathbf{k}}|C(\mathbf{k}+\mathbf{G})|^2)\cdot\Delta\mathbf{k}\right] \tag{12}$$

**晶格动量的变化**：当电子被晶格布拉格反射时，晶格获得动量 $-\hbar\mathbf{G}$。当系数变化 $\Delta|C|^2$ 时：

$$\Delta\mathbf{p}_{\mathrm{lat}} = -\sum_{\mathbf{G}}\hbar\mathbf{G}\left[(\nabla_{\mathbf{k}}|C(\mathbf{k}+\mathbf{G})|^2)\cdot\Delta\mathbf{k}\right] \tag{13}$$

#### 2.2.4 恰好抵消

$$\Delta\mathbf{p}_{\mathrm{el}} + \Delta\mathbf{p}_{\mathrm{lat}} = \hbar\Delta\mathbf{k} = \mathbf{J} \tag{15}$$

晶格动量的修正项**恰好抵消**电子动量中的修正项。因此：

$$\hbar\frac{d\mathbf{k}}{dt} = \mathbf{F} \tag{16}$$

> [!keypoint]
> 晶格通过布拉格反射与电子交换动量，但外力给予系统的全部冲量表现为 $\hbar\mathbf{k}$ 的变化。晶格内部动量的重新分配不改变总量。这就是 $\hbar\dot{\mathbf{k}}=\mathbf{F}$ 的物理基础。

---

### 2.3 HOLES（空穴）

> 价带中未被电子占据的态称为**空穴**。没有空穴就没有晶体管。空穴在电磁场中表现为**正电荷** $+e$。以下五步论证。

#### 2.3.1 第一步：$\mathbf{k}_h = -\mathbf{k}_e$

满带总波矢为零（布里渊区反演对称，$\mathbf{k}$ 和 $-\mathbf{k}$ 成对占据）。移走 $\mathbf{k}_e$ 处电子后，系统总波矢为 $-\mathbf{k}_e$，赋予空穴：

$$\mathbf{k}_h = -\mathbf{k}_e \tag{17}$$

> 空穴在图中画在 $\mathbf{k}_e$ 位置，但其**真实波矢**为 $-\mathbf{k}_e$。

图7：光子吸收产生电子-空穴对

![Fig. 7](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/cb2b8880-de0d-46c9-86bc-a8ed5d76e463/0f6dbc1655fe1e38ccb00f6160bcf5e77cc20014c0e67e72c61554c5cf49b3ff.jpg)

> Figure 7 光子将电子从价带 E 点激发到导带 Q 点。价带总波矢变为 $-\mathbf{k}_e$，即空穴波矢。整个系统总波矢守恒：$\mathbf{k}_e + \mathbf{k}_h = 0$。

#### 2.3.2 第二步：$\epsilon_h(\mathbf{k}_h) = -\epsilon_e(\mathbf{k}_e)$

价带能量零点在带顶。电子越低，移除所需功越大。空穴能量与缺失电子相反：

$$\epsilon_h(\mathbf{k}_h) = -\epsilon_e(\mathbf{k}_e) \tag{18}$$

由能带对称性 $\epsilon_e(\mathbf{k}_e) = \epsilon_e(-\mathbf{k}_e) = -\epsilon_h(-\mathbf{k}_e) = -\epsilon_h(\mathbf{k}_h)$。

图8：空穴能带

![Fig. 8](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/cb2b8880-de0d-46c9-86bc-a8ed5d76e463/d3a033f7b66966af57bd996dd5b33f21d8aa8a2b851ccefbe6a71a36212f6438.jpg)

> Figure 8 空穴能带由价带关于原点反转构造。空穴能带"正立"，便于分析。

#### 2.3.3 第三步：$\mathbf{v}_h = \mathbf{v}_e$

$$\mathbf{v}_h(\mathbf{k}_h) = \hbar^{-1}\nabla_{\mathbf{k}_h}\epsilon_h = \hbar^{-1}\nabla_{\mathbf{k}_e}\epsilon_e = \mathbf{v}_e(\mathbf{k}_e) \tag{19}$$

空穴速度等于缺失电子的速度。

#### 2.3.4 第四步：$m_h = -m_e$

有效质量与曲率成反比。价带顶曲率向下，电子有效质量为**负**。空穴能带反转后曲率向上：

$$m_h = -m_e > 0 \tag{20}$$

空穴具有**正的有效质量**。

#### 2.3.5 第五步：运动方程——正电荷粒子

将 $\mathbf{k}_e = -\mathbf{k}_h$、$\mathbf{v}_e = \mathbf{v}_h$ 代入电子运动方程，得：

$$\hbar\frac{d\mathbf{k}_h}{dt} = +e\left(\mathbf{E} + \frac{1}{c}\mathbf{v}_h \times \mathbf{B}\right) \tag{21}$$

> [!keypoint] 空穴 = 正电荷载体
> 空穴的运动方程与带**正电荷 $+e$** 的粒子完全相同。

#### 2.3.6 电流验证

价带仅一个空穴时，电流由未配对电子携带：

$$\mathbf{j} = (-e)\mathbf{v}(G) = (-e)[-\mathbf{v}(E)] = e\mathbf{v}(E) \tag{23}$$

这正是正电荷 $e$ 以速度 $\mathbf{v}(E)$ 运动产生的电流。

图9：电场中空穴的运动

![Fig. 9](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/cb2b8880-de0d-46c9-86bc-a8ed5d76e463/b9084ed3bac1f43565caeac11fa20d7451bb213e1390c2d0f4a275835440e875.jpg)

> Figure 9 (a) $t=0$ 所有态被占据除了 F 点（带顶，$v_x=0$）。(b) 施加 $E_x$，电子受力沿 $-k_x$ 方向，所有电子一起移动，空穴移到 E。(c) 进一步移动后空穴到 D。

图10：电子和空穴的漂移

![Fig. 10](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/cb2b8880-de0d-46c9-86bc-a8ed5d76e463/418679354c2ceb18d99210241b2dc0ae6b16ea3caa7b1d21233e75a43056db90.jpg)

> Figure 10 电子和空穴漂移速度方向相反，但**电流方向相同**（都沿电场方向）。

---

### 2.4 EFFECTIVE MASS（有效质量）

#### 2.4.1 定义

自由电子 $\epsilon = \hbar^2k^2/2m$，系数 $1/m$ 决定曲率。对能带中的电子，类似地定义**有效质量**。

对群速度 (1) 求导：

$$\frac{dv_g}{dt} = \hbar^{-1}\frac{d^2\epsilon}{dk\,dt} = \hbar^{-1}\frac{d^2\epsilon}{dk^2}\frac{dk}{dt}$$

利用 (5) $dk/dt = F/\hbar$：

$$\frac{dv_g}{dt} = \left(\frac{1}{\hbar^2}\frac{d^2\epsilon}{dk^2}\right)F$$

与牛顿第二定律 $F = ma$ 对比，定义：

$$\boxed{\frac{1}{m^*} = \frac{1}{\hbar^2}\frac{d^2\epsilon}{dk^2}} \tag{28}$$

三维各向异性情况推广为**有效质量张量**：

$$\left(\frac{1}{m^*}\right)_{\mu\nu} = \frac{1}{\hbar^2}\frac{\partial^2\epsilon}{\partial k_\mu \partial k_\nu} \tag{29}$$

> [!note]
> 晶体没有变轻，牛顿第二定律对晶体整体（离子+载流子）没有违反。有效质量描述的是电子在周期势中**相对于晶格**的加速行为。

#### 2.4.2 物理诠释：布拉格反射图像

从第7章近自由电子模型的结果（$U>0$）：

第二带底部电子：$\epsilon(K) = \epsilon_c + \hbar^2K^2/2m_e$，$m_e/m = 1/[(2\lambda/U)-1] \tag{24}$

第一带顶部电子：$\epsilon(K) = \epsilon_v - \hbar^2K^2/2m_h$，$m_h/m = 1/[(2\lambda/U)+1] \tag{25}$

其中 $K$ 为从区边界测量的波矢。

| 能带位置 | 曲率 | $m^*$ | 物理原因 |
|---------|------|-------|---------|
| 带底（区中心） | 向上 | $m^* \approx m > 0$ | 布拉格反射弱 |
| 带顶（区边界） | 向下 | $m^* < 0$ | 布拉格反射强，动量大量转给晶格 |
| 第二带底 | 向上 | $0 < m^* \ll m$ | 反射分量减小，晶格反冲小 |

半导体中带宽 $\sim 20$ eV，带隙 $\sim 0.2$~$2$ eV，曲率增强因子 $\sim 10$~$100$，故 $m^* \sim 0.1$~$0.01\,m$。

图11：负有效质量的实验

![Fig. 11a](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/cb2b8880-de0d-46c9-86bc-a8ed5d76e463/35e224d23e9033bd9778f973f5743d4235e7edf74936097b72fae52f15c481f8.jpg)

![Fig. 11b](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/cb2b8880-de0d-46c9-86bc-a8ed5d76e463/bdef987e2dabcc5ef2a7243a1f579892a0e4c08e37f72f29b17201659df4b685.jpg)

> Figure 11 电子束在晶体中的布拉格反射。(a) 能量略低于布拉格条件，电子透射。(b) 施加电压使布拉格条件满足，电子被反射。

---

## 3 半导体中的有效质量

### 3.1 直接带隙半导体

导带底在 $\mathbf{k}=0$，等能面为**球面**：

$$\epsilon_c = E_g + \frac{\hbar^2k^2}{2m_e} \tag{31}$$

价带顶有三条带（重空穴、轻空穴、分裂带）：

$$\epsilon_v(hh) = -\frac{\hbar^2k^2}{2m_{hh}}, \quad \epsilon_v(lh) = -\frac{\hbar^2k^2}{2m_{lh}}, \quad \epsilon_v(soh) = -\Delta - \frac{\hbar^2k^2}{2m_{soh}} \tag{32}$$

重空穴 (hh) 与轻空穴 (lh) 在 $\mathbf{k}=0$ 处**简并**，分裂带 (soh) 被自旋-轨道相互作用 $\Delta$ 分裂。

#### 图13：直接带隙半导体能带边结构

![Fig. 13](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/cb2b8880-de0d-46c9-86bc-a8ed5d76e463/8b74c9d6e50657eaaac741c10d31e001c5c77ce9e3b54128e9521b42884451af.jpg)

> Figure 13 直接带隙半导体的能带边结构。

### 3.2 电子有效质量与带隙的关系

微扰理论预言 $m_e \propto E_g$（直接带隙）。验证：

| 材料 | $m_e/m$ | $E_g$ (eV) | $m_e/(mE_g)$ (eV⁻¹) |
|------|---------|-----------|---------------------|
| InSb | 0.015 | 0.23 | 0.063 |
| InAs | 0.026 | 0.43 | 0.060 |
| InP | 0.073 | 1.42 | 0.051 |

比值近似常数，验证了理论。

### 3.3 Silicon and Germanium

**Ge**：
- 价带顶在 $\mathbf{k}=0$，导带底在 **L 点**（[111] 方向）
- 等能面为**旋转椭球面**：$m_l = 1.59m$，$m_t = 0.082m$
- 4个等价椭球（4个 $\langle 111 \rangle$ 方向）
- 价带源自 $p_{3/2}$ 和 $p_{1/2}$ 原子态，自旋-轨道分裂

**Si**：
- 价带顶在 $\mathbf{k}=0$，导带底在 **$\langle 100 \rangle$ 方向**（靠近X点）
- $m_l = 0.92m$，$m_t = 0.19m$
- 6个等价椭球（6个 $\langle 100 \rangle$ 方向）

椭球等能面的**回旋有效质量**（磁场与长轴夹角 $\theta$）：

$$\frac{1}{m_c^2} = \frac{\cos^2\theta}{m_t^2} + \frac{\sin^2\theta}{m_t m_l} \tag{34}$$

**GaAs**：直接带隙，各向同性电子质量 $m_e = 0.067m$。

图14：Ge 能带结构

![Fig. 14](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/cb2b8880-de0d-46c9-86bc-a8ed5d76e463/38533df85c3350a2d7284f841f96f51e55ee99e597faed36f4fc352d96301f2e.jpg)

> Figure 14 Ge 的能带结构。导带底在 L 点，等能面为椭球形。

图15：布里渊区对称点

![Fig. 15](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/cb2b8880-de0d-46c9-86bc-a8ed5d76e463/b1872c9dc21663d57124d8f413089834060e80feb4e5bcc873ae72f70014cfaa.jpg)

![Fig. 15b](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/cb2b8880-de0d-46c9-86bc-a8ed5d76e463/9855d1947be7dec18284e5b65d945303bf6e05112534bb633657e1270fec25d0.jpg)

> Figure 15 fcc 和 bcc 布里渊区的标准对称点标记。

图16：Ge 的回旋有效质量

![Fig. 16](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/cb2b8880-de0d-46c9-86bc-a8ed5d76e463/098e74ae16b397dd96d87025377ccc08b6c4efac3b773a4d45d283144cc5b30f.jpg)

> Figure 16 Ge 中电子的回旋有效质量随磁场方向的变化。

图17：Si 和 GaAs 的能带

![Fig. 17a](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/cb2b8880-de0d-46c9-86bc-a8ed5d76e463/91ae8946ec75b97ccbb81212f3d1d1d291573c2d22bc1734cdc4c5256292f441.jpg)

![Fig. 17b](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/cb2b8880-de0d-46c9-86bc-a8ed5d76e463/31f8947eb86cfbe2f98a4d263d95c6e694ae0cd9ba06d01f7f93da71a9d2e291.jpg)

> Figure 17 (a) Si 的等能椭球。(b) GaAs 的能带结构。

### 3.4 空穴有效质量

价带顶等能面**扭曲**（warped）：

$$\epsilon(\mathbf{k}) = Ak^2 \pm \left[B^2k^4 + C^2(k_x^2k_y^2 + k_y^2k_z^2 + k_z^2k_x^2)\right]^{1/2} \tag{33}$$

| 材料 | $m_{lh}/m$ | $m_{hh}/m$ |
|------|------------|------------|
| Ge | 0.043 | 0.34 |
| Si | 0.16 | 0.52 |
| Diamond | 0.7 | 2.12 |

### 3.5 有效质量数据表

| 晶体 | $m_e/m$ | $m_{hh}/m$ | $m_{lh}/m$ | $m_{soh}/m$ | $\Delta$ (eV) |
|------|---------|------------|------------|------------|--------------|
| InSb | 0.015 | 0.39 | 0.021 | (0.11) | 0.82 |
| InAs | 0.026 | 0.41 | 0.025 | 0.08 | 0.43 |
| InP | 0.073 | 0.4 | (0.078) | (0.15) | 0.11 |
| GaSb | 0.047 | 0.3 | 0.06 | (0.14) | 0.80 |
| GaAs | 0.066 | 0.5 | 0.082 | 0.17 | 0.34 |
| Cu₂O | 0.99 | — | 0.58 | 0.69 | 0.13 |

---

### 核心逻辑链

$$\text{布洛赫电子} \xrightarrow{\text{群速度}} \mathbf{v} = \hbar^{-1}\nabla_{\mathbf{k}}\epsilon \xrightarrow{\text{外力}} \hbar\dot{\mathbf{k}} = \mathbf{F} \xrightarrow{\text{加速度}} \frac{1}{m^*} = \frac{1}{\hbar^2}\frac{d^2\epsilon}{dk^2} \xrightarrow{\text{价带顶}} m_e^* < 0 \implies \text{空穴 } m_h = -m_e > 0 \xrightarrow{\text{运动方程}} \hbar\dot{\mathbf{k}}_h = +e(\mathbf{E} + \mathbf{v}_h \times \mathbf{B})$$

---

## 4 INTRINSIC CARRIER CONCENTRATION
