# DevOps in a Nutshell — MSc Course Slides

Interactive [Reveal.js 6.0.2](https://revealjs.com/) lecture deck introducing **DevOps culture, organizational topologies, CI/CD pipelines, GitOps, Cloud-Native Observability, and Site Reliability Engineering (SRE)** for MSc Computer Science & Software Engineering students.

## Authors

- **Laurent Grangeau** — Cloud Solution Architect @ Google ([@laurentgrangeau](https://twitter.com/laurentgrangeau) | [github.com/laurentgrangeau](https://github.com/laurentgrangeau))
- **Arthur Mauvezin** — DevOps Engineer @ Ouidou Consulting ([@arthurmauvezin](https://twitter.com/arthurmauvezin) | [github.com/arthurmauvezin](https://github.com/arthurmauvezin))

## Lecture Structure

| Module | File | Key Topics & Technical Assets |
|---|---|---|
| **1. Title & Authors** | `slides/title.md` | Course cover & speaker bios |
| **2. Introduction** | `slides/introduction.md` | Course motivation, market demand, Reveal.js navigation |
| **3. Agility Foundations** | `slides/agilite.md` | V-Model / Waterfall (`img/waterfall.svg`), Scrum (`img/agility.svg`), Agile Manifesto, limits of Agile |
| **4. DevOps Philosophy** | `slides/devops.md` | Devs vs. Ops, Wall of Confusion (`img/wall-of-confusion.svg`), Agile to DevOps (`img/devops.svg`), **CALMS** pillars, **DORA Metrics** |
| **5. Organizational Anti-Patterns** | `slides/antipattern.md` | 7 DevOps organizational anti-patterns (`img/anti-type-a.svg` – `img/anti-type-g.svg`) |
| **6. Organizational Patterns** | `slides/pattern.md` | 8 proven DevOps & SRE topologies (`img/type-1.svg` – `img/type-8.svg`) |
| **7. Working in a DevOps Team** | `slides/equipe.md` | Agile ceremonies, Pair/Mob programming, Coding Dojo, `TDD`/`BDD`, Git, Gitflow (`img/gitflow.svg`) vs. **Trunk-Based Development & Feature Flags** (`img/trunk-based.svg`), Pull Requests |
| **8. Continuous Integration (CI)** | `slides/cintegration.md` | CI workflow (`img/wf-cintegration.svg`), **The Testing Pyramid** (`img/testing-pyramid.svg`), Unit/Integration (`Testcontainers`, `Pact`), E2E (`Playwright`), Load (`k6`), Static Analysis, **Shift-Left Security** (`SAST`, `SCA`, `SBOM`, `DAST`) |
| **9. Continuous Delivery (CD)** | `slides/cdelivery.md` | CD workflow (`img/wf-cdelivery.svg`), traceability, **Semantic Versioning (`SemVer`)**, **Artifact Registries & Supply Chain Provenance** (`OCI`, `Sigstore Cosign`, `SLSA`, `SBOM`) |
| **10. Continuous Deployment** | `slides/cdeployment.md` | Deployment workflow (`img/wf-cdeployment.svg`), **Progressive Delivery** (Rolling, Blue/Green, Canary, Feature Flags), **GitOps** (`img/gitops.svg` — `Argo CD`, `Flux`) |
| **11. Continuous Operations & SRE** | `slides/coperations.md` | Operations workflow (`img/wf-coperations.svg`), **3 Pillars of Observability & `OpenTelemetry`** (`img/observability.svg`), **Immutable Infrastructure (`IaC`)**, **Auto-Scaling** (`HPA`, `KEDA`, `Karpenter`), **SRE (`SLI`, `SLO`, `SLA`, Error Budgets)**, **Chaos Engineering & Blameless Post-Mortems** |
| **12. Continuous Everything** | `slides/ceverything.md` | DevOps Infinity Loop (`img/devops-infinity-workflow.svg`), Continuous Feedback (`RUM`), **DevSecOps**, **Platform Engineering (`IDP` / `Backstage`)**, **FinOps & GreenOps**, **MLOps / LLMOps** |
| **13. Conclusion & References** | `slides/conclusion.md` | Key takeaways, organizational complexity, and curated reading (*The Twelve-Factor App*, *Accelerate / DORA*, *Google SRE Books*, *DevOps Topologies*, *The DevOps Handbook*) |

## Running Locally

Serve the repository root with any static HTTP server:

```bash
python3 -m http.server 8000
```

Then open `http://localhost:8000` in your browser.
