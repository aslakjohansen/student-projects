# List of Student Projects

**Update pending!**

# Themes

In a systems context:
- **Concurrency** Logic defined in a way that allows for parallelism but doesn't require it.
- **Availability** Keeping a service available despite faults in soft- and hardware. 
- **Responsiveness** Keeping the system responsive despite a high load.
- **Metadata** Modeling and interaction with data used to describe other data.
- **Efficiency** Software that operates at reasonable levels of efficiency.
- **Automation** Moving tasks to software to enable repeated processing at low cost.

This naturally leads to:
- Software-define metadata.
- In-network processing.
- Designing for polling-free/push-based operations.

# Building Blocks

- Metadata models:
  - [Brick](https://brickschema.org) Metadata model for buildings.
- Programming languages:
  - [Elixir](https://elixir-lang.org) Programming language with focus on concurrency, high availability, fault-tolerance, low-latency, scalability, hot-upgrades and system-wide live introspection.
    - [José Valim - Idioms for building distributed fault-tolerant applications with Elixir](https://www.youtube.com/watch?v=MMfYXEH9KsY)
    - [Saša Jurić - High availability with Elixir and Erlang - Full Stack Fest 2016](https://www.youtube.com/watch?v=Ba3aCm3A0o8)
    - [Phoenix LiveView](https://www.youtube.com/watch?v=k4mSbCoBTPI)
  - [Rust](https://www.rust-lang.org) Programming language with focus on reliability, efficiency and productivity.
  - [WebAssembly](https://webassembly.org) (WASM) JavaScript replacement. Usually through Rust (see above).
  - [Go](https://golang.org) Programming language with focus on concurrency on a single host.
- Alternative forms of databases:
  - (Proper) timeseries databases (potentially [Prometheus](https://en.wikipedia.org/wiki/Prometheus_(software))).
  - (Proper) graph databases and graph querying languages (e.g., [Gremlin](https://en.wikipedia.org/wiki/Gremlin_(query_language)) and [Neo4J](https://neo4j.com)).
- [FreeRTOS](https://www.freertos.org) Real-time operating system for microcontrollers.
- Hardware:
  - [Pine64 NutCracker](https://wiki.pine64.org/wiki/Nutcracker) Extremely cheap IoT devices based on the open source(ish) RISC-V architecture.
  - [Pine64 PineTime](https://www.pine64.org/pinetime/) Smart Watch (not really sure what to do with it):
    - [Sneak Peek of PineTime Smart Watch… And why it’s perfect for teaching IoT](https://medium.com/swlh/sneak-peek-of-pinetime-smart-watch-and-why-its-perfect-for-teaching-iot-81b74161c159)
    - [chip8.rs: CHIP-8 Game Emulator in Rust for PineTime Smart Watch](https://lupyuen.github.io/pinetime-rust-mynewt/articles/chip8)
  - [ESP32](http://esp32.net) Cheap and powerful microcontroller.
- [Cairo](https://www.cairographics.org) 2D vector graphics library.

