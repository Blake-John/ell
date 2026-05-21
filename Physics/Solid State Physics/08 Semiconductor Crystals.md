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
>
> 本章讨论半导体晶体的核心物理：带隙、电子运动方程、空穴、有效质量、本征载流子浓度、杂质导电等。

## 引言：什么是半导体？

### 电阻率分类

Kittel 在开篇用**电阻率**来定义半导体：

| 材料 | 电阻率范围 (ohm·cm) |
|------|---------------------|
| 导体 | $< 10^{-2}$ |
| **半导体** | $10^{-2}$ ~ $10^{9}$ |
| 绝缘体 | $> 10^{14}$ |

半导体的电阻率**强烈依赖温度**，这是它与金属最显著的区别之一。绝对零度时，纯净完美的半导体晶体是绝缘体。

> [!tip] 为什么电阻率能区分材料？
> 金属的电阻率源自电子被声子/缺陷散射，载流子浓度基本不随温度变化。半导体的电阻率则由**载流子浓度**（强烈依赖温度）和迁移率共同决定。温度升高 → 更多电子被热激发到导带 → 电阻率急剧下降。

### 常见半导体器件

晶体管、开关、二极管、光伏电池、探测器、热敏电阻。这些器件利用了半导体电学性质对外场、光照、温度、杂质的高度敏感性。

### 化合物半导体命名

| 类型 | 组成 | 示例 |
|------|------|------|
| III-V | A为三价，B为五价 | InSb, GaAs |
| II-VI | A为二价，B为六价 | ZnS, CdS |
| IV-IV | A、B均为四价 | SiC |
| 金刚石型 | 与金刚石同结构 | Si, Ge |

> [!note] 本征导电 vs. 杂质导电
> 高纯度半导体表现**本征导电**，杂质半导体表现**杂质导电**。在本征温区，电学性质由带隙 $E_g$ 决定，杂质的影响可忽略。

### 图1：载流子浓度的分类

![Fig. 1 - Carrier concentrations](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/cb2b8880-de0d-46c9-86bc-a8ed5d76e463/e7dee2a803e28e0f0e852b73dfb6e9530e3fd6c2029f02f22479ba36b51cc9d5.jpg)

> Figure 1 Carrier concentrations for metals, semimetals, and semiconductors.

这张图展示了金属、半金属和半导体的典型载流子浓度范围：

- **金属**：$\sim 10^{22}$ cm$^{-3}$，几乎不随温度变化
- **半金属**（如 Bi）：$\sim 10^{17}$~$10^{20}$ cm$^{-3}$，导带和价带轻微交叠
- **半导体**：$\sim 10^{6}$~$10^{19}$ cm$^{-3}$，强烈依赖温度和掺杂
- **绝缘体**：$< 10^{6}$ cm$^{-3}$

半导体的范围可以通过掺杂向上扩展（增加杂质浓度），也可以向下延伸最终与绝缘体重合。

---

## §1 BAND GAP（带隙）

> **带隙是半导体物理的核心参数。** 它决定了材料的导电性、光学吸收边、发光效率，以及几乎所有器件特性。

### 1.1 带隙的定义与核心作用

**带隙 $E_g$**：导带底（conduction band edge）与价带顶（valence band edge）之间的能量差。

$$\boxed{E_g = E_c - E_v}$$

其中 $E_c$ 是导带最低点能量，$E_v$ 是价带最高点能量。

Kittel 开宗明义：**本征电导率和本征载流子浓度由无量纲比值 $E_g / k_B T$ 控制**。

- $E_g \gg k_B T$：热激发很难把电子从价带拉到导带，载流子浓度低，导电性差
- $E_g \sim k_B T$ 或更小：热激发显著，载流子浓度高

室温下 $k_B T \approx 0.026$ eV：

| 材料 | $E_g$ (300 K) | $E_g / k_BT$ |
|------|--------------|--------------|
| Si | 1.11 eV | $\sim 43$ |
| Ge | 0.66 eV | $\sim 25$ |
| GaAs | 1.43 eV | $\sim 55$ |
| Diamond | 5.4 eV | $\sim 208$ |

> [!important] 与第6章自由电子气的类比
> 在第6章中，我们用费米温度 $T_F = \epsilon_F/k_B \sim 10^4$~$10^5$ K 来表征电子气的"简并度"。$k_BT \ll \epsilon_F$ 意味着电子气高度简并，只有费米面附近的电子参与热激发。
>
> 半导体中，$E_g/k_BT \gg 1$ 意味着"带隙远大于热能"，绝大多数价带电子无法被热激发跨越带隙。这是一个**相反**的极限：自由电子气中是"几乎所有电子都被泡利原理锁住"，半导体中是"几乎所有电子都被带隙锁住"。

### 1.2 图2：本征导电的能带图像

![Fig. 2 - Band scheme for intrinsic conductivity](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/cb2b8880-de0d-46c9-86bc-a8ed5d76e463/ecea33d957b0305e4fd60e7761ef1de86e458a7249aeea0a5abe3ee64db976cd.jpg)

> Figure 2 Band scheme for intrinsic conductivity in a semiconductor.

这张图展示了本征半导体在两个极限温度下的能带填充情况：

**$T = 0$ K：**
- 价带（valence band）**全满**——所有量子态都被电子占据
- 导带（conduction band）**全空**——没有任何电子
- 中间隔以带隙 $E_g$
- 电导率为零（没有可移动的载流子）

**$T > 0$ K：**
- 一些电子从价带顶获得足够热能，被激发到导带底
- 导带中出现**自由电子**（mobile electrons）
- 价带中留下**空位**（vacancies），即**空穴**（holes）
- 电子和空穴都参与导电，载流子称为"本征载流子"（intrinsic carriers）

> [!note] 能带图读图方法
> 能带图的纵轴是能量，横轴是波矢 $\mathbf{k}$（有时也画成位置 $x$）。导带底和价带顶之间的**最小垂直距离**就是带隙 $E_g$。
>
> 电子倾向于占据低能态（在价带顶附近），空穴则"浮"在价带顶（因为空穴能量越高，对应的缺失电子能量越低）。

