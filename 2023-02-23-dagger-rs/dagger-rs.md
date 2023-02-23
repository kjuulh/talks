---
theme: blood
---

### Introducing 

#### Rust sdk for dagger 

(contrib)

---

## Boring stuff

- github: [@kjuulh](https://github.com/kjuulh)
- discord: @Hermansen#4325

Platform Engineer [@lunar](https://www.lunar.app/en/personal)

---

###  Dagger sdk from scratch

[kjuuh/dagger-rs](https://github.com/kjuulh/dagger-rs/tree/main/crates/dagger-sdk)

- Native codegeneration
- Rust native code
- Uses rust tooling

---

## Demo: 

Adding dagger to [ripgrep](https://github.com/BurntSushi/ripgrep): 

[kjuulh/ripgrep](https://github.com/kjuulh/ripgrep/tree/dagger-demo/ci)

---


## Challenges

- Rusts memory model
	- It makes the API more verbose
- Weird bugs with long dot chains 
```rust
  client
    .container()
    .from()
    .with_exec([...])
    .with_exec([...])
    .with_exec([...])
    .with_exec([...])
    .with_exec([...])
    .file()
```
- Ergonomy vs simplicity

---

## What is next?

- Adding more ergonomic handles
- Adding more docker engine support (--quiet mode)
- Custom logging and tracing
- Fixing the codegeneration to be more ideomatic

---

## Slides

<a href="www.qr-code-generator.com/" border="0" style="cursor:default" rel="nofollow"></a><img src="https://chart.googleapis.com/chart?cht=qr&chl=https%3A%2F%2Fgithub.com%2Fkjuulh%2Ftalks%2Fblob%2Fmain%2F2023-02-23-dagger-rs%2Fdagger-rs.md&chs=180x180&choe=UTF-8&chld=L|2" width="400">