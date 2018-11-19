kubectl get deployments
kubectl delete deployment client-deployment
kubectl get services
kubectl delete service client-node-port
kubectl apply -f k8s/  # use file or directory

# PVC => Persistent Volume Claim
# Volume => mechanism that allows container to access a filesystem outside itself
# K8s Volume => An object type that allows a container to store data at the pod level
# K8s Types:
# - Volume: destroyed together with a Pod!
# - Persistent Volume: outside the Pod
# - Persistent Volume Claim:
#   - statically provisioned persistent volume
#   - dynamically provisioned persistent volume
# Access Mode:
# - ReadWriteOnce -> can be used by a single node
# - ReadOnlyMany -> can be read by multiple nodes
# - ReadWriteMany -> can be read and write by multiple nodes