### 1.3 图3：本征载流子浓度随温度的变化

![Fig. 3a - Ge intrinsic concentration](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/cb2b8880-de0d-46c9-86bc-a8ed5d76e463/1597ebd2373d5ccbcd8168af47f88ca762c75d188713898ddf791406718c6178.jpg)

![Fig. 3b - Si intrinsic concentration](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/cb2b8880-de0d-46c9-86bc-a8ed5d76e463/76fb9114eeab55e490b8649858e6eca509f8b212ba2f1109b9a29a1ce5cb1d9b.jpg)

> Figure 3 Intrinsic electron concentration as a function of temperature for (a) germanium and (b) silicon. Under intrinsic conditions the hole concentration is equal to the electron concentration.

**图像特征：**
- 纵轴：本征载流子浓度 $n_i$（对数刻度）
- 横轴：温度 $T$（或 $1/T$）
- 曲线在 $\ln n_i$ ~ $1/T$ 图中呈**直线**，斜率给出 $-E_g/2k_B$

**关键对比——Ge vs Si：**
- 在**相同温度**下，Ge 的 $n_i$ **高于** Si
- 原因：Ge 的带隙更窄（0.66 eV vs 1.11 eV），热激发更容易
- 例如在 300 K：$n_i(\text{Ge}) \approx 2.4 \times 10^{13}$ cm$^{-3}$，$n_i(\text{Si}) \approx 1.5 \times 10^{10}$ cm$^{-3}$

**本征条件**：$n = p = n_i$（电子浓度 = 空穴浓度 = 本征浓度）。这是因为每个被激发到导带的电子都在价带留下一个空穴，产生是成对的。

> [!tip] 与第6章的联系：费米能级的位置
> 在第6章自由电子气中，费米能 $\epsilon_F$ 是 $T=0$ 时最高被占据态的能量，$k_BT \ll \epsilon_F$ 意味着电子气高度简并。
>
> 半导体中，费米能级 $\mu$（即化学势）位于**带隙中间**附近（见 §7 的推导）。由于 $E_g \gg k_BT$，$\mu$ 远离导带底和价带顶，这使得导带底附近的电子态几乎全空、价带顶附近的态几乎全满——恰好可以用**玻尔兹曼近似**代替费米-狄拉克分布（详见 §7）。

---

### 1.4 直接吸收过程（Direct Absorption Process）

现在进入本节的核心：**光与半导体的相互作用**。这是理解半导体光学性质的基础。

#### 什么是直接吸收？

**条件**：导带底和价带顶在 **k 空间中处于同一位置**（如都在布里渊区中心 $\Gamma$ 点，$\mathbf{k}=0$）。

**典型材料**：GaAs、InSb、InP、CdS、CdTe 等 III-V 和 II-VI 化合物。

**物理过程**：

一个光子被半导体吸收，直接将一个电子从价带顶激发到导带底：

$$\text{光子} \to \text{电子（导带）} + \text{空穴（价带）}$$

为什么这个过程可以**只用光子**完成？关键在于**波矢守恒**。

#### 为什么光子可以"单独完成"？

光子的波矢为：

$$k_{photon} = \frac{\omega}{c} = \frac{E_g/\hbar}{c} = \frac{E_g}{\hbar c}$$

对于 $E_g \sim 1$ eV 的光子：

$$k_{photon} \sim \frac{1 \text{ eV}}{197.3 \text{ eV·nm}} \sim 5 \times 10^{-3} \text{ nm}^{-1} \sim 5 \times 10^{4} \text{ cm}^{-1}$$

而布里渊区尺度的典型值：

$$k_{BZ} \sim \frac{2\pi}{a} \sim \frac{2\pi}{0.5 \text{ nm}} \sim 10^{8} \text{ cm}^{-1}$$

**光子波矢比布里渊区尺度小了约 3~4 个数量级！**

这意味着光子在 k 空间中提供的动量变化**几乎为零**。电子跃迁前后的 $\mathbf{k}$ 值几乎不变——跃迁是"**竖直**"的（vertical）。

> [!important] 光子的角色：能量信使，不是动量信使
> 光子的能量 $\hbar\omega$ 很大（eV 量级），足以把电子从价带激发到导带。但光子的动量 $\hbar k = \hbar\omega/c$ 极小，因为光速 $c$ 极大。
>
> 类比：光子像一个"只传能量不传动量"的信使。电子在跃迁前后几乎保持在 k 空间的同一位置。

#### 守恒律

**能量守恒**：
$$\hbar\omega = E_g$$

**波矢守恒**：
$$\mathbf{k}_f = \mathbf{k}_i + \mathbf{k}_{photon} \approx \mathbf{k}_i$$

因为 $\mathbf{k}_{photon} \approx 0$，所以 $\mathbf{k}_f \approx \mathbf{k}_i$。

#### 图5(a)：直接带隙的 k 空间图像

![Fig. 5a - Direct gap in k-space](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/cb2b8880-de0d-46c9-86bc-a8ed5d76e463/104eee46a58ad3170e9422c84155f4d527936bde319dbbafeb3ea5f9c7373ba7.jpg)

> Figure 5(a) The lowest point of the conduction band occurs at the same value of k as the highest point of the valence band.

这张图画出了 k 空间中的能带结构：
- 价带顶（最高点）在 $\mathbf{k}=0$
- 导带底（最低点）也在 $\mathbf{k}=0$
- 光跃迁用**竖直箭头**表示，因为 $\Delta\mathbf{k} \approx 0$

#### 图4(a)：直接带隙的光吸收谱

![Fig. 4a - Direct optical absorption](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/cb2b8880-de0d-46c9-86bc-a8ed5d76e463/987350f6eb16b29f971f9d82556f7aba92ce512a8acd56be970f9a88252e5c00.jpg)

> Figure 4(a) Optical absorption in a crystal with direct gap at absolute zero.

