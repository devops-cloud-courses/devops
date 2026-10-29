## Continuous Delivery

----

### Builds on Continuous Integration

<img src="img/wf-cdelivery.svg" alt="Continuous Delivery workflow building on Continuous Integration" />

----

### What is delivery?

> Storing a deliverable that is potentially ready to go to production

----

### Deliverable Traceability

* The deliverable must be traceable across both previous and subsequent stages
* A deliverable maps to:
  * A requirement / request
  * N commits
  * A tag
  * A version visible to users so they can report bugs

----

### Versioning Challenges & Semantic Versioning

> To make deliverable traceability easier, adopt a strict **Semantic Versioning (`SemVer`)** scheme

* Format: `MAJOR.MINOR.PATCH` (e.g., `5.21.12` or `5.21.12+build.3`):
  * `MAJOR`: Incompatible API or breaking changes
  * `MINOR`: Backward-compatible new features
  * `PATCH`: Backward-compatible bug and security fixes
* Versioning sometimes even challenges release scope and delivery timelines

----

### Artifact Registries & Immutability

> Build once, deploy anywhere: promote the exact same signed artifact across `Dev` → `Staging` → `Prod`

* Never rebuild an application from source for each environment
* Store versioned, immutable artifacts and container images in a central **Artifact Registry**
* Attach provenance metadata, cryptographic signatures (`Cosign`), and an `SBOM` to every release artifact

----

### Manual Production Release

* Continuous Delivery does not deploy to production automatically
* Production deployments are triggered manually after human validation

----

### Skills / Tools

* Application & Container Packaging: `Docker` / `Podman` (`OCI`), `Cloud Native Buildpacks`, `Helm` (OCI charts), `Kustomize`, `Maven`, `npm`, `Python Wheels`, ...
* Artifact & Container Registries: `GitHub Container Registry (GHCR)`, `Google Artifact Registry`, `AWS ECR`, `Azure ACR`, `Harbor`, `JFrog Artifactory`, ...
* Supply Chain Security & Provenance: `Sigstore Cosign`, `SLSA` provenance, `Syft` (`CycloneDX` / `SPDX` `SBOM`), `OPA` / `Kyverno`, ...
