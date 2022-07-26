# argocd
##### Argo CD is a declarative, GitOps continuous delivery tool for Kubernetes.

## deploy the application using argocd on minikube

## prerequisite

```
kubectl create namespace argocd
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
```

## Commands to apply the script:

1. Push the code to the github

2. Start minikube

```
$ minikube start
```

3. Deploy the argocd on minikube from prerequisite

4. Access the argocd dashboard

```
$ kubectl port-forward <argocd-server-svc> 8088:443
```

5. Edit the repoURL in application.yaml

6. Apply application.yaml 

```
$ kubectl apply -f application.yaml 
```
7. Access the deployed application

```
<minikubeip:31412>
