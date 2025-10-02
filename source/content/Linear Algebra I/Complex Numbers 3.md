02/10/25

# Complex conjugation

If $z = a+bi$, $z^* = a - bi$
- Change the sign

If $z = re^{i\theta}$, $z^* = re^{-i\theta}$
- Multiply power by -1

## Properties of complex numbers and their conjugates:

$$
\begin{gather*}
z = z^* \text{ if } z \in \mathbb{R} \\
z \cdot z^* = |z|^2 \\
(z + w)^* = z^* + w^* \\
(zw)^* = z^* \cdot w^*
\end{gather*}
$$
$$
\begin{gather*}
\text{If } z = re^{i\theta}, \\
z^{-1} = \frac{1}{r}e^{-i\theta} \\ \\

\text{For } w \neq 0,\ z,w \in \mathbb{C} \\
\frac{z}{w} = zw^-1
\end{gather*}
$$

$$
\begin{gather*}
\text{If } z \in \mathbb{C} \text{ and } z \neq 0, \\
z^{-1}  = \frac{1}{|z|^2} \cdot z^*
\end{gather*}
$$
Example:

$$
\begin{align}
z^{-1} = \frac{1}{z} \\
\text{e.g. } (2 + i)^{-1} &\implies \frac{1}{(2+ i)} \\
&\implies \frac{1}{2 + i} \cdot \frac{2-i}{2-i}\\
&\implies \frac{2-i}{(2+i) \cdot (2 - i)} \\
&\implies \frac{2-i}{5} \\
&\implies \frac{1}{5} \cdot (2-i) = \frac{1}{|(2 + i)|^2} \cdot (2+i)^*
\end{align}
$$

# Solving for polynomial equations over $\mathbb{C}$

A polynomial of degree $n$ is:

$$
\begin{gather*}
a_nx^n + a_{n-1}x^{n-1} + \dots + a_1x + A_0 \\ \\

a_i \in \mathbb{C} \\
x \text{ is a variable} \\
a_n \neq 0
\end{gather*}
$$

Any degree complex polynomial has at least one complex root, $\alpha$
such that $\alpha \in \mathbb{C}$, $a_n\alpha^n + a_{n-1}\alpha^{n-1} + \dots + a_1\alpha + a_0 = 0$

There are at most $n$ complex roots

If each $a_i \in \mathbb{R}$ and $\alpha \in \mathbb{C}$ then $\alpha^*$ is also a root 
- Roots come in conjugate pairs
