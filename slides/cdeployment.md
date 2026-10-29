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

### Progressive Delivery & Deployment Strategies

> Decouple **deployment** (shipping code to servers) from **release** (exposing features to users)

* **Rolling Update**: Gradually replace old instances with new ones with zero downtime
* **Blue / Green Deployment**: Run two identical production environments (`Blue` live, `Green` new) and switch router traffic instantly
* **Canary Release**: Route a small fraction of live traffic (`1%` → `10%` → `100%`) to the new version while monitoring error rates
* **Feature Flags**: Enable or disable features dynamically at runtime for specific user segments without redeploying

----

### GitOps

> Git as the single source of truth for declarative infrastructure and application deployment

* Desired production state is fully declared in Git (`Kubernetes` manifests, `Helm` charts, `Kustomize`)
* An in-cluster controller (`Argo CD`, `Flux`) continuously pulls and reconciles live cluster state against Git
* Provides automatic **drift detection**, complete audit trails, and instant rollbacks via `git revert`

----

### Skills / Tools

* Orchestration & Packaging: `Kubernetes`, `Docker`, `Helm`, `Kustomize`, `Cloud Run`, ...
* GitOps & Progressive Delivery: `Argo CD`, `Flux`, `Argo Rollouts`, `Flagger`, `OpenFeature` / `LaunchDarkly`, ...
* Ingress, Service Mesh & Load Balancing: `Envoy`, `Traefik`, `NGINX`, `HAProxy`, `Istio`, `Cilium`, ...
* Scripting & Automation: `Python`, `Bash`, `Go`, ...
