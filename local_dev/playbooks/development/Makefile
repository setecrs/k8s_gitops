help:
	@echo "local_dev                   calls install_tools_localhost"
	@echo "                            calls bootstrap_k8s"
	@echo
	@echo "install_tools_localhost     install pip packages"
	@echo "                            install k3d command on ~/bin/"
	@echo "                            install argocd command on ~/bin/"
	@echo
	@echo "bootstrap_k8s               creates a local registry in docker, but outside k8s;"
	@echo "                            install a registry pull through cache in docker, but outside k8s"
	@echo "                            create a k3d cluster"
	@echo "                            append new cluster config on ~/.kube/config and switch to the new context"
	@echo "                            exports this repository in k8s as a local git server"
	@echo "                            install argocd in k8s"
	@echo "                            install argocd_apps in argocd; argocd_apps is an app that creates other apps"
	@echo

local_dev: install_tools_localhost bootstrap_k8s

install_tools_localhost:
	ansible-playbook install_tools_localhost.yml

bootstrap_k8s:
	ansible-playbook bootstrap_k8s.yml

.PHONY: help local_dev install_tools_localhost bootstrap_k8s

