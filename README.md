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

## Solution 

### Dependencies
 - [Docker](https://docs.docker.com/)
 - [minikube](https://minikube.sigs.k8s.io/docs/start/)
 - [kubectl](https://kubernetes.io/docs/reference/kubectl/kubectl/)

[Docker image used](https://hub.docker.com/r/mmumshad/simple-webapp/)

### To run the Kubernetes deployment using Helm 

```
git clone https://github.com/vishu-25/mavQ-problem-2.git
cd mavQ-problem-2/
helm repo add bitnami https://charts.bitnami.com/bitnami
helm repo update
helm dependency update helm-app
helm install helm-app ./helm-app
```

### Stopping the Helm deployment

```
helm uninstall helm-app
```

#### To scale down the deployment replicas to zero, use the following ` kubectl ` command:

```
kubectl scale deployment helm-app --replicas=0
```
