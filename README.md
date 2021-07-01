# eks-cluster-auto

```
Events:
  Type     Reason            Age                    From                Message
  ----     ------            ----                   ----                -------
  Warning  FailedScheduling  4m58s (x2 over 4m58s)  default-scheduler   0/2 nodes are available: 1 Insufficient cpu, 1 node(s) didn't match Pod's node affinity.
  Normal   TriggeredScaleUp  4m50s                  cluster-autoscaler  pod triggered scale-up: [{eks-40bd16d2-ecbd-df8a-2040-7bb5b1508a43 2->3 (max: 5)}]
  Warning  FailedScheduling  103s (x5 over 3m54s)   default-scheduler   0/3 nodes are available: 1 Insufficient cpu, 1 node(s) didn't match Pod's node affinity, 1 node(s) had taint {node.kubernetes.io/not-ready: }, that the pod didn't tolerate.
  Warning  FailedScheduling  92s                    default-scheduler   0/3 nodes are available: 1 Insufficient cpu, 2 node(s) didn't match Pod's node affinity.
  Warning  FailedScheduling  35s (x2 over 46s)      default-scheduler   0/4 nodes are available: 1 Insufficient cpu, 1 node(s) had taint {node.kubernetes.io/not-ready: }, that the pod didn't tolerate, 2 node(s) didn't match Pod's node affinity.
```

```
ip-10-1-2-3.eu-central-1.compute.internal   Ready    <none>   10d     v1.20.4-eks-6b7464   app=node-group,beta.kubernetes.io/arch=amd64,beta.kubernetes.io/instance-type=t3.medium,beta.kubernetes.io/os=linux,eks.amazonaws.com/capacityType=ON_DEMAND,eks.amazonaws.com/nodegroup-image=ami-00e3430a783549791,eks.amazonaws.com/nodegroup=node-group,failure-domain.beta.kubernetes.io/region=eu-central-1,failure-domain.beta.kubernetes.io/zone=eu-central-1b,kubernetes.io/arch=amd64,kubernetes.io/hostname=ip-10-2-3-4,kubernetes.io/os=linux,node.kubernetes.io/instance-type=t3.medium,topology.kubernetes.io/region=eu-central-1,topology.kubernetes.io/zone=eu-central-1b

```
