# eks-cluster-auto

Events:
  Type     Reason            Age                    From                Message
  ----     ------            ----                   ----                -------
  Warning  FailedScheduling  4m58s (x2 over 4m58s)  default-scheduler   0/2 nodes are available: 1 Insufficient cpu, 1 node(s) didn't match Pod's node affinity.
  Normal   TriggeredScaleUp  4m50s                  cluster-autoscaler  pod triggered scale-up: [{eks-40bd16d2-ecbd-df8a-2040-7bb5b1508a43 2->3 (max: 5)}]
  Warning  FailedScheduling  103s (x5 over 3m54s)   default-scheduler   0/3 nodes are available: 1 Insufficient cpu, 1 node(s) didn't match Pod's node affinity, 1 node(s) had taint {node.kubernetes.io/not-ready: }, that the pod didn't tolerate.
  Warning  FailedScheduling  92s                    default-scheduler   0/3 nodes are available: 1 Insufficient cpu, 2 node(s) didn't match Pod's node affinity.
  Warning  FailedScheduling  35s (x2 over 46s)      default-scheduler   0/4 nodes are available: 1 Insufficient cpu, 1 node(s) had taint {node.kubernetes.io/not-ready: }, that the pod didn't tolerate, 2 node(s) didn't match Pod's node affinity.