**图像解读**：
- 纵轴：吸收系数 $\alpha$
- 横轴：光子能量 $\hbar\omega$
- 在 $\hbar\omega < E_g$ 时，$\alpha = 0$（光子能量不够，无法激发电子）
- 在 $\hbar\omega = E_g$ 处，吸收突然开始（阈值）
- 在 $\hbar\omega > E_g$ 时，吸收很强且迅速增大

吸收阈值直接给出带隙：
$$\boxed{E_g = \hbar\omega_g}$$

> [!tip] 为什么吸收边很"陡峭"？
> 直接跃迁是**二体过程**（光子 + 电子），概率高。在阈值以上，导带和价带中都有大量可用的态供电子跃迁，吸收系数迅速增大。
>
> 这与间接吸收形成鲜明对比（见下文）。

---

### 1.5 间接吸收过程（Indirect Absorption Process）

#### 什么是间接吸收？

**条件**：导带底和价带顶在 **k 空间中相距很远**。

**典型材料**：Si、Ge、GaP、AlSb 等。

以 Si 为例：
- 价带顶在 $\Gamma$ 点（$\mathbf{k}=0$）
- 导带底在 $\langle 100 \rangle$ 方向，靠近 X 点（约 $0.85 \times 2\pi/a$）
- 两者之间的波矢差 $\Delta\mathbf{k}$ 很大

以 Ge 为例：
- 价带顶在 $\Gamma$ 点
- 导带底在 L 点（布里渊区边界的 [111] 方向）

#### 为什么光子"单独无法完成"？

如果电子从价带顶（$\mathbf{k}=0$）跃迁到导带底（$\mathbf{k}=\mathbf{k}_c$），波矢变化为 $\Delta\mathbf{k} = \mathbf{k}_c$。

但光子的波矢 $\mathbf{k}_{photon} \approx 0$，无法提供这个巨大的波矢变化。

**仅靠光子，波矢守恒无法满足！**

#### 声子登场：动量搬运工

解决方案：引入**声子（phonon）**——晶格振动的量子。

声子的特点：
- **能量很小**：$\hbar\Omega \sim 0.01$~$0.03$ eV（比 $E_g$ 小 1~2 个数量级）
- **波矢可以很大**：声子波矢可以覆盖整个布里渊区

声子充当"**动量搬运工**"的角色：它提供电子跃迁所需的**大波矢变化**，而能量代价极小。

#### 守恒律

**波矢守恒**：
$$\mathbf{k}_f = \mathbf{k}_i + \mathbf{k}_{photon} + \mathbf{K}_{phonon} \approx \mathbf{k}_i + \mathbf{K}_{phonon}$$

其中 $\mathbf{K}_{phonon}$ 是声子波矢。

**能量守恒**：

- **产生声子**（低温，晶格中尚未有足够热声子）：
$$\hbar\omega = E_g + \hbar\Omega$$

- **吸收声子**（高温，已有热激发的声子）：
$$\hbar\omega = E_g - \hbar\Omega$$

Kittel 给出的具体公式：
$$\mathbf{k}_{photon} = \mathbf{k}_c + \mathbf{K} \cong \mathbf{0}; \qquad \hbar\omega = E_g + \hbar\Omega$$

其中 $\mathbf{K} \cong -\mathbf{k}_g$（声子波矢近似等于电子需要补偿的波矢）。

> [!important] 三体过程 vs 二体过程
> - **直接吸收**：光子 → 电子 + 空穴（二体，概率高）
> - **间接吸收**：光子 + 声子 → 电子 + 空穴（三体，概率低）
>
> 三体过程需要光子、声子和电子三者"同时配合"，概率远低于二体过程。这就是为什么间接带隙材料的吸收系数远低于直接带隙材料。

#### 图5(b)：间接带隙的 k 空间图像

![Fig. 5b - Indirect gap in k-space](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/cb2b8880-de0d-46c9-86bc-a8ed5d76e463/5dec13c72b65ef81ab97d26c9f1cf974d90b11e9a8bd329d16e6fb04ac5b827b.jpg)

> Figure 5(b) The indirect transition involves both a photon and a phonon.

**图像解读**：
- 价带顶在 $\mathbf{k}=0$
- 导带底在 $\mathbf{k}=\mathbf{k}_c$（远离原点）
- 仅靠光子（竖直箭头）无法连接价带顶和导带底
- 必须借助声子提供水平方向的波矢变化
- 跃迁路径：价带顶 →（光子提供能量 + 声子提供动量）→ 导带底

Kittel 特别注明："The figure shows only the threshold transitions. Transitions occur generally between almost all points of the two bands for which the wavevectors and energy can be conserved." 也就是说，实际跃迁不只发生在带边之间，只要满足能量和波矢守恒，带内任意点之间都可以跃迁。

#### 图4(b)：间接带隙的光吸收谱

![Fig. 4b - Indirect optical absorption](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/cb2b8880-de0d-46c9-86bc-a8ed5d76e463/0e59b0f6add11f792e2fabbc9fb7cdd4a8b36be63c74df2e07d9047005a525a0.jpg)

> Figure 4(b) Optical absorption in a crystal with indirect gap at absolute zero.

**图像解读**：
- 纵轴：吸收系数 $\alpha$
- 横轴：光子能量 $\hbar\omega$
- 在 $\hbar\omega < E_g + \hbar\Omega$ 时，$\alpha \approx 0$
- 阈值在 $\hbar\omega = E_g + \hbar\Omega$（**大于**真实带隙！）
- 吸收边**平缓**，不像直接带隙那样陡峭
- 标记 $E_{vert}$：不需要声子的竖直跃迁阈值（见下节）

**为什么吸收边平缓？**
间接吸收是**三体过程**（光子+声子+电子），概率低。吸收系数正比于声子占据数（温度越高，可用声子越多，吸收越强）。

---

### 1.6 间接带隙中的竖直跃迁 $E_{vert}$

图4(b)中有一个重要标记 $E_{vert}$，代表**不需要声子**的竖直跃迁阈值。

这怎么理解？

