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

### Versioning Challenges

> To make deliverable traceability easier, it is important to have a well-designed versioning scheme
* Versioning sometimes even challenges release scope and delivery timelines
* Versioning example: MAJOR.MINOR.PATCH_BUILDNUMBER (5.21.12_3)

----

### Manual Production Release

* Continuous Delivery does not deploy to production automatically
* Production deployments are triggered manually after human validation

----

### Skills

* Application packaging: Maven, NPM, MSBuild, Python, Docker, ...
