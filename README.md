# DevOps in a Nutshell

Interactive [Reveal.js 6.0.2](https://revealjs.com/) presentation introducing **DevOps culture, organizational topologies, CI/CD pipelines, GitOps, Cloud-Native Observability, and Site Reliability Engineering (SRE)**.

---

## Speakers

| Speaker | Role | Links | Avatar Asset |
|---|---|---|---|
| **Laurent Grangeau** | Cloud Solution Architect @ Google | [@laurentgrangeau](https://twitter.com/laurentgrangeau) · [github.com/laurentgrangeau](https://github.com/laurentgrangeau) | `img/avatar-laurent.jpg` |
| **Arthur Mauvezin** | DevOps Engineer @ Ouidou Consulting | [@arthurmauvezin](https://twitter.com/arthurmauvezin) · [github.com/arthurmauvezin](https://github.com/arthurmauvezin) | `img/avatar-arthur.jpg` |

---

## Lecture Syllabus & Pedagogical Flow

The presentation is organized in `index.html` into **13 progressive modules** flowing from software engineering history and organizational design to daily engineering practices, automated delivery pipelines, production operations, and modern cloud-native extensions:

| # | Module | Slide Deck | Key Concepts, Tooling & Vector Diagrams |
|---|---|---|---|
| **1** | **Title & Speakers** | `slides/title.md` | Course cover, speaker links, and *Who are we?* author cards (`img/avatar-laurent.jpg`, `img/avatar-arthur.jpg`) |
| **2** | **Introduction** | `slides/introduction.md` | Course motivation, industry demand, and interactive Reveal.js navigation guide |
| **3** | **Agility Foundations** | `slides/agilite.md` | V-Model / Waterfall (`img/waterfall.svg`), Scrum (`img/agility.svg`), the Agile Manifesto (4 values, 12 principles), and why Agility stops at the staging boundary |
| **4** | **DevOps Philosophy & Metrics** | `slides/devops.md` | Devs vs. Ops conflict, the *Wall of Confusion* (`img/wall-of-confusion.svg`), extending Agile to Operations (`img/devops.svg`), **CALMS** pillars (Culture, Automation, Lean, Measurement, Sharing), and **DORA Metrics** (Deployment Frequency, Lead Time for Changes, Change Failure Rate, Failed Deployment Recovery Time / MTTR) |
| **5** | **Organizational Anti-Patterns** | `slides/antipattern.md` | 7 DevOps organizational anti-patterns (`img/anti-type-a.svg` through `img/anti-type-g.svg`): Dev vs. Ops silos, "No Ops", DevOps-as-a-separate-silo,Ops-embedded-in-Dev without authority, etc. |
| **6** | **Organizational Patterns** | `slides/pattern.md` | 8 proven DevOps & SRE team topologies (`img/type-1.svg` through `img/type-8.svg`): Dev & Ops collaboration, **Google SRE model**, Ops-as-Infrastructure-Platform, temporary enabling teams, and container-driven boundaries |
| **7** | **Working in a DevOps Team** | `slides/equipe.md` | Agile ceremonies, Pair & Mob Programming, Coding Dojo, **TDD & BDD**, Distributed VCS (`Git`), **Gitflow** (`img/gitflow.svg`) vs. **Trunk-Based Development & Feature Flags** (`img/trunk-based.svg` — `OpenFeature`, `LaunchDarkly`, `Unleash`, `Flagsmith`), and Pull Request code reviews |
| **8** | **Continuous Integration (CI)** | `slides/cintegration.md` | CI workflow (`img/wf-cintegration.svg`), **The Testing Pyramid** (`img/testing-pyramid.svg`), Unit Testing (`JUnit 5`, `pytest`, `Vitest`), Integration & Contract Testing (`Testcontainers`, `Pact`, `WireMock`), Acceptance & E2E (`Playwright`, `Cypress`, `Cucumber`), Performance & Load (`Grafana k6`, `Gatling`, `Locust`), Code Quality (`SonarQube`, `ESLint`, `Ruff`, `golangci-lint`), and **Shift-Left Security** (`Semgrep`, `CodeQL`, `Trivy`, `Snyk`, `Grype`, `Syft` SBOM, `OWASP ZAP`, `Nuclei`) |
| **9** | **Continuous Delivery (CD)** | `slides/cdelivery.md` | CD workflow (`img/wf-cdelivery.svg`), end-to-end artifact traceability, **Semantic Versioning (`SemVer 2.0.0`)**, and **Artifact Registries & Supply Chain Provenance** (`OCI` registries, `Harbor`, `GHCR`, `JFrog Artifactory`, `Sigstore Cosign`, `SLSA` provenance, `SBOM`) |
| **10** | **Continuous Deployment** | `slides/cdeployment.md` | Automated production deployment workflow (`img/wf-cdeployment.svg`), **Progressive Delivery & Zero-Downtime Releases** (Rolling Update, Blue/Green, Canary with `Argo Rollouts` / `Flagger`, Feature Flags / Dark Launches), and **GitOps** pull-based reconciliation (`img/gitops.svg` — `Argo CD`, `Flux`) |
| **11** | **Continuous Operations & SRE** | `slides/coperations.md` | Operations workflow (`img/wf-coperations.svg`), **Three Pillars of Observability & `OpenTelemetry`** (`img/observability.svg` — `Prometheus`, `Grafana Mimir/Loki/Tempo`, `Jaeger`, `Datadog`), **Immutable Infrastructure & IaC** (`Terraform` / `OpenTofu`, `Pulumi`, `Crossplane`, `Docker`, `Kubernetes`, `Helm`, `Packer`, `Ansible`), **Auto-Scaling & Traffic Management** (`Kubernetes Gateway API`, `Envoy`, `Cilium` eBPF, `Traefik`, `HPA`, `KEDA`, `Karpenter`), **SRE (`SLI`, `SLO`, `SLA`, Error Budgets)**, and **Chaos Engineering & Blameless Post-Mortems** (`Chaos Mesh`, `LitmusChaos`, `AWS FIS`) |
| **12** | **Continuous Everything** | `slides/ceverything.md` | The DevOps Infinity Loop (`img/devops-infinity-workflow.svg`), Continuous Feedback (`OpenTelemetry RUM`, `PostHog`, `Sentry`), and modern paradigms: **DevSecOps**, **Platform Engineering (`IDP` / `Backstage`)**, **FinOps & GreenOps** (`OpenCost`, `Kubecost`, `Kepler`), and **MLOps / LLMOps** |
| **13** | **Conclusion & References** | `slides/conclusion.md` | Key takeaways on culture vs. tooling, organizational complexity, and foundational reading (*The Twelve-Factor App*, *Accelerate / DORA*, *Google SRE Books*, *DevOps Topologies*, *The DevOps Handbook*) |

---

## Repository Structure

```text
.
├── index.html                  # Reveal.js 6.0.2 entry point & slide deck configuration
├── css/
│   └── custom.css              # Custom modern light theme, typography, cards, and layout styles
├── slides/                     # Modular Markdown slide decks (13 modules)
│   ├── title.md
│   ├── introduction.md
│   ├── agilite.md
│   ├── devops.md
│   ├── antipattern.md
│   ├── pattern.md
│   ├── equipe.md
│   ├── cintegration.md
│   ├── cdelivery.md
│   ├── cdeployment.md
│   ├── coperations.md
│   ├── ceverything.md
│   └── conclusion.md
└── img/                        # 29 custom vector SVG technical diagrams & 2 speaker avatars
    ├── avatar-laurent.jpg
    ├── avatar-arthur.jpg
    ├── waterfall.svg
    ├── agility.svg
    ├── wall-of-confusion.svg
    ├── devops.svg
    ├── devops-infinity-workflow.svg
    ├── anti-type-a.svg .. anti-type-g.svg
    ├── type-1.svg .. type-8.svg
    ├── gitflow.svg
    ├── trunk-based.svg
    ├── testing-pyramid.svg
    ├── wf-cintegration.svg
    ├── wf-cdelivery.svg
    ├── wf-cdeployment.svg
    ├── gitops.svg
    ├── wf-coperations.svg
    └── observability.svg
```

---

## Technical Stack

- **Presentation Engine:** [Reveal.js 6.0.2](https://revealjs.com/) loaded via jsDelivr CDN (`reset.css`, `reveal.css`, `white.css` theme, and `Markdown`, `Highlight`, and `Notes` plugins) — zero Node/Grunt build step required.
- **Typography:** Google Fonts (`Inter` for UI/headings and `JetBrains Mono` for code, metrics, and technical badges).
- **Diagrams:** 29 custom, resolution-independent SVG diagrams in `img/` styled with a unified color palette (`Indigo`, `Blue`, `Emerald`, `Amber`, `Rose`, `Slate`).

---

## Running Locally

Because Reveal.js loads external Markdown files (`slides/*.md`) via `fetch`, serve the repository root using any static HTTP server:

```bash
# Using Python 3
python3 -m http.server 8000

# Or using Node.js (npx)
npx serve -l 8000
```

Then open [http://localhost:8000](http://localhost:8000) in your browser.

### Keyboard Shortcuts

- <kbd>→</kbd> / <kbd>←</kbd> : Navigate between main sections
- <kbd>↓</kbd> / <kbd>↑</kbd> : Navigate vertical slides within a section
- <kbd>Space</kbd> : Advance through slides sequentially in lecture order
- <kbd>Esc</kbd> or <kbd>O</kbd> : Toggle slide overview mode
- <kbd>S</kbd> : Open speaker notes window
- <kbd>F</kbd> : Toggle fullscreen
- <kbd>?</kbd> : Show keyboard shortcut help overlay
