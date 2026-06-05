# 两数均值不等式——从入门到变形



## 一、从一个小发现出发

我们来看一道题：

> 两个正数 $a$ 和 $b$ 的平均数，和它们的积的平方根，哪个更大？

举几个例子感受一下：

| $a$ | $b$ | 算术平均 $\dfrac{a+b}{2}$ | 几何平均 $\sqrt{ab}$ | 谁大？ |
|-----|-----|--------------------------|----------------------|--------|
| 1 | 9 | 5 | 3 | 算术平均大 |
| 4 | 4 | 4 | 4 | **相等** |
| 2 | 8 | 5 | 4 | 算术平均大 |
| 1 | 1 | 1 | 1 | **相等** |

规律很明显：**算术平均 $\geq$ 几何平均**，只有两数相等时取等。

---

## 二、主定理

**定理（两数均值不等式）**

对任意正数 $a, b > 0$，有

$$\boxed{\dfrac{a+b}{2} \geq \sqrt{ab}}$$

等号成立，当且仅当 $a = b$。

也可以写成：

$$a + b \geq 2\sqrt{ab}$$

### 证明

**关键想法**：任何数的平方都 $\geq 0$。

$$(\sqrt{a} - \sqrt{b})^2 \geq 0$$

展开左边：

$$a - 2\sqrt{a}\cdot\sqrt{b} + b \geq 0$$

$$a + b \geq 2\sqrt{ab}$$

两边除以 $2$：

$$\frac{a+b}{2} \geq \sqrt{ab}$$

等号成立当且仅当 $\sqrt{a} - \sqrt{b} = 0$，即 $a = b$。$\blacksquare$

---

## 三、常见变形（换个面孔认一认）

### 变形 1：令 $a = x^2,\ b = y^2$

将 $a + b \geq 2\sqrt{ab}$ 中的 $a, b$ 换成 $x^2, y^2$（$x,y>0$）：

$$x^2 + y^2 \geq 2xy$$

**题目**：证明对任意正数 $x, y$，有 $x^2 + y^2 \geq 2xy$。

**证明**：

$$x^2 - 2xy + y^2 \geq 0$$

$$(x-y)^2 \geq 0 \quad \checkmark$$

等号当且仅当 $x = y$。$\blacksquare$

> **口诀**：平方和 $\geq$ 两倍乘积。

---

### 变形 2：令 $b = \dfrac{1}{a}$

在 $a + b \geq 2\sqrt{ab}$ 中令 $b = \dfrac{1}{a}$（$a > 0$）：

$$a + \frac{1}{a} \geq 2\sqrt{a \cdot \frac{1}{a}} = 2\sqrt{1} = 2$$

**题目**：证明对任意正数 $a$，有 $a + \dfrac{1}{a} \geq 2$。

**证明**：

两边乘以 $a$（$a>0$，不等号方向不变）：

$$a^2 + 1 \geq 2a$$

$$a^2 - 2a + 1 \geq 0$$

$$(a-1)^2 \geq 0 \quad \checkmark$$

等号当且仅当 $a = 1$。$\blacksquare$

---

### 变形 3：令 $a = \dfrac{x}{y},\ b = \dfrac{y}{x}$

在 $a + b \geq 2\sqrt{ab}$ 中令 $a = \dfrac{x}{y},\ b = \dfrac{y}{x}$（$x,y>0$）：

$$\frac{x}{y} + \frac{y}{x} \geq 2\sqrt{\frac{x}{y}\cdot\frac{y}{x}} = 2\sqrt{1} = 2$$

**题目**：证明对任意正数 $x, y$，有 $\dfrac{x}{y} + \dfrac{y}{x} \geq 2$。

**证明**：

两边乘以 $xy > 0$：

$$x^2 + y^2 \geq 2xy$$

即变形 1，已证。等号当且仅当 $x = y$。$\blacksquare$

---

### 变形 4：两边平方（利用倒过来的关系）

**题目**：已知正数 $a, b$ 满足 $\sqrt{ab} \leq 3$，能说明 $ab \leq 9$ 吗？

**分析**：因为 $a,b > 0$，所以 $\sqrt{ab} > 0$，对不等式两边平方，不等号方向不变：

$$ab = (\sqrt{ab})^2 \leq 3^2 = 9 \quad \checkmark$$

---

### 变形 5：两边取倒数

> 两个正数取倒数，不等号**方向改变**！

由 $\dfrac{a+b}{2} \geq \sqrt{ab}$，两边取倒数：

$$\frac{2}{a+b} \leq \frac{1}{\sqrt{ab}}$$

即

$$\frac{2}{\dfrac{1}{a}+\dfrac{1}{b}} \cdot \frac{1}{ab} \leq \frac{1}{\sqrt{ab}}$$

更简洁地，可得到**调和平均 $\leq$ 几何平均**：

$$\frac{2ab}{a+b} \leq \sqrt{ab}$$

**题目**：证明 $\dfrac{2ab}{a+b} \leq \sqrt{ab}$（$a,b>0$）。

**证明**：

由已知 $a + b \geq 2\sqrt{ab} > 0$，两边取倒数（正数，方向变）：

