An operational amplifier is designed so that it performs some mathematical operations when external components, such as resistors and capacitors, are connected to its terminals.

> An op amp is an active circuit element designed to perform mathematical operations of addition, subtraction, multiplication, division, differentiation, and integration.

![[Pasted image 20240828142402.png]]

The inputs are marked with minus (-) and plus (+) to specify inverting and non-inverting, respectively.

An input applied to the non-inverting terminal will appear with the same polarity at the output. An input applied to the inverting terminal will appear inverted at the output.

As an active element, the op amp must be powered by a voltage supply. Although the power supplies are often ignored in op amp circuit diagrams, the power supply currents must not be overlooked. By KCL,

$$ i_o = i_1 + i_2 + i_+ + i_\_ $$
The output section consists of a voltage-controlled source in series wit the output resistance $R_o$.

The input resistance $R_i$ is the Thevenin equivalent resistance seen at the input terminals. The output resistance $R_o$ is the Thevenin equivalent resistance seen at the output. The differential input voltage $v_d$ is given by

$$ v_d = v_2 - v_1 $$
where $v_1$ is the voltage between the inverting terminal and ground and $v_2$ is the voltage between the non-inverting terminal and ground. The op amp senses the difference between the two inputs, multiplies it by the gain $A$, and cause the resulting voltage to appear at the output. Thus, the output $v_o$ is given by

$$ v_o = Av_d = A(v_2 - v1) $$
$A$ is called the open loop voltage gain because it is the gain of the op amp without any external feedback from the output to input.

**In simple terms - the op amp amplifies the difference in voltage between the non-inverting and inverting inputs.**

Sometimes, the voltage gain is expressed in decibels (dB).

The concept of feedback is crucial to our understanding of op amp circuits. A negative feedback is achieved when the output is fed back to the inverting terminal of the op amp. 

When there is a feedback path from the output to input, the ratio of the output voltage to the input voltage is called the closed-loop again. As a result of the negative feedback, it can be shown that the closed-loop gain is almost insensitive to the open-loop gain A of the op amp. For this reason, op amps are used in circuits with feedback paths.

A practical limitation of the op amp is that the magnitude of its output voltage cannot exceed $|V_{CC}|$. In other words, the output voltage is dependent on and is limited by the power supply voltage.

![[Pasted image 20240828150039.png]]

The op amp can operate in three modes, depending on the differential input voltage $v_d$ :
1. Positive saturation, $v_o = V{CC}$
2. Linear saturation, $-V{CC} \leq v_o = Av_d \leq V{CC}$
3. Negative saturation, $v_o = - V{CC}$

Note that $v_d$ cannot exceed $V_{CC}$. An attempt to increase $v_d$ beyond the linear range, the op amp becomes saturated and yields $v_o = V{CC}$ or $v_o = - V{CC}$.

Although we will always operate the op amp in the linear region. The possibility of saturation must be borne in mind when one designs with op amps. Keep in mind the voltage constraint on the op amp.

### Ideal Op Amp

An op amp is ideal if it has the following characteristics:

1. Infinite open-loop gain, $A = \infty$
2. Infinite input resistance, $R_i = \infty$
3. Zero output resistance, $R_{o} = 0$

> An ideal op amp is an amplifier with infinite open-loop gain, infinite input resistance, and zero output resistance.

Although assuming ideal op amp provides only an approximate analysis, most modern amplifiers have such large gains and input impedances that the approximate analysis is good.








