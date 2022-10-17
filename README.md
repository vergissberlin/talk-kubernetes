# 💬 Talk: Von Docker bis Kubernetes

```text
Dauer:      1h 30min - 2h
Niveau:     Einsteiger (keine Vorkenntnisse notwendig)
Zielgruppe: Docker-User, die Kubernetes nutzen wollen
Sprache:    Deutsch
Author:     André Lademann <vergissberlin@gmail.com>
```

## Ziel des Talks

Am Ende des Talks weist Du, wie du wie Du grundlegend mit Kubernetes umgehen kannst. Du kannst Deine Docker-Container in Kubernetes deployen und skalieren. Du kannst Kubernetes-Cluster aufsetzen und verwalten.

## Vorraussetzungen

- [ ] Laptop mit Docker installiert
- [ ] Docker Hub Account
- [ ] GitHub Account
- [ ] (optional) Kubernetes Cluster
- [ ] (optional) Google Cloud Account
- [ ] (optional) Google Cloud SDK
- [ ] (optional) Google Cloud Shell

---

## Begriffe

### Kubernetes

Kubernetes ist eine Open-Source-Plattform für die Automatisierung der Bereitstellung, Skalierung und Verwaltung von Containeranwendungen.

#### Kubernetes Container

Ein Kubernetes Container ist eine ausführbare Instanz eines Docker Images. Ein Container ist eine isolierte Umgebung, die aus einer Reihe von Schichten besteht. Jede Schicht enthält eine Reihe von Anweisungen, die beim Erstellen eines Containers ausgeführt werden. Wenn ein Container mehrere Schichten enthält, wird die letzte Schicht als Basis verwendet und die vorherigen Schichten als Overlay hinzugefügt.

#### Kubernetes Pods

Ein Pod ist eine Gruppe von einem oder mehreren Containern, die gemeinsam ausgeführt werden und die gleiche Speicher- und Netzwerkressource teilen. Ein Pod ist die kleinste Einheit, die in Kubernetes erstellt und verwaltet werden kann.

#### Kubernetes Services

Ein Service ist eine Abstraktion, die eine Gruppe von Pods als ein logisches Set darstellt. Services ermöglichen es, Pods zu finden und miteinander zu kommunizieren, ohne dass die Pods sich selbst kennen. Services können auch verwendet werden, um Pods über einen Cluster hinweg zu verteilen.

#### Kubernetes Nodes

Ein Node ist eine virtuelle oder physische Maschine, auf der Kubernetes Pods ausgeführt werden. Ein Node kann einen oder mehrere Pods ausführen.

### Kubernetes Clusters

Ein Cluster ist eine Gruppe von Nodes, die zusammen arbeiten, um Containeranwendungen auszuführen. Ein Cluster besteht aus mindestens einem Master-Node und mehreren Worker-Node.


## Hands-On

# Workshop - Von Docker bis Kubertes

## Kubernetes

### MiniKube vs Docker Desktop vs Rancher Desktop vs Kind

Es gibt verschiedene Möglichkeiten Kubernetes lokal zu installieren. Wir werden uns hier auf die Installation von MiniKube konzentrieren.

Möchtest Du mehr über die jeweiligen Vor- und Nachteile erfahren, kannst Du gerne [hier](https://itnext.io/goodbye-docker-desktop-hello-minikube-3649f2a1c469
) nachlesen.

#### Docker Desktop

* Lokale Installation von Kubernetes
* Lokale Installation von Docker
* Verwendung von Docker Images
* Verwaltung von Kubernetes über Docker Desktop
* TBD

##### Installation von Docker Desktop

1. Installation von [Docker Desktop](https://www.docker.com/products/docker-desktop)

#### Rancher Desktop

* Lokale Installation von Kubernetes
* Lokale Installation von Docker
* TBD

#### MiniKube

* Lokale Installation von Kubernetes
* TBD

##### Installation von MiniKube

1. Installation von [minikube](https://minikube.sigs.k8s.io/docs/start/)
2. Shortcut für minikube in der Shell konfigurieren (z.B. `alias minikube="minikube.exe"`)
3. Installation von [kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/)
4. Shortcut für kubectl in der Shell konfigurieren (z.B. `alias kubectl="kubectl.exe"`)

##### Kubernetes Cluster starten

1. Starten des Kubernetes Clusters mit `minikube start`

##### Kubernetes Dashboard

1. Starten des Kubernetes Dashboard mit `minikube dashboard`

### Starten eines Pods

1. Erstellen eines Pods mit `kubectl run hello-world --image=hello-world`
2. Überprüfen des Pods mit `kubectl get pods`
3. Abstraktion von Pods mit `kubectl get deployments`
4. Anweisungen für Pods mit `kubectl describe pods`


---

## Unterm Strich

In diesem Artikel haben wir uns mit den Grundlagen von Docker und Kubernetes beschäftigt. Wir haben gesehen, wie Docker verwendet wird, um Container zu erstellen und zu verwalten. Wir haben auch gesehen, wie Kubernetes verwendet wird, um Containeranwendungen zu verwalten. Wir haben auch gesehen, wie Docker und Kubernetes zusammenarbeiten.
