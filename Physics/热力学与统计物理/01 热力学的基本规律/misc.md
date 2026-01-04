# Proof of 1.3.5

以下是**物态方程全微分循环关系式 (1.3.5)** 的详细推导过程：
## Relation

**循环关系式**：
$$\left(\frac{\partial V}{\partial p}\right)_T \left(\frac{\partial p}{\partial T}\right)_V \left(\frac{\partial T}{\partial V}\right)_p = -1$$

**意义**：该式揭示了描述同一平衡态的三个偏导数之间存在的普适数学约束，**与具体物质无关**。它是推导体胀系数 $\alpha$、压强系数 $\beta$、等温压缩系数 $\kappa_T$ 关系式 $\alpha = \kappa_T \beta p$ 的核心工具。

## Proof

#### **第1步：从一般物态方程出发**

任何简单系统的平衡态满足隐函数形式：
$$f(p, V, T) = 0$$

其**全微分**为：
$$\mathrm{d}f = \frac{\partial f}{\partial p}\mathrm{d}p + \frac{\partial f}{\partial V}\mathrm{d}V + \frac{\partial f}{\partial T}\mathrm{d}T = 0 \quad (1)$$

#### **第2步：在三种不同约束条件下求偏导**

**情况①：恒温过程 $(T = \text{const}, \mathrm{d}T = 0)$**

代入式(1)得：
$$\frac{\partial f}{\partial p}\mathrm{d}p + \frac{\partial f}{\partial V}\mathrm{d}V = 0$$

整理得到 **等温压缩的偏导数**：
$$\left(\frac{\partial V}{\partial p}\right)_T = -\frac{\partial f/\partial p}{\partial f/\partial V} \quad (2)$$

---

**情况②：恒容过程 $(V = \text{const}, \mathrm{d}V = 0)$**

代入式(1)得：
$$\frac{\partial f}{\partial p}\mathrm{d}p + \frac{\partial f}{\partial T}\mathrm{d}T = 0$$

整理得到 **恒容升压的偏导数**：
$$\left(\frac{\partial p}{\partial T}\right)_V = -\frac{\partial f/\partial T}{\partial f/\partial p} \quad (3)$$

---

**情况③：恒压过程 $(p = \text{const}, \mathrm{d}p = 0)$**

代入式(1)得：
$$\frac{\partial f}{\partial V}\mathrm{d}V + \frac{\partial f}{\partial T}\mathrm{d}T = 0$$

整理得到 **等压膨胀的偏导数**：
$$\left(\frac{\partial T}{\partial V}\right)_p = -\frac{\partial f/\partial V}{\partial f/\partial T} \quad (4)$$

---

#### **第3步：三式联立相乘**

将式(2)、(3)、(4)相乘：

$$\left(\frac{\partial V}{\partial p}\right)_T \left(\frac{\partial p}{\partial T}\right)_V \left(\frac{\partial T}{\partial V}\right)_p = \left(-\frac{\partial f/\partial p}{\partial f/\partial V}\right) \cdot \left(-\frac{\partial f/\partial T}{\partial f/\partial p}\right) \cdot \left(-\frac{\partial f/\partial V}{\partial f/\partial T}\right)$$

观察分子分母，$\partial f/\partial p$、$\partial f/\partial T$、$\partial f/\partial V$ 全部约去，剩下三个负号相乘：

$$\left(\frac{\partial V}{\partial p}\right)_T \left(\frac{\partial p}{\partial T}\right)_V \left(\frac{\partial T}{\partial V}\right)_p = (-1) \times (-1) \times (-1) = \boxed{-1}$$
