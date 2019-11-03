# missing:
# replicaset: autorestart crashed pods
# deployments: controlled updates

apps := postgres redis result-app vote-app worker-app
services := db redis result-app vote-app

create_pods := $(patsubst %, kubectl-create-pod-%.yaml, $(apps))
delete_pods := $(patsubst %, kubectl-delete-pod-%, $(apps))

create_deployments := $(patsubst %, kubectl-create-deployment-%.yaml, $(apps))
delete_deployments := $(patsubst %, kubectl-delete-deployment-%, $(apps))

create_services := $(patsubst %, kubectl-create-service-%.yaml, $(services))
delete_services := $(patsubst %, kubectl-delete-service-%, $(services))

all: create-all-deployments create-all-services

all-pods: create-all-pods create-all-services

clean: delete-all-deployments delete-all-services

clean-pods: delete-all-pods delete-all-services

test:
	curl localhost:30001
	curl localhost:30002

create-all-pods: $(create_pods)

delete-all-pods: $(delete_pods)

create-all-deployments: $(create_deployments)

delete-all-deployments: $(delete_deployments)

create-all-services: $(create_services)

delete-all-services: $(delete_services)

kubectl-create-%:
	kubectl create -f $*

kubectl-delete-pod-%:
	kubectl delete pod $*

kubectl-delete-deployment-%:
	kubectl delete deployment $*

kubectl-delete-service-%:
	kubectl delete service $*

info:
	kubectl get all
