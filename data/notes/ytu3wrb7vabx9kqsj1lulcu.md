Metal Oxide Semiconducter Field Effect Transistor
### Enhancement-Type
Gate voltage causes Source-Drain channel to close circuit

### Depletion-Type
Gate voltage causes Source-Drain channel to open circuit

### Doping
N-Channel = N-type Source, Drain, Channel with P-type substrate. Positive voltage is applied to the gate to operate.  
P-Channel = P-type Source, Drain, Channel with N-type substrate. Negative voltage is applied to the gate to operate.  

### Caluclations (NMOSFET-E)
saturation  
Triode = ohmic = linear  
cutoff   
$V_{GS} = V_G - R_SI_D$  
$V_S = R_SI_D$  
$R_D = \frac{V_{DD}-V_D}{I_D}$   
$I_{Dsat} = \frac{1}{2}k'_n\left(\frac{W}{L}\right)(V_{GS}-V_t)^2(1+\lambda*V_{DS}) \text{ for }V_{GS} \ge V_T \text{ and } V_{DS} \ge V_{GS}-V_T$  
$I_{Dlin} = k'_n\left(\frac{W}{L}\right)\left[(V_{GS}-V_t)V_{DS}-\frac{1}{2}V_{DS}^2\right] \text{ for }V_{GS} \ge V_T \text{ and } V_{DS} \le V_{GS}-V_T$  
$I_D = 0 \text{ for } V_{GS} \lt V_T$


### Constants
$\text{conduction parameter} = K_n = \frac{k'_n}{2}*\frac{W}{L}$   
$\text{process conduction parameter} = k'_n = \mu_nC_{Ox} = \text{electron mobility} * \text{oxide capacitance per unit area}$  
$\text{transistor design variable} = \frac{W}{L} = \frac{\text{Width}}{\text{Length}}$   
$\lambda$
