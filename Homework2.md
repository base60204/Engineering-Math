Problem (4)

Find the inverse Laplace transform of

$$
F(s)=\frac{s+3}{(s+1)^2(s+2)}
$$

---

Step 1: Partial Fraction Expansion

Assume

$$
\frac{s+3}{(s+1)^2(s+2)}

\frac{A}{s+1}
+
\frac{B}{(s+1)^2}
+
\frac{C}{s+2}
$$

Multiply both sides by $(s+1)^2(s+2)$:

$$
s+3=A(s+1)(s+2)+B(s+2)+C(s+1)^2
$$

Expanding:

$$
s+3=A(s^2+3s+2)+B(s+2)+C(s^2+2s+1)
$$

Collecting terms:

$$
s+3=(A+C)s^2+(3A+B+2C)s+(2A+2B+C)
$$

Comparing coefficients:

$$
A+C=0
$$

$$
3A+B+2C=1
$$

$$
2A+2B+C=3
$$

---

Step 2: Solve the Coefficients

From

$$
A+C=0
$$

we get

$$
C=-A
$$

Substitute into the remaining equations:

$$
A+B=1
$$

$$
2-A=3
$$

Therefore

$$
A=-1
$$

$$
B=2
$$

$$
C=1
$$

Thus

$$
F(s)

-\frac1{s+1}
+
\frac2{(s+1)^2}
+
\frac1{s+2}
$$

---

Step 3: Apply the Inverse Laplace Transform

Using

$$
L^{-1}\left(\frac1{s+a}\right)=e^{-at}
$$

and

$$
L^{-1}\left(\frac1{(s+a)^2}\right)=te^{-at}
$$

we obtain

$$
f(t)

-e^{-t}
+
2te^{-t}
+
e^{-2t}
$$

---

Answer

$$
\boxed{
f(t)

-e^{-t}
+
2te^{-t}
+
e^{-2t}
}
$$

---

Problem (6)

Find the Fourier Transform of

$$
f(t)=te^{-5t}
$$

---

Step 1: Apply the Fourier Transform Definition

The Fourier Transform is

$$
F(\omega)

\int_{0}^{\infty}
f(t)e^{-j\omega t}dt
$$

Substituting $f(t)=te^{-5t}$:

$$
F(\omega)

\int_{0}^{\infty}
te^{-5t}e^{-j\omega t}dt
$$

Combine the exponential terms:

$$
F(\omega)

\int_{0}^{\infty}
t,e^{-(5+j\omega)t}dt
$$

---

Step 2: Use the Standard Integral Formula

Let

$$
a=5+j\omega
$$

Then

$$
F(\omega)

\int_{0}^{\infty}
te^{-at}dt
$$

Using the standard result

$$
\int_{0}^{\infty}
te^{-at}dt

\frac1{a^2}
\qquad
(\operatorname{Re}(a)>0)
$$

we obtain

$$
F(\omega)

\frac1{(5+j\omega)^2}
$$

---

Answer

$$
\boxed{
F(\omega)

\frac1{(5+j\omega)^2}
}
$$
