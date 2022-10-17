# 💬 Talk: Kubernetes for beginners

```text
Dauer:      1h 30min - 2h
Niveau:     Einsteiger (keine Vorkenntnisse notwendig)
Zielgruppe: Docker-User, die Kubernetes nutzen wollen
Sprache:    Deutsch
Author:     André Lademann <vergissberlin@gmail.com>
```

## goal of the talk

At the end of the talk, you will show how you can basically deal with Kubernetes. You can deploy and scale your Docker containers in Kubernetes. You can set up and manage Kubernetes clusters.

## requirements

-   [ ] Laptop with Docker installed
-   [ ] Docker Hub Account
-   [ ] GitHub Account
-   [ ] (optional) Kubernetes Cluster
-   [ ] (optional) Google Cloud Account
-   [ ] (optional) Google Cloud SDK
-   [ ] (optional) Google Cloud Shell

If you don't fulfill all the points, that's no problem. Together we will fulfill the points that you have not fulfilled.

* * *

## terms

### Kubernetes

Kubernetes is an open-source platform for automating the deployment, scaling, and management of containerized applications.

#### Kubernetes Container

A Kubernetes container is an executable instance of a Docker image. A container is an isolated environment made up of a number of layers. Each layer contains a set of instructions that are executed when a container is created. If a container contains multiple layers, the last layer is used as the base and the previous layers are added as an overlay.

#### Kubernetes Pods

A pod is a group of one or more containers that run together and share the same storage and network resource. A pod is the smallest unit that can be created and managed in Kubernetes.

#### Kubernetes Services

A service is an abstraction that represents a group of pods as a logical set. Services allow pods to find and talk to each other without the pods knowing each other. Services can also be used to distribute pods across a cluster.

#### Kubernetes Nodes

A node is a virtual or physical machine that runs Kubernetes pods. A node can run one or more pods.

### Kubernetes Clusters

A cluster is a group of nodes working together to run containerized applications. A cluster consists of at least one master node and several worker nodes.

## Hands-On

# Workshop - From Docker to Kubernetes

## Kubernetes

### MiniKube vs Docker Desktop vs Rancher Desktop vs Kind

There are several ways to install Kubernetes locally. We will focus on installing MiniKube here.

If you would like to know more about the advantages and disadvantages of each, you are welcome to do so[here](https://itnext.io/goodbye-docker-desktop-hello-minikube-3649f2a1c469)read.

#### Docker Desktop

-   Local installation of Kubernetes
-   Local installation of Docker
-   Using Docker images
-   Managing Kubernetes via Docker Desktop
-   TBD

##### Installing Docker Desktop

1.  installation of[Docker Desktop](https://www.docker.com/products/docker-desktop)

#### Rancher Desktop

-   Local installation of Kubernetes
-   Local installation of Docker
-   TBD

#### ugly

-   Local installation of Kubernetes
-   TBD

##### Installing MiniKube

1.  installation of[ugly](https://minikube.sigs.k8s.io/docs/start/)
2.  Configure shortcut for minikube in shell (e.g.`alias minikube="minikube.exe"`)
3.  installation of[kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/)
4.  Configure shortcut for kubectl in the shell (e.g.`alias kubectl="kubectl.exe"`)

##### Start Kubernetes Cluster

1.  Start the Kubernetes cluster with`minikube start`

##### Kubernetes Dashboard

1.  Start the Kubernetes Dashboard with`minikube dashboard`

### Launch a pod

1.  Creating a pod with`kubectl run hello-world --image=hello-world`
2.  Checking the pod with`kubectl get pods`
3.  Abstraction from pods with`kubectl get deployments`
4.  Instructions for pods with`kubectl describe pods`
5.  Logs from pods with`kubectl logs <pod-name>`
6.  Delete pods with`kubectl delete pods <pod-name>`
7.  Deleting deployments with`kubectl delete deployments <deployment-name>`

* * *

## bottom line

In this article we covered the basics of Docker and Kubernetes. We've seen how Docker is used to create and manage containers. We also saw how Kubernetes is used to manage containerized applications. We also saw how Docker and Kubernetes work together.

## Contribute

Do you have suggestions for improvement? Then feel free to create a pull request or write a few lines in[discussion forum](https://github.com/vergissberlin/talk-docker/discussions)or[Twitter](https://twitter.com/vergissberlin).
