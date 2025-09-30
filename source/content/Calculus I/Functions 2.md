30/09/25

# Injective and Surjective functions

$$
\displaylines{
f(x) = \frac{1}{1+x^2} \\
f(x): \mathbb{R}  \to \mathbb{R}^+ \\
\text{Domain } f: \mathbb{R} \\
\text{Range } f: (0, 1]
}
$$
Not injective as f(-1) = f(1)
Not subjective as range(f) < R

Changing the target set can turn a function [surjective](Functions%201.md)
Looking at a smaller part of the domain can make a periodic function no longer periodic

$$
\displaylines{
f: \mathbb{R} \to \mathbb{R} \\
f(x) = \sin(x) \\
\text{not injective as sinx is periodic} \\ 
\text{not surjective as the range of } f \subsetneq \mathbb{R}
}
$$

$$
\displaylines{
f_2: \mathbb{R} \to [-1, 1] \\
f_2(x) = \sin(x) \\
\text{not injective as } \sin(x) \text{ is still periodic} \\
\text{surjective as range} f_2 \subseteq [-1, 1]
}
$$
$$
\displaylines{
f_3: [-\frac{\pi}{2}, \frac{\pi}{2}] \to [-1, 1] \\
f_3(x) = \sin(x) \\
\text{injective as this area of } \sin(x) \text{ is not periodic} \\
\text{surjective as range of } f_3 \subseteq [-1,1]
}
$$

# Composing functions
$$
\displaylines{
	\begin{align}
		\text{Suppose } & f: \mathbb{X} \to \mathbb{Y} \\
		& g: \mathbb{Y}  \to \mathbb{Z} 
	\end{align} \\

g \cdot f: \mathbb{X}  \to \mathbb{Z}  
}
$$

ex.
$$
\displaylines{
	\begin{align}
		f: \mathbb{R} \to \mathbb{R},\   & f(x) = 2x + 1 \\
		g: \mathbb{R} \to \mathbb{R}^+,\ & g(x) = x^2
	\end{align} \\
}
$$

$$
\displaylines{
(g \cdot f)(x) = g(f(x)) = (2x + 1)^2 \\
however, \\
(f \cdot g)(x) = f(g(x)) = 2x^2 + 1 \\
therefore\  f \cdot g \neq g \cdot f
}
$$

<u>Composite functions are not commutative</u>

# Inverse functions

For a function to have an inverse function it must be bijective.

e.g. f(x): A -> B
- If the function is not injective, then there may be multiple elements in set A which result in set B.
- If the function is not surjective, then there are elements in set B which are not attainable through the function.

The graph of an inverse function is a reflection of the original function along the line } x=y

The identity function on a set X is a function I: x->x defined by I(x) = x

## <u>Proving injectivity and surjectivity</u>

$$
\displaylines{
f: \mathbb{R} \to \mathbb{R} \\
f(x) = 2x + 1
}
$$

**Prove f(x) is injective **

- Prove that each output can only have 1 input

$$
\displaylines{
\text{suppose } f(x_1) = f(x_2) \\
2x_1 + 1 = 2x_2 + 1 \\
2x_1 = 2x_2 \\
x_1 = x_2 \\
\text{this proves that each output has only one input}
}
$$

**Prove f(x) is surjective 

- Prove that the range can be the used in the inverse 

$$
\begin{gather*}
let\ y \in \mathbb{R} \\
\text{for  some } x,\ y = 2x + 1 \\
y-1 = 2x \\
\frac{y-1}{2} = x \\
\text{therefore, } f(x) = y \text{ hence surjective}
\end{gather*}
$$

f is surjective and therefore bijective

