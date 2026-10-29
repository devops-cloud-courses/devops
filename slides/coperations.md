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

* **Distributed Tracing**: Track a single user request end-to-end across microservices using a shared trace ID
* **`OpenTelemetry` (`OTel`)**: The cloud-native industry standard for collecting and correlating metrics, logs, and traces

<img src="img/observability.svg" alt="Three Pillars of Observability and OpenTelemetry architecture diagram" />

----

### Infrastructure as Code & Immutable Infra

> Automatically provision machines and all dependencies required for applications to run properly

* **Pets vs. Cattle**: Stop manually patching long-lived servers (*Pets*); treat infrastructure as disposable, reproducible units provisioned from code (*Cattle*)
* **Immutable Infrastructure**: Never modify servers in place—replace them with freshly built images or containers on every change

----

### Auto-Scaling

> Dynamically adjust compute capacity to match real-time demand and optimize cloud cost

* **Workload Auto-Scaling**: `HPA` (Horizontal Pod Autoscaler), `VPA`, and **`KEDA`** (event-driven scaling on queue depth, HTTP traffic, or custom `Prometheus` metrics, including scale-to-zero)
* **Node / Cluster Auto-Scaling**: **`Karpenter`** and Cloud Cluster Autoscalers provision right-sized compute nodes in seconds

----

### SRE Fundamentals: SLI, SLO, SLA & Error Budgets

> Resolving the tension between **Dev velocity** and **Ops stability** through objective data

* **`SLI` (Service Level Indicator)**: Quantitative measure of service health (e.g., `HTTP 2xx` rate, `p99` latency `< 200 ms`)
* **`SLO` (Service Level Objective)**: Target reliability threshold for an SLI (e.g., `99.9%` availability over 30 days)
* **`SLA` (Service Level Agreement)**: External business contract defining penalties if reliability commitments are breached
* **`Error Budget` (`100% - SLO`)**: Allowed unreliability (e.g., `0.1%` = `43 min/month`)—while budget remains, ship fast; if exhausted, prioritize reliability

----

### Chaos Engineering & Blameless Culture

> Proactively test system resilience in production before real outages happen

* **Chaos Engineering**: Inject controlled failures (terminate instances, add network latency, simulate zone outages) to verify auto-healing and fallback mechanisms
* **Blameless Post-Mortems**: Focus on fixing systemic root causes and automated guardrails rather than blaming individuals

----

### Skills / Tools

* Observability & Metrics: `OpenTelemetry` (`OTel`), `Prometheus` / `VictoriaMetrics` / `Thanos`, `Grafana`, `Datadog`, `Cilium Hubble` (`eBPF`), ...
* Logs & Distributed Tracing: `Grafana Loki`, `Grafana Tempo`, `Jaeger`, `OpenSearch` / `Elasticsearch`, `Fluent Bit` / `Vector`, ...
* Infrastructure & Policy as Code (`IaC` / `PaC`): `Terraform` / `OpenTofu`, `Pulumi`, `Crossplane`, `Ansible`, `Packer`, `OPA` / `Kyverno`, ...
* Auto-Scaling, Chaos & Incident Response: `KEDA`, `Karpenter`, `Chaos Mesh`, `LitmusChaos`, `PagerDuty` / `Grafana OnCall`, ...
* Advanced Linux, cloud-native networking, and distributed systems skills
