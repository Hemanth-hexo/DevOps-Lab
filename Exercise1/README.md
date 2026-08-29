# Exercise 1: Kubernetes Getting Started

## Objective

Deploy and access an Nginx application using Kubernetes and Minikube on macOS.

## Environment

- Operating System: macOS
- Architecture: Apple Silicon (arm64)
- Shell: Terminal / zsh
- Container Runtime: Docker
- Kubernetes: Minikube
- Kubernetes CLI: kubectl

## Prerequisites

The following tools are required:

- Homebrew
- Docker Desktop
- Minikube
- kubectl

## 1. Install Minikube

Minikube was installed on macOS using Homebrew.

```bash
brew install minikube

```

### 2 Create the Kubernetes Pod

Created an Nginx Pod using:

```bash
kubectl run hello-k8s --image=nginx --port=80
```

### 3. Verify the Pod

Checked the status of the Pod:

```bash
kubectl get pods
```

The Pod was successfully created and reached the `Running` state.

### 4. Expose the Pod

Exposed the Pod using a NodePort service:

```bash
kubectl expose pod hello-k8s --type=NodePort --port=80
```

### 5. Access the Application

Opened the deployed Nginx application using:

```bash
minikube service hello-k8s
```

The Nginx welcome page was successfully displayed in the browser.

---

## Screenshots

### Minikube Installation

![Minikube Installation](./Screenshots/01-minikube-installation.png)

### Minikube Cluster Started

![Minikube Start](./Screenshots/02-minikube-start.png)

### Kubernetes Pod and Service

![Pod and Service](./Screenshots/03-kubernetes-pod-and-service.png)

### Nginx Welcome Page

![Nginx Welcome Page](./Screenshots/04-nginx-welcome-page.png)

---

##  Result

Successfully deployed an **Nginx container as a Kubernetes Pod** using Minikube, exposed it through a Kubernetes Service, and accessed the application through a web browser.

---
