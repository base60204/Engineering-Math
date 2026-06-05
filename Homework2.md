## Problem (4)

Find the inverse Laplace transform of

```math
F(s)=\frac{s+3}{(s+1)^2(s+2)}
```

### Step 1: Partial Fraction Expansion

Assume

```math
\frac{s+3}{(s+1)^2(s+2)}
=
\frac{A}{s+1}
+
\frac{B}{(s+1)^2}
+
\frac{C}{s+2}
```

Multiply both sides by

```math
(s+1)^2(s+2)
```

to obtain

```math
s+3
=
A(s+1)(s+2)
+
B(s+2)
+
C(s+1)^2
```

Expand:

```math
s+3
=
A(s^2+3s+2)
+
B(s+2)
+
C(s^2+2s+1)
```

Collect terms:

```math
s+3
=
(A+C)s^2
+
(3A+B+2C)s
+
(2A+2B+C)
```

Compare coefficients:

```math
A+C=0
```

```math
3A+B+2C=1
```

```math
2A+2B+C=3
```

From

```math
A+C=0
```

we have

```math
C=-A
```

Substitute into the second equation:

```math
3A+B-2A=1
```

```math
A+B=1
```

```math
B=1-A
```

Substitute into the third equation:

```math
2A+2(1-A)-A=3
```

```math
2-A=3
```

```math
A=-1
```

Therefore,

```math
C=1
```

```math
B=2
```

Hence,

```math
F(s)
=
-\frac{1}{s+1}
+
\frac{2}{(s+1)^2}
+
\frac{1}{s+2}
```

### Step 2: Inverse Laplace Transform

Using

```math
L^{-1}\left\{\frac{1}{s+a}\right\}
=
e^{-at}
```

and

```math
L^{-1}\left\{\frac{1}{(s+a)^2}\right\}
=
te^{-at}
```

we obtain

```math
f(t)
=
-e^{-t}
+
2te^{-t}
+
e^{-2t}
```

### Answer

```math
f(t)
=
-e^{-t}
+
2te^{-t}
+
e^{-2t}
```

---

## Problem (6)

Find the Fourier Transform of

```math
f(t)=te^{-5t}
```

### Step 1: Apply the Fourier Transform Definition

The Fourier Transform is

```math
F(\omega)
=
\int_0^{\infty}
f(t)e^{-j\omega t}\,dt
```

Substitute

```math
f(t)=te^{-5t}
```

Then

```math
F(\omega)
=
\int_0^{\infty}
te^{-5t}e^{-j\omega t}\,dt
```

Combine the exponential terms:

```math
F(\omega)
=
\int_0^{\infty}
t\,e^{-(5+j\omega)t}\,dt
```

Let

```math
a=5+j\omega
```

Then

```math
F(\omega)
=
\int_0^{\infty}
te^{-at}\,dt
```

### Step 2: Use the Integration Formula

Using

```math
\int_0^{\infty}
te^{-at}\,dt
=
\frac{1}{a^2}
```

where

```math
\operatorname{Re}(a)>0
```

we obtain

```math
F(\omega)
=
\frac{1}{(5+j\omega)^2}
```

### Answer

```math
F(\omega)
=
\frac{1}{(5+j\omega)^2}
```