在间接带隙材料中，虽然导带底和价带顶不在同一 $\mathbf{k}$ 位置，但价带中某个 $\mathbf{k}_i$ 处的电子可以被**竖直**（$\Delta\mathbf{k}=0$）激发到导带中**相同** $\mathbf{k}_i$ 处的态。这个跃迁不需要声子，因为波矢守恒自动满足。

**代价**：导带中 $\mathbf{k}_i$ 处的能量远高于导带底。所以需要的能量 $E_{vert} > E_g$。

因此间接带隙材料有**两个**特征能量：
- $E_g$：**真实带隙**（导带底到价带顶），需要声子辅助
- $E_{vert}$：**竖直跃迁阈值**（不需要声子），但能量更高

> [!example] 以 Ge 为例
> Ge 的间接带隙 $E_g = 0.66$ eV（价带顶 $\Gamma$ → 导带底 L）。
> 但竖直跃迁 $E_{vert}$ 可达 $\sim 0.8$ eV 以上，因为导带在 $\Gamma$ 点的能量远高于 L 点。
>
> 这就是为什么 Ge 在垂直入射光下的吸收边看起来比 0.66 eV 更高。

---

### 1.7 激子（Exciton）

Kittel 在图4的注释中提到了一段容易被忽略但很重要的内容：

> *"These plots do not show absorption lines that sometimes are seen lying just to the low energy side of the threshold. Such lines are due to the creation of a bound electron-hole pair, called an exciton."*

**激子**：电子和空穴通过库仑吸引形成的**束缚态**，类似于氢原子中质子和电子的束缚。

- 激子能量 = $E_g - E_b$，其中 $E_b$ 为束缚能（通常几到几十 meV）
- 激子吸收线出现在吸收阈值**以下**（低能侧）
- 激子整体电中性，不直接贡献电导
- 激子可以在晶体中移动（作为整体扩散）
- 在高温或高纯度样品中，激子线清晰可辨

> [!tip] 激子的物理图像
> 把电子激发到导带后，导带电子和价带空穴之间存在库仑吸引。如果这个束缚能 $E_b$ 足够大，电子和空穴会形成一个"类氢原子"——激子。
>
> 激子类似于第6章中提到的电子-离子芯的相互作用，但这里是电子-空穴的相互作用。激子的玻尔半径通常远大于晶格常数（因为介电屏蔽和有效质量小），所以可以用连续介质近似处理。

---

### 1.8 带隙的测量方法

Kittel 提到了三种确定带隙的方法：

#### 方法1：光学吸收法（最佳方法）

- **直接带隙**材料：尖锐的吸收边，阈值直接给出 $E_g$
- **间接带隙**材料：分析吸收系数 $\alpha$ 与 $\hbar\omega$ 的关系
  - 对于间接跃迁：$\alpha \propto (\hbar\omega - E_g \pm \hbar\Omega)^2$
  - 作 $(\alpha\hbar\omega)^{1/2}$ ~ $\hbar\omega$ 图，外推到横轴截距给出 $E_g$
  - 光学测量还能**判断**带隙是直接还是间接

#### 方法2：电学法（霍尔效应）

- 在本征温区测量**霍尔电压**，得到载流子浓度 $n_i$
- 利用 $n_i \propto \exp(-E_g/2k_BT)$ 的 Arrhenius 关系
- 作 $\ln(n_i)$ ~ $1/T$ 图，斜率给出 $-E_g/2k_B$

> [!note] 与第6章霍尔效应的联系
> 第6章中我们用霍尔效应测量**金属**的载流子浓度 $n$，得到霍尔系数 $R_H = -1/nec$。
>
> 半导体中，霍尔效应测量的是**本征载流子浓度** $n_i$，但原理相同。不同的是，半导子的 $n_i$ 强烈依赖温度，通过温度依赖关系可以提取 $E_g$。

#### 方法3：电导率测量

- 测量电阻率的温度依赖
- 在本征区：$\rho \propto \exp(E_g/2k_BT)$
- 与霍尔效应互补

---

### 1.9 带隙的温度依赖性

Kittel 的表1同时列出了 0 K 和 300 K 的带隙值，一个明显的趋势是：**温度升高，带隙减小**。

| 材料 | $E_g$ (0 K) | $E_g$ (300 K) | $\Delta E_g$ |
|------|-------------|---------------|--------------|
| Si | 1.17 eV | 1.11 eV | −0.06 eV |
| Ge | 0.744 eV | 0.66 eV | −0.084 eV |
| GaAs | 1.52 eV | 1.43 eV | −0.09 eV |
| InP | 1.42 eV | 1.27 eV | −0.15 eV |
| InSb | 0.23 eV | 0.17 eV | −0.06 eV |

**物理来源**：

1. **晶格热膨胀**：温度升高 → 晶格常数增大 → 能带宽度变化 → 带隙减小
2. **电子-声子相互作用**：原子振动加剧 → 对电子能级产生重整化效应 → 带隙减小

> [!tip] 与第6章热膨胀的联系
> 第5章和第6章讨论了晶格热膨胀。热膨胀导致原子间距增大，直接影响能带结构。带隙的温度依赖性中，热膨胀贡献约占 1/3~1/2，其余来自电子-声子相互作用。

**经验公式（Varshni 公式）**：

$$E_g(T) = E_g(0) - \frac{\alpha T^2}{T + \beta}$$

其中 $\alpha$ 和 $\beta$ 是材料相关的经验参数。

> [!example] Si 的 Varshni 参数
> $\alpha = 4.73 \times 10^{-4}$ eV/K，$\beta = 636$ K。在室温附近，$dE_g/dT \approx -2.7 \times 10^{-4}$ eV/K。

---

### 1.10 图6：InSb 的直接吸收实验

![Fig. 6 - InSb optical absorption](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/cb2b8880-de0d-46c9-86bc-a8ed5d76e463/f46130f5eb5298709d7f2cbf1957115a885512d5f0d0f2a173711717817cfdb2.jpg)

