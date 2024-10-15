---
theme: night
progress: false
---
## Crafting Highly-Efficient Workflows

Kasper J. Hermansen

Platform Engineer / Architect @ Lunar

contact@nonothing.io

---

# Slides

Slides will be available for download on github

[github.com/kjuulh/talks](https://github.com/kjuulh/talks)

---

### So which problem are we solving?

notes:

This talk will be about how to make engineers in your organisation more effective, reduce overhead, and reduce complexity. I'll go through we've done at Lunar, and in the industry as a whole, to make you as an engineer more effective in your job.

This talk will partly be about platform engineering, its role in an organisation, and how to leverage that as your superpower to build opinionated and fast workflows.

---

## Define workflow

---

Create a code project

---

Get feature in the hands of our customers

---

Get the right signals to know it is doing the right thing

---

Keep it updated and secure

---

## History

---

There once was a team with developers and operations people

---

Much code was thrown over the wall

---

Then came DevOps

---

Now we've got buckets of software everywhere, lets consolidate

---

Platform Engineering was born

---

But what should we build, and for whom?

---

Developer Experience was created to figure out exactly that

---
# Demo

notes:

showcase developer workflow, create a repository, run code, create upstream repository, push code, and sync to ci

As platform engineers working on a developer efficiency journey, we want to get you go be the most effective you can be at providing the most value to the business as possible.

And that means focusing as much as possible on feature development as you can, with the highest quality, security and reliable, while still being end-2-end responsible for the feature.

---
## So you want to build a platform?

notes:

You want to build a platform? Strap in. But lets first start with what I am talking about when I say platform

---

## Platform is an abstraction

And hopefully a good one at that

notes:

Our role as engineers working for other engineers is do our damnest to build the best abstraction you've ever seen. That is it, talk over... =D

---
## Examples

---

![heroku](2024-10-17-devops/assets/heroku.svg)

Push -> Test -> Deploy

notes:

On heroku you do a git push to repository, it builds your code, tests it, and deploys it without downtime. This is generally the experience you should aim for if you're interested in building your own platform, just know that there isn't a perfect answer to what to build.

---

![aws](2024-10-17-devops/assets/aws.jpeg)

The complexity!

notes:

AWS is an awesome tool, and allows you to scale up a higher level of abstraction faster than would normally be possible, you can rely on AWS' services to be the bedrock of your platform, but it can sometimes be a too complex tool to expose directly

---

![k8s](2024-10-17-devops/assets/k8s.jpeg)

Friends don't let friends write YAML

notes:

Kubernetes can also be treated as a platform, but it is again probably not a good choice to expose directly, as it can be complex and unwieldy, instead we may choose to adopt it as a runtime, and instead raise the abstraction level.

---
## It is what you rely on to do your job

notes: 

It is what you as a feature engineer relies on to do your job. Be it a Kubernetes, AWS, GitHub, Okta etc. All of it together constitutes a platform, even if it isn't necessarily a cohesive solution.

---

## Technologies doesn't matter

Journeys do

notes:

We're solving a problem, not selling a technology, we want the why. As an engineer you want to ship code to production, build new features, have good metrics to understand what is going on in your products. Platform Engineering helps facilitate that

---
## Golden Path

---

## Get in control

---
## Demo

notes:

Show a git push, build and release, and be able to hit it

---
### Platform Engineering

notes:

Like any other software gig, except our customers are other engineers, and not just Backend engineers, frontend, data, analytics, ai, etc.

We build software and setup infrastructure to provide a holistic abstraction that helps other engineers be more effective, or solve a cross cutting concern

---

## Building a platform is a Journey

And you can't have everything at once

notes:

we build it piecemeal, we always develop against a certain requirement, but think creatively about how to go about solving said problem. 

---
## Finding a problem to solve

notes:

What do we actually want to solve.

---

### Being a developer yourself

---

### Talking to developers

---

### Gather data

---

### Feedback loops are important

notes:

We want to make to feedback cycles as short and reliable as possible. Imagine you're building a product and you need to ship it to production every time

---

### Example of a bad feedback loop

```
20 minutes to build
1 hour to deploy
1 deploy every week
= 
1 change to get it right every week
```

---

## Example of a great feedback loop

```
1 minute to build code
2 minutes to deploy
* deploys are on demand
=
3 minute feedback for shipping code
```

---

## Demo

 notes: 

Run pipeline locally, should be prewarmed

See it run

---

## Why is fast feedback loops necessary


---
## Individual deployability

notes: communication layers hurt

---

## End to end responsibility


---

## Minimize cognitive load

notes:

The team should only need to focus on


---

### Preserving flow state

- Keep our developers hands on keyboard
  
- Minimise distractions
  
- Context switch is death

---


## DORA

- Deployment frequency 
	- 100 pr week
- Lead time to change 
	- 2 minutes
- Change failure rate 
	- 5%
- Time to restore 
	- 5 minutes

---


## Example metrics

- How long does CI take?
- Code review turnaround time
- First time to PR
- Commit Cadence
- Deployment time

---

## How to build a workflow

---

## Who is the user

---

## Which problems do they have

---

## Design a solution

---
## Wardley mapping

Choose technologies

![[2024-10-17-devops/assets/wardley.png]]

---

## GitHub Actions with Dagger

---

### GitHub actions

---

### Dagger

Write pipelines in code

---
## Build for yourself first

---

### The platform should be testable by itself

Bash is hard to test

---

## Gradually releasable

Do we want to release to everybody at once

---
# Demo

notes: 
Show a simple pipeline using dagger (dagger cuddle-rust-service-plan) and see it being deployed. hit it with curl
