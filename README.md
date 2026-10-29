# DevOps in a Nutshell

An interactive presentation on **DevOps Culture, Organizational Topologies, CI/CD Pipelines, GitOps, Cloud-Native Observability, and Site Reliability Engineering (SRE)**, powered by [Reveal.js 6.0.2](https://revealjs.com/).

* **Live Presentation:** [https://devops-cloud-courses.github.io/devops](https://devops-cloud-courses.github.io/devops)
* **PDF Export View:** [https://devops-cloud-courses.github.io/devops/?print-pdf&pdfSeparateFragments=false](https://devops-cloud-courses.github.io/devops/?print-pdf&pdfSeparateFragments=false)

---

## Course Curriculum

1. **Agility Foundations** (`slides/agilite.md`)
   * Traditional V-Model / Waterfall (`img/waterfall.svg`) vs. iterative delivery (`img/agility.svg`)
   * The Agile Manifesto (4 core values, 12 principles) and Scrum framework
   * Why Agility alone stops at the staging boundary
2. **DevOps Philosophy & Metrics** (`slides/devops.md`)
   * Devs vs. Ops conflicting incentives and the *Wall of Confusion* (`img/wall-of-confusion.svg`)
   * Extending Agile principles from development through operations (`img/devops.svg`)
   * The 5 **CALMS** pillars (`Culture`, `Automation`, `Lean`, `Measurement`, `Sharing`)
   * Measuring software delivery performance with **DORA Metrics** (`Deployment Frequency`, `Lead Time for Changes`, `Change Failure Rate`, `Failed Deployment Recovery Time / MTTR`)
3. **Organizational Anti-Patterns** (`slides/antipattern.md`)
   * 7 common DevOps organizational anti-patterns (`img/anti-type-a.svg` – `img/anti-type-g.svg`)
   * Siloed Dev and Ops, "NoOps" pitfalls, DevOps as a separate isolated silo, and Ops embedded without authority
4. **Organizational Patterns & Topologies** (`slides/pattern.md`)
   * 8 proven DevOps & SRE team topologies (`img/type-1.svg` – `img/type-8.svg`)
   * Smooth Dev & Ops collaboration, the **Google SRE Model**, Ops as an Infrastructure-as-a-Service platform, and temporary enabling teams
5. **Working in a DevOps Team** (`slides/equipe.md`)
   * Agile ceremonies, Pair & Mob Programming, Coding Dojo, and **TDD / BDD**
   * Distributed Version Control with `Git` (`GitHub`, `GitLab`, `Bitbucket`) and Pull Request code reviews
   * **Gitflow** (`img/gitflow.svg`) vs. **Trunk-Based Development & Feature Flags** (`img/trunk-based.svg` — `OpenFeature`, `LaunchDarkly`, `Unleash`, `Flagsmith`)
6. **Continuous Integration (CI)** (`slides/cintegration.md`)
   * Automated CI pipeline workflow (`img/wf-cintegration.svg` — `GitHub Actions`, `GitLab CI`, `Tekton`, `Dagger`) and **The Testing Pyramid** (`img/testing-pyramid.svg`)
   * Unit (`JUnit 5`, `pytest`, `Vitest`), Integration & Contract (`Testcontainers`, `Pact`, `WireMock`), E2E (`Playwright`, `Cypress`), and Load testing (`Grafana k6`, `Gatling`, `Locust`)
   * Static Code Analysis (`SonarQube`, `ESLint`, `Ruff`, `golangci-lint`) and **Shift-Left Security** (`Semgrep`, `CodeQL`, `Trivy`, `Snyk`, `Syft` SBOM, `OWASP ZAP`, `Nuclei`)
7. **Continuous Delivery (CD)** (`slides/cdelivery.md`)
   * CD promotion workflow (`img/wf-cdelivery.svg`), end-to-end traceability, and **Semantic Versioning (`SemVer 2.0.0`)**
   * **Artifact Registries & Supply Chain Provenance**: immutable `OCI` artifacts (`Harbor`, `GHCR`, `Artifactory`), cryptographic signing (`Sigstore Cosign`), `SLSA` provenance, and `SBOM` (`CycloneDX`, `SPDX`)
8. **Continuous Deployment & GitOps** (`slides/cdeployment.md`)
   * Automated production release workflow (`img/wf-cdeployment.svg`) and why every change goes straight to production
   * **Progressive Delivery & Zero-Downtime Releases**: Rolling Updates, Blue/Green, Canary Analysis (`Argo Rollouts`, `Flagger`), and Feature Flags / Dark Launches
   * **GitOps** pull-based continuous reconciliation (`img/gitops.svg` — `Argo CD`, `Flux`)
9. **Continuous Operations & SRE** (`slides/coperations.md`)
   * Operations workflow (`img/wf-coperations.svg`) and the **Three Pillars of Observability** (`Metrics`, `Logs`, `Traces`) unified with `OpenTelemetry` (`img/observability.svg` — `Prometheus`, `Grafana Mimir/Loki/Tempo`, `Jaeger`, `Datadog`)
   * **Immutable Infrastructure & IaC** (`Terraform` / `OpenTofu`, `Pulumi`, `Crossplane`, `Docker`, `Kubernetes`, `Helm`, `Packer`, `Ansible`)
   * **Auto-Scaling & Traffic Management** (`Kubernetes Gateway API`, `Envoy`, `Cilium` eBPF, `Traefik`, `HPA`, `KEDA`, `Karpenter`)
   * **Site Reliability Engineering (SRE)**: `SLI`, `SLO`, `SLA`, Error Budgets, **Chaos Engineering** (`Chaos Mesh`, `LitmusChaos`, `AWS FIS`), and Blameless Post-Mortems
10. **Continuous Everything & Conclusion** (`slides/ceverything.md`, `slides/conclusion.md`)
    * The DevOps Infinity Loop (`img/devops-infinity-workflow.svg`) and Continuous User Feedback (`OpenTelemetry RUM`, `PostHog`, `Sentry`)
    * Modern extensions: **DevSecOps**, **Platform Engineering (`IDP` / `Backstage`)**, **FinOps & GreenOps** (`OpenCost`, `Kubecost`, `Kepler`), and **MLOps / LLMOps**
    * Key takeaways and foundational references (*The Twelve-Factor App*, *Accelerate / DORA*, *Google SRE Books*, *DevOps Topologies*, *The DevOps Handbook*)

---

## Repository Structure

```text
.
├── index.html          # Reveal.js 6.0.2 entrypoint (jsDelivr CDN, zero-build setup)
├── css/
│   └── custom.css      # Custom light theme, typography (Inter & JetBrains Mono), and responsive layout
├── img/                # Custom vector SVG architecture diagrams & author avatars
└── slides/             # Modular Markdown slide decks loaded dynamically by Reveal.js
```

---

## Running Locally

Because Reveal.js loads external Markdown files (`slides/*.md`) via `fetch`, serve the repository over a local HTTP server rather than opening `index.html` via `file://`:

### Option 1: Python (built-in)
```bash
python3 -m http.server 8000
```
Then open [http://localhost:8000](http://localhost:8000).

### Option 2: Node.js (`npx`)
```bash
npx serve .
```

### Option 3: Docker (`nginx`)
```bash
docker run --rm -p 8080:80 -v "$PWD":/usr/share/nginx/html:ro nginx:alpine
```
Then open [http://localhost:8080](http://localhost:8080).

---

## Exporting to PDF (Chrome / Chromium)

1. Open [https://devops-cloud-courses.github.io/devops/?print-pdf&pdfSeparateFragments=false](https://devops-cloud-courses.github.io/devops/?print-pdf&pdfSeparateFragments=false)
2. Press `Cmd + P` (macOS) or `Ctrl + P` (Windows/Linux)
3. Configure the print dialog settings:

| Setting | Value |
|---|---|
| **Destination** | Save as PDF |
| **Pages** | All |
| **Margins** | None / Default |
| **Options** | Enable **Background graphics** |

---

## Authors

* **Laurent Grangeau** — Cloud Solution Architect @ Google ([@laurentgrangeau](https://twitter.com/laurentgrangeau) | [github.com/laurentgrangeau](https://github.com/laurentgrangeau))
* **Arthur Mauvezin** — DevOps Engineer @ Ouidou Consulting ([@arthurmauvezin](https://twitter.com/arthurmauvezin) | [github.com/arthurmauvezin](https://github.com/arthurmauvezin))
