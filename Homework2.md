# Assignment 02

## Problem (4)

Find the inverse Laplace transform of

```text
F(s) = (s + 3) / [(s + 1)^2(s + 2)]
```

---

### Step 1: Partial Fraction Expansion

Assume

```text
F(s)

= A/(s + 1)

+ B/(s + 1)^2

+ C/(s + 2)
```

Multiply both sides by

```text
(s + 1)^2(s + 2)
```

Then

```text
s + 3

= A(s + 1)(s + 2)

+ B(s + 2)

+ C(s + 1)^2
```

Expand

```text
s + 3

= A(s^2 + 3s + 2)

+ B(s + 2)

+ C(s^2 + 2s + 1)
```

Collect terms

```text
s + 3

= (A + C)s^2

+ (3A + B + 2C)s

+ (2A + 2B + C)
```

Compare coefficients

```text
A + C = 0

3A + B + 2C = 1

2A + 2B + C = 3
```

---

### Step 2: Solve for A, B and C

From

```text
A + C = 0
```

we obtain

```text
C = -A
```

Substitute into

```text
3A + B + 2C = 1
```

```text
3A + B - 2A = 1

A + B = 1

B = 1 - A
```

Substitute into

```text
2A + 2B + C = 3
```

```text
2A + 2(1 - A) - A = 3

2 - A = 3

A = -1
```

Therefore

```text
C = 1

B = 2
```

Thus

```text
F(s)

= -1/(s + 1)

+ 2/(s + 1)^2

+ 1/(s + 2)
```

---

### Step 3: Inverse Laplace Transform

```text
L^-1[F(s)]

= L^-1[-1/(s + 1)]

+ L^-1[2/(s + 1)^2]

+ L^-1[1/(s + 2)]
```

Using

```text
L^-1[1/(s + a)] = e^(-at)

L^-1[1/(s + a)^2] = t·e^(-at)
```

We obtain

```text
f(t)

= -e^(-t)

+ 2te^(-t)

+ e^(-2t)
```

---

### Answer

```text
f(t)

= -e^(-t)

+ 2te^(-t)

+ e^(-2t)
```

==================================================

## Problem (6)

Find the Fourier Transform of

```text
f(t) = te^(-5t)
```

---

### Step 1: Apply the Fourier Transform Definition

```text
F(w)

= ∫[0→∞] f(t)e^(-jwt)dt
```

Substitute f(t)

```text
F(w)

= ∫[0→∞] te^(-5t)e^(-jwt)dt
```

Combine the exponential terms

```text
F(w)

= ∫[0→∞] te^(-(5 + jw)t)dt
```

---

### Step 2: Let

```text
a = 5 + jw
```

Then

```text
F(w)

= ∫[0→∞] te^(-at)dt
```

Using

```text
∫[0→∞] te^(-at)dt

= 1/a^2
```

Therefore

```text
F(w)

= 1/(5 + jw)^2
```

---

### Answer

```text
F(w)

= 1/(5 + jw)^2
```
