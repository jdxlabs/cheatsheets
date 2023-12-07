# Kubernetes

## Kubectl CheatSheet
```bash
alias k='kubectl'

k --help


# kubectx/ns cmds, for contexts and namespaces
kubectx
kubens
kubectx -c && kubens -c

=> alias kcontext='echo "cluster : " && kubectx -c && echo "namespace : " && kubens -c'


# native cmds, for contexts and namespaces

k config get-contexts
k config current-context
k config use-context <selected-context>
k cluster-info --context <current-context>

k get namespaces
k config view --minify | grep namespace:
k config set-context --current --namespace=<selected-namespace>

=> alias kcontext='echo "cluster : " && kubectl config current-context && echo "namespace : " && kubectl config view --minify | grep namespace:'


# cmds on the selected cluster

k get nodes -o wide

k get all
k get all -A
k get all -n mynamespace

k apply -f myfile.yml
k delete -f myfile.yml

k get po [-o wide] [-w]
k get svc [-o wide] [-w]
k get deploy [-o wide] [-w]
k get ns
k get secret
k get configmap
k delete svc,deploy NAME

k logs <po-name>
k describe po <po-name>

k get secret
k get secret -A
k get secret <secret-name> -o yaml
k create secret generic <secret-name> --from-literal=mykey=myvalue [--from-file=./myfile.txt] -n <my-namespace>

```

## Install Minikube and Kubectl to work locally
Follow instructions here :
  * [[https://kubernetes.io/docs/setup/minikube/|Running Kubernetes Locally via Minikube]]
  * [[https://kubernetes.io/docs/tasks/tools/install-kubectl/#install-kubectl-on-linux|Install kubectl on Linux]]

Then, you have a VM with Kubernetes installed :
```bash
minikube start # to start the VM
minikube stop # to stop the VM
minikube dashboard # to see the K8S Dashboard
minikube ssh # to connect to the VM with SSH, to see your docker images, etc.
```

## Other local solutions
  * [[kind|Kind]]
  * [[https://github.com/kubernetes/kubeadm|Kubeadm]]

## Training resources
  * https://killer.sh/
  * https://kodekloud.com/
  * https://github.com/dgkanatsios/CKAD-exercises

## Usefull links
  * [[http://kubernetes.io/docs/user-guide/kubectl-cheatsheet/|Kubectl Cheat Sheet]]
  * [[https://dev.to/pragyanatvade/comprehensive-kubernetes-cheatsheet-34gm|Comprehensive Kubernetes Cheat Sheet]]
  * [[https://www.oreilly.com/library/view/kubernetes-up-and/9781491935668/ch04.html#:~:text=The%20most%20basic%20command%20for,%3E%20.|O.REILLY - Common kubectl Commands]]
  * https://www.padok.fr/en/blog/minikube-kubeadm-kind-k3s
  * https://github.com/mmumshad/kubernetes-the-hard-way


