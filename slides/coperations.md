## Continuous Operations

----

### Builds on Continuous Deployment

<img src="img/wf-coperations.svg" alt="Continuous Operations workflow building on Continuous Deployment" />

----

### Metrics Collection

> Application monitoring across key operational signals

* Resources (`RAM`, `CPU`, `Network`, ...)
* Health status (`UP` / `Down`)
* Response time

----

### Log Centralization

> Aggregated view of logs to extract valuable metrics

* Usage
* Critical alerts
* Response time
* Number of bugs

----

### Distributed Tracing & Observability

> The **3 Pillars of Observability**: **Metrics** (*what* is broken), **Logs** (*why* it broke), and **Traces** (*where* it broke)

* **Distributed Tracing**: Track a single user request end-to-end across dozens of microservices using a shared trace ID
* Pinpoints latency bottlenecks, cascading failures, and broken service dependencies
* **`OpenTelemetry` (`OTel`)**: The cloud-native industry standard for collecting and exporting metrics, logs, and traces

----

### SRE Fundamentals: SLI, SLO, SLA & Error Budgets

> Resolving the tension between **Dev velocity** and **Ops stability** through objective data

* **`SLI` (Service Level Indicator)**: Quantitative measure of service health (e.g., `HTTP 2xx` rate, `p99` latency `< 200 ms`)
* **`SLO` (Service Level Objective)**: Target reliability threshold for an SLI (e.g., `99.9%` availability over 30 days)
* **`SLA` (Service Level Agreement)**: External business contract defining penalties if reliability commitments are breached
* **`Error Budget` (`100% - SLO`)**: Allowed unreliability (e.g., `0.1%` = `43 min/month`)—while budget remains, ship fast; if exhausted, prioritize reliability

----

### Auto-Scaling

* Allow applications to scale automatically when facing a sudden surge in traffic
* Traffic surges are measured through metrics collection and centralized logging solutions

----

### Infrastructure as Code & Immutable Infra

> Automatically provision machines and all dependencies required for applications to run properly

* **Pets vs. Cattle**: Stop manually patching long-lived servers (*Pets*); treat infrastructure as disposable, reproducible units provisioned from code (*Cattle*)
* **Immutable Infrastructure**: Never modify servers in place—replace them with freshly built images or containers on every change

----

### Chaos Engineering & Blameless Culture

> Proactively test system resilience in production before real outages happen

* **Chaos Engineering**: Inject controlled failures (terminate instances, add network latency, simulate zone outages) to verify auto-healing and fallback mechanisms
* **Blameless Post-Mortems**: Focus on fixing systemic root causes and automated guardrails rather than blaming individuals

----

### Skills / Tools

* Observability & Metrics: `OpenTelemetry`, `Prometheus`, `Grafana`, `Datadog`, ...
* Logs & Distributed Tracing: `Grafana Loki`, `Jaeger`, `Grafana Tempo`, `Elasticsearch` / `Kibana`, `Fluent Bit`, ...
* Infrastructure as Code (`IaC`): `Terraform` / `OpenTofu`, `Pulumi`, `Ansible`, `Crossplane`, ...
* Chaos Engineering & Incident Response: `Chaos Mesh`, `LitmusChaos`, `PagerDuty`, ...
* Advanced system, cloud, and networking skills
