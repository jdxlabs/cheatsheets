# Kind - Kubernetes in Docker

It allows you to have a lightweight local Kubernetes cluster, with clustering basic notions.
You can manage several Kubernetes clusters, very easily.

## Commands

```bash
brew install kind


kind create cluster -n kind1 [--config conf.yml]
kind create cluster -n kind2

# Get the list of clusters
kind get clusters

# Select the cluster you want, by selecting context
k config get-contexts
k config use-context kind-kind1

# Display available addresses for the current cluster
k cluster-info

# Export logs about the cluster
kind export logs -n kind1

# You can delete clusters, when you want
kind delete cluster -n kind1
kind delete cluster -n kind2
```

## Links
* [A local Kubernetes cluster in seconds with Kind](https://dev.to/jdxlabs/a-local-kubernetes-cluster-in-seconds-with-kind-31lc)
* [Kind - Quick Start](https://kind.sigs.k8s.io/docs/user/quick-start/)
* [Kind - Using WSL2](https://kind.sigs.k8s.io/docs/user/using-wsl2/)
* [Guide to Running Kubernetes with Kind](https://phoenixnap.com/kb/kubernetes-kind)
* [Kubernetes KIND Cheat Sheet](https://itnext.io/kubernetes-kind-cheat-shee-2605da77984)
