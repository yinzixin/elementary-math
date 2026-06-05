# 调和平均与几何平均——$G \geq H$ 的变形与证明


---

## 一、四种平均数回顾

对两个正数 $a, b > 0$，定义：

$$H = \frac{2ab}{a+b}, \quad G = \sqrt{ab}, \quad A = \frac{a+b}{2}, \quad Q = \sqrt{\frac{a^2+b^2}{2}}$$

我们已经知道 $A \geq G$（算术平均 $\geq$ 几何平均）。

这篇文章的主角是更靠左的不等式：

$$\boxed{G \geq H}$$

即**几何平均 $\geq$ 调和平均**。

---

## 二、先看几个例子

| $a$ | $b$ | $G = \sqrt{ab}$ | $H = \dfrac{2ab}{a+b}$ | 谁大？ |
|-----|-----|-----------------|------------------------|--------|
| 1 | 9 | 3 | $\frac{18}{10} = 1.8$ | $G$ 大 |
| 4 | 4 | 4 | $\frac{32}{8} = 4$ | **相等** |
| 2 | 8 | 4 | $\frac{32}{10} = 3.2$ | $G$ 大 |
| 1 | 4 | 2 | $\frac{8}{5} = 1.6$ | $G$ 大 |

规律很清楚：$G \geq H$，只有 $a = b$ 时取等。

---

## 三、主定理

**定理**（几何平均 $\geq$ 调和平均）

对任意正数 $a, b > 0$，有

$$\sqrt{ab} \geq \frac{2ab}{a+b}$$

等号成立当且仅当 $a = b$。

### 证明

想要证明 $\sqrt{ab} \geq \dfrac{2ab}{a+b}$。

因为 $\sqrt{ab} > 0$，$a + b > 0$，两边乘以 $a + b$，不等号方向不变：

$$\sqrt{ab}\,(a+b) \geq 2ab$$

两边再除以 $\sqrt{ab} > 0$：

$$a + b \geq 2\sqrt{ab}$$

而这正是我们熟悉的**均值不等式** $A \geq G$，它等价于 $(\sqrt{a}-\sqrt{b})^2 \geq 0$，恒成立。

等号成立当且仅当 $\sqrt{a} = \sqrt{b}$，即 $a = b$。$\blacksquare$

---

## 四、常见变形

### 变形 1：两边平方

由 $\sqrt{ab} \geq \dfrac{2ab}{a+b}$，两边均为正数，平方后不等号方向不变：

$$ab \geq \frac{4a^2b^2}{(a+b)^2}$$

两边乘以 $(a+b)^2 > 0$：

$$ab(a+b)^2 \geq 4a^2b^2$$

两边除以 $ab > 0$：

$$(a+b)^2 \geq 4ab$$

**题目**：证明对任意正数 $a, b$，有 $(a+b)^2 \geq 4ab$，并指出等号成立的条件。

**证明**：

展开并移项：

$$(a+b)^2 - 4ab = a^2 + 2ab + b^2 - 4ab = a^2 - 2ab + b^2 = (a-b)^2 \geq 0$$

等号当且仅当 $a = b$。$\blacksquare$

> 口诀：和的平方 $\geq$ 四倍积。

---

### 变形 2：两边取倒数（方向改变！）

由 $\sqrt{ab} \geq \dfrac{2ab}{a+b}$，两边均为正数，取倒数后**方向改变**：

$$\frac{1}{\sqrt{ab}} \leq \frac{a+b}{2ab}$$

注意到 $\dfrac{a+b}{2ab} = \dfrac{1}{2b} + \dfrac{1}{2a} = \dfrac{1}{2}\!\left(\dfrac{1}{a}+\dfrac{1}{b}\right)$，故：

$$\frac{1}{a} + \frac{1}{b} \geq \frac{2}{\sqrt{ab}}$$

**题目**：证明对任意正数 $a, b$，有 $\dfrac{1}{a} + \dfrac{1}{b} \geq \dfrac{2}{\sqrt{ab}}$，并指出等号成立的条件。

**证明**：

两边乘以 $\sqrt{ab} > 0$：

$$\frac{\sqrt{ab}}{a} + \frac{\sqrt{ab}}{b} \geq 2$$

$$\sqrt{\frac{b}{a}} + \sqrt{\frac{a}{b}} \geq 2$$

令 $t = \sqrt{\dfrac{a}{b}} > 0$，原式变为 $t + \dfrac{1}{t} \geq 2$，即

$$(t-1)^2 = t^2 - 2t + 1 \geq 0 \quad \checkmark$$

等号当且仅当 $t = 1$，即 $a = b$。$\blacksquare$

---

### 变形 3：两边除以 $\sqrt{ab}$

由 $\sqrt{ab} \geq \dfrac{2ab}{a+b}$，两边除以 $\sqrt{ab} > 0$：

$$1 \geq \frac{2\sqrt{ab}}{a+b}$$

即 $a + b \geq 2\sqrt{ab}$，这正是熟悉的 $A \geq G$。

**结论**：$G \geq H$ 和 $A \geq G$ 是**等价**的，可以互推。

