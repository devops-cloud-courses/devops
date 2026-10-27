<!-- .slide: class="center-slide" -->
<span class="section-badge">Partie 07</span>

## Continuous Deployment

----

<!-- .slide: class="center-slide" -->
### S'appuie sur le Continuous Delivery

<img src="img/wf-cdeployment.png" class="diagram-light" />

----

### Qu'est ce que le continuous deployment

> Le continuous deployment ajoute la dimension de mise en production automatique au continuous delivery

----

### Etre sûr de ses tests

* La validation par les tests doit être **béton** <!-- .element: class="fragment fade-up" -->
* Il faut donc un niveau de maturité des tests suffisant <!-- .element: class="fragment fade-up" -->

----

### Livrer au commit

* La mise en place du continuous delivery permet de livrer directement à chaque commit <!-- .element: class="fragment fade-up" -->
* Livrer souvent permet de livrer peu de changements à chaque fois, et donc moins de régression en cas d'erreur <!-- .element: class="fragment fade-up" -->
* Il est plus simple de faire un rollback sur une fonctionnalité que sur 15 --> Moins de désagréments pour les clients <!-- .element: class="fragment fade-up" -->

----

### Compétences / Outils

* Outil de déploiement/orchestrateur : puppet, docker, rancher, swarm, kubernetes, ... <!-- .element: class="fragment fade-up" -->
* Outils de scripting : python, powershell, bash, ... <!-- .element: class="fragment fade-up" -->
* Load Balancer : Nginx, HaProxy, Traefik, ... <!-- .element: class="fragment fade-up" -->
