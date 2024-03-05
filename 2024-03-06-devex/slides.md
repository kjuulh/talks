---
theme: white
progress: false
---

### Developer Experience

Crafting High-Effeciency developer workflows @ Lunar

Kasper Juul Hermansen
---

### @me

Kasper Juul Hermansen

Platform Engineer @ Lunar

- github.com/kjuulh
- git.front.kjuulh.io/kjuulh
- blog.kasperhermansen.com

---

### Developer Experience

- What is Developer Experience
- Developer Experience at Lunar
- Questions

note: Intro to talk 

---

#### Developer Experience, DevEx, DX - What?

- Focusing on Developer Happiness
	- Better results
	- More consistently
	- Sustainability

note:

The practice on focusing on Developer Happiness, to achieve maximum performance and sustainability.

---

### Developer Experience

-  What is the problem we want to solve
	- Surveys
	- Research
- How should it be solved
	- Communicate the problem
	- Implement the solution

---
### Recent hype

- Marketing: DX
- But an old term: https://wiki.mozilla.org/DeveloperExperience ~ 2012

note:

Along with Platform Engineering, Developer experience is becoming a new fad, especially because of marketing push by companies such as DX, but also many of the big tech companies opening up for their practices

However, keep in mind that developer experience isn't a new thing, it is putting words on the practice of solving problems for our Developers 

---
### Team Topologies

- @Lunar
- At a large company
- At a really large company

note:

Needs diagrams, what does this actually mean

---

### Team Topologies: Small scale

- Exists as part of a team, or a subset of 
 
![[team-topologies-platform-engineering.excalidraw|500]]

---

### Team Topologies: Medium scale

- Exists as a team with 

![[team-topologies-part-researcher.excalidraw|600]]

---

### Team Topologies: Large scale

- Exists as a separate team

![[team-topologies-researcher.excalidraw|700]]


---

### Developer Experience @ Lunar

note: 

We are gonna focus on Developer Experience at Lunar, there are plenty of resources online for how and when you may want to use Developer Experience, and many of you probably have already chosen to do so.

I will focus mainly on our experience at Lunar, what it looks like, what we've chosen to use, what we haven't, and a few examples of things built from practicing Developer Experience

---

### Topology

<split left="1.5" right="2">

- Developer Relations
- Platform Engineer
- Architect
- No Academics?
  
<div>
![[composition.excalidraw]]
</div>
</split>

---

### Developer Experience in practice

- Finding problems to solve
	- Actually talking to people
	- Some times they come to us on their own
	- Looking at data, DORA metrics,  our own observability

---

###  What problems to solve

- 80/20 rule
- Solve classes of problems
- Couple data with user feedback
- Be conservative
	- Don't feel bad for your ideas, they're not puppies


---

### Executing

- Quickly build and test tools
- Rolling out solutions
	- Gathering feedback
	- Remember to reflect on feedback before acting
- Communication is key

---

### Aspirations

- Focusing on the golden path
- We take on platform complexities and abstractions
- Letting Developers be in control what is necessary for them to succeed


---

### Example: Creating a new service

- 1 form in backstage
- 1 commit to a github repository to go to production
- around 10 minutes for a service with a database, message queue, grpc, http, logging, metrics, etc.

---

![[backstage-catalog.png]]

---

![[backstage-create-service.png]]

---

![[service-fresh.png]]

---

![[shuttle-yaml.png]]

---
### What you get

- Signals:
	- Dashboards in grafana
	- Shared logs
	- Alerts
- Dependency updates:
	- Renovate

---

### What you get...

- Security:
	- Security notices and updates
- Continuous integration
- Continuous deployment
- Alerting on keystone metrics

---

### Time to prod

Zero to prod

~4 minutes

---

### Application as a Service

- No kubernetes yaml files
- No CI pipeline
- No bash scripts
- Only code and a bit of configuration

---
### Building tools from first principles

- If nothing better isn't out there
- Focus entirely on the problem at hand
	- Use any means, open source, proprietary, bought
- Only expose necessary parts that our developers needs to use

---
### Example: CI

- New CI system
	- Focusing on solving reliability problems
	- Lots of feedback from developers
	- Solving their specific needs

---

![[ci-success.png]]

---

```yaml
# file: .github/workflows/ci.yaml
name: ci
on:
  push:
    branches:
      - "**"
  pull_request:
  workflow_dispatch:
jobs:
  ci:
    uses: lunarway/lw-shuttle-go-plan/.github/workflows/plan-ci.yml@stable
    secrets: inherit
    with:
      lifecycle: stable
```

---

### What you get

- Build times from seconds to a few minutes
	- 99th percentile ~4 minutes
	- 95th percentile ~ 1 minute


---

### Centralized CI pipeline

- Built from entirely in Golang
- Packaged like regular software libraries
- Tested like normal software
- Teams can own their own parts of the pipeline, if they desire


---

### Forming connections

- Let people become ambassadors for you
- Small victories over big bangs

---

# Questions? :rocket:

Slides

![[slides.png|400]]