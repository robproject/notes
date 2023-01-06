$\begin{array}{l l l}
\textbf{Operation} & \bold{f(t)} & \bold{F(s)} \\ \\
\text{Multiplication by a constant} & Kf(t) & KF(s) \\ \\
\text{Addition/subtraction} & f_1(t) + f_2(t) - f_3(t) + ... & F_1(s) + F_2(s) - F_3(s) + ... \\ \\
\text{First derivative (time)} & \displaystyle\frac{df(t)}{dt} & sF(s) - f(0^-) \\ \\
\text{Second derivative (time)} & \displaystyle\frac{d^2f(t)}{dt^2} & s^2F(s) - sf(0^-) - \frac{df(0^-)}{dt} \\ \\
n\text{th derivative (time)} & \displaystyle\frac{d^nf(t)}{dt^n} & s^nF(s) - s^{n-1}f(0^-)-s^{n-2}\frac{df(0^-)}{dt} - s^{n-3}\frac{df^2(0^-)}{dt^2} - ... - \frac{d^{n-1}f(0^-)}{dt^{n-1}} \\ \\
\text{Time integral} & \displaystyle\int_0^t f(x) dx & \frac{F(s)}{s} \\ \\
\text{Translation in time} & f(t-a)u(t-a), a \gt 0 & e^{-as}F(s) \\ \\
\text{Translation in frequency} & e^{-at}f(t) & F(s+a) \\ \\
\text{Scale changing} & f(at), a \gt 0 & \frac{1}{a}F(\frac{s}{a}) \\ \\
\text{First derivative (s)} & tf(t) & -\frac{dF(s)}{ds} \\ \\
n\text{th derivative (s)} & t^nf(t) & (-1)^n \displaystyle\frac{d^nF(s)}{ds^n} \\ \\
s\text{ integral} & \frac{f(t)}{t} & \displaystyle\int_s^\infty F(u) du \\ \\
\end{array}$



$F(\omega) = \mathscr{F}\{f(t)\} = \displaystyle\int^\infty_{-\infty} f(t)e^{-j\omega t}dt$

![](https://drive.google.com/uc?export=view&id=12nUtjy8as15CGE4jU4yy9uCVXWb8rUTV)

### Inverse
$f(t) = \mathscr{F}^{-1}\{F(\omega)\} = \frac{1}{2\pi} \displaystyle\int^\infty_{-\infty} F(\omega)e^{j\omega t}dt$