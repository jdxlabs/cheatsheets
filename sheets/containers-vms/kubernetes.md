# Kubernetes

## Kubectl CheatSheet

```bash
# in .bashrc
alias k='kubectl'
export f='--force'
export dry='--dry-run=client'
export o='-oyaml'
alias kshow='kubectl config get-contexts'
alias kx='kubectl config use-context'
alias kn='kubectl config set-context --current --namespace '
```

```bash
k --help
```

Kubectx/ns cmds, for contexts and namespaces
```bash
kubectx
kubens
kubectx -c && kubens -c
```

Native commands, for contexts and namespaces
```bash
k config get-contexts
k config current-context
k config use-context <selected-context>
k cluster-info --context <current-context>

k get namespaces
k config view --minify | grep namespace:
k config set-context --current --namespace=<selected-namespace>
```

Commands on the selected cluster
```bash
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

## Install K3S to work locally

```bash
# install K3S (and avoid using sudo)
curl -sfL https://get.k3s.io | sh -s -- --write-kubeconfig-mode 644

# Check the status of K3S
sudo systemctl status k3s
export KUBECONFIG=/etc/rancher/k3s/k3s.yaml
k get nodes

# uninstall K3S
sudo /usr/local/bin/k3s-uninstall.sh
rm -rf /var/lib/rancher/k3s
rm -rf /etc/rancher/k3s
rm -rf ~/.kube
```
Note : You have a lot of possibilities to install Kubernetes locally (like Kind, KubeADM, etc.).

## Training resources
* [Killer.sh](https://killer.sh/)
* [KodeKloud](https://kodekloud.com/)
* [CKAD exercises](https://github.com/dgkanatsios/CKAD-exercises)

## Usefull links
* [Kubectl Cheat Sheet](http://kubernetes.io/docs/user-guide/kubectl-cheatsheet/)
* [Comprehensive Kubernetes Cheat Sheet](https://dev.to/pragyanatvade/comprehensive-kubernetes-cheatsheet-34gm)
* [O.REILLY - Common kubectl Commands](https://www.oreilly.com/library/view/kubernetes-up-and/9781491935668/ch04.html)
* [Kubernetes - The hard way](https://github.com/mmumshad/kubernetes-the-hard-way)
* [Kubernetes - The easier way](https://github.com/darxkies/k8s-tew)
* [Awesome Kubernetes Resources](https://github.com/tomhuang12/awesome-k8s-resources)
