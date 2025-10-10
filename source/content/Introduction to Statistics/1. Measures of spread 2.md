$Range$- Difference between upper and lower value
$IQR$- Difference between first and third quartile

$$
\begin{gather*}
Q_1 = \frac{1}{4}(3n + 1) \\
Q_3 = \frac{3}{4}(3n + 1)
\end{gather*}
$$
## <u>Variance</u>

$$
\frac{1}{n-1}\underbrace{\sum_{i = 1}^{n}(x - \bar x)^2}_{SSE(\bar x)}, \text{ where } \bar x = \frac{1}{n}\sum^{n}_{i = 1}x_i
$$

$$
\begin{align}
\sum_{i = 1}^{n}(x_i - \bar x)^2 &= \sum_{i = 1}^{n}(x_i^2 - 2 \bar x x_i + \bar x^2) \\
&= \sum_{i = 1}^{n}x_i^2 - \sum_{i = 1}^{n}2\bar xx_i + \sum_{i = 1}^{n} \bar x^2 \\
&= \sum_{i = 1}^{n}x_i^2 - 2 \bar x \sum_{i = 1}^{n}x_i + n \bar x^2 \\
(\text{We have } \bar x = \frac{1}{n}\sum_{i = 1}^{n}x_i, \text{ so},\ n \bar x =\sum_{i = 1}^{n}x+i) \\
&= \sum_{i = 1}^{n}x_i^2 - 2n \bar x ^2 + n \bar x \\
&=\sum_{i = 1}^{n} (x_i^2) - n \bar x^2
\end{align}
$$
Therefore we can calculate variance as
$$
Var(x) = \frac{1}{n-1}(\sum_{i = 1}^{n}(x_i^2) - n \bar x^2)
$$
