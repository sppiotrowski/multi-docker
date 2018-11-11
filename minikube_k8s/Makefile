install:
	# install VirtualBox first!
	brew install kubectl
	brew cask install minikube
	kubectl apply -f client-node-port.yml 
	kubectl apply -f client-pod.yml 
start:
	minikube start
status:
	minikube status && \
	minikube ip && \
	kubectl cluster-info
stop:
	minikube stop

