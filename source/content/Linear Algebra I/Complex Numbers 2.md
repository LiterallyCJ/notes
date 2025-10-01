01/10/25

# Modulus of a complex number

Complex numbers can be shown on an Argand Diagram, where the $x$ coordinate symbolises the real value of a complex number and the $y$ coordinate symbolises the imaginary part.
$$
\begin{gather*}
\text{Modulus of } z = a+bi \\
\text{The length of the complex number as a vector} \\
|z| \in \mathbb{R} \\
|z| = \sqrt{a^2 + b^2} \\
if\ |z| = 0 \implies z = 0 + 0i
\end{gather*}
$$

$$
\begin{gather*}
\text{For any }z, w \in \mathbb{C} \\
|zw| = |z|\cdot|w|
\end{gather*}
$$
e.g.
$$
\begin{gather*}
z = a + bi \\
w = c + di\\
\end{gather*}
$$

$$
\begin{align}
zw &= ac + adi + cbi - bd \\
&= (ac - bd) + (ad + cb)i \\
|zw| &= \sqrt{(ac-bd)^2 + (ad + cb)^2} \\
&= \sqrt{a^2c^2 + b^2d^2 + a^2d^2 + b^2c^2} \\
&= \sqrt{(a^2 + b^2)(c^2 + d^2)}
\end{align}
$$
# Argument of a complex number

The argument arg$(z)$ of $z \in \mathbb{C}$ is the angle between $z$ and the positive $x$ axis between 
The principle argument is one such that arg$(z): [-2\pi, 2\pi]$
$$
\begin{gather*}
z = a + bi \\
|z| = r = \sqrt{a^2 + b^2} \\
\text{arg}(z) = \tan^{-1}(\frac{b}{a})
\end{gather*}
$$
# Forms of a complex number
## <u>Cartesian</u>
$$
z = a + bi
$$
## <u>Polar</u>
$$
\begin{gather*}
r = |z| \\
\theta = \arg(z) \\
z = r(\cos(\theta) + i\sin(\theta))
\end{gather*}
$$
## <u>Exponential</u>
$$
\begin{gather*}
\text{Using same definitions of } r \text{ and }\theta, \\
z= r\cdot e^{i\theta}
\end{gather*}
$$
note: $e^{i\pi} = -1$
$$
\begin{gather*}
a = r\cos(\theta) \\
b = r\sin(\theta) \\
\text{a symbolises the real x-axis, and b is the imaginary y-axis}
\end{gather*}
$$
# Properties of a complex number

$$
\begin{gather*}
\text{For any angles, } \theta_1,\ \theta_2 \in \mathbb{R} \\
|e^{i\theta}| = 1 \\
e^{i\theta_1} \cdot e^{i\theta_2} = e^{i(\theta_1 + \theta_2)}
\end{gather*}
$$
Proof:

$$
\begin{align}
|e^{i\theta}| &= |\cos(\theta) + i\sin(\theta)| \\
&= \sqrt{\cos^2(\theta) + \sin^2(\theta)} \\
&= 1
\end{align}
$$
$$
\begin{align}
e^{i\theta_1} \cdot e^{i\theta_2} &= (\cos(\theta_1) + i\sin(\theta_1)) \cdot (\cos(\theta_2) + i\sin(\theta_2)) \\
&= (\cos(\theta_1)\cos(\theta_2) - \sin(\theta_1)\sin(\theta_2)) + i(\cos(\theta_1)\sin(\theta_2) + \sin(\theta_1)\cos(\theta_2)) \\
&= \cos(\theta_1 + \theta_2) + i\sin(\theta_1 + \theta_2)\\
&= e^{i(\theta_1 + \theta_2)}
\end{align}
$$
