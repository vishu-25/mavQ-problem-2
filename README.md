# mavQ Devops Internship Practical Assignment 

## Problem 2

### Objective

Write a helm chart that deploys your application which utilizes the following Kubernetes objects :
 - Deployments
 - Service
 - k8s secrets

### Specification 

- The credentials of the database should be stored in a Kubernetes secret and should be
exported to deployment as environment variables
- Database should be a stateful-set, (Can use bitnami’s chart as sub chart)
- Deployment should have min two replicas
- Connection between database and application should be via kube dns

### Deliverables

A zip file containing:
- The helm charts of your components
- Document explaining your work

