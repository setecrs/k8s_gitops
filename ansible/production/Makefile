help:
	@echo "production                  calls bootstrap_k8s"
	@echo
	@echo "bootstrap_k8s               install argocd in k8s"
	@echo "                            install argocd_apps in argocd; argocd_apps is an app that creates other apps"
	@echo

production: bootstrap_k8s

bootstrap_k8s:
	ansible-playbook bootstrap_k8s.yml

.PHONY: help local_dev install_tools_localhost bootstrap_k8s

