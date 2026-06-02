Problem (4)

Find the inverse Laplace transform of

F(s) = (s + 3) / [(s + 1)^2(s + 2)]

---

Step 1: Partial Fraction Expansion

Assume

F(s)

= A/(s + 1)

+ B/(s + 1)^2

+ C/(s + 2)

Multiply both sides by

(s + 1)^2(s + 2)

Then

s + 3

= A(s + 1)(s + 2)

+ B(s + 2)

+ C(s + 1)^2

Expand

= A(s² + 3s + 2)

+ B(s + 2)

+ C(s² + 2s + 1)

Collect terms

= (A + C)s²

+ (3A + B + 2C)s

+ (2A + 2B + C)

Compare coefficients

A + C = 0

3A + B + 2C = 1

2A + 2B + C = 3

---

Step 2: Solve for A, B, and C

From

A + C = 0

C = -A

Substitute into

3A + B + 2C = 1

3A + B - 2A = 1

A + B = 1

B = 1 - A

Substitute into

2A + 2B + C = 3

2A + 2(1 - A) - A = 3

2 - A = 3

A = -1

Therefore

C = 1

B = 2

Thus

F(s)

= -1/(s + 1)

+ 2/(s + 1)^2

+ 1/(s + 2)

---

Step 3: Inverse Laplace Transform

L^-1[F(s)]

= L^-1[-1/(s + 1)]

+ L^-1[2/(s + 1)^2]

+ L^-1[1/(s + 2)]

= -e^(-t)

+ 2te^(-t)

+ e^(-2t)

---

Answer

f(t)

= -e^(-t)

+ 2te^(-t)

+ e^(-2t)

==================================================

Problem (6)

Find the Fourier Transform of

f(t) = te^(-5t)

---

Step 1: Fourier Transform Definition

F(w)

= ∫[0→∞] f(t)e^(-jwt)dt

Substitute f(t)

= ∫[0→∞] te^(-5t)e^(-jwt)dt

Combine exponents

= ∫[0→∞] te^(-(5+jw)t)dt

---

Step 2: Let

a = 5 + jw

Then

F(w)

= ∫[0→∞] te^(-at)dt

Using

∫[0→∞] te^(-at)dt

= 1/a²

Therefore

F(w)

= 1/(5 + jw)²

---

Answer

F(w)

= 1/(5 + jw)²
