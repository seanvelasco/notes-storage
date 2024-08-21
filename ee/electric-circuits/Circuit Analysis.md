
Nodal Analysis is a systematic application of KCL. Mesh analysis is a systemic application of KVL.

WE can analyze linear circuit by obtaining a set of simultaneous equations that are then solved to obtain the required values of current of voltage.

One method of solving simultaneous equations is Cramer's Rule.

### Nodal Analysis

Nodal analysis provides a general procedure for analyzing circuits using nodal voltages instead of element voltage as the circuit variables.

For simplicity, no circuit in this page will contain voltage sources. 

In nodal analysis, the interest lies in finding node voltages. 

Steps:

1. Select a node as the reference node. Assign voltages v1, v2, ..., n-1 to the remaining n -1 nodes. The voltages are references with respect to the reference node. This is typically called the ground node since it is assumed to have zero potential. 
2. Apply KCL to each of the n - 1 non-reference nodes. Use Ohm's law to express the branch currents in terms of node voltages.
3. Solve the resulting simultaneous equations to obtain the unknown node voltages

Currents entering the node are positive. Currents leaving the node are positive.

If we apply KCL to n - 1 non-reference nodes, we obtain  n -1 simultaneous equations.

Apply KCL to Node 1
$$ I_1 - I_2 - i_1 - i_2= 0 $$
$$ I_1 = I_2 + i_1 + i_2 $$
Apply KCL to Node 2
$$ I_2 + i_2 - i_3 = 0 $$
$$ I_2 + i_2 = i_3 $$
Use Ohm's law to express the unknown currents in terms of node voltages
$$ I_1 = I_2 + G_1v_1 + G_2(v_1-v_2) $$
$$ I_2 + G_2(v_1-v_2) = G_3v_2 $$
Solve the simultaneous equations using Algebra or Linear Algebra

### Nodal Analysis with Voltage Sources

Case 1:

If a voltage source is connected between the reference node and non-reference node, we set the voltage at the non-reference node equal to the voltage source. 

Case 2:

If the voltage source (dependent or independent) is connected between two non-reference nodes, the two non-reference nodes form a generalized node or a supernode. We apply both KCL and KVL to determmine the node votlages.

##### Supernode

> A **supernode** is formed by enclosing a (dependent or independent) voltage source connected between two non-reference nodes and any elements connected  in parallel with it.

The properties of a supernode:
1. The voltage source inside the supernode provides a constraint equation needed to solve for the node voltages
2. A supernode has no voltage of its own
3. A supernode requires the application of both KCL and KVL
### Mesh Analysis

A mesh is a loop that does not contain any other loop within it.

Nodal analysis applies KCL to find unknown voltages in a given circuit. Mesh analysis applies KVL to find unknown currents.

Mesh analysis is not quite as general as nodal analysis because it is only applicable to a circuit that is planar.

A planar circuit is one that can be drawn in a plane with no branches corssing one another; otherwise it is nonplanar. A circuit may have crossing branches and still be planar if it can be redrawn such that it has no crossing branches.

Non-planar circuits can be handled using nodal analysis (complicated).

1. Assign mesh currents i, i2, ...m in to the n meshes.
2. Apple KVL to each of the n meshes. Use Ohm's law to express the voltages in terms of the mesh currents.
3. Solve the resulting n simultaneous equations to get the mesh currents.
### Mesh Analysis with Current Sources

Case 1:

When a current source exists only in one mesh. Use this information for the other meshes.

Case 2:

When a current source exists between two meshes, we create a supermesh by ecluding the current source and any elements connected in series with it.

> A supermesh results when two meshes have a (dependent or independent) current source in common.

### Nodal and Mesh Analysis by Inspection

(watch ali hajimiri)


