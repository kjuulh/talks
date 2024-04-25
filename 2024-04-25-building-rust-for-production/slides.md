---
theme: white
progress: false
---
# Building Rust for Production

Kasper Juul Hermansen 

Platform Engineer @ Lunar

---
## Goal

- Have fast feedback loops; locally as well as in ci
- Shipping great product for your customers

---
## About

- Learning how to build rust effectively can save both time and money
	- Fast feedback loops
	- Compact and efficient production apps
- Unlock additional features

---
## Rust stages

- Local development
- Continuous integration
- Production
---
#  <pre>$ man Rust </rust>

- Compiled binaries
- Can build for a *lot* of targets, including: 
	- Webassembly (frontend & backend)
	- Static / dynamic linking (musl vs glibc)
	- Embedded in other languages (dll, statically)
	- Embedded devices. (#[no-std])
	- Blockchain protocols
- A lot closer to compiling C++ than golang/c#
---
## Rust locally

- You want :rabbit: iteration speed
- Preferably instant build times
- You don't care about large binaries
- Should be simple to run

---
#  <pre>$ man cargo </pre>

- Package manager
- Build system
- Calls out to formatter, linter, everything rust, basically.

---
### Local: Current techniques

- Different linker (mold vs ld)
- Dynamic linking (useful for large projects) 
- Split into multiple crates
- Optimize timings / remove unused dependencies

---
## Cargo is your friend

*Demo time*

[kjuulh/building-rust-for-production/local](https://github.com/kjuulh/building-rust-for-production/tree/main/01-local)

notes:

1. Show sample app
2. Show timings

---
## Rust in CI

- You want cacheable builds, they should be :fire: fast
- Complexity isn't a huge issue
- Preferably same as in production, especially for tests

---
## CI is a different :alien:

- Tooling sucks (bash & yaml)
- Complexity everywhere (bash, bazel, groovy, docker, nix, etc)

---
### The new kid on the block *Dagger*

- Docker builds directly in Rust (using `dagger-sdk` crate)

*Demo time*

[kjuulh/building-rust-for-production/ci](https://github.com/kjuulh/building-rust-for-production/tree/main/02-ci)

---
### CI: A little of the same as local

- Separate `cargo build` into multiple cache layers.
	- A source code change shouldn't cause download and compilation of dependencies

---
##  Rust in Production

- The smallest binaries possible (within reason)
- Most performance, all platforms/targets aren't equal

---
### Prod: Tune those binary settings!

*Demo time*

[kjuulh/building-rust-for-production/production](https://github.com/kjuulh/building-rust-for-production/tree/main/03-production)

---
### Bonus: Actually statically linked binaries

> Ever tried to compile to `musl` and just gotten a `not found` when trying to execute your binary?

[kjuulh/building-rust-for-production/cross-compile-musl](https://github.com/kjuulh/building-rust-for-production/tree/main/02-cross-compile/cross-compile-musl)

---
### Bonus: Wasm the weird compile target

- Interoperable binaries out of the box
- That is if you can wrangle the tooling and limitations

---

# Questions?

- Please give feedback 
	- contact@kasperhermansen.com
- Slides: 
	- Markdown/pdf: [github.com/kjuulh/building-rust-for-production](github.com/kjuulh/building-rust-for-production)

---

![[2024-04-25-building-rust-for-production/assets/slides.png]]