$$\frac{1}{a+b} \leq \frac{1}{2\sqrt{ab}}$$

两边乘以 $2ab > 0$：

$$\frac{2ab}{a+b} \leq \frac{2ab}{2\sqrt{ab}} = \sqrt{ab} \quad \checkmark$$

等号当且仅当 $a = b$。$\blacksquare$

---

### 变形 6：分母换元

**题目**：证明对正数 $a, b$，有

$$\frac{a}{b} + \frac{b}{a} + 2 \geq \frac{(a+b)^2}{ab}$$

**证明**：

右边展开：

$$\frac{(a+b)^2}{ab} = \frac{a^2+2ab+b^2}{ab} = \frac{a}{b} + 2 + \frac{b}{a}$$

所以两边相等！这是恒等式，自然成立。$\blacksquare$

> 这说明 $\dfrac{(a+b)^2}{ab} = \dfrac{a}{b}+\dfrac{b}{a}+2 \geq 2+2 = 4$，即 $(a+b)^2 \geq 4ab$，正是均值不等式两边平方。

---

### 变形 7：加同一个数后取倒数

**题目**：证明 $\dfrac{1}{1+a} + \dfrac{1}{1+b} \geq \dfrac{4}{2+a+b}$（$a,b>0$）。

**证明**：

设 $x = 1+a > 1$，$y = 1+b > 1$，原式变为

$$\frac{1}{x} + \frac{1}{y} \geq \frac{4}{x+y}$$

两边乘以 $xy(x+y) > 0$：

$$y(x+y) + x(x+y) \geq 4xy$$

$$(x+y)^2 \geq 4xy$$

$$x^2 - 2xy + y^2 \geq 0$$

$$(x-y)^2 \geq 0 \quad \checkmark$$

等号当且仅当 $x=y$，即 $a=b$。$\blacksquare$

---

## 四、用均值不等式求最值

均值不等式最强大的用途：**已知和求积的最大，已知积求和的最小**。

### 例题 1：已知和，求积最大

**题目**：$x + y = 10$，$x,y > 0$，求 $xy$ 的最大值。

**解**：由均值不等式：

$$\frac{x+y}{2} \geq \sqrt{xy}$$

$$\frac{10}{2} \geq \sqrt{xy}$$

$$5 \geq \sqrt{xy}$$

两边平方：$xy \leq 25$。

等号当 $x = y = 5$ 时取到，故 $xy$ 最大值为 $\boxed{25}$。

---

### 例题 2：已知积，求和最小

**题目**：$xy = 9$，$x,y > 0$，求 $x + y$ 的最小值。

**解**：由均值不等式：

$$x + y \geq 2\sqrt{xy} = 2\sqrt{9} = 6$$

等号当 $x = y = 3$ 时取到，故 $x + y$ 最小值为 $\boxed{6}$。

---

### 例题 3：求含倒数的式子的最小值

**题目**：$x > 0$，求 $x + \dfrac{4}{x}$ 的最小值。

**解**：令 $a = x$，$b = \dfrac{4}{x}$，由均值不等式：

$$x + \frac{4}{x} \geq 2\sqrt{x \cdot \frac{4}{x}} = 2\sqrt{4} = 4$$

等号当 $x = \dfrac{4}{x}$，即 $x^2 = 4$，$x = 2$ 时取到。

故最小值为 $\boxed{4}$。

---

### 例题 4：积固定时，面积最大的矩形

**题目**：用 20 米篱笆围一个矩形，怎样围面积最大？

设两边长为 $x$ 和 $y$，则 $2(x+y) = 20$，即 $x + y = 10$。

由例题 1，面积 $S = xy \leq 25$ 平方米，当 $x = y = 5$（正方形）时最大。

---

## 五、常见错误提醒

| 错误做法 | 正确理解 |
|----------|----------|
| 对负数取倒数，方向不变 | 负数取倒数，方向**改变** |
| 两边平方，方向不变 | 只有两边都**非负**时，平方方向才不变 |
| 忘记验证等号能取到 | 求最值时必须验证等号成立的条件 |
| $\sqrt{ab} = \sqrt{a}\cdot\sqrt{b}$ 用于负数 | 只对**非负数**成立 |

---

## 六、总结

$$a + b \geq 2\sqrt{ab} \quad (a,b>0)$$

| 变形 | 式子 | 等号条件 |
|------|------|----------|
| 原式 | $\dfrac{a+b}{2} \geq \sqrt{ab}$ | $a=b$ |
| 换 $x^2,y^2$ | $x^2+y^2 \geq 2xy$ | $x=y$ |
| 令 $b=1/a$ | $a+\dfrac{1}{a} \geq 2$ | $a=1$ |
| 令 $a=x/y$ | $\dfrac{x}{y}+\dfrac{y}{x} \geq 2$ | $x=y$ |
| 两边平方 | $(a+b)^2 \geq 4ab$ | $a=b$ |
| 取倒数 | $\dfrac{2ab}{a+b} \leq \sqrt{ab}$ | $a=b$ |

**一句话记住核心**：正数的算术平均 $\geq$ 几何平均，等号当两数相等。
