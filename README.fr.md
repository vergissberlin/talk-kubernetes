{% include_relatif .github / modèles / en-tête.md%}

## 💬 Talk: Kubernetes pour les débutants

```text
Dauer:      1h 30min - 2h
Niveau:     Einsteiger (keine Vorkenntnisse notwendig)
Zielgruppe: Docker-User, die Kubernetes nutzen wollen
Sprache:    Deutsch
Author:     André Lademann <vergissberlin@gmail.com>
```

### Ziel des Talks

À la fin du talc, vous montrez comment vous pouvez fondamentalement gérer Kubernetes. Vous pouvez mettre à l'échelle et mettre à l'échelle vos conteneurs Docker dans Kubernetes. Vous pouvez mettre et gérer les clusters Kubernetes.

### Condition préalable

-   [ ] Ordinateur portable installé avec Docker
-   [ ] Compte Docker Hub
-   [ ] Compte github
-   [ ] (facultatif) cluster kubernetes
-   [ ] (facultatif) Google Cloud Compte
-   [ ] (Facultatif) Google Cloud SDK
-   [ ] (Facultatif) Google Cloud Shell

Si vous ne rencontrez pas tous les points, ce n'est pas un problème. Nous allons rencontrer les points que vous n'avez pas rencontrés ensemble.

* * *

### Termes

#### Kubernetes

Kubernetes est une plate-forme open source pour automatiser la fourniture, la mise à l'échelle et la gestion des applications de conteneurs.

##### Conteneur de Kubernetes

Un conteneur Kubernetes est une instance exécutable d'une image docker. Un conteneur est un environnement isolé qui se compose d'une série de couches. Chaque couche contient un certain nombre d'instructions qui sont effectuées lors de la création d'un conteneur. Si un conteneur contient plusieurs couches, la dernière couche est utilisée comme base et les couches précédentes sont ajoutées comme superposition.

##### Cube

Un pod est un groupe d'un ou plusieurs conteneurs qui sont effectués ensemble et partagent la même mémoire et la même ressource réseau. Un pod est la plus petite unité qui peut être créée et gérée à Kubernetes.

##### Services Kubernetes

Un service est une abstraction qui représente un groupe de pods comme un ensemble logique. Les services permettent de trouver des pods et de communiquer entre eux sans que les gousses se connaissent. Les services peuvent également être utilisés pour distribuer des pods via un cluster.

##### Nœuds kubernetes

Un nœud est une machine virtuelle ou physique sur laquelle des pods kubernetes sont effectués. Un nœud peut exécuter une ou plusieurs pods.

#### Clusters de Kubernetes

Un cluster est un groupe de nœuds qui travaillent ensemble pour effectuer des applications de conteneurs. Un cluster se compose d'au moins d'un nœud maître et de plusieurs nœuds de travailleur.

## Pratique

### Minikube vs Docker Desktop vs Rancher Desktop vs Kind

Il existe différentes façons d'installer Kubernetes localement. Nous nous concentrerons sur l'installation de Miniube.

Si vous souhaitez en savoir plus sur les avantages et les inconvénients respectifs, vous êtes les bienvenus[ici](https://itnext.io/goodbye-docker-desktop-hello-minikube-3649f2a1c469)lire.

### Docker Desktop

-   Installation locale de Kubernetes
-   Installation locale de Docker
-   Utilisation d'images Docker
-   Gestion de Kubernetes via Docker Desktop
-   TBD

#### Installation Von Docker Desktop

1.  Installation de[Docker Desktop](https://www.docker.com/products/docker-desktop)

#### Bureau de rancher

-   Installation locale de Kubernetes
-   Installation locale de Docker
-   TBD

#### Laid

-   Installation locale de Kubernetes
-   TBD

##### Installation de minikube

1.  Installation de[Laid](https://minikube.sigs.k8s.io/docs/start/)
2.  Configurez le raccourci pour Minikube dans le shell (par exemple.`alias minikube="minikube.exe"`)
3.  Installation de[à Berctl](https://kubernetes.io/docs/tasks/tools/install-kubectl/)
4.  Configurez le raccourci pour Kubectl dans le shell (par exemple.`alias kubectl="kubectl.exe"`)

##### Démarrer le cluster de Kubernetes

1.  Démarrer le cluster Kubernet`minikube start`

##### Tableau de bord Kubernetes

1.  Démarrez le tableau de bord Kubernet avec`minikube dashboard`

### Début d'un pod

1.  Créer une pod avec`kubectl run hello-world --image=hello-world`
2.  Vérifiez le pod avec`kubectl get pods`
3.  Abstraction des gousses avec`kubectl get deployments`
4.  Instructions pour les gousses avec`kubectl describe pods`
5.  Journaux à partir des gousses avec`kubectl logs <pod-name>`
6.  Suppression des gousses avec`kubectl delete pods <pod-name>`
7.  Suppression de déploiements avec`kubectl delete deployments <deployment-name>`

* * *

## À côté de

Dans cet article, nous avons traité les bases de Docker et Kubernetes. Nous avons vu comment Docker est utilisé pour créer et gérer des conteneurs. Nous avons également vu comment Kubernetes est utilisé pour gérer les applications de conteneurs. Nous avons également vu comment Docker et Kubernetes travaillent ensemble.

## Contribuer

Avez-vous des suggestions d'amélioration? Puis aime créer une demande de traction ou écrire quelques lignes dans[Forum pour la discussion](https://github.com/vergissberlin/talk-docker/discussions)ou[Gazouillement](https://twitter.com/vergissberlin).

{% inclut_relative .github / modèles / footter.md%}
