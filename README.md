# HelloApp Helm Chart 🚀

This repository contains a **Helm chart for deploying HelloApp on Kubernetes** using cloud-native best practices.

The chart provides a complete deployment setup including:

* Kubernetes Deployment
* Service exposure
* Ingress configuration
* Gateway API HTTPRoute support
* Horizontal Pod Autoscaling
* ServiceAccount configuration
* Helm templating for flexible configuration

This project demonstrates how to package and manage Kubernetes applications using **Helm charts**.

---

# 🧰 Technologies Used

* Kubernetes
* Helm
* YAML
* Kubernetes Gateway API
* Horizontal Pod Autoscaler (HPA)

---

# 📦 Repository Structure

```
helloapp/
├── Chart.yaml
├── values.yaml
├── .helmignore
└── templates/
    ├── deployment.yaml
    ├── service.yaml
    ├── ingress.yaml
    ├── httproute.yaml
    ├── hpa.yaml
    ├── serviceaccount.yaml
    ├── _helpers.tpl
    ├── NOTES.txt
    └── tests/
        └── test-connection.yaml
```

### Chart.yaml

Defines metadata for the Helm chart including version, name, and description.

### values.yaml

Contains configurable parameters for the deployment such as:

* image settings
* service configuration
* ingress settings
* autoscaling configuration

### templates/

This directory contains Kubernetes resource templates rendered by Helm.

---

# ☸️ Kubernetes Resources Created

The Helm chart deploys the following resources:

### Deployment

Defines the HelloApp container deployment.

Features:

* configurable image
* scalable replicas
* environment configuration

---

### Service

Exposes the application inside the Kubernetes cluster.

Used for internal communication between services.

---

### Ingress

Allows external HTTP access to the application through an Ingress controller.

---

### HTTPRoute

Provides Gateway API support for modern Kubernetes traffic routing.

---

### Horizontal Pod Autoscaler (HPA)

Automatically scales the application based on resource usage.

Benefits:

* dynamic scaling
* improved reliability
* better resource utilization

---

### ServiceAccount

Defines a dedicated service account for the application.

This improves security and allows RBAC configuration.

---

# ⚙️ Installation

## 1️⃣ Start a Kubernetes cluster

Example using Minikube:

```
minikube start
```

---

## 2️⃣ Install Helm

Verify Helm installation:

```
helm version
```

---

## 3️⃣ Deploy the Helm Chart

From the project directory run:

```
helm install helloapp ./helloapp
```

---

## 4️⃣ Verify Deployment

Check running resources:

```
kubectl get pods
kubectl get services
kubectl get ingress
```

---

# 🔄 Upgrading the Deployment

To upgrade the release after changing values:

```
helm upgrade helloapp ./helloapp
```

---

# ❌ Uninstall the Deployment

```
helm uninstall helloapp
```

---

# 📊 Features Demonstrated

This project demonstrates several Kubernetes and Helm concepts:

* Helm chart structure
* Kubernetes application deployment
* Service exposure
* Ingress configuration
* Gateway API HTTPRoute usage
* Horizontal Pod Autoscaling
* Template-driven infrastructure configuration

---

# 🎯 Learning Purpose

This repository is designed as a **learning project for deploying applications on Kubernetes using Helm**.

It demonstrates how to package Kubernetes resources into reusable Helm charts.

---

# 📜 License

This project is intended for educational and demonstration purposes.
