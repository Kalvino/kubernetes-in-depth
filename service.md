# SERVICES

provides:
- stable IP address
- load balancing - get request targeted to application/services and forwards it to one of the pods
- loose coupling
- communication withing & outside the cluster 

##  Types of Services

### ClusterIp Services
- default type
- abstraction layer that represents IP address
- has a port
- has a targetPort
- has a selector (key/value pair - app: microservice) that matches the labels of a particular kind (app: microservice). selectors must completely match the labels - the number of selectors === number of labels. 
- registers all the label matches (pods) as service endpoints