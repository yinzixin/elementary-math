# 均值不等式链

## 1. 基本形式

对正实数 $a_1, a_2, \ldots, a_n > 0$，定义四种平均数：

| 名称 | 符号 | 定义 |
|------|------|------|
| 调和平均数 (HM) | $H_n$ | $\dfrac{n}{\displaystyle\sum_{i=1}^n \dfrac{1}{a_i}}$ |
| 几何平均数 (GM) | $G_n$ | $\displaystyle\sqrt[n]{\prod_{i=1}^n a_i}$ |
| 算术平均数 (AM) | $A_n$ | $\dfrac{1}{n}\displaystyle\sum_{i=1}^n a_i$ |
| 平方平均数 (QM) | $Q_n$ | $\sqrt{\dfrac{1}{n}\displaystyle\sum_{i=1}^n a_i^2}$ |

**均值不等式链**：

$$\boxed{H_n \leq G_n \leq A_n \leq Q_n}$$

等号成立当且仅当 $a_1 = a_2 = \cdots = a_n$。

---

## 2. 两数情形的完整证明

设 $a, b > 0$，记

$$H = \frac{2}{\frac{1}{a}+\frac{1}{b}} = \frac{2ab}{a+b}, \quad G = \sqrt{ab}, \quad A = \frac{a+b}{2}, \quad Q = \sqrt{\frac{a^2+b^2}{2}}$$

### 2.1 $A \geq G$（AM-GM）

$$A - G = \frac{a+b}{2} - \sqrt{ab} = \frac{(\sqrt{a}-\sqrt{b})^2}{2} \geq 0$$

等号当且仅当 $a = b$。$\blacksquare$

### 2.2 $G \geq H$

由 AM-GM 对 $\frac{1}{a}, \frac{1}{b}$ 应用：

$$\frac{\frac{1}{a}+\frac{1}{b}}{2} \geq \sqrt{\frac{1}{ab}} = \frac{1}{\sqrt{ab}} = \frac{1}{G}$$

两边取倒数（不等号方向改变）：

$$G = \sqrt{ab} \geq \frac{2}{\frac{1}{a}+\frac{1}{b}} = H$$

等号当且仅当 $a = b$。$\blacksquare$

### 2.3 $Q \geq A$

$$Q^2 - A^2 = \frac{a^2+b^2}{2} - \left(\frac{a+b}{2}\right)^2 = \frac{a^2+b^2}{2} - \frac{a^2+2ab+b^2}{4} = \frac{(a-b)^2}{4} \geq 0$$

由于 $Q, A > 0$，故 $Q \geq A$，等号当且仅当 $a = b$。$\blacksquare$

---

## 3. 一般情形：$A_n \geq G_n$ 的证明（Cauchy 前向-后向归纳法）

**引理**：对任意正整数 $n$，有 $A_n \geq G_n$。

**证明**：

**步骤一（前向：$n = 2^k$ 的情形）**

$n = 2$ 时已证。假设 $n = 2^k$ 成立，证 $n = 2^{k+1}$：

将 $2^{k+1}$ 个数分为前后各 $2^k$ 个，设

$$A' = \frac{a_1+\cdots+a_{2^k}}{2^k}, \quad A'' = \frac{a_{2^k+1}+\cdots+a_{2^{k+1}}}{2^k}$$

$$G' = \sqrt[2^k]{a_1\cdots a_{2^k}}, \quad G'' = \sqrt[2^k]{a_{2^k+1}\cdots a_{2^{k+1}}}$$

由归纳假设 $A' \geq G'$，$A'' \geq G''$，再由 $n=2$ 的情形：

