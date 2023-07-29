.POSIX:

default: namespace argocd root

namespace:
	kubectl --kubeconfig /etc/rancher/k3s/config.yaml create namespace argocd --dry-run=client --output=yaml \
		| kubectl apply -f -

.PHONY: argocd
argocd:
	cd argocd && ./apply.sh

.PHONY: root
root:
	cd root && ./apply.sh
