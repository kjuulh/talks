---
theme: blood
---

### Alternative ways to use dagger

@kjuulh / @Hermansen4325

---

### What do you mean

Dagger as 

- CI
- programmable orchestration
- a deployment tool
- a distribution mechanism

---

#### CI

> You probably know this one, so I won't go into it here

---

### Dagger as Programmable Orchestration

- Service containers
- Tooling
- Tests etc

---

#### Different ways to use dagger as tooling

1. build a container (slowest)
2. pull an application image (fast)
3. run a wasm binary in a wasm runtime container (fast)
4. run a regular binary in a scratch image (fastest)

Benchmark: [benchmark](https://git.front.kjuulh.io/kjuulh/dagger-runtime-benchmark)

---

#### Dagger as Programmable Orchestration: Demo

Demo: [renovate sharding](https://github.com/kjuulh/renovate-gitea-sharding)

---

#### Dagger as Programmable Orchestration: Demo 2

Demo: [dagger-wasm-runtime](https://git.front.kjuulh.io/kjuulh/dagger-wasm)

---

### Dagger as a Deployment tool

package a simple cli and use the pull application image approach

---

#### Dagger as a Deployment tool: Demo

1.  [pull-articles](https://git.front.kjuulh.io/kjuulh/pull-articles)
1.  [kasperhermansen-blog](https://git.front.kjuulh.io/kjuulh/kasperhermansen-blog/src/branch/main/ci/src/main.rs)
1.  [update-deployment](https://git.front.kjuulh.io/kjuulh/update-deployment)

---

### Dagger as a Distribution mechanism

1. [shuttle](https://github.com/lunarway/shuttle/tree/master/examples/moon-base)
1. [clank-shuttle-infrastructure-plan](https://git.front.kjuulh.io/kjuulh/clank-shuttle-infrastructure-plan)
2. [clank-vault](https://git.front.kjuulh.io/kjuulh/clank-vault)