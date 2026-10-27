<!-- .slide: class="center-slide" -->
<span class="section-badge">Partie 04</span>

## Travailler dans une équipe DevOps

----

### L'utilisation d'un VCS

* VCS: Version Control System <!-- .element: class="fragment fade-up" -->
* Gestionnaire de source <!-- .element: class="fragment fade-up" -->
* Capable de naviguer à travers un historique de commit <!-- .element: class="fragment fade-up" -->
* Capable de travailler dans des branches séparées <!-- .element: class="fragment fade-up" -->
<!-- .element: class="grid-2" -->

----

#### Présentation d'un VCS : Git

* Créé en 2005 par Linus Torvalds <!-- .element: class="fragment fade-up" -->
* Le plus populaire <!-- .element: class="fragment fade-up" -->
* Gratuit et open source <!-- .element: class="fragment fade-up" -->
* Système distribué <!-- .element: class="fragment fade-up" -->
<!-- .element: class="grid-2" -->

----

#### Serveurs Git connus

* Github <!-- .element: class="fragment fade-up" -->
* Gitlab <!-- .element: class="fragment fade-up" -->
* Bitbucket <!-- .element: class="fragment fade-up" -->
<!-- .element: class="grid-3" -->

----

#### Utiliser Git sur des petits projets

On peut travailler sur une seule branche

Problèmes:
* Conflits récurrents si plusieurs personnes commit en même temps <!-- .element: class="fragment fade-up" -->
* Séparer les évolutions fonctionnelles différentes <!-- .element: class="fragment fade-up" -->
* Comment savoir de quelle commit repartir quand il y a un bug en production <!-- .element: class="fragment fade-up" -->

----

<!-- .slide: class="center-slide" -->
### Utiliser Git en équipe : Gitflow

<img src="https://i.ytimg.com/vi/w2r0oLFtXAw/maxresdefault.jpg" class="diagram-light" />

----

### Apprendre à utiliser Git

* [Le site officiel](https://git-scm.com/book/en/v2) <!-- .element: class="fragment fade-up" -->
* [Tutoriel pas à pas](https://www.atlassian.com/git/tutorials/what-is-git) <!-- .element: class="fragment fade-up" -->
<!-- .element: class="grid-2" -->

----

### Pratiques agiles: Les cérémonies

* Sprint Planning <!-- .element: class="fragment fade-up" -->
* Stand-up meeting <!-- .element: class="fragment fade-up" -->
* Sprint review / Demo <!-- .element: class="fragment fade-up" -->
* Sprint retrospective <!-- .element: class="fragment fade-up" -->
<!-- .element: class="grid-2" -->

----

#### Sprint Planning

* Temps: 4h pour un sprint de 2 semaines <!-- .element: class="fragment fade-up" -->
* Participants: Tout le monde (Dev, PO, SM) <!-- .element: class="fragment fade-up" -->
* But: Velocité, Definition of Done, Liste des tâches à faire sur le sprint <!-- .element: class="fragment fade-up" -->

> Vélocité: Valeur indicative de la capacité de l'équipe à réaliser N tâches au cours d'un sprint <!-- .element: class="fragment fade-up" -->

----

#### Stand-up meeting

* Temps: 15 minutes tous les matins <!-- .element: class="fragment fade-up" -->
* Participants: Tout le monde (Dev, PO, SM) <!-- .element: class="fragment fade-up" -->
* But: Discuter des problèmes rencontrés par chacun <!-- .element: class="fragment fade-up" -->

----

#### Sprint Review / Demo

* Temps: 1-2h pour un sprint de 2 semaines <!-- .element: class="fragment fade-up" -->
* Participants: Tout le monde (Dev, PO, SM) et toutes personnes intérressées par l'avancement du projet <!-- .element: class="fragment fade-up" -->
* But: Démonstration du produit et récupération du feedback <!-- .element: class="fragment fade-up" -->

----

#### Sprint retrospective

* Temps: 2h pour un sprint de 2 semaines <!-- .element: class="fragment fade-up" -->
* Participants: Tout le monde (Dev, PO, SM); la présence du PO est optionnelle <!-- .element: class="fragment fade-up" -->
* But: Débrieffer sur ce qui a marché, ce qui n'a pas marché, ce qu'on pourrait améliorer <!-- .element: class="fragment fade-up" -->

----

### DevOps team practices

* Pull Request / Code Review <!-- .element: class="fragment fade-up" -->
* Coding Dojo <!-- .element: class="fragment fade-up" -->
* Pair Programming <!-- .element: class="fragment fade-up" -->
* Technical Breakfast <!-- .element: class="fragment fade-up" -->
<!-- .element: class="grid-2" -->

----

#### Pull Request / Code Review

* Au lieu de merger une branche dans une autre, faire une demande de merge <!-- .element: class="fragment fade-up" -->
* D'autres membres de l'équipe vont effectur une revue de code des changements apportés <!-- .element: class="fragment fade-up" -->
* Permet une baisse des bugs détectables à l'oeil nu <!-- .element: class="fragment fade-up" -->

----

#### Pair programming

* Programmer à deux : Un **driver** et un **navigator** <!-- .element: class="fragment fade-up" -->
* Les rôles sont échangés régulièrement <!-- .element: class="fragment fade-up" -->
* Permet la montée en compétence des personnes impliquées <!-- .element: class="fragment fade-up" -->
* Permet au driver de se concentrer sur les tâches de développement <!-- .element: class="fragment fade-up" -->
* Permet au navigator de se concentrer sur le design et les problèmes de fond <!-- .element: class="fragment fade-up" -->

----

#### Coding Dojo

* Rencontre entre plusieurs personnes souhaitant se confronter à un défi de programmation <!-- .element: class="fragment fade-up" -->
* Le but est de proposer la solution la plus optimisée, choisie par l'ensemble des participants <!-- .element: class="fragment fade-up" -->
* Permet de ne pas déclencher des débats d'idée plus tard sur les choix techniques pris dans le passé <!-- .element: class="fragment fade-up" -->

----

#### Technical Breakfast

* Se réunir autour d'un présentateur qui fait un retour d'expérience sur une techno ou méthodo <!-- .element: class="fragment fade-up" -->
* Permet de partager le savoir efficacement au sein d'une entreprise <!-- .element: class="fragment fade-up" -->
* Permet au présentateur d'approfondir ses connaissances pour présenter le sujet <!-- .element: class="fragment fade-up" -->

----

#### Et pleins d'autres ...

* TDD - Test Driven Development <!-- .element: class="fragment fade-up" -->
* BDD - Behavior Driven Development <!-- .element: class="fragment fade-up" -->
* Feature Flipping <!-- .element: class="fragment fade-up" -->
* Test A/B <!-- .element: class="fragment fade-up" -->
<!-- .element: class="grid-2" -->
