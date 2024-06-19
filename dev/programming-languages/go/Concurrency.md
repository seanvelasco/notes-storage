

### Atomicity

Atomicity is important because if something is atomic, it is implicitly safe within concurrent contexts. This allows us to compose logically correct programs. 

We can force atomicity by employing several techniques. The art then becomes which areas of the code need to be atomic, and at what level of granularity.

### Memory access synchronization

Deadlocks, livelocks, and starvation - these issues all concern ensuring the program has something useful to do at all times. If not handled properly, the program could enter a state in which it will stop functioning altogether.

#### Deadlock

A deadlocked program is one which all concurrent processes are waiting on one another. In this state, the program will never recover without outside intervention.

The Go runtime attempts to detect some deadlocks - all goroutines must be blocked, or asleep - but this does not help us prevent deadlocks.


### Coffman Conditions

These are the basis for techniques to help detect, prevent, and correct deadlocks.

**Mutual exclusion**
A concurrent process holds exclusive rights to a resource at any one time.

Wait For Condition
A concurrent process must simultaneously hold a resource and be waiting for an additional resource.

No Preempting
A resource held by a concurrent process can only be released by that process, so it fulfills this condition.

Circular Wait
A concurrent process (P1) must be waiting on a chain of other concurrent processes (P2), which are in turn waiting on it (P1), so it fulfills this final condition too.