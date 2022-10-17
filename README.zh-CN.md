# 💬 讲座：面向初学者的 Kubernetes

```text
Dauer:      1h 30min - 2h
Niveau:     Einsteiger (keine Vorkenntnisse notwendig)
Zielgruppe: Docker-User, die Kubernetes nutzen wollen
Sprache:    Deutsch
Author:     André Lademann <vergissberlin@gmail.com>
```

## 谈话的目标

在演讲的最后，您将展示如何基本处理 Kubernetes。您可以在 Kubernetes 中部署和扩展 Docker 容器。您可以设置和管理 Kubernetes 集群。

## 要求

-   [ ] 安装了 Docker 的笔记本电脑
-   [ ] Docker Hub 帐户
-   [ ] GitHub 帐户
-   [ ] （可选）Kubernetes 集群
-   [ ] （可选）谷歌云账户
-   [ ] （可选）谷歌云 SDK
-   [ ] （可选）Google Cloud Shell

如果你不满足所有的点，那没问题。我们将一起完成您尚未完成的要点。

* * *

## 条款

### Kubernetes

Kubernetes 是一个开源平台，用于自动部署、扩展和管理容器化应用程序。

#### Kubernetes 容器

Kubernetes 容器是 Docker 映像的可执行实例。容器是由多个层组成的隔离环境。每一层都包含一组在创建容器时执行的指令。如果一个容器包含多个层，则最后一层用作基础层，前面的层用作叠加层。

#### Kubernetes Pod

Pod 是一组一个或多个容器，它们一起运行并共享相同的存储和网络资源。 Pod 是 Kubernetes 中可以创建和管理的最小单元。

#### Kubernetes 服务

服务是一种抽象，将一组 pod 表示为一个逻辑集。服务允许 pod 在不知道彼此的情况下找到并相互交谈。服务也可用于跨集群分发 pod。

#### Kubernetes 节点

节点是运行 Kubernetes pod 的虚拟机或物理机。一个节点可以运行一个或多个 Pod。

### Kubernetes 集群

集群是一组节点一起工作以运行容器化应用程序。一个集群至少由一个主节点和多个工作节点组成。

## 动手实践

# 研讨会 - 从 Docker 到 Kubernetes

## Kubernetes

### MiniKube vs Docker Desktop vs Rancher Desktop vs Kind

有几种方法可以在本地安装 Kubernetes。我们将在这里重点安装 MiniKube。

如果您想了解更多关于每个优点和缺点的信息，欢迎您这样做[这里](https://itnext.io/goodbye-docker-desktop-hello-minikube-3649f2a1c469)读。

#### 码头工人桌面

-   本地安装 Kubernetes
-   本地安装 Docker
-   使用 Docker 镜像
-   通过 Docker Desktop 管理 Kubernetes
-   待定

##### 安装 Docker 桌面

1.  安装[码头工人桌面](https://www.docker.com/products/docker-desktop)

#### 牧场主桌面

-   本地安装 Kubernetes
-   本地安装 Docker
-   待定

#### 丑陋的

-   本地安装 Kubernetes
-   待定

##### 安装 MiniKube

1.  安装[丑陋的](https://minikube.sigs.k8s.io/docs/start/)
2.  在 shell 中为 minikube 配置快捷方式（例如`alias minikube="minikube.exe"`)
3.  安装[kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/)
4.  在 shell 中为 kubectl 配置快捷方式（例如`alias kubectl="kubectl.exe"`)

##### 启动 Kubernetes 集群

1.  启动 Kubernetes 集群`minikube start`

##### Kubernetes 仪表板

1.  启动 Kubernetes 仪表板`minikube dashboard`

### 启动一个 pod

1.  创建一个 pod`kubectl run hello-world --image=hello-world`
2.  检查吊舱`kubectl get pods`
3.  从 pod 中抽象出来`kubectl get deployments`
4.  豆荚的说明`kubectl describe pods`

* * *

## 底线

在本文中，我们介绍了 Docker 和 Kubernetes 的基础知识。我们已经了解了如何使用 Docker 创建和管理容器。我们还看到了 Kubernetes 如何用于管理容器化应用程序。我们还看到了 Docker 和 Kubernetes 如何协同工作。
