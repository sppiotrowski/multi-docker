# Kubernetes: system to deploy Docker containers
# - did not build images
# - support imperative and declarative approach
# Nodes: machines/vm's that run containers
# Masters: machines/vm's that manages Nodes

# Pod: runs a set of related containers (limitated, rarely used in prod)
# Deployment: maintains a set of identical pods (good for dev & prod)

kubectl apply -f client-node-port.yml
kubectl get services

# kubectl apply -f <conf.yml>
kubectl apply -f client-pod.yml 
kubectl get pods
# kubectl describe pod <conf.yml => metadata.name>
kubectl describe pod client-pod
kubectl delete -f client-pod.yml 

kubectl apply -f client-deployment.yml 
kubectl get deployments
kubectl get pods  # auto created from template

open http://$(minikube ip):31515

kubectl get pods -o wide  # with internal ip
