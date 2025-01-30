# List of Student Projects

# Themes

In a systems context:
- **Concurrency** Logic defined in a way that allows for parallelism but doesn't require it.
- **Availability** Keeping a service available despite faults in soft- and hardware.
  - Supervision in systems based on the [actor model](https://en.wikipedia.org/wiki/Actor_model) (e.g., through [Elixir](https://elixir-lang.org)).
  - Netsplits and resulting split brain scenarios.
- **Responsiveness** Keeping the system responsive despite a high load.
  - Bounding concurrency through back pressure.
  - Push-based data flow transformes problems to routing problems.
- **Metadata** Modeling and interaction with data used to describe other data.
  - Graphs and ontologies.
- **Efficiency** Software that operates at reasonable levels of efficiency.
- **Automation** Moving tasks to software to enable repeated processing at low cost.

This naturally leads to:
- Software-define metadata.
- In-network processing.
- Designing for polling-free/push-based operations.

# Building Blocks

Metadata models:
- [Brick](https://brickschema.org) Metadata model for buildings.

Programming languages:
- [Elixir](https://elixir-lang.org) Programming language with focus on concurrency, high availability, fault-tolerance, low-latency, scalability, hot-upgrades and system-wide live introspection.
  - [LiveBook](https://livebook.dev) An interactive notebook platform for Elixir ([videos](https://www.youtube.com/@livebookdev)).
  - [José Valim - Idioms for Building Fault-tolerant Applications with Elixir](https://www.youtube.com/watch?v=mkGq1WoEvI4)
  - [Saša Jurić - High availability with Elixir and Erlang - Full Stack Fest 2016](https://www.youtube.com/watch?v=Ba3aCm3A0o8)
  - [Phoenix LiveView](https://www.youtube.com/watch?v=k4mSbCoBTPI)
- [Rust](https://www.rust-lang.org) Programming language with focus on reliability, efficiency and productivity.
- [Zig](https://ziglang.org) Natural successor to the C language.
- [WebAssembly](https://webassembly.org) (WASM) JavaScript replacement. Usually through Rust (see above).
- [Go](https://golang.org) Programming language with focus on concurrency on a single host.
- [Julia](https://julialang.org) High-level language with low-level performance developed by [greedy](https://julialang.org/blog/2012/02/why-we-created-julia/) people.
- [Python](https://www.python.org) for scripting purposes.

Alternative forms of databases:
- Timeseries databases like:
  - [TimescaleDB](https://www.timescale.com)
  - [Prometheus](https://en.wikipedia.org/wiki/Prometheus_(software))
  - [Riak TS](https://riak.com/products/riak-ts/)
- Graph databases and graph querying languages like:
  - [OpenCypher](https://opencypher.org)
  - [Neo4J](https://neo4j.com) A property graph database.
  - [Gremlin](https://en.wikipedia.org/wiki/Gremlin_(query_language))
- Wide-column data stores like:
  - [ScyllaDB](https://www.scylladb.com) Like Cassandra, but with significantly better performance.
- Misc:
  - [CouchDB](https://couchdb.apache.org) Distributed document storage with eventual consistency that is built for intermittently offline nodes.

Embedded Frameworks:
- [FreeRTOS](https://www.freertos.org) Real-time operating system for microcontrollers.
- [AtomVM](https://www.atomvm.net) Running BEAM code (e.g., Elixir) on microcontrollers.
- [Nerves](https://nerves-project.org) Running Elixir on top of small general-purpose hardware (e.g., Raspberry Pi).

Hardware:
- [ESP32](http://esp32.net) Cheap and powerful microcontroller.
- [Pine64 Ox64](https://wiki.pine64.org/wiki/Ox64) High performance/cost device with WiFi, BT and Zigbee radios that can be used hosting either a general purpose OS or a realtime OS. I am really hoping for a Nerves port.
- [Hardkernel ODROID-H3+](ODROID-H3+) for a home cluster.
- [Pine64 NutCracker](https://wiki.pine64.org/wiki/Nutcracker) Extremely cheap IoT devices based on the open source(ish) RISC-V architecture.

Graphics:
- [Cairo](https://www.cairographics.org) 2D vector graphics library.
- [D3](https://d3js.org) for bespoke graphics visualization on the web.