> Figure 6 Optical absorption in pure indium antimonide, InSb. The transition is direct because both conduction and valence band edges are at k = 0.

**图像解读**：
- InSb 是最经典的直接带隙半导体之一
- 导带底和价带顶都在 $\mathbf{k}=0$（布里渊区中心）
- 吸收阈值非常**尖锐**——这是直接带隙的典型特征
- 阈值频率直接给出 $E_g = \hbar\omega_g \approx 0.17$ eV（300 K）

Kittel 标注 "Notice the sharp threshold"——尖锐的吸收边是直接带隙材料的"指纹"。

这与间接带隙材料（如 Si、Ge）的吸收谱形成鲜明对比：后者的吸收边平缓得多。

---

### 1.11 代表性材料的带隙数据

| 晶体 | 类型 | $E_g$ (0 K) | $E_g$ (300 K) | 晶体 | 类型 | $E_g$ (0 K) | $E_g$ (300 K) |
|------|------|-------------|---------------|------|------|-------------|---------------|
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

几个值得注意的点：

- **金刚石**：$E_g = 5.4$ eV，带隙太大，室温下几乎是绝缘体
- **SiC**：$E_g = 3.0$ eV，宽禁带半导体，适合高温、高功率应用
- **α-Sn**：$E_g = 0$，处于半导体到半金属的**临界点**
- **HgTe**：$E_g = -0.30$ eV，**负带隙**！导带和价带交叠，是半金属

> [!warning] 半金属（Semimetals）
> HgTe 和 HgSe 的带隙为**负值**，意味着导带底低于价带顶——两带**交叠**。
>
> 即使在绝对零度，也有电子和空穴同时存在。它们的行为介于金属和半导体之间：
> - 载流子浓度远高于典型半导体（$\sim 10^{17}$~$10^{19}$ cm$^{-3}$）
> - 但远低于典型金属（$\sim 10^{22}$ cm$^{-3}$）
> - 电阻率比金属高，但温度依赖性与半导体类似
>
> 这与图1中半金属的载流子浓度范围一致。

---

### 1.12 直接/间接带隙对比总结

| 特征 | 直接带隙 | 间接带隙 |
|------|---------|---------|
| 带边位置 | 同一 $\mathbf{k}$ | 不同 $\mathbf{k}$ |
| 跃迁参与粒子 | 仅光子 | 光子 + 声子 |
| 吸收阈值 | $\hbar\omega_g = E_g$ | $E_g \pm \hbar\Omega$ |
| 吸收强度 | 强，陡峭 | 弱，平缓 |
| 过程阶数 | 二体，概率高 | 三体，概率低 |
| 发光效率 | 高（LED、激光器） | 低（Si 几乎不发光） |
| 代表材料 | GaAs, InSb, CdS | Si, Ge, GaP |

> [!tip] 核心物理图像
> 直接带隙像"竖直上抛"：只需要能量，不需要水平动量。电子从价带顶竖直跃迁到导带底，光子提供全部能量。
>
> 间接带隙像"斜抛"：需要同时匹配能量和水平动量。光子提供能量，但还需要声子"推一把"提供水平动量。这个配合过程远不如直接跃迁来得容易。
>
> 这就是为什么 GaAs（直接带隙）被广泛用于发光器件（LED、激光器），而 Si（间接带隙）几乎不能做发光器件。

---

## §2 EQUATIONS OF MOTION（运动方程）

> 本节推导电子在能带中的运动方程。核心结果是 $\hbar\dot{\mathbf{k}} = \mathbf{F}$，它把晶格的全部复杂性能量色散"吸收"进了 $\epsilon(\mathbf{k})$，使得外力与 $\mathbf{k}$ 的变化率之间的关系具有极其简洁的形式。

### 2.1 群速度：为什么是 $\nabla_{\mathbf{k}}\epsilon$？

Kittel 从波包的群速度出发。一个布洛赫电子不是平面波，而是由特定 $\mathbf{k}$ 附近的一组波函数叠加而成的**波包**。波包的整体运动速度（即信号/能量传播的速度）是群速度：

$$v_g = \frac{d\omega}{dk}$$

量子力学中，频率与能量的关系为 $\omega = \epsilon/\hbar$（普朗克-爱因斯坦关系），因此：

$$\boxed{\mathbf{v} = \hbar^{-1} \nabla_{\mathbf{k}} \epsilon(\mathbf{k})} \tag{1}$$

> [!tip] 与第6章自由电子的对比
> 第6章中自由电子的群速度为 $\mathbf{v} = \hbar\mathbf{k}/m$，色散关系为抛物线 $\epsilon = \hbar^2k^2/2m$。
>
> 晶体中的电子，色散关系 $\epsilon(\mathbf{k})$ 不再是简单的抛物线，而是由能带结构决定的复杂函数。但群速度的公式形式不变，只是把 $d\epsilon/dk$ 替换为 $\nabla_{\mathbf{k}}\epsilon$。
>
> **晶格对电子运动的全部影响都编码在 $\epsilon(\mathbf{k})$ 中。** 这是能带理论的强大之处：不管晶格势多复杂，只要知道了 $\epsilon(\mathbf{k})$，就能直接写出电子的速度。

**一维情况的直觉**：
- 在能带底部，$\epsilon(k)$ 向上弯曲，$d\epsilon/dk > 0$（$k>0$ 时），速度与 $k$ 同向
- 在能带顶部，$\epsilon(k)$ 向下弯曲，$d\epsilon/dk < 0$（$k>0$ 时），速度与 $k$ 反向——这就是负有效质量的起源
- 在能带拐点处，$d\epsilon/dk = 0$，群速度为零（驻波）

### 2.2 电场中的运动方程：$\hbar\dot{\mathbf{k}} = \mathbf{F}$

现在推导电子在外力作用下的运动方程。

**第1步：外力做功**

电子在电场 $\mathbf{E}$ 中受到的力为 $\mathbf{F} = -e\mathbf{E}$。在时间 $\delta t$ 内，电场对电子做的功等于电子能量的变化：

