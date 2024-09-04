### Linearity

Linearity is the property of an element describing a linear relationship between cause and effect. The property is a combination of both the homogeneity (scaling) property an the additive property.

The homogeneity property requires that if the input (also called the excitation) is multiplied by a constant, then the output (also called the response) is multiplied by the same constant.

The additive property requires that the response to a sum of inputs is the sum of the responses to each input applied separately.

> A linear circuit is one whose output is linearly related (or directly proportional) to its input.
### Superposition

If a circuit has two or more independent sources, one way to determine the value of a specific variable (voltage or current) is to use nodal or mesh analysis. Another way is to determine the contribution of each independent source to the variable and then add them up. This approach is known as the superposition.

The idea of superposition rests on the linearity property. For this reason, it is not applicable to the effect on power due to each source, because the power absorbed by a resistor depends on the square of the voltage or current.

> The superposition principle states that the voltage across or current through an element in a linear circuit is the algebraic sum of the voltages across or currents though that element due to each independent source acting alone.

Ali Hajimiri:  

Remember:
1. We consider one independent source at a time while all other independent sources are turned off. This implies that we replace every voltage source by 0 V or a short circuit, and every current source by a 0 V or an open circuit.
2. Dependent sources are left intact because they are controlled by circuit variables.

Steps:
1. Turn of independent sources except one source. Find the output voltage or current due to that active source.
2. Repeat the previous step for each of the other independent sources.
3. Find the total contribution by adding algebraically all the contributions due to the independent sources.

Analyzing a circuit using superposition is more work.

----

v = v1 + v2

(1)

-6V +12i = 0
12i = 6
i = 1/2 A or 0.5 A

v1 = 4i = 2 V

(2)

(8 * 4) / 8 + 4 = 8 / 3 ohm

v2 = (8 / 3 ohm)(3)
v2 = 8 V


(ans)

v = 2V + 8V = 10V

---
### Source Transformation

Series-parallel combinations and wye-delta transformations help simplify circuits. Source transformation is another tool for simplifying circuits.

> Source transformation is the process of replacing a voltage source $V_s$ in series with a series $R$ by a current source $i_s$ in parallel with a resistor $R_i$, or vice versa.

### Thevenin's Theorem

> Thevenin's theorem states that a linear two-terminal circuit can be replaced by an equivalent circuit consisting of a voltage source $V_{TH}$ in series with a resister $R_{TH}$ where $V_{TH}$ is the open-circuit voltage at the terminals and $R_{TH}$ is the input or equivalent resistance at the terminals when the independent sources are turned off.

Two circuits are said to be equivalent if they have the same voltage-current relation at their terminals.

If he terminals a-b are made open-circuit (by removing load), no current flows, so that the open-circuit voltage across the terminals a-b must be equal to the voltage source $V_{Th}$. 

To find the Thevenin resistance $R_{Th}$, we need to consider two cases:
1. If the network has no dependent sources, we turn off all independent sources. $R_{Th}$ is the input resistance of the network looking between terminals a and b.
2. If the network has dependent sources, we turn off all independent sources. As with superposition, dependent sources are not to be turned off because they are controlled by circuit variables. We apply a voltage across source vo at terminals a and b and determine the resulting io. Then RTh = vo/lio. Alternatively, we may insert a current source io at terminals a-b and find the terminal voltage vo. Again, RTh = vo/lo. Both appraoches will give the same result.

It often occurs that $R_{Th}$ takes a negative value. In this case, the negative resistance implies that the circuit is supplying power. This is possible in a circuit with dependent sources.

Find the Thevenin resistance
$$ (4 \cdot 12) / (4 + 12) + 1 = R_{Th} $$
$$ 4\ohm = R_{Th} $$
Find the Thevenin voltage using Mesh Analysis

i2 = -2A

-32 + 4i1+ 12(i1 - i2) = 0
-32 + 4i1 + 12(i1 - (-2)) = 0
-32 + 4i +12i +24 = 0
16i = 8
i1 = 0.5 A

12(0.5A - (-2A)) = 30 V

Find the Thevenin voltage using Nodal Analysis



 
### Norton's Theorem

> Norton's theorem states that a linear two-terminal circuit can be replaced by an equivalent circuit consisting of a current source $I_N$ in parallel with a resistor $R_N$ where $I_N$ is the short-circuit current through the terminals and $R_N$ is the input or equivalent resistance at the terminals when the independent sources are turned off.

Thevenin and Norton resistances are equal.

$$ R_N = R_{Th} $$
$$ I_N=\frac{V_{Th}}{R_{Th}} $$
The above is essentially source transformation. For this reason, source transformation is often called Thevenin-Norton transformation.
### Maximum Power Transfer

In many practical applications, a circuit is designed to provide power to a load, such as communications where it is desirable to maximize the power delivered to a load.

We now address the problem of delivering the maximum power to a load when given a system with known internal losses. It should be noted that this will result in significant internal losses greater than or equal to the power delivered to the load.

The Thevenin equivalent is useful in finding the maximum power a linear circuit can deliver to a load. We assume we can adjust the load resistance $R_L$. If the entire circuit is replaced by its Thevenin equivalent except for the load, the power delivered is

> Maximum power is transferred to the load when the load resistance equals the Thevenin resistance as seen from the load ($R_L = R_{Th}$).

> Maximum power transfer occurs when the internal resistance of the source device is equal to the resistance of the load device.

- **If RLR_LRL​ is too small**: The current III will be large, but most of the voltage will drop across the internal resistance RsR_sRs​, leaving less voltage across the load. Thus, the power PLP_LPL​ delivered to the load will be low.
    
- **If RLR_LRL​ is too large**: The current III will be small because the total resistance in the circuit is high, resulting in low power delivered to the load.

This is also called impedance matching.