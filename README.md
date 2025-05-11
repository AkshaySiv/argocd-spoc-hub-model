# `argocd-spoc-hub-model`

This repository demonstrates the implementation of a **multi-cluster GitOps deployment model** using **ArgoCD** with a **centralized Single Point of Contact (SPOC) hub architecture**. The architecture involves a **hub cluster** and **two SPOC clusters**, all hosted on **AWS EKS**. This setup enables centralized management of ArgoCD applications across multiple Kubernetes clusters, ensuring streamlined operations, scalability, and visibility.

## Architecture Overview

![alt text](images/image.png)

1. **Hub Cluster (ArgoCD SPOC Hub)**
   - The **hub cluster** acts as the centralized control plane.
   - It runs the **ArgoCD instance**, responsible for managing application deployments and synchronizing changes to the **SPOC clusters**.
   - The hub cluster is the entry point for all administrative tasks, such as managing applications, defining policies, and viewing logs.
   
2. **SPOC Clusters (Single Point of Contact)**
   - The **SPOC clusters** are dedicated Kubernetes clusters that receive the configurations and applications managed by the **hub cluster**.
   - These clusters contain the workloads and services deployed from the hub, with ArgoCD maintaining synchronization between the hub and SPOC clusters.
   - The SPOC clusters can be **multi-region** and **multi-availability zone (AZ)** to ensure high availability and fault tolerance.
