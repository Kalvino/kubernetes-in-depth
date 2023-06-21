# What is Helm?

Helm is a package manager for Kubernetes (like apt, yum) - packaging YAML files and distribute them in public/private repositories 

# Helm Charts
Are bundles of private/public YAML Files (in Helm repos) -eg
  - Database Apps
  - Monitoring Apps

# Usage
- sharing of Helm Charts
- Templating engine eg:
- deploy same applications across different environmments (dev, staging, prod)
- release management (tracking chart executions the Helm client sent to server (Tiller) for future reference)

/* Tiller has too much power (create/update/delete) creating security issues  Tiller was removed in Helm 3 and replaced with helm binary*/


# Helm Chart Structure

mychart/          #top level folder
  Chart.yaml      #info about chart(name, dep, versio)
  values.yaml # default values for template files
  charts/ # chart dependencies
  templates/ #actual template files

  helm install <chartname>
  helm install <chartname>
  helm rollback <chartname>