$$\delta\epsilon = -e E v_g \, \delta t \tag{2}$$

这里 $v_g$ 是群速度沿电场方向的分量。

**第2步：能量变化与 $\delta k$ 的关系**

另一方面，当波矢变化 $\delta k$ 时，由色散关系 $\epsilon(k)$ 的微分：

$$\delta\epsilon = \frac{d\epsilon}{dk}\,\delta k$$

利用群速度公式 (1)，$v_g = \hbar^{-1}d\epsilon/dk$，即 $d\epsilon/dk = \hbar v_g$，所以：

$$\delta\epsilon = \hbar v_g \,\delta k \tag{3}$$

**第3步：比较得出运动方程**

比较 (2) 和 (3)：

$$\hbar v_g \,\delta k = -e E v_g \, \delta t$$

消去 $v_g$（假设 $v_g \neq 0$）：

$$\delta k = -\frac{eE}{\hbar}\,\delta t \tag{4}$$

推广到一般外力 $\mathbf{F}$（不限于电场），得到：

$$\boxed{\hbar\frac{d\mathbf{k}}{dt} = \mathbf{F}} \tag{5}$$

> [!important] 核心方程的物理含义
> $\hbar\dot{\mathbf{k}} = \mathbf{F}$ 是**晶体中电子运动的基本方程**。
>
> - 形式上与牛顿第二定律 $F = dp/dt$ 类似
> - 但这里的"动量"是**晶体动量** $\hbar\mathbf{k}$，不是真实动量 $m\mathbf{v}$
> - 晶格周期势的影响被完全藏进了 $\epsilon(\mathbf{k})$，不显式出现在方程中
> - Kittel 特别强调："We have not overthrown Newton's second law"——电子在晶体中受晶格力和外力共同作用，但净效果等价于只有外力作用于一个具有晶体动量 $\hbar\mathbf{k}$ 的粒子

> [!note] 与第6章的联系
> 第6章中我们用类似的方法推导了费米球的运动方程：$\hbar(d/dt + 1/\tau)\delta\mathbf{k} = \mathbf{F}$（含碰撞项）。
>
> 第8章的推导更基础：没有碰撞项，纯粹是量子力学波包在周期势中的运动。碰撞是额外加入的（用弛豫时间 $\tau$ 近似）。

### 2.3 磁场中的运动方程

当同时存在电场和磁场时，电子受到洛伦兹力。方程 (5) 的右端应包含完整的洛伦兹力：

$$\hbar\frac{d\mathbf{k}}{dt} = -e\left(\mathbf{E} + \frac{1}{c}\mathbf{v} \times \mathbf{B}\right) \quad \text{(CGS)}$$

$$\hbar\frac{d\mathbf{k}}{dt} = -e\left(\mathbf{E} + \mathbf{v} \times \mathbf{B}\right) \quad \text{(SI)} \tag{6}$$

> [!note] CGS vs SI
> Kittel 使用 CGS 单位制，其中洛伦兹力为 $-e(\mathbf{E} + \mathbf{v}/c \times \mathbf{B})$。SI 单位制中光速 $c$ 不出现在洛伦兹力中。两种单位制下物理本质相同。

**纯磁场情况**（$\mathbf{E} = 0$）：

$$\hbar\frac{d\mathbf{k}}{dt} = -e\mathbf{v} \times \mathbf{B}$$

将群速度 $\mathbf{v} = \hbar^{-1}\nabla_{\mathbf{k}}\epsilon$ 代入，得到**纯 k 空间的运动方程**：

$$\boxed{\frac{d\mathbf{k}}{dt} = -\frac{e}{\hbar^2} \nabla_{\mathbf{k}}\epsilon \times \mathbf{B}} \tag{7}$$

这个方程的**两端都是 k 空间的量**，非常优雅。

### 2.4 磁场中运动的物理图像

方程 (7) 中的叉积 $\nabla_{\mathbf{k}}\epsilon \times \mathbf{B}$ 决定了电子在 k 空间中的运动方向。由叉积的几何性质：

$$d\mathbf{k}/dt \perp \nabla_{\mathbf{k}}\epsilon$$

即电子在 k 空间中沿**垂直于等能面法线**的方向运动。这意味着：

> [!keypoint] 磁场中电子在 k 空间的运动
> 1. **电子在等能面上运动**——能量守恒（磁场不做功）
> 2. **$k_B$（$\mathbf{k}$ 在 $\mathbf{B}$ 方向的投影）守恒**——沿磁场方向没有力
> 3. **轨道 = 等能面 $\cap$ 垂直于 $\mathbf{B}$ 的平面**

**详细解释**：

- $\nabla_{\mathbf{k}}\epsilon$ 是等能面的法线方向（指向能量增加最快的方向）
- $d\mathbf{k}/dt$ 垂直于法线 $\implies$ 运动方向在等能面的切平面内 $\implies$ 能量不变
- 同时 $d\mathbf{k}/dt$ 也垂直于 $\mathbf{B}$ $\implies$ 沿 $\mathbf{B}$ 方向没有运动分量 $\implies$ $k_B$ 守恒

**实空间中的对应**：

电子在实空间中做**螺旋运动**：
- 垂直于 $\mathbf{B}$ 的平面内：圆周运动（回旋）
- 沿 $\mathbf{B}$ 方向：匀速直线运动
- 合成轨迹：螺旋线

k 空间中的轨道投影到垂直于 $\mathbf{B}$ 的平面，就是实空间中回旋运动的"影子"。

> [!tip] 与第6章回旋共振的联系
> 第6章中我们讨论了金属中电子的回旋共振：$\omega_c = eB/m^*c$（CGS）。
>
> 第8章的方程 (7) 是更普遍的描述——适用于任意能带结构 $\epsilon(\mathbf{k})$，不假设抛物线色散。对于各向异性能带（如 Si、Ge），有效质量是张量，回旋频率依赖于磁场方向（见 §6 中的公式 34）。

### 2.5 运动方程的物理意义总结

