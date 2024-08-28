### Ohm's Laws

Materials in general have a characteristic behavior of resisting the flow of electric charge. This physical property, or ability to resist current, is known as resistance and is represented by the symbol R. The resistance of any material with a uniform cross-sectional area A depends on its length $l$. Mathematically,
$$ R = p \frac{l}{A} $$
where p is known as the resistivity of the material in ohm-meters. 

Ohm's law states that the voltage v across a resistor is directly proportional to the current i flowing through the resistor.

The constant of proportionality for a resistor is the resistance R. Thus,
$$ v = iR $$
which is the mathematical form of Ohm's law. $R$ is measured in the unit of ohms ($\ohm$).
##### Short circuit and open circuit

Since the value of R can range from 0 to infinity, it is important we consider the two extreme possible values of R.

An element with $R = 0$ is called a short circuit. For a short circuit,
$$ v = iR = 0 $$showing that the voltage is zero but the current could be anything.

In practice, a short circuit is usually a connecting wire assumed to be a perfect conductor. Thus,

**A short circuit is a circuit element with resistance approaching to zero.**

An element with $R = \infty$ is known as an open circuit.

For an open circuit,

$$ i = \lim_{R\rightarrow\infty} \frac{v}{R} = 0 $$

indicating that the current is zero, but the voltage could be anything

An open circuit is a circuit is a circuit element with resistance approaching infinity.

A useful quantity in circuit analysis is the reciprocal of resistance R, known as conductance denoted by G:

G = 1 / R = i / v

The conductance is a measure of how well an element will conduct electric current. The unit of conductance is the mho ($\mho$). The SI unit of conductance is the siemens (S).

1 S = 1 mho = 1 A/V

Conductance is the ability of an element to conduct electric current, measured in mhos or siemens.

### Nodes, Branches, and Loops

A network with b branches, n nodes, and l independent loops will satisfy the fundamental theorem of network topology:

$$ n = l + n - 1 $$
Circuit topology is of great importance to the study of voltages and currents in an electric circuit. 

- Two or more elements are in series if they exclusively share a single node and consequently carry the same current.
- Two or more elements are in parallel if they are connected to the same two nodes and consequently have the same voltage across them.

Elements are in series when they are chain-connected or connected sequentially, end to end. For example, two elements are in series if they share one common node and no other element is connected to that common node.

Elements are in parallel are connected to the same pair of terminals.

Elements may be connected in a way that are neither in series nor in parallel
### Kirchhoff’s Current Law (KCL)

> Kirchhoff’s current law (KCL) states that the algebraic sum of currents entering a node or a closed boundary is zero.

The sum of the currents entering a node is equal to the sum of the currents leaving the node.

Ali Hajimiri: the instantaneous current at one side of the component is the same on the other side of the component.
### Kirchhoff’s voltage law (KVL)

Kirchhoff’s second law is based on the principle of conservation of energy:

> Kirchhoff’s voltage law (KVL) states that the algebraic sum of all voltages around a closed path (or loop) is zero.

Ali Hajimiri: comes from the Faraday Law. If there is no magnetic flux, summation is zero - no changing magnetic flux
### Wye-Delta Transformation

$$ \int $$








### Passivity

