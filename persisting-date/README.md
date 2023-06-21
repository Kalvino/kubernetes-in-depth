# Persisting data

database, directory

# components of Kubernetes Storage
## Persistent Volume (PV) -  
  * needs actual physical storage(local,nfs, cloud)
  * 
## Persistent Volume Claim (PVC) - 
  * pod request the volume through PVC
  * PVC finds the volume in cluster that satisfies the claim
  * volume is mounted into the pod
  * volume is mounted into the container  * 

## Storage Class(SC)
  * provisions Persistent Volumes (PV) dynamically whenever PVC claims it
  * it's claimed by PVC like PV  


# Other
## ConfigMap/Secret
* local volumes
* not created via PV/PVC

NOTE: PV are not namespaced, they are accessible to the whole cluster

NOTE: PVC must be in the same namespace as the pod using the claim