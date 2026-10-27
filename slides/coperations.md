<!-- .slide: class="center-slide" -->
<span class="section-badge">Partie 08</span>

## Continuous Operations

----

<!-- .slide: class="center-slide" -->
### S'appuie sur le Continuous Deployment

<img src="img/wf-coperations.png" class="diagram-light" />

----

### Récolte des metrics

Monitoring des applications:
* Ressources (RAM, CPU, Network,...) <!-- .element: class="fragment fade-up" -->
* Etat (UP/Down) <!-- .element: class="fragment fade-up" -->
* Temps de réponse <!-- .element: class="fragment fade-up" -->
<!-- .element: class="grid-3" -->

----

### Centralisation des logs

Vue aggrégée des logs permettant de dégager des metrics intérressantes :
* L'usage <!-- .element: class="fragment fade-up" -->
* Alertes critiques <!-- .element: class="fragment fade-up" -->
* Temps de réponse <!-- .element: class="fragment fade-up" -->
* Nombre de bugs <!-- .element: class="fragment fade-up" -->
<!-- .element: class="grid-2" -->

----

### Scalabilité automatique

* Permettre aux applications de se scaler automatiquement en cas d'un afflux trop important de demandes <!-- .element: class="fragment fade-up" -->
* L'afflux est mesuré grâce aux solutions de collecte de metrics et de centralisation des logs <!-- .element: class="fragment fade-up" -->

----

### Infrastructure as Code

> Déployer automatiquement les machines et toutes les dépendances nécéssaires au bon fonctionnement des applicatifs

----

### Compétences / Outils

* Monitoring : Centreon, Prometheus, InfluxDB, Grafana <!-- .element: class="fragment fade-up" -->
* Centralisation des logs : ElasticSearch, Logstash, Kibana, Filebeat, ... <!-- .element: class="fragment fade-up" -->
* Outils d'infra as code : Terraform, Puppet, Ansible, Chef, Salt, ... <!-- .element: class="fragment fade-up" -->
* Compétences système et réseau avancées <!-- .element: class="fragment fade-up" -->
<!-- .element: class="grid-2" -->
