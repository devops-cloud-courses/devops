## Working in a DevOps Team

----

### Using a VCS

* VCS: Version Control System
* Source code manager
* Able to navigate through commit history
* Able to work in separate branches

----

### Introducing a VCS: Git

* Created in 2005 by Linus Torvalds
* The most popular
* Free and open source
* Distributed system

----

### Well-known Git Servers

* `GitHub`
* `GitLab`
* `Bitbucket`

----

### Using Git on small projects

> You can work on a single branch, but this quickly leads to challenges

* Recurring conflicts if several people commit at the same time
* Separating different functional evolutions
* Knowing which commit to branch from when there is a bug in production

----

### Using Git in a team: Gitflow

<img src="img/gitflow.svg" alt="Gitflow branching model diagram" />

----

### Trunk-Based Development vs. Gitflow

> Modern high-performing CI/CD teams favor short-lived branches over complex long-lived branch trees

* **Gitflow**: Designed for scheduled release trains and multiple maintained versions, but long-lived branches often cause *"merge hell"* and slow down Continuous Integration
* **Trunk-Based Development / GitHub Flow**: Developers merge small, frequent pull requests into `main` daily
* **Feature Flags**: Incomplete features are merged safely behind runtime toggles, decoupling **code integration** from **feature release**

----

### Learn how to use Git

* [The official website](https://git-scm.com/book/en/v2)
* [Step-by-step tutorial](https://www.atlassian.com/git/tutorials/what-is-git)

----

### Agile practices: Ceremonies

* Sprint Planning
* Stand-up meeting
* Sprint review / Demo
* Sprint retrospective

----

### Sprint Planning

* Duration: 4 hours for a 2-week sprint
* Participants: Everyone (Dev, PO, SM)
* Goal: Velocity, Definition of Done, List of tasks to complete during the sprint

> Velocity: Indicative metric of the team's capacity to complete N tasks during a sprint

----

### Stand-up meeting

* Duration: 15 minutes every morning
* Participants: Everyone (Dev, PO, SM)
* Goal: Discuss blockers and issues encountered by each team member

----

### Sprint Review / Demo

* Duration: 1-2 hours for a 2-week sprint
* Participants: Everyone (Dev, PO, SM) and anyone interested in the project's progress
* Goal: Product demonstration and feedback collection

----

### Sprint retrospective

* Duration: 2 hours for a 2-week sprint
* Participants: Everyone (Dev, PO, SM); PO attendance is optional
* Goal: Debrief on what went well, what didn't go well, and what could be improved

----

### DevOps team practices

* Pull Request / Code Review
* Coding Dojo
* Pair Programming
* Technical Breakfast

----

### Pull Request / Code Review

* Instead of merging a branch directly into another, open a merge request
* Other team members review the code changes introduced
* Reduces bugs that can be spotted by human review

----

### Pair programming

* Programming in pairs: A **driver** and a **navigator**
* Roles are swapped regularly
* Helps everyone involved level up their skills
* Allows the driver to focus on writing the code
* Allows the navigator to focus on design and deeper architectural issues

----

### Coding Dojo

* Meeting where multiple people tackle a programming challenge together
* The goal is to come up with the most optimized solution, agreed upon by all participants
* Prevents endless debates later on about technical choices made in the past

----

### Technical Breakfast

* Gather around a speaker sharing feedback and experience on a technology or methodology
* Helps share knowledge effectively across a company
* Helps the speaker deepen their own knowledge while preparing the topic

----

### And many more...

* `TDD` - Test Driven Development
* `BDD` - Behavior Driven Development
* Feature Flipping
* A/B Testing
