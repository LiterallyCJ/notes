01/10/25

# <u>Trig inverse functions</u>


$$
f: \mathbb{R} \to \mathbb{R},\ f(x) = \sin(x)
$$

Not bijective therefore has no inverse function.
Change the range to give it an inverse function:

$$
f: [-\frac{\pi}{2}, \frac{\pi}{2}] \to [-1, 1],\ f(x) = \sin(x)
$$

Now it is bijective and therefore has an inverse function

$$
\begin{gather*}
\text{Let the inverse function } \sin^{-1}(x) \\
\sin^{-1}(\sin(x)) = x \text{ so }\\ 
\sin(\sin^{-1}(x)) = x
\end{gather*}
$$

note: $sin^1(x) : [-1,1] \to [-\frac{\pi}{2}, \frac{\pi}{2}]$ 

$\cos(x): (0, \pi) \to (-1, 1)$ is bijective
Therefore the inverse has range and domain: $cos^{-1}(x) : (-1, 1) \to (0, \pi)$

# <u>Exponential and logarithmic functions</u>

Format for an exponential function:

$$
\begin{gather*}
\text{let } a > 0 \in \mathbb{R} \\
f: \mathbb{R} \to (0, \infty),\ f(x) = a^x
\end{gather*}
$$

e.g $f(x) = 2^x$

Properties of exponentials

$$
\begin{gather*}
a^0 = 1 \\
a^x \cdot a^y = a^{(x+y)} \\
a^{-x} = \frac{1}{a^x} \\
(ab)^x = a^x \cdot b^x
\end{gather*}
$$

$f(x) = a^x$ is a bijective function so it has an inverse- the logarithm

The logarithm of base a is  the function $\log_a  : (0, \infty) -> \mathbb{R}$
It is defined by $\log_a(x) = y$ if $a^y = x$

$$
\begin{gather*}
log_a(a^x) = x \\
a^{(log_a x)} = x
\end{gather*}
$$


Properties of logarithms:

$$
\begin{gather*}
\log_a(1) = 0 \\
\log_a(xy) = \log_a(x) + \log_a(y) \\
\log_a(x^y) = y\log_a(x) \\
\log_a(\frac{1}{x}) = -\log_a(x) \\
\log_a(x) = \frac{\log_b(x)}{\log_b(a)}
\end{gather*}
$$

Proof:

$$
\begin{gather*}
\log_a(xy) = \log_a(x) + \log_a(y) \\
\text{let } c = \log_a(xy),\ d = \log_a(x) + \log_a(y) 
\end{gather*}
$$

$$
\begin{gather*}
\text{Show } a^c = a^d \\
\text{Then show } c = d
\end{gather*}
$$
$$
a^c = a^{(log_a(xy))} = xy
$$
$$
\begin{align}
a^d &= a^{(log_a(x) + log_a(y))} \\ &= a^{(log_a(x))} \cdot a^{(log_a(x))} \\ &= xy
\end{align}
$$
$$
\text{therefore, } a^c = a^d
$$

Now take logs:

$$
\begin{gather*}
log_a(a^c) = log_a(a^d) \\
c = d
\end{gather*}
$$


# <u>Even and odd functions</u>

$$
\begin{gather*}
\text{A function } f \text{ is even if } f(-x) = f(x)\ \text{for all } x\in \text{domain f}
\end{gather*}
$$

$$
\begin{gather*}
\text{A function } f \text{ is odd if } f(-x) = -f(x)\ \text{for all } x\in \text{domain f}
\end{gather*}
$$

<u>e.g</u>
$$
\begin{align}
\text{let }f(x) = x^2 \\
f(-x) &= (-x^2)\\ 
&= x^2\\ 
&= f(x)
\text{ therefore even }
\end{align}
$$

<u>e.g 2</u>
$$
\begin{align}
\text{let } f(x) = x^3 \\
f(-x) &= (-x)^3 \\
&= -x^3 \\
&= -f(x) \text{ therefore odd}
\end{align}
$$

Even functions are symmetric about the y axis
Odd functions are symmetric about the origin