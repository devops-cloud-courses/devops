# Draft cours DevOps ECE

## Introduction
### Qui on est 
* Présentation des intervenants (Arthur et Laurent) et des sociétes des intervenants
* Quel est notre métier
### Pourquoi ce cours et quoi en attendre
* C'est une formation qui est proposée en interne dans les sociétés
* Les sujets traités dans cette formation augmentent considérablement la valeur des profils sur le marché

## DevOps

### Les différentes sous parties du Devops
* Mentalité /
* Bonnes pratiques
* Continous Integration
* Continuous Delivery

## Continuous Integration

Quoi 
qui 
ou
quand
comment 
combien 
pourquoi

## Reveal useful
<img src="images/waterfall.png">
<img src="images/waterfall.png" height="200" width="200" />
<img src="images/waterfall.png" style="background:none; border:none; box-shadow:none;"/>
![Image](https://images.techhive.com/images/article/2016/03/amazon-cloud-dc-map-100651841-large.idge.gif)
<img src="https://www.agileit.com/wp-content/uploads/2017/11/az-graphic-two.png" width="35%" />

- Value
 - Subvalue


## Parties
### Intro
### Situation actuelle / Pourquoi le DevOps ?
* Cycle en V
* Cycle de dev long
* invention de l'agilité
* qu'est ce que l'agilité 
* Limites de l'agilité
  * Dépassement de projets en thunes en temps
  * Et les autres autour (PO, Resp produit, User) ? Tous le monde n'est pas concerné

Notes:
* Suivi des specs de bases vers un livrable qui correspond pas > agilité
* Cycle en V --> Constat : peu de projets sont réussis, dépassent le délai et un paquet des fontionnalités développées sont inutilisées
* Ken Shwaber et consort se sont réunis pour faire une évole à l'XP --> Manifeste agile [image des cases du cycle en V vs mini cycles en V)

### Qu'est ce que le DevOps
#### Devs vs Ops
* Devs: Toute personne impliqué dans la fabrication du logiciel jusqu’à la livraison de celui-ci => recherche le changement continuelle afin de satisfaire le client final (nouvelles fonctionnalités amélioration des performances, expérience utilisateur)
* Ops: Toute personne impliqué dans la maintenance et l’exploitation de la production => recherche la stabilité organisationnelle et de la plateforme de production afin de maintenir un niveau de satisfaction client élevé
#### Definition
Le DevOps est un mouvement visant à l’alignement de l’ensemble des équipes du système d’information sur un objectif commun, à commencer par les équipes de Dev chargées de faire évoluer le système d’information et les Ops responsables des infrastructures.
DevOps est la pratique où les ingénieurs de développement (Dev) et d’exploitation (Ops) participent ensemble à l’intégralité du cycle de vie de services : de la conception au support de production en passant par le développement.
#### Faire tomber le mur
Faire tomber le mur de la confusion
#### L'agile et le scrum dans tout ça
#### Keep CALMS: Pilier du DevOps
* Culture : Les individus et les interactions plutôt que les processus et les outils
* Automatisation : Les machines sont vraiment bonnes à faire la même tâche encore et encore.
* Lean : Les équipes Devs et les équipes Ops doivent trouver des moyens pour réduire les déchets et rationaliser les processus en entier.
* Mesure : Etre capable de mesurer les performances et les améliorations apportées au produit #Monitoring #KPI
* Sharing/Solidarité : Il est important de partager les avantages entre les équipes ==> #Communication #Collaboration #Partage #Interaction

Notes:
* DevOps s'appuie sur l'agilité 
* Je comprend pas ça marche sur mon poste
* DevOps == Petite itérations qui visent à être complète (build, test, deliver, deploy, feedback)
* Piliers de l'agilité et piliers du DevOps (a voir sur le net)

### Continous Integration
#### Qu'est ce que l'intégration
#### Gitflow
#### Build
#### Test
* unit
* fonctionnal / end-to-end
* load
* security
* ...

### Continous Delivery

### Continuous Deployment
### Continuous Operations
### Continuous everything
* Mettre l'image avec toutes les flèches de la vidéo
* Etre réactif
* Etre réactif !!! (débug, deployement, ) 

### Conclusion
* Métier très logique

### Glossaire
* DAT = dossier d'architecture technique (fait dès le début) --> Adaptation au changemetn plutot que suivre le plan



* livrer souvent, livrer vite, livrer sans régression
* Développer avec la cible (tous les environements son ISO)
* Culture des logs, de la mesure
* le dev a le métier qui est entre la prod et ĺ'exploitant (bof comme phrase)
* Feature flipping
* Test AB
* TDD - Test Driven Development
* BDD - Behavior Driven Development

* un max de résilience (capacité de mon app à rendre du service même en cas de tombage d'une partie du système)

* Waterfall
Waterfall : Design > Code > Test > Deploy
Agile: Design > Code > Test > Design > Code > Test > Design > Code > Test > Deploy
Devops: Design > Code > Test > Deploy > Design > Code > Test > Deploy > Design > Code > Test > Deploy
(With big design at first and little design then)

Plan > Code > Build > Test > Release > Deploy > Operate
* Agile (Plan > Code > Build )
* COntinuous integration (Plan > Code > Build > Test)
* Continuous delivery (Plan > Code > Build > Test > Release)
* Continuous Deployment (Plan > Code > Build > Test > Release > Deploy)
* Continuous Operations (Plan > Code > Build > Test > Release > Deploy > Operate)
  * Continuous optimiser le temps perdu et feedback de la prod et amélioration continue sur tout le cycle 

* TTM - Time to market
* Equipe pluridisciplinaire - tout le monde doit tout savoir (très compliqué à faire) - Couteau suisse
* MVP - Minimum viable product
* Test fonctionnels - Cucumber (BDD) scenario de gherkin - Attention à ne pas trop en faire (très lourd à garder à jour) - trouver son rythme, son niveau d'acceptation
* Sonar - qualité du code source
* Réduire toutes les taches et automatiser un maximum
* Tests de charge - 
* Jenkins - pipeline - validation + tampon de l'appli
* Toutes les confs sont du code - donc faisable par tous les devs logiques

* Truck/Bus factor : si quelqu'un se fait écraser en rentrant du taff, il faut qu'elle puisse être remplacée facilement
* Protocole de validation post mise en prod et suivi après les mises en prod + test a/b pour ouvrir petit à petit pour tout le monde. Le dev suit ce qui se passe avec un l'ops pour vérifier si ça se passe bien

COntinuous Operations:
* vérification de la résilience (rien a foutre dans cette partie mais il fallait le noter)
* Recolte des metrics : Monitoring
* Centralisation des logs
* Scalabilité automatique
* Analyse des tiers de charges (monitoring+logs) - pic d'activités
* Chaos monkey - péter un truc au hasard en prod et vérifier que ca continue à marcher ou que ca remarche vite - on peut faire des chaos monkey à la main en butant un site de manière volontaire
PRA - Plan de reprise de l'activité

* Livraison à chaque sprint == le rève !!

RAF:
* Reste à rendre scalable
* Démarche Lean --> Commit to prod == méga dream
* Gestion des perturbations - Build vs Run (que faire quand beaucoup de retour de la prod)
* Tout le monde n'est pas vraiment polyvalent
* Remise en question perpetuelle
* Un nouvel arrivant prend super cher pour apprendre tout en arrivant

* Sonar
* 12 factor app

COnclusion d'un devops:
* Tout le monde peut/doit être moteur
* NE pas hésiter à automatiser ou a proposer une automatisation


--------------------------------
## Deuxième pres
* Automation engineer - un bon titre je trouve
* 

* 12 factor app
* Difficulté de Docker en prod
* Pet vs Cattle
* Gestion de logs
* Gestion du monitoring

