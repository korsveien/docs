Fag 🪚
======

Systemutvikling
---------------

### God praksis

#### Expand and contract

https://martinfowler.com/bliki/ParallelChange.html

Sikkerhet
---------

-	Sertifikater
	-	X509
	-	pkcs12
-	Oauth

Monitorering
------------

-	Prometheus
-	Grafana
-	pghero

Nettverk
--------

-	Apple Bonjour

Databaser
---------

### Postgres

### SQL

Plattform
---------

### Terraform

### Docker

### Kubernetes

Kubernetes
==========

Konsepter
---------

Se [dokumentasjon](https://kubernetes.io/docs) for detaljer.

### Pods

Som regel en samling av containere som alltid vil kjøre på samme host og som deler ressurser som minne og lagring. Om podden flyttes vil alt den inneholder flyttes. Kan dermed tenkes på som en slags *logisk host*.

### Workload

En applikasjon i Kubernetes som består av pods. Noen workloads kommer ut av boksen og kalles *Workload Resources*. Disse inkluderer *Deployments*, *ReplicaSets* og *Jobs*.

### Deployments

Ved å definere en *ønsket tilstand* vil Deployments sørge for at endringer blir utført for å oppnå denne tilstanden. Som eksempel deployer man applikasjoner ved å oppdatere image-tag i specc-en til en Deployment. Dette er nå ny ønsket tilstand. Endring til denne tilstanden gjøres i dette eksempelet ved å opprette et nytt *ReplicaSet* og draine det gamle. (Så lenge *StrategyType* i Deployment er satt til *RollingUpdate*).

### ReplicaSets

Sørger for at et definert antall pods alltid kjører. ReplicaSets blir håndert av Deployments og bør sjelden brukes direkte.

### Nodes

En virtuell eller fysisk maskin som kjører *Pods*. Hver node inneholder følgende komponenter:

#### kubelet

Sørger for at containere kjører i en Pod.

#### kube-proxy

Håndterer nettverksregler ved å filtrere trafikk inn og ut.

#### container runtime

Programvaren som kjører containere, som regel [containerd](https://containerd.io/docs/).

### Control Plane

En samling komponenter som håndterer *Nodes*, *Pods*, skedulering og responderer på events.

#### kube-apiserver

#### etcd

#### kube-scheduler

#### kube-controller-manager

#### cloud-controller-manager

#### kubectl

#### krew

#### Helm

Programmeringsspråk
-------------------

### Go

### Lua

### Swift

Leseliste
---------

-	[Kubernetes in Action](https://www.manning.com/books/kubernetes-in-action)
-	[Core Kubernetes](https://www.manning.com/books/core-kubernetes)
-	[Accelerate](https://books.apple.com/no/book/accelerate-the-science-of-lean-software-and/id1604511060)
