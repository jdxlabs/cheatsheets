# Google Cloud CLI cheatsheet

## Install

First, install the client

```bash
brew install gcloud
```

## Login

```bash
gcloud auth list
gcloud auth login
gcloud auth application-default list  # used by Terraform

gcloud config configurations list
gcloud config configurations activate <wanted-config>

gcloud config set project <prj-id>
gcloud projects list
gcloud config get-value project

# connect to gcr
gcloud auth configure-docker
```

## Commons

Cheatsheet
```bash
gcloud cheat-sheet
```

List storages
```bash
gcloud storage ls

# or
gsutil ls
```

List compute instances
```bash
gcloud compute addresses list
```

List available services
```bash
gcloud services list --available
```

## GKE cluster

First, install the GKE auth component
```bash
gcloud components install gke-gcloud-auth-plugin
```

Create a GKE cluster
```bash
gcloud container clusters create gke1 --num-nodes=1 --region europe-west1 --project=PROJECT_ID

# or, with autopilot
gcloud container clusters create-auto gke1 --region europe-west1 --project=PROJECT_ID
```

Get the kubeconfig file
```bash
gcloud container clusters get-credentials gke1 --region=europe-west1
```

Delete the cluster
```bash
gcloud container clusters delete gke1 --region europe-west1 --project=infra-jdxlabs
```

## Usefull links
* [The gcloud CLI cheat sheet](https://cloud.google.com/sdk/docs/cheatsheet?hl=en)
* [Install the Google Cloud CLI](https://cloud.google.com/sdk/docs/install-sdk?hl=en)
* [Google Kubernetes Engine (GKE)](https://cloud.google.com/kubernetes-engine?hl=en)