$$A_{2^{k+1}} = \frac{A'+A''}{2} \geq \sqrt{A' \cdot A''} \geq \sqrt{G' \cdot G''} = G_{2^{k+1}}$$

**步骤二（后向：由 $n$ 推 $n-1$）**

设 $A_n \geq G_n$ 对 $n$ 成立。取 $a_n = A_{n-1} = \frac{a_1+\cdots+a_{n-1}}{n-1}$，则

$$A_n = \frac{a_1+\cdots+a_{n-1}+A_{n-1}}{n} = \frac{(n-1)A_{n-1}+A_{n-1}}{n} = A_{n-1}$$

由归纳假设：

$$A_{n-1} = A_n \geq G_n = \sqrt[n]{a_1 \cdots a_{n-1} \cdot A_{n-1}}$$

$$A_{n-1}^n \geq a_1 \cdots a_{n-1} \cdot A_{n-1}$$

$$A_{n-1}^{n-1} \geq a_1 \cdots a_{n-1}$$

$$A_{n-1} \geq \sqrt[n-1]{a_1 \cdots a_{n-1}} = G_{n-1}$$

即 $n-1$ 时也成立。$\blacksquare$

### 3.1 $H_n \leq G_n$ 的证明

对 $\frac{1}{a_1}, \ldots, \frac{1}{a_n}$ 应用 AM-GM：

$$\frac{\frac{1}{a_1}+\cdots+\frac{1}{a_n}}{n} \geq \sqrt[n]{\frac{1}{a_1\cdots a_n}} = \frac{1}{G_n}$$

故 $\frac{n}{G_n} \leq \sum \frac{1}{a_i}$，即

$$G_n \geq \frac{n}{\sum \frac{1}{a_i}} = H_n \quad \blacksquare$$

### 3.2 $Q_n \geq A_n$ 的证明

由 Cauchy-Schwarz 不等式：

$$\left(\sum_{i=1}^n a_i\right)^2 \leq n \sum_{i=1}^n a_i^2$$

两边除以 $n^2$：

$$A_n^2 = \left(\frac{\sum a_i}{n}\right)^2 \leq \frac{\sum a_i^2}{n} = Q_n^2$$

故 $Q_n \geq A_n$。$\blacksquare$

---

## 4. 常见变形与推论

### 4.1 加权 AM-GM 不等式

设 $w_i > 0$，$\sum w_i = 1$，则

$$\sum_{i=1}^n w_i a_i \geq \prod_{i=1}^n a_i^{w_i}$$

**证明**：利用 $\ln$ 的凹性（Jensen 不等式）：

$$\ln\!\left(\sum w_i a_i\right) \geq \sum w_i \ln a_i = \ln \prod a_i^{w_i}$$

单调性给出结论。$\blacksquare$

### 4.2 $a + b \geq 2\sqrt{ab}$ 的常用推论

对正数 $a, b$，令 $a = x^2, b = y^2$：

$$x^2 + y^2 \geq 2xy$$

令 $a = \frac{x}{y}, b = \frac{y}{x}$（$x,y>0$）：

$$\frac{x}{y} + \frac{y}{x} \geq 2$$

令 $a = x, b = \frac{1}{x}$（$x>0$）：

$$x + \frac{1}{x} \geq 2$$

### 4.3 Nesbitt 不等式

对正数 $a, b, c$：

$$\frac{a}{b+c} + \frac{b}{a+c} + \frac{c}{a+b} \geq \frac{3}{2}$$

**证明**：每项加 $1$：

$$\frac{a+b+c}{b+c} + \frac{a+b+c}{a+c} + \frac{a+b+c}{a+b} \geq \frac{9}{2}$$

设 $s = a+b+c$，由调和-算术均值不等式：

$$\frac{3}{\frac{1}{b+c}+\frac{1}{a+c}+\frac{1}{a+b}} \leq \frac{(b+c)+(a+c)+(a+b)}{3} = \frac{2s}{3}$$

故 $\frac{1}{b+c}+\frac{1}{a+c}+\frac{1}{a+b} \geq \frac{9}{2s}$，乘以 $s$ 得结论。$\blacksquare$

### 4.4 幂平均不等式（Power Mean）

定义 $r$ 阶幂平均：

$$M_r = \left(\frac{1}{n}\sum_{i=1}^n a_i^r\right)^{1/r}, \quad r \neq 0; \qquad M_0 = G_n$$

则 $r \leq s \Rightarrow M_r \leq M_s$，即幂平均关于阶数单调不减。

对应关系：$M_{-1} = H_n$，$M_0 = G_n$，$M_1 = A_n$，$M_2 = Q_n$。

均值不等式链是 $M_{-1} \leq M_0 \leq M_1 \leq M_2$ 的特例。

### 4.5 Cauchy-Schwarz 不等式

对实数 $a_i, b_i$：

$$\left(\sum_{i=1}^n a_i b_i\right)^2 \leq \left(\sum_{i=1}^n a_i^2\right)\left(\sum_{i=1}^n b_i^2\right)$$

**证明（配方法）**：考虑关于 $t$ 的二次多项式

$$f(t) = \sum_{i=1}^n (a_i t - b_i)^2 = \left(\sum a_i^2\right)t^2 - 2\left(\sum a_i b_i\right)t + \sum b_i^2 \geq 0$$

判别式非正：$\Delta = 4\left(\sum a_i b_i\right)^2 - 4\left(\sum a_i^2\right)\!\left(\sum b_i^2\right) \leq 0$。$\blacksquare$

### 4.6 均值不等式的极值应用

**例**：已知 $x + y = s$（$x,y>0$），求 $xy$ 的最大值。

由 AM-GM：$\dfrac{x+y}{2} \geq \sqrt{xy}$，故 $xy \leq \dfrac{s^2}{4}$，等号当 $x = y = \dfrac{s}{2}$ 时成立。

**例**：已知 $xy = p$（$x,y>0$），求 $x+y$ 的最小值。

由 AM-GM：$x + y \geq 2\sqrt{xy} = 2\sqrt{p}$，等号当 $x = y = \sqrt{p}$ 时成立。

---

## 5. 总结

$$H_n \leq G_n \leq A_n \leq Q_n$$

| 不等式 | 核心工具 |
|--------|----------|
| $G \geq H$ | 对倒数用 AM-GM |
| $A \geq G$ | Cauchy 前向-后向归纳 / Jensen 不等式 |
| $Q \geq A$ | Cauchy-Schwarz 不等式 |

等号均在 $a_1 = a_2 = \cdots = a_n$ 时成立。
