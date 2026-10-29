## DevOps Patterns

----

### Dev and Ops Collaboration

* The "Holy Grail" of DevOps
* Work across separate products
* Ops must be comfortable with Git, and Devs with production concerns

<img src="img/type-1.svg" alt="Dev and Ops Collaboration topology" />

----

### Fully Shared Ops Responsibilities

* Little separation between Devs and Ops
* Ops are fully integrated within the Dev team
* Focused on a single product or service

<img src="img/type-2.svg" alt="Fully Shared Ops Responsibilities topology" />

----

### Ops as Infrastructure-as-a-Service

* Common when using public or private cloud platforms
* Follows TDD, CI, iterative development, and related practices
* Remains a Dev-driven team consuming platform services

<img src="img/type-3.svg" alt="Ops as Infrastructure-as-a-Service topology" />

----

### DevOps as an External Service

* Also known as DevOps-as-a-Service
* Devs rely on external providers or cloud services (AWS, Azure, GCP, ...)
* Typically suited for smaller teams

<img src="img/type-4.svg" alt="DevOps as an External Service topology" />

----

### Temporary DevOps Team

* Acts as a bridge between Devs and Ops
* Has a limited lifespan, unlike Anti-pattern B (DevOps Team Silo)
* Goal is to bring Dev and Ops closer together and evolve company practices

<img src="img/type-5.svg" alt="Temporary DevOps Team topology" />

----

### DevOps Advocacy Team

* Helps spread and facilitate DevOps practices
* Especially effective when the gap between Dev and Ops is wide
* Speaks the language of both Devs and Ops

<img src="img/type-6.svg" alt="DevOps Advocacy Team topology" />

----

### SRE Model

* Google's Site Reliability Engineering model
* Heavily automates deployment and operations
* Can reject releases if code or operational quality standards are not met

<img src="img/type-7.svg" alt="Google SRE Model topology" />

----

### Container-Driven Collaboration

* The container becomes the universal delivery artifact
* Breaks down if Devs ignore production constraints

<img src="img/type-8.svg" alt="Container-Driven Collaboration topology" />

----

### How to get started

* DevOps can start from the bottom up: a single team can be the driving force
* Start with simple methodologies to apply within a team
* Set up automation solutions:
  * Continuous Integration
  * Continuous Delivery
  * Continuous Deployment
  * Continuous Operations
