# eks-cluster-auto

```
[root@ip-10-176-17-50 cluster-auto-scaler]# kubectl logs -l app=cluster-autoscaler -n kube-system -f
I0708 08:02:21.088107       1 flags.go:52] FLAG: --skip-nodes-with-system-pods="false"
I0708 08:02:21.088112       1 flags.go:52] FLAG: --stderrthreshold="0"
I0708 08:02:21.088116       1 flags.go:52] FLAG: --unremovable-node-recheck-timeout="5m0s"
I0708 08:02:21.088121       1 flags.go:52] FLAG: --v="4"
I0708 08:02:21.088126       1 flags.go:52] FLAG: --vmodule=""
I0708 08:02:21.088131       1 flags.go:52] FLAG: --write-status-configmap="true"
I0708 08:02:21.088143       1 main.go:379] Cluster Autoscaler 1.20.0
I0708 08:02:21.184652       1 leaderelection.go:243] attempting to acquire leader lease kube-system/cluster-autoscaler...
I0708 08:02:21.196241       1 leaderelection.go:346] lock is held by cluster-autoscaler-75f86f8d74-hwrmr and has not yet expired
I0708 08:02:21.196268       1 leaderelection.go:248] failed to acquire lease kube-system/cluster-autoscaler
I0708 08:02:24.653363       1 leaderelection.go:346] lock is held by cluster-autoscaler-75f86f8d74-hwrmr and has not yet expired
I0708 08:02:24.653384       1 leaderelection.go:248] failed to acquire lease kube-system/cluster-autoscaler
I0708 08:02:28.917362       1 leaderelection.go:346] lock is held by cluster-autoscaler-75f86f8d74-hwrmr and has not yet expired
I0708 08:02:28.917383       1 leaderelection.go:248] failed to acquire lease kube-system/cluster-autoscaler
I0708 08:02:32.523848       1 leaderelection.go:346] lock is held by cluster-autoscaler-75f86f8d74-hwrmr and has not yet expired
I0708 08:02:32.523867       1 leaderelection.go:248] failed to acquire lease kube-system/cluster-autoscaler
I0708 08:02:35.587689       1 leaderelection.go:346] lock is held by cluster-autoscaler-75f86f8d74-hwrmr and has not yet expired
I0708 08:02:35.587708       1 leaderelection.go:248] failed to acquire lease kube-system/cluster-autoscaler
I0708 08:02:38.631571       1 leaderelection.go:253] successfully acquired lease kube-system/cluster-autoscaler
I0708 08:02:38.631677       1 event_sink_logging_wrapper.go:48] Event(v1.ObjectReference{Kind:"Lease", Namespace:"kube-system", Name:"cluster-autoscaler", UID:"15e798fe-ba6b-4635-9b1b-e7dc29a44657", APIVersion:"coordination.k8s.io/v1", ResourceVersion:"3850", FieldPath:""}): type: 'Normal' reason: 'LeaderElection' cluster-autoscaler-75f86f8d74-rzkr7 became leader
I0708 08:02:38.634411       1 reflector.go:219] Starting reflector *v1.Pod (1h0m0s) from k8s.io/autoscaler/cluster-autoscaler/utils/kubernetes/listers.go:188
I0708 08:02:38.634434       1 reflector.go:255] Listing and watching *v1.Pod from k8s.io/autoscaler/cluster-autoscaler/utils/kubernetes/listers.go:188
I0708 08:02:38.634632       1 reflector.go:219] Starting reflector *v1.DaemonSet (1h0m0s) from k8s.io/autoscaler/cluster-autoscaler/utils/kubernetes/listers.go:320
I0708 08:02:38.634640       1 reflector.go:255] Listing and watching *v1.DaemonSet from k8s.io/autoscaler/cluster-autoscaler/utils/kubernetes/listers.go:320
I0708 08:02:38.634840       1 reflector.go:219] Starting reflector *v1.Pod (1h0m0s) from k8s.io/autoscaler/cluster-autoscaler/utils/kubernetes/listers.go:212
I0708 08:02:38.634848       1 reflector.go:255] Listing and watching *v1.Pod from k8s.io/autoscaler/cluster-autoscaler/utils/kubernetes/listers.go:212
I0708 08:02:38.634918       1 reflector.go:219] Starting reflector *v1.ReplicationController (1h0m0s) from k8s.io/autoscaler/cluster-autoscaler/utils/kubernetes/listers.go:329
I0708 08:02:38.634926       1 reflector.go:255] Listing and watching *v1.ReplicationController from k8s.io/autoscaler/cluster-autoscaler/utils/kubernetes/listers.go:329
I0708 08:02:38.635024       1 reflector.go:219] Starting reflector *v1.Job (1h0m0s) from k8s.io/autoscaler/cluster-autoscaler/utils/kubernetes/listers.go:338
I0708 08:02:38.635031       1 reflector.go:255] Listing and watching *v1.Job from k8s.io/autoscaler/cluster-autoscaler/utils/kubernetes/listers.go:338
I0708 08:02:38.635095       1 reflector.go:219] Starting reflector *v1.Node (1h0m0s) from k8s.io/autoscaler/cluster-autoscaler/utils/kubernetes/listers.go:246
I0708 08:02:38.635102       1 reflector.go:255] Listing and watching *v1.Node from k8s.io/autoscaler/cluster-autoscaler/utils/kubernetes/listers.go:246
I0708 08:02:38.635170       1 reflector.go:219] Starting reflector *v1.ReplicaSet (1h0m0s) from k8s.io/autoscaler/cluster-autoscaler/utils/kubernetes/listers.go:347
I0708 08:02:38.635177       1 reflector.go:255] Listing and watching *v1.ReplicaSet from k8s.io/autoscaler/cluster-autoscaler/utils/kubernetes/listers.go:347
I0708 08:02:38.635260       1 reflector.go:219] Starting reflector *v1.StatefulSet (1h0m0s) from k8s.io/autoscaler/cluster-autoscaler/utils/kubernetes/listers.go:356
I0708 08:02:38.635267       1 reflector.go:255] Listing and watching *v1.StatefulSet from k8s.io/autoscaler/cluster-autoscaler/utils/kubernetes/listers.go:356
I0708 08:02:38.635337       1 reflector.go:219] Starting reflector *v1.Node (1h0m0s) from k8s.io/autoscaler/cluster-autoscaler/utils/kubernetes/listers.go:246
I0708 08:02:38.635346       1 reflector.go:255] Listing and watching *v1.Node from k8s.io/autoscaler/cluster-autoscaler/utils/kubernetes/listers.go:246
I0708 08:02:38.635403       1 reflector.go:219] Starting reflector *v1beta1.PodDisruptionBudget (1h0m0s) from k8s.io/autoscaler/cluster-autoscaler/utils/kubernetes/listers.go:309
I0708 08:02:38.635456       1 reflector.go:255] Listing and watching *v1beta1.PodDisruptionBudget from k8s.io/autoscaler/cluster-autoscaler/utils/kubernetes/listers.go:309
I0708 08:02:38.986747       1 cloud_provider_builder.go:29] Building aws cloud provider.
I0708 08:02:38.986800       1 aws_util.go:76] fetching https://pricing.us-east-1.amazonaws.com/offers/v1.0/aws/AmazonEC2/current/eu-central-1/index.json
I0708 08:02:38.988703       1 reflector.go:219] Starting reflector *v1.Pod (0s) from k8s.io/client-go/informers/factory.go:134
I0708 08:02:38.988720       1 reflector.go:255] Listing and watching *v1.Pod from k8s.io/client-go/informers/factory.go:134
I0708 08:02:38.989143       1 reflector.go:219] Starting reflector *v1.ReplicationController (0s) from k8s.io/client-go/informers/factory.go:134
I0708 08:02:38.989158       1 reflector.go:255] Listing and watching *v1.ReplicationController from k8s.io/client-go/informers/factory.go:134
I0708 08:02:38.989455       1 reflector.go:219] Starting reflector *v1.ReplicaSet (0s) from k8s.io/client-go/informers/factory.go:134
I0708 08:02:38.989463       1 reflector.go:255] Listing and watching *v1.ReplicaSet from k8s.io/client-go/informers/factory.go:134
I0708 08:02:38.989807       1 reflector.go:219] Starting reflector *v1beta1.PodDisruptionBudget (0s) from k8s.io/client-go/informers/factory.go:134
I0708 08:02:38.989816       1 reflector.go:255] Listing and watching *v1beta1.PodDisruptionBudget from k8s.io/client-go/informers/factory.go:134
I0708 08:02:38.990156       1 reflector.go:219] Starting reflector *v1.PersistentVolumeClaim (0s) from k8s.io/client-go/informers/factory.go:134
I0708 08:02:38.990164       1 reflector.go:255] Listing and watching *v1.PersistentVolumeClaim from k8s.io/client-go/informers/factory.go:134
I0708 08:02:38.990472       1 reflector.go:219] Starting reflector *v1.StorageClass (0s) from k8s.io/client-go/informers/factory.go:134
I0708 08:02:38.990480       1 reflector.go:255] Listing and watching *v1.StorageClass from k8s.io/client-go/informers/factory.go:134
I0708 08:02:38.990900       1 reflector.go:219] Starting reflector *v1.Node (0s) from k8s.io/client-go/informers/factory.go:134
I0708 08:02:38.990908       1 reflector.go:255] Listing and watching *v1.Node from k8s.io/client-go/informers/factory.go:134
I0708 08:02:38.991201       1 reflector.go:219] Starting reflector *v1.Service (0s) from k8s.io/client-go/informers/factory.go:134
I0708 08:02:38.991210       1 reflector.go:255] Listing and watching *v1.Service from k8s.io/client-go/informers/factory.go:134
I0708 08:02:38.991373       1 reflector.go:219] Starting reflector *v1.StatefulSet (0s) from k8s.io/client-go/informers/factory.go:134
I0708 08:02:38.991380       1 reflector.go:255] Listing and watching *v1.StatefulSet from k8s.io/client-go/informers/factory.go:134
I0708 08:02:38.991703       1 reflector.go:219] Starting reflector *v1.PersistentVolume (0s) from k8s.io/client-go/informers/factory.go:134
I0708 08:02:38.991767       1 reflector.go:255] Listing and watching *v1.PersistentVolume from k8s.io/client-go/informers/factory.go:134
I0708 08:02:38.991946       1 reflector.go:219] Starting reflector *v1.CSINode (0s) from k8s.io/client-go/informers/factory.go:134
I0708 08:02:38.991953       1 reflector.go:255] Listing and watching *v1.CSINode from k8s.io/client-go/informers/factory.go:134
I0708 08:02:39.084471       1 request.go:591] Throttling request took 93.180061ms, request: GET:https://172.20.0.1:443/api/v1/services?limit=500&resourceVersion=0
I0708 08:02:39.488645       1 request.go:591] Throttling request took 496.662178ms, request: GET:https://172.20.0.1:443/api/v1/persistentvolumes?limit=500&resourceVersion=0

```
