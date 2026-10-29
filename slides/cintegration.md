## Continuous Integration

----

### Builds on Agile Development

<img src="img/wf-cintegration.svg" alt="Continuous Integration workflow building on Agile Development" />

----

### What is integration?

* Bringing together parts developed separately

----

### CI: Build

> Avoid the "Wait, I don't get it! It works on my machine!" effect

* Download dependencies
* Build the application

----

### CI: Tests

* Test everything that can be tested automatically
* Which means: Almost everything!
* There are many different types of tests

> Testing is putting a quality stamp of approval on a deliverable

----

### The Testing Pyramid

> Balance test execution speed, maintenance cost, and confidence across layers

<img src="img/testing-pyramid.svg" alt="The Testing Pyramid: Unit, Integration, and End-to-End tests" />

----

### Unit Tests

* Tests aimed at verifying that a single component works on its own
* These tests can run during the build, or right after the build

----

### Integration Tests

* Tests building upon unit tests
* Ensure that components tested individually work together properly
* Spin up ephemeral dependencies (`Testcontainers`) or verify API contracts (`Pact`)

----

### Functional / End-to-End Tests

* Also called browser or user-journey tests (`Playwright`, `Cypress`)
* Simulate inputs just as users would perform them (clicks, forms, navigation, Gherkin scenarios)
* Validate the outcome: the right view, state, or API side-effect is produced
* Use resilient, accessible locators (`getByRole`, `getByLabel`) or dedicated `data-testid` attributes

----

### Load Tests

* Tests aimed at ensuring application resilience under heavy load
* Start with simple requests and then move to scenarios representative of real user actions
* First test with a single instance of each application component
* Then increase the number of instances (**scale**) to see how the application reacts overall
* This methodology helps find the critical path between instance count and user count

----

### Code Analysis

* Static or dynamic code analysis tools
* Report metrics on code quality, vulnerabilities, and potential bugs
* Highlight the most critical issues
* Provide real insight into overall code quality and the effort required to get closer to perfection

----

### Security Tests & Shift-Left Security

> Integrate security checks directly into every CI pipeline run (**DevSecOps**)

* **`SAST` (Static Application Security Testing)**: Scan source code for security flaws and coding anti-patterns
* **`SCA` (Software Composition Analysis)**: Audit third-party dependencies for known `CVEs` and generate an `SBOM` (Software Bill of Materials)
* **Secret & Container Scanning**: Block leaked credentials/API keys in commits and scan container base images for vulnerabilities
* **`DAST` (Dynamic Application Security Testing)**: Probe the running application for known vulnerabilities (injections, `XSS`, brute-force)

----

### Tests: Disadvantages

* Time-consuming to maintain: test updates must be planned within development cycles
* Time-consuming to set up: many different technologies exist and benchmarking them takes time

----

### Tests: Conclusion

* Tests are not optional
* Tests drastically reduce the time spent validating a deliverable
* Tests increase our confidence in our deliverables
* Tests let us stay focused on creating value instead of spending all our time debugging applications

----

### Skills / Tools

* CI/CD Platforms: `GitHub Actions`, `GitLab CI/CD`, `Dagger`, `Tekton`, `Cloud Build`, `Jenkins`, ...
* Scripting & Automation: `Bash`, `Python`, `Go`, `TypeScript`, `PowerShell`, ...
* Build & Dependency Management: `Maven`, `Gradle`, `pnpm` / `npm`, `uv` / `Poetry`, `Go modules`, `Cargo`, `NuGet`, ...
* Unit Tests: `JUnit`, `pytest`, `Vitest` / `Jest`, `Go test`, `NUnit`, ...

----

### Skills / Tools (cont.)

* Integration & Contract Tests: `Testcontainers`, `Pact`, `WireMock`, `Bruno` / `Postman`, `REST Assured`, ...
* Functional / E2E Tests: `Playwright`, `Cypress`, `Selenium`, `Cucumber`, ...
* Load & Performance Tests: `k6`, `Gatling`, `Locust`, ...
* Security & Supply Chain (`SAST` / `SCA` / `DAST`): `Trivy`, `Snyk`, `Semgrep`, `Gitleaks`, `Dependabot` / `Renovate`, `OWASP ZAP` / `Nuclei`, ...
* Code Quality & Linting: `SonarQube`, `CodeQL`, `ESLint` / `Biome`, `Ruff`, `golangci-lint`, ...
