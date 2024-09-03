# Summing Amplifier

![[Pasted image 20240829170439.png]]

> A summing amplifier is an op amp circuit that combines several inputs and produces an output that is the weighted sum of the inputs.

The above is a variation of the inverting amplifier. It takes advantage of the fact that the inverting configuration can handle many inputs at the same time.

The summing amplifier is just an inverting amplifier but the many inputs are all connected in parallel. And each input voltage is in series with a resistor.

$$ v_o = - (\frac{R_f}{R_1}v_1 + \frac{R_f}{R_2}v_2 + \frac{R_f}{R_3}v_3) $$
This indicates that the output voltage is a weighted sum of the inputs. For this reason, the circuit is called a summer. Note that it can have more than 3 inputs.

# Difference amplifier

![[Pasted image 20240829171416.png]]

> A difference amplifier is a device that amplifies the difference between **two inputs** but rejects any signals common to the inputs.


$$ v_o = \frac{R_2}{R_1}(v_2 - v_1) $$
If $R_2 = R_1$ and $R_3 = R_4$, the difference amplifier becomes a subtractor
$$ v_o = v_2 - v_1 $$
