# DevOps Lab

## Exercise 1: Kubernetes Getting Started

### Objective

Deploy an Nginx application as a Kubernetes Pod using Minikube and verify that it is running successfully.

### Steps

#### 1. Install Minikube

Minikube was already installed on macOS using Homebrew.

```bash
brew install minikube

#### 2. Start Minikube

Started the local Kubernetes cluster using:

```bash
minikube start
```

Minikube used Docker as the driver.

#### 3. Create the Nginx Pod

Created an Nginx Pod using:

```bash
kubectl run hello-k8s --image=nginx --port=80
```

#### 4. Verify the Pod

Checked the Pod status using:

```bash
kubectl get pods
```

The Pod was running successfully.

#### 5. Access the Nginx Application

The Nginx application was accessed through Minikube.

The browser displayed the **"Welcome to nginx!"** page, confirming that the Nginx Pod was successfully deployed and running.

### Result

Successfully deployed and accessed an Nginx application using Kubernetes and Minikube.

