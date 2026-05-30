Problem (4)

Find the inverse Laplace transform of

F(s) = (s + 3) / [(s + 1)^2 (s + 2)]

---

Step 1: Partial Fraction Expansion

Assume

(s + 3) / [(s + 1)^2 (s + 2)]

= A/(s + 1) + B/(s + 1)^2 + C/(s + 2)

Multiply both sides by

(s + 1)^2 (s + 2)

Then

s + 3

= A(s + 1)(s + 2)

+ B(s + 2)
+ C(s + 1)^2

Expand:

= A(s^2 + 3s + 2)

+ B(s + 2)
+ C(s^2 + 2s + 1)

Collect terms:

(A + C)s^2 + (3A + B + 2C)s + (2A + 2B + C)

Compare coefficients:

A + C = 0

3A + B + 2C = 1

2A + 2B + C = 3

---

Step 2: Solve for A, B and C

From

A + C = 0

we get

C = -A

Substitute into the second equation:

A + B = 1

B = 1 - A

Substitute into the third equation:

2A + 2(1 - A) - A = 3

2 - A = 3

A = -1

Therefore

B = 2

C = 1

Thus

F(s)

= -1/(s + 1)

+ 2/(s + 1)^2
+ 1/(s + 2)

---

Step 3: Apply Inverse Laplace Transform

Using

L^-1[1/(s + a)] = e^(-at)

L^-1[1/(s + a)^2] = t·e^(-at)

we obtain

f(t)

= -e^(-t)

+ 2t·e^(-t)
+ e^(-2t)

---

Answer

f(t) = -e^(-t) + 2t·e^(-t) + e^(-2t)

==================================================

Problem (6)

Find the Fourier Transform of

f(t) = t·e^(-5t)

---

Step 1: Apply the Fourier Transform Definition

F(w)

= ∫[0→∞] f(t)e^(-jwt)dt

Substitute f(t):

F(w)

= ∫[0→∞] t·e^(-5t)e^(-jwt)dt

Combine the exponential terms:

F(w)

= ∫[0→∞] t·e^(-(5 + jw)t)dt

---

Step 2: Use the Standard Formula

Let

a = 5 + jw

Then

F(w)

= ∫[0→∞] t·e^(-at)dt

Using the standard result

∫[0→∞] t·e^(-at)dt = 1/a^2

Therefore

F(w)

= 1/(5 + jw)^2

---

Answer

F(w) = 1/(5 + jw)^2
