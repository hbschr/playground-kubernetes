# demo for `oc` commands.
# use `create` and `delete` for simple definitions.
# use `process` for template magic and pipe that to `apply` or `delete`.

VERSION=1-0-0

init:
	oc project playground-heiko

def-create:
	oc create -f pod-definition.yml

def-delete:
	oc delete -f pod-definition.yml

tmpl-process:
	oc process -f pod-template.yml \
		-p VERSION=$(VERSION)

tmpl-apply:
	oc process -f pod-template.yml \
		-p VERSION=$(VERSION) \
		| oc apply -f -

tmpl-delete:
	oc process -f pod-template.yml \
		-p VERSION=$(VERSION) \
		| oc delete -f -
