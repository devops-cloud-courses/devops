## DevOps Patterns

----

### Dev and Ops Collaboration

<img src="img/type-1.svg" alt="Dev and Ops Collaboration topology" />

* The "Holy Grail" of DevOps
* Work across separate products
* Ops must be comfortable with Git, and Devs with production concerns

----

### Fully Shared Ops Responsibilities

<img src="img/type-2.svg" alt="Fully Shared Ops Responsibilities topology" />

* Little separation between Devs and Ops
* Ops are fully integrated within the Dev team
* Focused on a single product or service

----

### Ops as Infrastructure-as-a-Service

<img src="img/type-3.svg" alt="Ops as Infrastructure-as-a-Service topology" />

* Common when using public or private cloud platforms
* Follows TDD, CI, iterative development, and related practices
* Remains a Dev-driven team consuming platform services

----

### DevOps as an External Service

<img src="img/type-4.svg" alt="DevOps as an External Service topology" />

* Also known as DevOps-as-a-Service
* Devs rely on external providers or cloud services (AWS, Azure, GCP, ...)
* Typically suited for smaller teams

----

### Temporary DevOps Team

<img src="img/type-5.svg" alt="Temporary DevOps Team topology" />

* Acts as a bridge between Devs and Ops
* Has a limited lifespan, unlike Anti-pattern B (DevOps Team Silo)
* Goal is to bring Dev and Ops closer together and evolve company practices

----

### DevOps Advocacy Team

<img src="img/type-6.svg" alt="DevOps Advocacy Team topology" />

* Helps spread and facilitate DevOps practices
* Especially effective when the gap between Dev and Ops is wide
* Speaks the language of both Devs and Ops

----

### SRE Model

<img src="img/type-7.svg" alt="Google SRE Model topology" />

* Google's Site Reliability Engineering model
* Heavily automates deployment and operations
* Can reject releases if code or operational quality standards are not met

----

### Container-Driven Collaboration

<img src="img/type-8.svg" alt="Container-Driven Collaboration topology" />

* The container becomes the universal delivery artifact
* Breaks down if Devs ignore production constraints
