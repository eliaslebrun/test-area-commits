# Resume — Projects Section

> Two versions provided: a **concise one** (pick the best ~7 projects) and a **full one** (all notable projects).
> Ordered by relevance and recency (Semester 5 → 4 → 2).

---

## ✅ VERSION A — Concise (recommended for a 1-page resume)

### Projects

---

**FerrumOS — Operating System in Rust** | *Rust / Systems Programming / OS Kernel / Memory Management / ELF* | Ongoing
> Building a fully custom operating system from scratch in Rust as a team project. Implementing all core kernel layers: boot sequence, CPU interrupt handling, virtual memory management with strict kernel/user space isolation, basic device drivers, process scheduling, syscall interface, filesystem, and ELF binary loading. Chose Rust for its compile-time memory safety guarantees — eliminating use-after-free and data races — while retaining full low-level control, with `unsafe` confined to audited zones.

---

**AREA — Action REAction** | *Node.js / React / Flutter / Docker / REST API / OAuth2* | Semester 5
> Built a full-stack automation platform similar to IFTTT/Zapier as a team project. Designed and implemented a REST API application server, a React web client, and a Flutter mobile client, all orchestrated via Docker Compose. Integrated multiple third-party services through OAuth2, enabling users to compose automated triggers (Actions → REActions) across platforms.

---

**GLaDOS — Custom Programming Language** | *Haskell / CI/CD / LLVM / Compiler Design* | Semester 5
> Designed and implemented a full programming language from scratch in Haskell. Phase 1: built a minimal LISP interpreter (S-expression parser, lambda calculus, recursion, built-in functions). Phase 2: evolved it into a custom-grammar language with its own AST, a stack-based virtual machine and bytecode compilation. Set up a full CI/CD pipeline with unit & integration test coverage reports.

---

**Zappy — Networked Strategy Game** | *C / C++ / TCP Sockets / Multi-client / Game AI* | Semester 4
> Year-end group project: built a complete networked game from scratch. Implemented a single-threaded, `select`-based C server managing multiple AI clients and a graphical client over TCP. Designed the communication protocol, the resource/player/incantation game logic, and an autonomous AI client that devises and executes survival strategies on a toroidal map.

---

**MyTorch — Neural Network Library** | *C++ / Machine Learning / FEN / Supervised Learning* | Semester 5
> Built a neural network framework from scratch without ML libraries (no PyTorch, no TensorFlow). Implemented forward/backward propagation, configurable layers, gradient descent variants (mini-batch/stochastic), weight initialization strategies (Xavier/LeCun), and dropout to prevent overfitting. Applied it to classify chess board states (Check / Checkmate / Nothing) from FEN notation with benchmarked accuracy.

---

**Arcade — Retro Gaming Platform** | *C++ / Dynamic Libraries / Design Patterns / SDL2 / SFML / nCurses* | Semester 4
> Engineered an extensible retro gaming platform using dynamic library loading at runtime (`dlopen`/`dlclose`/`dlsym`). Implemented multiple graphical backends (nCurses, SDL2, SFML) and games (Pacman, Nibbler) as hot-swappable shared libraries, with no hard dependencies from the core. Collaborated with another group to share a common ABI.

---

