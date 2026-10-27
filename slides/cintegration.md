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

### Unit Tests

* Tests aimed at verifying that a single component works on its own
* These tests can run during the build, or right after the build

----

### Integration Tests

* Tests building upon unit tests
* Ensure that components tested individually work together properly
* Typically perform external technical calls to a component and validate the response

----

### Functional / End-to-End Tests

* Also called browser tests
* Simulate inputs just as users would perform them (Gherkin scenarios)
* Simulate clicks, typing characters into text fields, scrolling, double taps, ...
* Validate the outcome: the right page or right information is displayed, ...
* Require technical prerequisites: an ID on every selectable UI element, ...

----

### Load Tests

* Tests aimed at ensuring application resilience under heavy load
* Start with simple requests and then move to scenarios representative of real user actions
* First test with a single instance of each application component
* Then increase the number of instances (**scale**) to see how the application reacts overall
* This methodology helps find the critical path between instance count and user count

----

### Security Tests

* Test for known vulnerabilities (injections, XSS, ...)
* Stress the application to see how it responds
* Brute-force testing

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

### Code Analysis

* Static or dynamic code analysis tools
* Report metrics on code quality, vulnerabilities, and potential bugs
* Highlight the most critical issues
* Provide real insight into overall code quality and the effort required to get closer to perfection

----

### Skills / Tools

* Continuous Integration servers: `Jenkins`, `TeamCity`, `Bamboo`, `Travis (SaaS)`, `GitLab`, ...
* Scripting: `bash`, `python`, `powershell`, `groovy`, ...
* Building: `Maven`, `MSBuild`, `NPM`, ...
* Dependency management: `Maven`, `NuGet`, `Pip`, `Bower`, `NPM`, ...
* Unit Tests: `JUnit`, `NUnit`, `unittest`, `unit-test`, ...

----

### Skills / Tools (cont.)

* Integration Tests: `Failsafe`, `curl`, `SoapUI`, `Postman`, ...
* Functional Tests: `Selenium`, `Cucumber`, `Test IO`, `HP UFT`, `SoapUI`, `Postman`, `Ranorex`, ...
* Load Tests: `JMeter`, `Gatling`, `Locust`, ...
* Security Tests: `Netsparker`, `Acunetix`, `Metasploit`
* Code Analysis: `Sonar`, `Coverity`, `Fortify`