| 方程 | 含义 | 与经典力学的对比 |
|------|------|-----------------|
| $\mathbf{v} = \hbar^{-1}\nabla_{\mathbf{k}}\epsilon$ | 群速度由能带梯度决定 | 经典：$\mathbf{v} = \mathbf{p}/m$ |
| $\hbar\dot{\mathbf{k}} = \mathbf{F}$ | 外力驱动 $\mathbf{k}$ 变化 | 经典：$\dot{\mathbf{p}} = \mathbf{F}$ |
| $\dot{\mathbf{k}} = -(e/\hbar^2)\nabla_{\mathbf{k}}\epsilon \times \mathbf{B}$ | 磁场使 $\mathbf{k}$ 在等能面上偏转 | 经典：$\dot{\mathbf{p}} = -e\mathbf{v} \times \mathbf{B}$ |

**核心思想**：晶格周期势的全部复杂性被"吸收"进了 $\epsilon(\mathbf{k})$。运动方程的形式极其简洁，但所有丰富的物理（有效质量、负质量、各向异性等）都藏在色散关系中。

---

## §3 Physical Derivation of $\hbar\dot{\mathbf{k}} = \mathbf{F}$

### 动量守恒论证

考虑电中性绝缘晶体，仅一个电子在某能带中。施加外力冲量 $\mathbf{J} = \int\mathbf{F}\,dt$。

**自由电子情况**：$\mathbf{J} = \Delta\mathbf{p}_{tot} = \hbar\Delta\mathbf{k}$

**晶体中的电子**：总动量变化 = 电子动量变化 + 晶格动量变化。布洛赫波函数包含多个平面波分量：

$$\psi_{\mathbf{k}} = \sum_{\mathbf{G}} C(\mathbf{k}+\mathbf{G}) e^{i(\mathbf{k}+\mathbf{G})\cdot\mathbf{r}}$$

电子动量期望值：

$$\mathbf{p}_{el} = \hbar\mathbf{k} + \sum_{\mathbf{G}} \hbar\mathbf{G}|C(\mathbf{k}+\mathbf{G})|^2 \tag{9}$$

当 $\mathbf{k} \to \mathbf{k}+\Delta\mathbf{k}$ 时：
- 电子动量变化含两项：$\hbar\Delta\mathbf{k}$ + 各傅里叶分量权重变化的贡献
- 晶格动量变化恰好**抵消**第二项（布拉格反射时晶格获得相反动量）

最终：

$$\Delta\mathbf{p}_{el} + \Delta\mathbf{p}_{lat} = \hbar\Delta\mathbf{k} = \mathbf{J}$$

因此 $\hbar\,d\mathbf{k}/dt = \mathbf{F}$，与 (5) 一致。

> [!note] 物理直觉
> 晶格通过布拉格反射与电子交换动量，但外力给予系统的全部冲量表现为 $\hbar\mathbf{k}$ 的变化。晶格内部动量的重新分配不改变总量。

---

## §4 HOLES（空穴）

### 4.1 基本图像

价带几乎全满，仅 $\mathbf{k}_e$ 态空缺。这个空缺即为**空穴**。没有空穴就没有晶体管。

### 4.2 空穴的五步论证

**第1步：波矢 $\mathbf{k}_h = -\mathbf{k}_e$**

满带总波矢为零（布里渊区反演对称）。移走 $\mathbf{k}_e$ 处电子后，系统总波矢为 $-\mathbf{k}_e$，赋予空穴：

$$\mathbf{k}_h = -\mathbf{k}_e \tag{17}$$

> 虽然空穴在图中画在 $\mathbf{k}_e$ 位置，但其真实波矢为 $-\mathbf{k}_e$。

**第2步：能量 $\epsilon_h(\mathbf{k}_h) = -\epsilon_e(\mathbf{k}_e)$**

价带能量零点在带顶。电子越低，移除所需功越大。空穴能量与缺失电子相反：

$$\epsilon_h(\mathbf{k}_h) = -\epsilon_e(\mathbf{k}_e) \tag{18}$$

由此构造**空穴能带**：将价带倒置，空穴能带"正立"。

**第3步：速度 $\mathbf{v}_h = \mathbf{v}_e$**

由 $\nabla_{\mathbf{k}_h}\epsilon_h = \nabla_{\mathbf{k}_e}\epsilon_e$（反演对称性），得：

$$\mathbf{v}_h(\mathbf{k}_h) = \mathbf{v}_e(\mathbf{k}_e) \tag{19}$$

**第4步：有效质量 $m_h = -m_e$**

价带顶曲率向下 $\implies$ 电子有效质量为**负**。空穴能带反转后曲率向上：

$$m_h = -m_e > 0 \tag{20}$$

**第5步：运动方程——正电荷粒子**

将 $\mathbf{k}_e = -\mathbf{k}_h$、$\mathbf{v}_e = \mathbf{v}_h$ 代入电子运动方程，得：

$$\hbar\frac{d\mathbf{k}_h}{dt} = +e\left(\mathbf{E} + \frac{1}{c}\mathbf{v}_h \times \mathbf{B}\right) \tag{21}$$

> [!keypoint] 空穴 = 正电荷载体
> 空穴的运动方程与带**正电荷 $+e$** 的粒子完全相同。

### 4.3 电流验证

价带仅一个空穴时，总电流等价于正电荷 $e$ 以空穴速度运动产生的电流：

$$\mathbf{j} = (-e)[-\mathbf{v}(E)] = +e\mathbf{v}(E)$$

### 4.4 电场中的漂移

在电场中，电子逆场方向漂移，空穴顺场方向漂移，但**两者电流方向相同**（均沿电场方向）。

---

## §5 EFFECTIVE MASS（有效质量）

### 5.1 定义

对群速度求导并利用 $\hbar\dot{k}=F$：

$$\frac{d\mathbf{v}}{dt} = \left(\frac{1}{\hbar^2}\frac{d^2\epsilon}{dk^2}\right)\mathbf{F}$$

与牛顿第二定律对比，定义**有效质量**：