**MyPGP — Cryptography Suite** | *C / Cryptography / RSA / AES-128 / XOR / Big Integers* | Semester 5
> Implemented a complete cryptographic toolchain from scratch: symmetric encryption (XOR stream/block mode, AES-128 ECB), asymmetric encryption (RSA key generation with Carmichael's totient, big-integer modular exponentiation), and a PGP-style hybrid cryptosystem combining both. Handled full little-endian hex I/O and both block and stream cipher modes.

---

---

## 📋 VERSION B — Full Projects List (for portfolio / LinkedIn / detailed CV)

### Projects

---

### Ongoing

**FerrumOS — Operating System in Rust** | *Rust / Systems Programming / OS Kernel / Memory Management / ELF / x86-64*
> Team project building a complete operating system from scratch in Rust, designed for learning, experimentation, and progressively growing toward real daily use. Implementing every kernel layer from the ground up: boot sequence (multiboot), CPU interrupt and exception handling (IDT/GDT), virtual memory with paging and strict kernel/user space isolation, basic device drivers, process management, a simple scheduler, a syscall interface, filesystem support, and ELF binary loading. A server-oriented variant (FerrumOS Server) is also planned, focused on networking, monitoring, and deployment workloads.
- Enforced `unsafe` isolation: all direct hardware access confined to audited, documented zones
- Roadmap structured across three phases — Foundations, Functional Kernel, Maturity — with full technical documentation at each stage
- Tested continuously in virtual machines; all architectural decisions justified with trade-offs documented

---

### Semester 5

**AREA — Action REAction** | *Node.js / React / Flutter / Docker Compose / REST API / OAuth2*
> Developed a full-stack automation platform (IFTTT/Zapier clone) in a team. Architecture: Docker-Compose orchestrated server (port 8080), web client (port 8081), and mobile client (Android APK). Server exposes a REST API with JWT authentication, OAuth2 service subscription, and a trigger engine that polls Actions and fires REActions across integrated third-party services.
- Designed scalable microservice architecture with Docker Compose
- Implemented OAuth2 flows for multiple external services
- Delivered REST API, responsive web UI, and cross-platform mobile app simultaneously

---

**GLaDOS — Custom Programming Language** | *Haskell / Stack / CI/CD / Compiler Design / Virtual Machine*
> Implemented a full programming language in Haskell in two stages. Stage 1: LISP interpreter with S-expression parser, 64-bit integers, booleans, lambdas, closures, named functions, recursion, conditionals, and built-in operators. Stage 2: designed a custom grammar (BNF documented), extended the AST, and compiled to a custom stack-based bytecode VM. CI/CD pipeline automates build, tests, and release.
- Custom parser built from scratch (no parsing libraries)
- Achieved comprehensive unit + integration test coverage with automated reporting
- Designed and documented a formal grammar with infix operators and syntactic sugar

---

**Gomoku AI Bot** | *C++ / Game AI / Alpha-Beta Pruning / Minimax / Piskvork Protocol*
> Built a competitive AI player for the Gomoku board game (5-in-a-row, 20×20 board) compliant with the Piskvork communication protocol. Implemented a game tree search algorithm (Minimax with Alpha-Beta pruning), board evaluation heuristics, threat detection (open fours, fives), and optimized data structures for fast pattern recognition within the 5-second per-move time limit and 70 MB memory budget.
- Competed in a multi-group AI tournament
- Optimized search depth and evaluation within strict resource constraints

---

**MyTorch — Neural Network Framework** | *C++ / Machine Learning / Supervised Learning / NumPy-style math*
> Built a reusable neural network library from scratch without any ML frameworks. Implemented: layer abstraction, configurable activation functions, forward/backward propagation, cost functions, weight initialization (LeCun, Xavier), mini-batch and stochastic gradient descent, MC dropout for regularization, and model save/load. Applied library to a chessboard analyzer trained to classify FEN-encoded board positions as Check, Checkmate, or Nothing.
- No ML library dependencies; entire math layer implemented manually
- Produced benchmarks and learning curves to justify hyperparameter choices
- Pre-trained model shipped with the repository for automated evaluation

---

**MyPGP — Cryptography Suite** | *C / XOR / AES-128 / RSA / PGP / Big-Integer Arithmetic*
> Implemented a cryptographic toolbox from scratch: XOR cipher (stream and block modes), AES-128 ECB (SubBytes, ShiftRows, MixColumns, AddRoundKey, key schedule), RSA (key generation from prime inputs using Carmichael's totient and Fermat prime public exponents, big-integer modular exponentiation), and a hybrid PGP system (symmetric key wrapped with RSA, message encrypted with AES/XOR). All values in little-endian hexadecimal.
- Implemented AES from the NIST spec without library support
- Handled arbitrarily large integers for RSA (256-bit and 1024-bit prime pairs)

---

### Semester 4

**Zappy — Networked Strategy Game** | *C / C++ / TCP / select() / Multiplayer / AI / GUI*
> Year-end group project spanning a server, a graphical client, and an autonomous AI client. The C server is single-process, single-threaded, using `select()` for socket multiplexing, managing a tile-based toroidal world with resources, player movement, vision, sound propagation, forking, and elevation rituals. The AI client autonomously collects resources and orchestrates multi-player incantations to reach max level.
- Designed a complete binary TCP protocol from scratch
- Implemented real-time resource spawning, player lifecycle, and game event scheduling
- Built a 2D/3D graphical client rendering live game state

---

**Arcade — Extensible Retro Gaming Platform** | *C++ / Dynamic Libraries / OOP / SDL2 / SFML / nCurses*
> Designed a plugin-based gaming platform using runtime dynamic library loading. The core program loads graphical backends (nCurses, SDL2, SFML, …) and games (Pacman, Nibbler, …) as `.so` files at runtime via `dlopen`, switching between them seamlessly without recompilation. Defined a clean `IComponent` interface to ensure full interchangeability. Collaborated with another group to validate ABI compatibility.
- Applied Factory, Strategy, and Interface patterns for extensibility
- Shared common interface with external team enabling cross-compatible libraries

---

**NanoTekSpice — Digital Logic Circuit Simulator** | *C++ / OOP / Design Patterns / Boolean Logic / Parser*
> Built a logic circuit simulator that parses a netlist configuration file to construct a component graph and simulates signal propagation tick by tick. Implemented a full chipset library (AND/OR/XOR/NOT gates, NAND/NOR, flip-flops, counters, shift registers, RAM/ROM) with a tri-state signal model (True / False / Undefined). Factory pattern used for generic component instantiation via `IComponent`.
- Implemented 20+ chipset types with correct undefined-state propagation
- Interactive REPL: simulate, display, set inputs, loop mode

---

**Plazza — Pizzeria Concurrent Simulation** | *C++ / Multithreading / IPC / Thread Pool / Load Balancing*
> Simulated a pizzeria using multi-process architecture with inter-process communication. The reception process parses pizza orders, balances them across kitchen child processes (spawned via `fork()`), each running a thread pool of cooks. Implemented C++ RAII wrappers for processes, threads, mutexes, and condition variables. Kitchens self-destruct after 5 seconds of inactivity.
- Designed IPC serialization/deserialization for pizza objects across process boundaries
- Implemented work-stealing load balancing across dynamically spawned kitchens

---

**MyTeams — Collaborative Chat Application** | *C / TCP Sockets / Custom Protocol / UUID / Persistence*
> Implemented a Microsoft Teams-like server and CLI client in C. Server handles concurrent clients with `select()`, persisting users, teams, channels, threads, and messages across restarts. Designed a custom RFC-style protocol. Enforced access control (unauthenticated users cannot see connected users; unsubscribed users do not receive team events).
- Designed a stateful custom text-based protocol with session management
- Implemented persistent storage and full server state reload on restart

---

**MyFTP — FTP Server** | *C / TCP / RFC 959 / Active & Passive Mode / fork()*
> Implemented an RFC 959-compliant FTP server in C supporting anonymous authentication, active and passive data transfer modes, and simultaneous clients managed via `poll()`. Data transfers are handled in forked child processes. Tested against real FTP clients (FileZilla, lftp).

---

**Malloc — Custom Memory Allocator** | *C / Systems Programming / brk/sbrk / Best-Fit Algorithm*
> Reimplemented `malloc`, `calloc`, `realloc`, `reallocarray`, and `free` as a shared library using only `brk`/`sbrk`. Implemented best-fit free-block selection, power-of-2 memory alignment, and break-pointer alignment to multiples of 2 pages. Drop-in replacement tested against real programs.

---

**Strace — System Call Tracer** | *C / Linux / ptrace / x86-64 / ELF*
> Built a `strace` alternative using `ptrace` to intercept and display system calls in real time for a traced process or by PID. Default mode outputs hex arguments and return values. With `-s` flag, displays human-readable strings, decimal integers, and expanded structs, matching the behavior of the system `strace`.

---

**Wolfram — Elementary Cellular Automaton** | *Haskell / Functional Programming / Infinite Sequences*
> Implemented Wolfram's elementary cellular automaton (rules 30, 90, 110) in Haskell using idiomatic functional patterns: infinite lazy lists, pattern matching, higher-order functions, pure/impure separation, and partial application. The world is infinite in all directions; the terminal window is a sliding viewport over it.

---

**My Marvin — Jenkins CI/CD** | *Jenkins / JCasC / Job DSL / Groovy / DevOps*
> Configured a full Jenkins instance using Configuration-as-Code (JCasC YAML) and Job DSL Groovy scripts. Set up role-based authorization with fine-grained permissions, user management, a `SEED` job that dynamically generates project pipelines triggered by GitHub SCM polling, and a `clone-repository` freestyle job. All passwords injected via environment variables (no hardcoded secrets).

---

**Octopus — Ansible Configuration Management** | *Ansible / DevOps / systemd / PostgreSQL / Redis / Flask / Node.js*
> Automated the deployment of a multi-tier voting application (Flask poll → Redis → Java worker → PostgreSQL → Node.js result) across 5 separate virtual machines using Ansible playbooks and roles. All services managed by systemd with environment-variable-based configuration. Vault-encrypted secrets, fully idempotent playbooks (0 changed tasks on repeated runs).

---

### Semester 2

**Corewar — Virtual Machine** | *C / Assembly / Virtual Machine / Scheduling*
> Implemented the Corewar virtual machine: a multi-program, simulated-parallel execution environment. The VM loads champion `.cor` binaries into a shared memory arena, decodes and executes 16 custom assembly instructions (live, ld, st, add, sub, and/or/xor, zjmp, ldi, sti, fork, lld, lldi, lfork, aff), manages process scheduling, carry flag, and death-cycle logic until one champion remains.

---

**42sh — Unix Shell** | *C / POSIX / Process Management / Job Control / Lexer/Parser*
> Built a feature-complete Unix shell compatible with TCSH in a 4-5 person team. Implemented: inhibitors (`''`, `""`), globbing (`*`, `?`, `[]`), job control (`&`, `fg`, `bg`), backtick substitution, parentheses, local/environment variables, special variables (`cwd`, `history`), `!` history expansion, aliases, multi-line line editing with dynamic auto-completion, and shell scripting.

---

**EpyTodo — RESTful TODO API** | *Node.js / Express / MySQL / JWT / bcrypt*
> Built a RESTful backend for a task management application. Designed a MySQL schema with `user` and `todo` tables with foreign key relationships. Implemented JWT-based authentication middleware protecting private routes, bcrypt password hashing, and full CRUD endpoints for users and todos.

---

---

## 🏷 Skills Summary (extracted from projects)

| Category | Technologies |
|---|---|
| Languages | C, C++, Haskell, Rust, Python, JavaScript/TypeScript, Node.js |
| AI / ML | Neural networks (from scratch), Minimax/Alpha-Beta, Supervised Learning |
| Cryptography | AES-128, RSA, PGP, XOR, Big-integer arithmetic |
| Systems | OS kernel (boot, interrupts, virtual memory, syscalls), ptrace, malloc/brk, ELF, virtual machines, process scheduling |
| Networks | TCP sockets, select/poll, FTP (RFC 959), custom protocols |
| DevOps | Docker, Docker Compose, Jenkins, Ansible, CI/CD, JCasC |
| Web | REST APIs, JWT, OAuth2, Express, MySQL, React |
| Concurrency | Threads, mutexes, IPC, thread pools, fork, load balancing |
| Compilers | Lexer, parser (from scratch), AST, bytecode VM, code generation |
| OOP/Design | Dynamic libraries, factory pattern, interface design, RAII |
