---
id: pws0082b391as5fin3qih16
title: Series
desc: ''
updated: 1670966515981
created: 1651011253390
---

$\omega_0 = 2\pi  f_0 = \frac{2\pi}{T_0}$

$f(t) = a_v + \displaystyle\sum_{n=1}^\infin a_n \ \cos\ n\omega_0t + b_n \ sin \  n\omega_0 t$
## Fourier Coefficients
$a_v = \frac{1}{T} \displaystyle\int_{t_0}^{t_0+T}f(t)dt$  

$a_k = \frac{2}{T}\displaystyle\int_{t_0}^{t_0+T}f(t) \cos \ k\omega_0t \ dt$  

$b_k = \frac{2}{T}\displaystyle\int_{t_0}^{t_0+T}f(t)sin \ k\omega_0t \ dt$  
### Even
Even = cosine  
 $f(x) = f(-x)$  

$a_v = \frac{2}{T} \displaystyle\int_0^{\frac{T}{2}}f(t)dt$   

$a_k = \frac{4}{T} \displaystyle\int_0^{\frac{T}{2}}f(t) \cos \ k\omega_0t \ dt$  

$b_k = 0$

### Odd
Odd = Sine   
$f(x) = -f(-x)$  

$a_v = \frac{2}{T} \displaystyle\int_0^{\frac{T}{2}}f(t)dt$   

$a_k = 0$  

$b_k = \frac{4}{T} \displaystyle\int_0^{\frac{T}{2}}f(t)sin \ k\omega_0t \ dt$  
  

### Half-Wave
Half-Wave = $f(x) = -f(x\pm\frac{T}{2})$  

$a_v = 0$  

$a_k = \begin{cases}
 0 \qquad \qquad \qquad \qquad \quad \text{ for k even } \\ 
\frac{4}{T} \displaystyle\int_0^{\frac{T}{2}}f(t) \cos \ k\omega_0t \ dt \quad \text{ for k odd}
\end{cases}$  

$b_k = \begin{cases}
 0 \qquad \qquad \qquad \qquad \quad \text{ for k even } \\ 
\frac{4}{T} \displaystyle\int_0^{\frac{T}{2}}f(t)sin \ k\omega_0t \ dt \quad \text{ for k odd}
\end{cases}$  

### Quarter-Wave Even
Quarter-wave = (Even || Odd) && Half-Wave  (parent rule inherited)  
$a_v = 0 \text{ (half-wave)}$ 

$a_k = \begin{cases}
0 \qquad \qquad \qquad \qquad \quad \text{ for k even (half-wave)} \\
\frac{8}{T} \displaystyle\int_0^{\frac{T}{4}} f(t) \ \cos \ k\omega_0t \ dt  \quad \text{ for k odd}
\end{cases}$  

$b_k = 0 \text{ (even)}$

### Quarter-Wave Odd
Quarter-wave = (Even || Odd) && Half-Wave  (parent rule inherited)  
$a_v = 0 \text{ (half-wave)}$  
$a_k = 0 \text{ (odd)}$  

$b_k = \begin{cases}
0 \qquad \qquad \qquad \qquad \quad \text{ for k even (half-wave)}  \\
 \frac{8}{T} \displaystyle\int_0^{\frac{T}{4}} f(t) \ sin \ k\omega_0t \ dt \quad \text{ for k odd}
 \end{cases}$    

### Alternative Trigonometric Form
$f(t) = a_v + \displaystyle\sum_{n=1}^\infin A_n  \ \cos(n\omega_0t-\theta_n)$  

$a_n - jb_n = \sqrt{a_n^2+b_n^2} \ \angle{-\theta_n}= A_n \angle{-\theta_n}$  
  
$\theta_n = -tan^{-1}(\frac{b_n}{a_n})$   

$A_n, \theta_n = \begin{cases} 
a_n, 0 \qquad \text{for even } f(t) \\
b_n, 90 \qquad \text{for odd } f(t) \\
\end{cases}$

### Exponential Form
$f(t) = \displaystyle\sum_{n=-\infin}^\infin C_n e^{jn\omega_0t}$

$C_n = \frac{1}{T} \displaystyle\int_{t_0}^{t_0 + T} f(t) e^{-jn\omega_0 t}dt$  
  
$C_n = \frac{1}{2} (a_n - jb_n) = \frac{A_n}{2}\angle{-\theta_n}, \  n = 1, 2, 3, ...$  

$C_0 = \frac{1}{T} \displaystyle\int_{t_0}^{t_0+T}f(t)dt$  
