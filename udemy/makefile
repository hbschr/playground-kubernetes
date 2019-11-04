info:
	kubectl get pods
	kubectl get replicationcontroller
	kubectl get replicaset
	kubectl get deployments
	kubectl get services
	kubectl get namespaces

rollout-status:
	kubectl rollout status deployment/myapp-deployment

rollout-history:
	kubectl rollout history deployment/myapp-deployment

create-pod:
	kubectl create -f pod-definition.yml

create-rc:
	kubectl create -f rc-definition.yml

create-replicaset:
	kubectl create -f replicaset-definition.yml

create-deployment:
	kubectl create -f deployment-definition.yml

create-service:
	kubectl create -f service-definition.yml

create-namespace:
	kubectl create -f namespace-definition.yaml

clean-pod:
	kubectl delete pod myapp-pod

clean-rc:
	kubectl delete replicationcontroller myapp-rc

clean-replicaset:
	kubectl delete replicaset myapp-replicaset

clean-deployment:
	kubectl delete deployment myapp-deployment

clean-service:
	kubectl delete service myapp-service

clean-namespace:
	kubectl delete namespace udemy-dev
