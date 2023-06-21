# KUBERNETES - REFRESHER SHEET

## container - is a runnable instance of an image
 - is a lightweight, standalone, executable package of software that includes everything needed to run an application: code, runtime, system tools, system libraries and settings.

## Pods
 - the lowest level object in K8s
 - can contain one or more containers
 - applications can be spread out amogst multiple pods or across 
 VM -architect your application acoirding your needs

NB:K8s layers (worker/master)

## Worker/Node
 - contains one or more pods - number depends on the resources/size of the worker
 - resposible for running containerised applications
 - amount of worker nodes depends o the resources needed to run the application

## Master
 - is the brain of the kubernetes
 - it is packed with services required for the functioning of the cluster. Carries all the components required for deploying applications to the workers themselves:

  ### API Server
  - central communication hub
  - provides REST based services for the components to talk to one another, user actions when deploying applications.
  - provides the front-end for cluster by exposing the K8s API (for both internal (Scheduler/nodes) and external (kubectl/API driven systems) components).

  ### Controller Manager
  - service that watches the shared state of the cluster through the API Server and makes changes attempting to move the current state towards a desired state. Runs all the reconciliation state machine services. 

  ### Scheduler
  - watches the new pods as they are requested and created

  ### etcd
  - database. Saves the current state of the cluster.
  - replicates changes across the master nodes (multiple master for scaled - front-ended with load-balancers) 

## Cluster
- K8s masters and workers

