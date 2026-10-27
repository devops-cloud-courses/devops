## Continuous Deployment

----

### Builds on Continuous Delivery

<img src="img/wf-cdeployment.svg" alt="Continuous Deployment workflow building on Continuous Delivery" />

----

### What is Continuous Deployment?

> Continuous Deployment adds automatic production deployment on top of Continuous Delivery

----

### Being Confident in Your Tests

* Validation through automated tests must be **rock-solid**
* A sufficient level of test maturity is therefore required

----

### Deploy on Every Commit

* Implementing Continuous Deployment makes it possible to release directly on every commit
* Releasing often means shipping smaller changes each time, and therefore fewer regressions when an error occurs
* It is much easier to roll back 1 feature than 15 --> Less disruption for customers

----

### Skills / Tools

* Deployment / orchestration tools: Puppet, Docker, Rancher, Swarm, Kubernetes, ...
* Scripting tools: Python, PowerShell, Bash, ...
* Load Balancers: Nginx, HAProxy, Traefik, ...
