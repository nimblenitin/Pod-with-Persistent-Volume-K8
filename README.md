# Pod-with-Persistent-Volume-K8
A PersistentVolume (PV) is a piece of storage in the cluster that can be provisioned. A PersistentVolumeClaim (PVC) is a request for storage by a user. Claims can request specific size and access modes (e.g., they can be mounted ReadWriteOnce, ReadOnlyMany or ReadWriteMany)

Simple example to demonstrate Persistent Volume in a Pod-

Steps followed:

*As Root*
```

1. Create the YAML file to create Persistent volume.
$ vi pv.yaml

2. Create the Persistent volume and check it out.
$ kubectl apply -f pv.yaml --record
$ kubectl get pv

3. Create the YAML file to create Persistent volume claim.
$ vi pvc.yaml

4. Create the Persistent volume and check it out.
$ kubectl apply -f pvc.yaml --record
$ kubectl get pvc

5. Create the YAML file to create the POD
$ vi pod_pvc.yaml

6. Create the Pod using Persistent Volume
$ kubectl apply -f pod_pvc.yaml --record

7. Describe the pod to see whether Persistent Volume is applied to the Pod
$ kubectl describe pod pod-using-pvc

```
*As Root*
