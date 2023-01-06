## Passive
### Low Pass
Series RC  
$\text{When } X_C = \frac{1}{2 \pi f_c C} = R$  
$\text{Cutoff Frequency (3dB point)} \quad f_c = \frac{1}{2 \pi RC}$
### High Pass
Parallel RC  
$\text{When } X_C = \frac{1}{2 \pi f_c C} = R$  
$\text{Cutoff Frequency (3dB point)} \quad f_c = \frac{1}{2 \pi RC}$

### Band Pass & Reject
$\begin{array}{l l}
\text{Resonant Frequency } f_o & \frac{1}{2 \pi \sqrt{LC}} \\ \\
\text{Quality Factor:} &  \\ 
Q_{series} & \frac{2 \pi f_o L}{R} \ or \ \frac{1}{2 \pi f_o R C} \\ \\
Q_{parallel} & \frac{R}{2 \pi f_o L} \ or \ 2\pi f_o R C \\ \\
\text{Bandwidth } BW & \frac{f_o}{Q}  \\  \\ 
\text{Half-power frequencies for } Q\lt 10: f_1, f_2 & f_o \sqrt{1 + (\frac{1}{2Q})^2 } \pm \frac{f_o}{2Q}  \\ \\
\text{Half-power frequencies for } Q\ge 10: f_1, f_2 & f_o \pm \frac{BW}{2} \\
\end{array}$

## Active
### Low Pass & High Pass Sallen Key
$\text{Cutoff frequency } f_c = \frac{1}{2 \pi \sqrt{R_1 R_2 C_1 C_2}}$

### Band Pass & Reject (Combo)
$\begin{array}{l l}
F_H \ or \ F_L & F_c  \\ \\
\text{Center Frequency } f_o & \sqrt{F_H F_L}  \\ \\
\text{Bandwidth } BW & F_H - F_L  \\ \\
\text{Quality Factor } Q & \frac{f_o}{BW} \\ \\
\end{array}$
