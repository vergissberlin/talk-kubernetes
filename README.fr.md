# 💬 Conférence : Kubernetes pour les débutants

```text
Dauer:      1h 30min - 2h
Niveau:     Einsteiger (keine Vorkenntnisse notwendig)
Zielgruppe: Docker-User, die Kubernetes nutzen wollen
Sprache:    Deutsch
Author:     André Lademann <vergissberlin@gmail.com>
```

## Ziel des Talks

À la fin de l'exposé, vous montrerez comment vous pouvez gérer Kubernetes. Vous pouvez déployer et mettre à l'échelle vos conteneurs Docker dans Kubernetes. Vous pouvez configurer et gérer des clusters Kubernetes.

## conditions

-   [ ] Ordinateur portable avec Docker installé
-   [ ] Compte Hub Docker
-   [ ] Compte GitHub
-   [ ] (facultatif) Cluster Kubernetes
-   [ ] (facultatif) Compte Google Cloud
-   [ ] (facultatif) SDK Google Cloud
-   [ ] (facultatif) Google Cloud Shell

Si vous ne remplissez pas tous les points, ce n'est pas un problème. Ensemble, nous remplirons les points que vous n'avez pas remplis.

* * *

## termes

### Kubernetes

Kubernetes est une plate-forme open source permettant d'automatiser le déploiement, la mise à l'échelle et la gestion des applications conteneurisées.

#### Conteneur Kubernetes

Un conteneur Kubernetes est une instance exécutable d'une image Docker. Un conteneur est un environnement isolé composé de plusieurs couches. Chaque couche contient un ensemble d'instructions qui sont exécutées lors de la création d'un conteneur. Si un conteneur contient plusieurs couches, la dernière couche est utilisée comme base et les couches précédentes sont ajoutées en superposition.

#### Capsules Kubernetes

Un pod est un groupe d'un ou plusieurs conteneurs qui s'exécutent ensemble et partagent les mêmes ressources de stockage et de réseau. Un pod est la plus petite unité pouvant être créée et gérée dans Kubernetes.

#### Services Kubernetes

Un service est une abstraction qui représente un groupe de pods sous la forme d'un ensemble logique. Les services permettent aux pods de se trouver et de se parler sans que les pods se connaissent. Les services peuvent également être utilisés pour distribuer des pods dans un cluster.

#### Nœuds Kubernetes

Un nœud est une machine virtuelle ou physique qui exécute des pods Kubernetes. Un nœud peut exécuter un ou plusieurs pods.

### Grappes Kubernetes

Un cluster est un groupe de nœuds travaillant ensemble pour exécuter des applications conteneurisées. Un cluster se compose d'au moins un nœud maître et de plusieurs nœuds de travail.

## Pratique

# Atelier - De Docker à Kubernetes

## Kubernetes

### MiniKube contre Docker Desktop contre Rancher Desktop contre Kind

Il existe plusieurs façons d'installer Kubernetes localement. Nous nous concentrerons ici sur l'installation de MiniKube.

Si vous souhaitez en savoir plus sur les avantages et les inconvénients de chacun, n'hésitez pas à le faire[ici](https://itnext.io/goodbye-docker-desktop-hello-minikube-3649f2a1c469)lis.

#### Bureau Docker

-   Installation locale de Kubernetes
-   Lokale Installation von Docker
-   Utilisation d'images Docker
-   Gérer Kubernetes via Docker Desktop
-   À déterminer

##### Installation de Docker Desktop

1.  installation de[Bureau Docker](https://www.docker.com/products/docker-desktop)

#### Bureau de l'éleveur

-   Installation locale de Kubernetes
-   Installation locale de Docker
-   À déterminer

#### moche

-   Installation locale de Kubernetes
-   À déterminer

##### Installer MiniKube

1.  installation de[moche](https://minikube.sigs.k8s.io/docs/start/)
2.  Configurez le raccourci pour minikube dans le shell (par ex.`alias minikube="minikube.exe"`)
3.  installation de[kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/)
4.  Configurez le raccourci pour kubectl dans le shell (par ex.`alias kubectl="kubectl.exe"`)

##### Démarrer le cluster Kubernetes

1.  Démarrez le cluster Kubernetes avec`minikube start`

##### Tableau de bord Kubernetes

1.  Démarrez le tableau de bord Kubernetes avec`minikube dashboard`

### Lancer un module

1.  Création d'un module avec`kubectl run hello-world --image=hello-world`
2.  Vérification du pod avec`kubectl get pods`
3.  Prélèvement des gousses avec`kubectl get deployments`
4.  Instructions pour les dosettes avec`kubectl describe pods`

* * *

## ligne de fond

Dans cet article, nous avons couvert les bases de Docker et Kubernetes. Nous avons vu comment Docker est utilisé pour créer et gérer des conteneurs. Nous avons également vu comment Kubernetes est utilisé pour gérer les applications conteneurisées. Nous avons également vu comment Docker et Kubernetes fonctionnent ensemble.
