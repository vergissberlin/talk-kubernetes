{% include_relative .github/templates/header.md %}

## 💬 Talk: Kubernetes for beginners

```text
Dauer:      1h 30min - 2h
Niveau:     Einsteiger (keine Vorkenntnisse notwendig)
Zielgruppe: Docker-User, die Kubernetes nutzen wollen
Sprache:    Deutsch
Author:     André Lademann <vergissberlin@gmail.com>
```

### Goal of the talk

At the end of the talc you show how you can fundamentally deal with Kubernetes. You can scale and scale your docker containers in Kubernetes. You can put on and manage Kubernetes clusters.

### Prerequisites

-   [ ] Laptop installed with docker
-   [ ] Docker Hub Account
-   [ ] GitHub Account
-   [ ] (optional) Kubernetes Cluster
-   [ ] (optional) Google Cloud Account
-   [ ] (optional) Google Cloud SDK
-   [ ] (optional) Google Cloud Shell

If you do not meet all the points, that's not a problem. We will meet the points that you have not met together.

* * *

### Terms

#### Kubernetes

Kubernetes is an open source platform for automating the provision, scaling and management of container applications.

##### Kubernetes Container

A Kubernetes container is an executable instance of a Docker Image. A container is an isolated environment that consists of a series of layers. Each layer contains a number of instructions that are carried out when creating a container. If a container contains several layers, the last layer is used as the base and the previous layers are added as an overlay.

##### Cube

Ein Pod ist eine Gruppe von einem oder mehreren Containern, die gemeinsam ausgeführt werden und die gleiche Speicher- und Netzwerkressource teilen. Ein Pod ist die kleinste Einheit, die in Kubernetes erstellt und verwaltet werden kann.

##### Kubernetes Services

A service is an abstraction that represents a group of pods as a logical set. Services make it possible to find pods and communicate with each other without the pods know themselves. Services can also be used to distribute pods over a cluster.

##### Kubernetes Nodes

A node is a virtual or physical machine on which Kubernetes pods are carried out. A node can run one or more pods.

#### Kubernetes Clusters

A cluster is a group of nodes who work together to carry out container applications. A cluster consists of at least one master node and several worker node.

## Hands-On

### MiniKube vs Docker Desktop vs Rancher Desktop vs Kind

There are various ways to install Kubernetes locally. We will concentrate on the installation of miniube.

If you want to learn more about the respective advantages and disadvantages, you are welcome to[here](https://itnext.io/goodbye-docker-desktop-hello-minikube-3649f2a1c469)read.

### Docker Desktop

-   Local installation of Kubernetes
-   Local installation of Docker
-   Use of Docker Images
-   Management of Kubernetes via Docker Desktop
-   TBD

#### Installation von Docker Desktop

1.  Installation of[Docker Desktop](https://www.docker.com/products/docker-desktop)

#### Rancher Desktop

-   Local installation of Kubernetes
-   Local installation of Docker
-   TBD

#### Ugly

-   Local installation of Kubernetes
-   TBD

##### Installation of Minikube

1.  Installation of[Ugly](https://minikube.sigs.k8s.io/docs/start/)
2.  Configure Shortcut for Minikube in the Shell (e.g.`alias minikube="minikube.exe"`)
3.  Installation of[to Berctl](https://kubernetes.io/docs/tasks/tools/install-kubectl/)
4.  Configure Shortcut for Kubectl in the Shell (e.g.`alias kubectl="kubectl.exe"`)

##### Start Kubernetes cluster

1.  Start the Kubernet cluster`minikube start`

##### Kubernetes Dashboard

1.  Start the Kubernet dashboard with`minikube dashboard`

### Start of a pod

1.  Creating a pod with`kubectl run hello-world --image=hello-world`
2.  Check the pod with`kubectl get pods`
3.  Abstraction of pods with`kubectl get deployments`
4.  Instructions for pods with`kubectl describe pods`
5.  Logs from pods with`kubectl logs <pod-name>`
6.  Deleting pods with`kubectl delete pods <pod-name>`
7.  Deleting deployments with`kubectl delete deployments <deployment-name>`

* * *

## Beside

In this article we dealt with the basics of Docker and Kubernetes. We saw how Docker is used to create and manage containers. We also saw how Kubernetes is used to manage container applications. We also saw how Docker and Kubernetes work together.

## Contribute

Do you have suggestions for improvement? Then like to create a pull request or write a few lines in[Forum for discussion](https://github.com/vergissberlin/talk-docker/discussions)or[Twitter](https://twitter.com/vergissberlin).

{% include_relative .github/templates/footer.md %}
