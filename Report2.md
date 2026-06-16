# Laplace Transformation

## RC 電路充電分析

### 已知條件

```math
U_s = 5V
```

```math
R = 10k\Omega
```

```math
C = 100\mu F
```

```math
u_c(0)=0V
```

求：

1. 電容電壓 $u_c(t)$
2. 充電電流 $i(t)$
3. 達到穩態 95% 所需時間

---

## Step 1：建立電路微分方程式

由 KVL：

```math
U_s=u_R(t)+u_c(t)
```

而

```math
u_R(t)=Ri(t)
```

```math
i(t)=C\frac{du_c(t)}{dt}
```

因此

```math
U_s=RC\frac{du_c(t)}{dt}+u_c(t)
```

代入數值：

```math
5=(10\times10^3)(100\times10^{-6})
\frac{du_c(t)}{dt}+u_c(t)
```

因為

```math
RC=1
```

故方程式化為

```math
\frac{du_c(t)}{dt}+u_c(t)=5
```

---

## Step 2：拉氏轉換

對兩邊取 Laplace Transform：

```math
sU_c(s)-u_c(0)+U_c(s)=\frac{5}{s}
```

由

```math
u_c(0)=0
```

得

```math
(s+1)U_c(s)=\frac{5}{s}
```

因此

```math
U_c(s)=\frac{5}{s(s+1)}
```

---

## Step 3：部分分式分解

設

```math
\frac{5}{s(s+1)}
=
\frac{A}{s}
+
\frac{B}{s+1}
```

則

```math
5=A(s+1)+Bs
```

令

```math
s=0
```

得

```math
A=5
```

令

```math
s=-1
```

得

```math
B=-5
```

因此

```math
U_c(s)
=
\frac{5}{s}
-
\frac{5}{s+1}
```

---

## Step 4：反拉氏轉換

利用

```math
L^{-1}
\left\{
\frac{1}{s}
\right\}
=1
```

```math
L^{-1}
\left\{
\frac{1}{s+1}
\right\}
=e^{-t}
```

得到

```math
u_c(t)
=
5(1-e^{-t})
```

---

## 電容電壓答案

```math
u_c(t)=5(1-e^{-t})V
```

---

## Step 5：求充電電流

由

```math
i(t)=C\frac{du_c(t)}{dt}
```

先微分：

```math
\frac{du_c(t)}{dt}
=
5e^{-t}
```

因此

```math
i(t)
=
100\times10^{-6}
\times5e^{-t}
```

```math
i(t)
=
5\times10^{-4}e^{-t}
```

---

## 電流答案

```math
i(t)=0.5mA\;e^{-t}
```

---

## Step 6：求達到 95% 穩態時間

穩態電壓：

```math
u_c(\infty)=5V
```

95% 時：

```math
u_c(t)=0.95\times5
```

```math
u_c(t)=4.75V
```

代入

```math
4.75=5(1-e^{-t})
```

```math
0.95=1-e^{-t}
```

```math
e^{-t}=0.05
```

兩邊取自然對數：

```math
t=-\ln(0.05)
```

```math
t\approx2.996
```

---

## Final Answers

電容電壓：

```math
u_c(t)=5(1-e^{-t})V
```

電流：

```math
i(t)=0.5mA\,e^{-t}
```

達到穩態 95% 所需時間：

```math
t\approx3s
```
