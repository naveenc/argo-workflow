setup:
	@helm repo add nats https://nats-io.github.io/k8s/helm/charts/
	@kubectl create ns nats
	@kubectl apply -f nats-pvc.yaml

install:
	@helm install --namespace nats sesuite-nats nats/nats -f ./values.yaml

delete:
	@helm delete --namespace nats sesuite-nats

shell:
	@kubectl exec -n nats -it deployment/sesuite-nats-box -- /bin/sh -l