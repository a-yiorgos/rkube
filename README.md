**rkube: Rancher2 single VM kubernetes cluster based on rke**
---
There exist plenty of single VM kubernetes clusters available, like minikube and microk8s to name a couple.  They are very nice, but since I work a lot with Rancher2, I wanted something that closely followed that and deployed via RKE. Hence this repository, _rkube_.

Prerequisites:
- VirtualBox
- vagrant
- kubectl

How to boot: `vagrant up` at the directory you have cloned the repository.

To test the installation with a simple echo server run: `kubectl --kubeconfig kube_cluster_config.yml apply -f echo.yml`

The VM is accessible at `192.168.98.100`. You can change this at the Vagrantfile. So the echo server above is reachable at http://192.168.98.100/echo Ignore the SSL warning if you access https://192.168.98.100/echo since we have not created any specific certificate for the echo server Ingress controller.
