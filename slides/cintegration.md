<!-- .slide: class="center-slide" -->
<span class="section-badge">Partie 05</span>

## Continuous Integration

----

### Qu'est ce que l'intégration

* Mettre en commun des parties développées de façon séparées <!-- .element: class="fragment fade-up" -->

----

### CI : Build

> Eviter l'effet : "Eh mais je comprend pas ! Ca marche sur mon poste pourtant"

* Télécharger les dépendances <!-- .element: class="fragment fade-up" -->
* Builder l'application <!-- .element: class="fragment fade-up" -->
<!-- .element: class="grid-2" -->

----

### CI : Tests

* Tester tout ce qu'il est possible de tester de manière automatique <!-- .element: class="fragment fade-up" -->
* C'est à dire : Quasiment tout ! <!-- .element: class="fragment fade-up" -->
* Il existe un grand nombre de types de tests différents <!-- .element: class="fragment fade-up" -->

> Tester, c'est mettre un coup de tampon sur un livrable <!-- .element: class="fragment fade-up" -->

----

#### Tests unitaires

* Tests visant à assurer le bon fonctionnement d'une brique unitairement <!-- .element: class="fragment fade-up" -->
* Ces tests peuvent être réalisés au build, ou juste après le build <!-- .element: class="fragment fade-up" -->

----

#### Tests d'intégration

* Tests s'appuyant sur les tests unitaires <!-- .element: class="fragment fade-up" -->
* Permet de s'assurer que les briques testées unitairement fonctionnent ensemble <!-- .element: class="fragment fade-up" -->
* On réalise souvent des appels externes techniques à une des briques puis on valide le retour <!-- .element: class="fragment fade-up" -->

----

#### Tests fonctionnels / Bout-en-bout

* Aussi appelé tests navigateur <!-- .element: class="fragment fade-up" -->
* On simule les input tels qu'ils seront réalisés par les utilisateurs (scénario de Gherkin) <!-- .element: class="fragment fade-up" -->
* Simulation de cliques, d'entrée de caractères dans un champ texte, scrolling, double tap, ... <!-- .element: class="fragment fade-up" -->
* On valide le retour : l'apparition de la bonne page, de la bonne information, ... <!-- .element: class="fragment fade-up" -->
* Demande des prérequis techniques : id sur chaque élément sélectionnable dans une IHM, ... <!-- .element: class="fragment fade-up" -->

----

#### Tests de charge

* Test visant à s'assurer de la résilience de l'application en cas de montée en charge <!-- .element: class="fragment fade-up" -->
* On part de requêtes simples puis on bascule sur des scénarios représentatifs des actions des utilisateurs <!-- .element: class="fragment fade-up" -->
* On commence par tester avec une seule instance de chaques briques de l'application <!-- .element: class="fragment fade-up" -->
* Puis on augmente le nombre d'instance (**scale**) pour voir comment l'application réagit globalement <!-- .element: class="fragment fade-up" -->
* Cette méthodologie permet de trouver un chemin critique entre nombre d'instances et nombre d'utilisateurs <!-- .element: class="fragment fade-up" -->

----

#### Tests de sécurité

* Test des failles connues (injections, XSS, ...) <!-- .element: class="fragment fade-up" -->
* Charge l'application pour voir comment elle répond <!-- .element: class="fragment fade-up" -->
* Bruteforce <!-- .element: class="fragment fade-up" -->

----

#### Tests : Désavantages

* Long à maintenir : il faut prévoir la mise à jour des tests dans les cycles de développement <!-- .element: class="fragment fade-up" -->
* Long à mettre en place : il existe un grand nombre de technologies diverses et les bencher prend du temps <!-- .element: class="fragment fade-up" -->

----

#### Tests : Conclusion

* Les tests ne sont pas facultatifs <!-- .element: class="fragment fade-up" -->
* Les tests permettent de réduire drastiquement le temps passer à valider un livrable <!-- .element: class="fragment fade-up" -->
* Les tests augmentent notre confiance en nos livrables <!-- .element: class="fragment fade-up" -->
* Les tests permettent de rester concentré sur la création de valeur au lieu de passer son temps à débuguer les applications <!-- .element: class="fragment fade-up" -->

----

### Analyse de code

* Outils d'analyse de code statique ou dynamique <!-- .element: class="fragment fade-up" -->
* Remonte des statistiques sur la qualité du code, les vulnérabilités, les bugs possibles <!-- .element: class="fragment fade-up" -->
* Met en avant les problèmes les plus dangereux <!-- .element: class="fragment fade-up" -->
* Permet une vrai introspection sur la qualité générale du code et sur les efforts à faire pour s'approcher de la perfection <!-- .element: class="fragment fade-up" -->

----

### Compétences / Outils

* Serveurs d'intégration continu : Jenkins, TeamCity, Bamboo, Travis (SaaS), Gitlab, ... <!-- .element: class="fragment fade-up" -->
* Scripting : bash, python, powershell, groovy, ... <!-- .element: class="fragment fade-up" -->
* Building : Maven, MsBuild, NPM, ... <!-- .element: class="fragment fade-up" -->
* Dependency management : Maven, Nuget, Pip, Bower, NPM, ... <!-- .element: class="fragment fade-up" -->
* Unit Tests : JUnit, NUnit, unittest, unit-test, ... <!-- .element: class="fragment fade-up" -->

----

### Compétences / Outils (suite)

* Integration Tests : Failsafe, curl, SoapUI, Postman, ... <!-- .element: class="fragment fade-up" -->
* Functional Tests : Selenium, Cucumber, Test IO, HP UFT, SoapUI, Postman, Ranorex ... <!-- .element: class="fragment fade-up" -->
* Load Tests : JMeter, Gatling, Locust, ... <!-- .element: class="fragment fade-up" -->
* Security Tests : Netsparker, Acunetix, Metasploit <!-- .element: class="fragment fade-up" -->
* Code Analysis : Sonar, Coverity, Fortify <!-- .element: class="fragment fade-up" -->
