# Covid-19 Statistics Helm Charts
This repository contains the Helm charts necessary to successfully deploy the Covid-19 Statistics web application to a Kubernetes cluster. These charts are designed to be used as part of a GitOps implementation using ArgoCD.

## Prerequisites
Before deploying the application using these charts, please make sure that you have the following prerequisites installed:

- A Kubernetes cluster
- Helm version 3
- envValues.yaml file updated with valid API Key

## Installation
To install the application using these Helm charts, please follow these steps:

1. Clone the repository using the command: git clone https://github.com/Patryk-Stefanski/CovidStatsHelmCharts.git
2. Navigate to the root directory of the project: cd CovidStatsHelmCharts
3. Install the application using the command: helm install -f myapp/envValues.yaml myapp ./myapp
4. Once the installation is complete, you can access the application by navigating to http://<cluster-ip>:<node-port> in your web browser.

## Configuration
The charts provided in this repository include configuration options that allow you to customize the deployment of the Covid-19 Statistics web application. These options include:

- image.repository: The Docker repository for the application image.
- image.tag: The tag of the application image.
- replicaCount: The number of replicas to deploy.
- service.type: The type of Kubernetes service to use (ClusterIP, NodePort, or LoadBalancer).
- service.port: The port number to use for the Kubernetes service.
- ingress.enabled: Whether to enable ingress for the application.
- ingress.hosts: A list of hostnames to use for the ingress resource.
- ingress.tls: A list of TLS configuration options to use for the ingress resource.

To customize the deployment of the application, you can either modify the values.yaml file directly, or you can create a separate values file and pass it to the helm install command using the --values flag.

## GitOps Implementation
These Helm charts are designed to be used as part of a GitOps implementation using ArgoCD. ArgoCD is a declarative, GitOps continuous delivery tool for Kubernetes. By using ArgoCD with these Helm charts, changes to the application can be automatically deployed to a Kubernetes cluster whenever changes are pushed to the Git repository.

