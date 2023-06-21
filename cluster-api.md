# CLUSTER API

- accepted tool by K8s community for building and deploying K8s clusters in an automated fashion - using K8s principles  - declarative API (scale upgrade, delete clusters)
- Cluster API is a set of CRD's that allows K8s to know how to interface with an infrastructure provider and it knows how an object of type machine or cluster is represented

## How it works
- a user defines a cluster specification which include:
  - type of machine making up the cluster
- use Kubectl commnad-line to apply the k8s cluster that has cluster API components installed
- Cluster API & Kubernetes cluster becomes the management cluster and isrespnsible for communicating to the infrastructure provider of choice and deploy K8s cluster base on the specs provided

- to make changes, edit the specification and apply to the management cluster