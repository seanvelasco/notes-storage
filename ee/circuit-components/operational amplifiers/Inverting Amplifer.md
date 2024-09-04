![[Pasted image 20240829012047.png]]

![[Pasted image 20240829013421.png]]

In this circuit,

the non-inverting input is grounded.

$v_i$ is connected to the inverting input through $R_1$

The feedback resistor $R_f$ is connected between the inverting input and output

> The key feature of the inverting amplifier is that both input signal and the feedback are applied at the inverting terminal of the op amp.

> In simple words, the output is fed back to the inverting input through a resistor. The input signal is applied to this pin through a resistor.

> An inverting amplifier reverses the polarity of the input signal while amplifying it.

The output is out of phase with the input. The gain of the circuit is determined by the ratio of the resistors used.

This is evident in the special case where R1 and R2 are equal. This configuration allows for the production of a signal that is complementary to the input, as the output is exactly the opposite of the input signal.

The gain is given by
$$ A_v = \frac{v_o}{v_i} = - \frac{R_f}{R_1} $$
The output voltage is given by
$$ v_o = - \frac{R_f}{R_1}v_i $$
Notice that the gain is the feedback resistance divided by the input resistance, which means that the gain depends only on the external elements connected to the op amp.