---

### 变形 4：令 $a = x^2,\ b = y^2$

将 $\sqrt{ab} \geq \dfrac{2ab}{a+b}$ 中的 $a, b$ 换成 $x^2, y^2$（$x, y > 0$）：

$$\sqrt{x^2 y^2} \geq \frac{2x^2y^2}{x^2+y^2}$$

$$xy \geq \frac{2x^2y^2}{x^2+y^2}$$

两边乘以 $\dfrac{x^2+y^2}{xy} > 0$：

$$x^2 + y^2 \geq 2xy$$

**题目**：证明对任意正数 $x, y$，有 $x^2 + y^2 \geq 2xy$，并指出等号成立的条件。

**证明**：

$$x^2 + y^2 - 2xy = (x-y)^2 \geq 0 \quad \checkmark$$

等号当且仅当 $x = y$。$\blacksquare$

---

### 变形 5：两边乘以 $\dfrac{a+b}{ab}$

由 $\sqrt{ab} \geq \dfrac{2ab}{a+b}$，两边乘以 $\dfrac{a+b}{ab} > 0$：

$$\frac{(a+b)\sqrt{ab}}{ab} \geq 2$$

$$\frac{a+b}{\sqrt{ab}} \geq 2$$

注意到 $\dfrac{a+b}{\sqrt{ab}} = \dfrac{a}{\sqrt{ab}} + \dfrac{b}{\sqrt{ab}} = \sqrt{\dfrac{a}{b}} + \sqrt{\dfrac{b}{a}}$，故：

$$\sqrt{\frac{a}{b}} + \sqrt{\frac{b}{a}} \geq 2$$

**题目**：证明对任意正数 $a, b$，有 $\sqrt{\dfrac{a}{b}} + \sqrt{\dfrac{b}{a}} \geq 2$，并指出等号成立的条件。

**证明**：

令 $t = \sqrt{\dfrac{a}{b}} > 0$，则 $\sqrt{\dfrac{b}{a}} = \dfrac{1}{t}$，原式变为：

$$t + \frac{1}{t} \geq 2$$

两边乘以 $t > 0$：

$$t^2 + 1 \geq 2t \iff (t-1)^2 \geq 0 \quad \checkmark$$

等号当且仅当 $t = 1$，即 $a = b$。$\blacksquare$

---

### 变形 6：$H$ 的分子分母同除以 $ab$

将 $H$ 改写：

$$H = \frac{2ab}{a+b} = \frac{2}{\dfrac{1}{a}+\dfrac{1}{b}}$$

由变形 2 已知 $\dfrac{1}{a}+\dfrac{1}{b} \geq \dfrac{2}{\sqrt{ab}}$，取倒数（方向改变）：

$$\frac{2}{\dfrac{1}{a}+\dfrac{1}{b}} \leq \frac{2}{\dfrac{2}{\sqrt{ab}}} = \sqrt{ab}$$

即 $H \leq G$，与主定理一致。$\blacksquare$

**题目**：已知 $\dfrac{1}{a}+\dfrac{1}{b} = 1$，证明 $\sqrt{ab} \geq 2$，并指出等号成立的条件。

**证明**：

由变形 2：$\dfrac{1}{a}+\dfrac{1}{b} \geq \dfrac{2}{\sqrt{ab}}$，代入条件：

$$1 \geq \frac{2}{\sqrt{ab}}$$

两边乘以 $\sqrt{ab} > 0$：

$$\sqrt{ab} \geq 2$$

等号当且仅当 $a = b$，此时 $\dfrac{1}{a}+\dfrac{1}{a}=1$，故 $a = b = 2$。$\blacksquare$

---

## 五、用 $G \geq H$ 求最值

### 例题 1：已知几何平均，求调和平均的上界

**题目**：$a, b > 0$，$\sqrt{ab} = 6$，求 $\dfrac{2ab}{a+b}$ 的最大值。

**解**：由 $G \geq H$：

$$\frac{2ab}{a+b} \leq \sqrt{ab} = 6$$

等号当 $a = b$ 时取到（此时 $ab = 36$，$a = b = 6$），故最大值为 $\boxed{6}$。

---

### 例题 2：分式的最小值

**题目**：$a > 0$，求 $\dfrac{a^2+1}{a}$ 的最小值。

**解**：

$$\frac{a^2+1}{a} = a + \frac{1}{a}$$

由变形 5（令 $a = b$）或直接用 $t + \dfrac{1}{t} \geq 2$：

$$a + \frac{1}{a} \geq 2$$

等号当 $a = 1$ 时取到，故最小值为 $\boxed{2}$。

---

### 例题 3：和固定时，调和平均的最大值

**题目**：$a + b = 10$，$a, b > 0$，求 $\dfrac{2ab}{a+b}$ 的最大值。

**解**：

$$H = \frac{2ab}{a+b} = \frac{2ab}{10} = \frac{ab}{5}$$

由 $(a+b)^2 \geq 4ab$（变形 1）：

$$100 \geq 4ab \implies ab \leq 25$$

