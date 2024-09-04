A Deployment provides declarative updates for Pods and ReplicaSets.

You describe your desired state in a Deployment, and the Deployment Controller's job is to make the current state match the desired state.

![[Pasted image 20240619211425.png]]

### Replica sets

A ReplicaSet maintains a set of replica Pods running at any given time. It's the thing that makes sure that the number of Pods you want running is the same as the number of Pods that are actually running.

BUT, isn't that what a deployment does? Yes, but:

A Deployment is a higher-level abstraction that manages ReplicaSets for you. You can think of a Deployment as a wrapper around a ReplicaSet.

You will never use ReplicaSets directly.

To see the ReplicaSets running in the cluster

```
kubectl get replicasets
```
