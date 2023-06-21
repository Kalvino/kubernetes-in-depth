# Using Multi-Node Clusters
It is recommended to run this tutorial on a cluster with at least two nodes

start a multi-node clusters on minikube and deploy a service to it: 

`minikube start --nodes 2 -p minikube`

- NOTE you may have to delete all cluster profiles
`minikube delete --all`

## get the list of your nodes
`kubectl get nodes`

## check the status of your nodes
`minikube status -p minikube`


https://minikube.sigs.k8s.io/docs/tutorials/multi_node/
# Enable Ingress controller
`minikube addons enable ingress`

OR with a different profile

`minikube addons enable ingress -p profile-name`

# Create an Ingress
`kubectl apply -f dashboard-ingress.yaml`

# Get status of cluster (profile )
`minikube status -p profile-name`

<!-- TODO --> reinstall minikube to continue with the dashboard-ingress tutorial