故 $H = \dfrac{ab}{5} \leq \dfrac{25}{5} = 5$。

等号当 $a = b = 5$ 时取到，最大值为 $\boxed{5}$。

---

### 例题 4：速度问题中的调和平均

**题目**：小明去学校走路速度为 $a$ 米/分钟，回家速度为 $b$ 米/分钟，设学校距家 $d$ 米，求往返的平均速度，并说明它不超过 $\sqrt{ab}$。

**解**：

往返总路程 $= 2d$，总时间 $= \dfrac{d}{a} + \dfrac{d}{b} = d\!\left(\dfrac{1}{a}+\dfrac{1}{b}\right)$。

$$\text{平均速度} = \frac{2d}{d\!\left(\frac{1}{a}+\frac{1}{b}\right)} = \frac{2}{\frac{1}{a}+\frac{1}{b}} = \frac{2ab}{a+b} = H$$

由 $G \geq H$：$H \leq \sqrt{ab} = G$，即平均速度 $\leq \sqrt{ab}$。$\blacksquare$

---

## 六、常见错误提醒

| 错误做法 | 正确理解 |
|----------|----------|
| 取倒数后方向不变 | 正数取倒数，不等号**方向改变** |
| 两边都是正数才能平方保向 | 若有一边可能为负，平方前需判断 |
| 忘记验证等号能取到 | 求最值时必须验证等号成立的条件 |
| 将 $H = \frac{2ab}{a+b}$ 化简时出错 | 分子分母不能随意约分，需整体处理 |

---

## 七、总结

$$H = \frac{2ab}{a+b} \leq G = \sqrt{ab}$$

| 变形 | 结论 | 等号条件 |
|------|------|----------|
| 两边平方 | $(a+b)^2 \geq 4ab$ | $a=b$ |
| 两边取倒数 | $\dfrac{1}{a}+\dfrac{1}{b} \geq \dfrac{2}{\sqrt{ab}}$ | $a=b$ |
| 两边除以 $\sqrt{ab}$ | $a+b \geq 2\sqrt{ab}$（即 $A \geq G$） | $a=b$ |
| 令 $a=x^2, b=y^2$ | $x^2+y^2 \geq 2xy$ | $x=y$ |
| 两边乘以 $\frac{a+b}{ab}$ | $\sqrt{\frac{a}{b}}+\sqrt{\frac{b}{a}} \geq 2$ | $a=b$ |

**一句话记住核心**：几何平均 $\geq$ 调和平均，与算术平均 $\geq$ 几何平均可以互推，等号都在两数相等时成立。

---

## 八、练习题（无答案）

### A 组：仿照例题 1（已知积，求调和平均的最大值）

**A1.** 已知正数 $a, b$ 满足 $ab = 4$，求 $\dfrac{2ab}{a+b}$ 的最大值，并指出取到最大值时 $a, b$ 各为多少。

**A2.** 已知正数 $a, b$ 满足 $\sqrt{ab} = 5$，求 $\dfrac{2ab}{a+b}$ 的最大值，并指出取到最大值时 $a, b$ 各为多少。

**A3.** 已知正数 $a, b$ 满足 $\dfrac{1}{a}+\dfrac{1}{b} = 2$，求 $\sqrt{ab}$ 的最小值，并指出等号成立时 $a, b$ 各为多少。

---

### B 组：仿照例题 2（含倒数的分式求最小值）

**B1.** 已知 $a > 0$，求 $\dfrac{a^2 + 4}{a}$ 的最小值，并指出取到最小值时 $a$ 的值。

**B2.** 已知 $a > 0$，求 $\dfrac{a^2 + 9}{a}$ 的最小值，并指出取到最小值时 $a$ 的值。

**B3.** 已知 $a > 0$，求 $4a + \dfrac{1}{a}$ 的最小值，并指出取到最小值时 $a$ 的值。

---

### C 组：仿照例题 3（已知和，求调和平均的最大值）

**C1.** 已知正数 $a, b$ 满足 $a + b = 6$，求 $\dfrac{2ab}{a+b}$ 的最大值，并指出取到最大值时 $a, b$ 各为多少。

**C2.** 已知正数 $a, b$ 满足 $a + b = 4$，求 $ab$ 的最大值以及 $\dfrac{2ab}{a+b}$ 的最大值。

---

### D 组：仿照例题 4（实际问题）

**D1.** 一辆汽车从 $A$ 城到 $B$ 城，上坡路段速度为 $u$ 千米/时，下坡路段速度为 $v$ 千米/时（$u < v$）。设上坡与下坡路程相等，均为 $d$ 千米。
1. 写出全程平均速度的表达式。
2. 证明全程平均速度不超过 $\sqrt{uv}$。

**D2.** 小李完成一项工作，前半段时间效率为每小时完成 $a$ 件，后半段时间效率为每小时完成 $b$ 件（$a \neq b$）。
1. 写出全程平均效率（每小时完成件数）的表达式。
2. 判断全程平均效率与 $\dfrac{a+b}{2}$ 的大小关系，并给出理由。