$$\boxed{\frac{1}{m^*} = \frac{1}{\hbar^2}\frac{d^2\epsilon}{dk^2}} \tag{28}$$

三维各向异性情况推广为**有效质量张量**：

$$\left(\frac{1}{m^*}\right)_{\mu\nu} = \frac{1}{\hbar^2}\frac{\partial^2\epsilon}{\partial k_\mu \partial k_\nu} \tag{29}$$

### 5.2 物理诠释：布拉格反射图像

| 能带位置 | 曲率 | $m^*$ | 物理原因 |
|---------|------|-------|---------|
| 带底（区中心） | 向上 | $m^* \approx m > 0$ | 布拉格反射弱 |
| 带顶（区边界） | 向下 | $m^* < 0$ | 布拉格反射强，动量大量转给晶格 |
| 第二带底 | 向上 | $0 < m^* \ll m$ | 反射分量减小，晶格反冲小 |
| 平坦带 | $\approx 0$ | $m^* \gg m$ | 波函数重叠小（紧束缚） |

**负有效质量的直觉**：外力增加 $\mathbf{k}$ 时，布拉格反射增强，电子净前进动量反而减小，等效于"负质量"响应。

**小有效质量的直觉**：第二带底部，反射分量减小，给定外力产生的加速度大于自由电子，"节省"的晶格反冲给了电子。

**定量估算**：半导体带宽 $\sim 20$ eV，带隙 $\sim 0.2$~$2$ eV，曲率增强因子 $\sim 10$~$100$，故 $m^* \sim 0.1$~$0.01\,m$。

### 5.3 回旋共振测量

磁场中载流子回旋频率：

$$\omega_c = \frac{eB}{m^*} \quad \text{(SI)} \tag{30}$$

测量共振频率即可直接得到 $m^*$。要求 $\omega_c\tau \geq 1$（高纯样品、低温）。

---

## §6 半导体中的有效质量

### 6.1 直接带隙半导体

导带底在 $\mathbf{k}=0$，等能面为**球面**：

$$\epsilon_c = E_g + \frac{\hbar^2 k^2}{2m_e} \tag{31}$$

价带顶有三条带：

$$\epsilon_v(hh) = -\frac{\hbar^2 k^2}{2m_{hh}}, \quad \epsilon_v(lh) = -\frac{\hbar^2 k^2}{2m_{lh}}, \quad \epsilon_v(soh) = -\Delta - \frac{\hbar^2 k^2}{2m_{soh}} \tag{32}$$

- 重空穴 (hh) 与轻空穴 (lh) 在 $\mathbf{k}=0$ 处**简并**
- 分裂带 (soh) 被自旋-轨道相互作用 $\Delta$ 分裂

### 6.2 电子有效质量与带隙的关系

微扰理论预言 $m_e \propto E_g$（直接带隙）。验证：

| 材料 | $m_e/m$ | $E_g$ (eV) | $m_e/(mE_g)$ (eV⁻¹) |
|------|---------|-----------|---------------------|
| InSb | 0.015 | 0.23 | 0.063 |
| InAs | 0.026 | 0.43 | 0.060 |
| InP | 0.073 | 1.42 | 0.051 |

比值近似常数，验证了理论。

### 6.3 Si 和 Ge 的能带结构

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

**GaAs**：
- 直接带隙，各向同性电子质量 $m_e = 0.067m$
- 价带参数：$A=-6.98$, $B=-4.5$, $|C|=6.2$, $\Delta=0.341$ eV

### 6.4 空穴有效质量

价带顶等能面**扭曲**（warped）：

$$\epsilon(\mathbf{k}) = Ak^2 \pm \left[B^2k^4 + C^2(k_x^2k_y^2 + k_y^2k_z^2 + k_z^2k_x^2)\right]^{1/2} \tag{33}$$

近似值：

| 材料 | $m_{lh}/m$ | $m_{hh}/m$ |
|------|------------|------------|
| Ge | 0.043 | 0.34 |
| Si | 0.16 | 0.52 |
| Diamond | 0.7 | 2.12 |

### 6.5 直接带隙半导体有效质量表

| 晶体 | $m_e/m$ | $m_{hh}/m$ | $m_{lh}/m$ | $m_{soh}/m$ | $\Delta$ (eV) |
|------|---------|------------|------------|------------|--------------|
| InSb | 0.015 | 0.39 | 0.021 | (0.11) | 0.82 |
| InAs | 0.026 | 0.41 | 0.025 | 0.08 | 0.43 |
| InP | 0.073 | 0.4 | (0.078) | (0.15) | 0.11 |
| GaSb | 0.047 | 0.3 | 0.06 | (0.14) | 0.80 |
| GaAs | 0.066 | 0.5 | 0.082 | 0.17 | 0.34 |
| Cu₂O | 0.99 | — | 0.58 | 0.69 | 0.13 |

---

## 核心逻辑链

$$\text{布洛赫电子} \xrightarrow{\text{群速度}} \mathbf{v} = \hbar^{-1}\nabla_{\mathbf{k}}\epsilon \xrightarrow{\text{外力}} \hbar\dot{\mathbf{k}} = \mathbf{F} \xrightarrow{\text{加速度}} \frac{1}{m^*} = \frac{1}{\hbar^2}\frac{d^2\epsilon}{dk^2} \xrightarrow{\text{价带顶}} m_e^* < 0 \implies \text{空穴 } m_h = -m_e > 0 \xrightarrow{\text{运动方程}} \hbar\dot{\mathbf{k}}_h = +e(\mathbf{E} + \mathbf{v}_h \times \mathbf{B})$$

> [!tip] 总结
> $\hbar\dot{\mathbf{k}}=\mathbf{F}$ 是晶体中电子运动的基石。有效质量把晶格的全部复杂性能量色散浓缩为一个参数。空穴理论则把价带顶电子的负质量响应重新诠释为正电荷载流子。这条链子是整个半导体器件物理的理论基础。

---

## §7 INTRINSIC CARRIER CONCENTRATION（本征载流子浓度）

*（待续）*
