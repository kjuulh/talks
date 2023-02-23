## Introducing 

### Rust sdk for dagger 

https://github.com/kjuulh/dagger-rs

(contrib)

---

# Boring stuff

- github: [@kjuulh](https://github.com/kjuulh)
- discord: @Hermansen#4325

<br>

Platform Engineer [@lunar](https://www.lunar.app/en/personal)

<br>

Slides: [dagger-rs](https://github.com/kjuulh/talks/blob/main/2023-02-23-dagger-rs/dagger-rs.md)

---

# Dagger sdk from scratch

- Native codegeneration
- Rust native code
- Uses rust tooling

---

# Demo: 

Adding dagger to [ripgrep](https://github.com/BurntSushi/ripgrep): 

[kjuulh/ripgrep](https://github.com/kjuulh/ripgrep/tree/dagger-demo/ci)

---


# Challenges

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

# What is next?

- Adding more ergonomic handles
- Adding more docker engine support (--quiet mode)
- Custom logging and tracing
- Fixing the codegeneration to be more ideomatic