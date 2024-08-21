### Linearity

Linearity is the property of an element describing a linear relationship between cause and effect. The property is a combination of both the homogeneity (scaling) property an the additive property.

The homogeneity property requires that if the input (also called the excitation) is multiplied by a constant, then the output (also called the response) is multiplied by the same constant.

The additive property requires that the response to a sum of inputs is the sum of the responses to each input applied separately.

> A linear circuit is one whose output is linearly related (or directly proportional) to its input.

### Superposition

If a circuit has two or more indepnedent sources, one way to determin the value of a specific variable (voltage or current) is to use nodal or mesh analysis. Another way is to determine the contribution of each independent source to the variable and then add them up. This approach is known as the superposition.

The idea of superposition rests on the linearity property.

The superposition principle states that the voltage across or current through an element in a linear circuit is the algebraic sum of the voltages across or currents though that element due to each independent source acting alone.

Remember:
1. We consider one independent source at a time while all other independent sources are turned off. This implies that we replace every voltage source by 0 V or a short circuit, and every current source by a 0 V or an open circuit.
2. Dependent sources are left intact because they are controlled by circuit variables.

Steps:
1. Turn of independent sources except one source. Find the output voltage or current due to that active source.
2. Repeat the previous step for each of the other independent sources.
3. Find the total contribution by adding algebraically all the contributions due to the independent sources.

Analyzing a circuit using superposition is more work.

