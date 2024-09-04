
*idea - if the folder and the markdown file are of the same name. the markdown file should appear as the index page*

![[Pasted image 20240829015206.png]]

The input voltage $v_i$ is applied directly at the non-inverting input terminal, and resistor $R_1$ is connected between the ground and the inverting terminal.

**Derivation of the formula for $v_o$

Apply KCL at the inverting terminals
$$ i_1 = i_2 => \frac{0-v_1}{R_1} = \frac{v_1-v_o}{R_f} $$
But $v_1 = v_2 = v_i$
$$ \frac{-v_i}{R_1} = \frac{v_i-v_o}{R_f} $$
$$ v_o = (1 +\frac{R_f}{R_1})v_i $$
or 
$$ v_o = v_i +\frac{R_f}{R_1}v_i $$
The voltage gain is 

$$ A_v = \frac{v_o}{v_i} = 1 + \frac{R_f}{R_1} $$
Again, we notice that the gain depends only on the external resistors.

### Voltage follower

![[Pasted image 20240829173331.png]]

If $R_f = 0$ (short circuit) or $R_1 = \infty$ (open circuit) or both, the gain becomes 1.

Under these conditions ($R_f = 0$ and $R_1 = \infty$), the circuit becomes a voltage follower (or unity gain amplifier) because the output follows the input.

$$ v_0 = v_i $$

Such a circuit has very high input impedance and is therefore useful for intermediate-stage (or buffer) amplifier to isolate one circuit from another. The voltage follower minimizes interaction between the two stages and eliminates interstage loading.