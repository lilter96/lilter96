# Terentiy Gatsukov

### Senior .NET Backend Engineer · Distributed Systems & iGaming

**Durable workflows · Real-time systems · Slot mathematics · BIM automation**

I have **5+ years of commercial experience** across gaming, marketplace SaaS,
transportation and IoT. I build backend systems where state, concurrency,
probability and failure handling need explicit contracts.

At **Custom Games Studio, November 2023–July 2026**, my work included:

- Approximately **15 game backends** delivered from implementation to production.
- A shared **C# / F# library used in 20+ titles**, including probability composition,
  samplers, nested-feature execution and simulation infrastructure.
- **5,000+ RPS** bet processing with duplicate-charge protection, and simulations
  of **1 billion+ spins** across multiple machines.
- A **6× calculation speedup**, reducing a simulation workload from three hours
  to 30 minutes through memory and allocation optimizations.

These are commercial results reported in my
[CVs and experience](https://lilter96.github.io/portfolio/#experience).
The public projects below provide separate, inspectable engineering evidence.

**[Portfolio & game videos](https://lilter96.github.io/portfolio/)** ·
[LinkedIn](https://www.linkedin.com/in/terentiy-gatsukov/) ·
[Email](mailto:lilter96dotnet@gmail.com) ·
[Telegram](https://t.me/lilter96) ·
[Technical reading guide](docs/ENGINEERING.md)

## Selected engineering work

| Project                                                                           | Engineering perspective                                                                                                                                                                                 | Evidence to inspect                                                                                                                                                                                                                                              |
| --------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **[JobFinder](https://github.com/lilter96/jobfinder-showcase)**                   | **Durable .NET workflows and AI integration.** .NET 10 / PostgreSQL / Wolverine / Blazor; transactional outbox, revision witnesses, typed LLM recipes and reconciliation of uncertain external effects. | **939 selected publication tests**, including actual PostgreSQL transport and process-termination recovery. [Verification](https://github.com/lilter96/jobfinder-showcase/blob/main/docs/PUBLICATION-VERIFICATION.md).                                           |
| **[TGSlots](https://github.com/lilter96/tgslots)**                                | **Playable games, probability models and cross-language backend boundaries.** Five games; **Nine Lives flagship**; TypeScript/Bun, PixiJS 8, GSAP, shared math and simulation tooling; X7 supports Bun or **Go + RabbitMQ**.     | **812 workspace tests**, **7 Go race-tested cases**; Le Militare has **81.6M complete verification rounds**. [Math walkthrough](https://github.com/lilter96/tgslots/blob/master/docs/mathematics.md) · [Promos](https://lilter96.github.io/portfolio/#showreel). |
| **[Slot Math Lab](https://github.com/lilter96/slot-math-lab)**                    | **Exact and sampled computation in .NET.** Rational distributions and Monte Carlo interpreters, deterministic RNG streams, graph compilation and a React 19 editor.                                     | **704 core tests** verified locally. Research prototype; complete CI/E2E still requires follow-up. [Implementation and scope](https://github.com/lilter96/slot-math-lab#readme).                                                                                 |
| **[Realtime Primitives](https://github.com/lilter96/dotnet-realtime-primitives)** | **Concurrency and resilience contracts.** .NET 10 circuit breakers, typed HTTP failures, retained audio replay and a bounded, nonblocking flight recorder.                                              | **89 offline tests** and public CI. [Contracts and test map](https://github.com/lilter96/dotnet-realtime-primitives#readme).                                                                                                                                     |
| **[AccessRoute for Revit](https://github.com/lilter96/access-route-revit)**       | **Geometry and BIM integration.** BVH spatial search, Dijkstra routing, versioned storage, Revit 2021–2025 adapters and WPF/MVVM.                                                                       | **68 shared core/ViewModel tests**; indexed queries **~11.2× faster** in a synthetic benchmark. [Raw evidence](https://github.com/lilter96/access-route-revit/blob/main/docs/evidence/benchmark-2026-10-07.json). Revit-host execution remains unverified.       |
| **[Engineering Portfolio](https://github.com/lilter96/portfolio)**                | **Full-stack delivery.** Versioned .NET 10 API, PostgreSQL/Redis, React 19, Testcontainers, Docker, ADRs and CI.                                                                                        | **56 backend + 43 frontend tests** recorded during verification. [Architecture decisions](https://github.com/lilter96/portfolio/tree/main/docs/adr) · [Published website](https://lilter96.github.io/portfolio/).                                                |

## Game engineering you can see and review

[![Nine Lives: the new TGSlots flagship, cat Reaper and cluster cascades](https://raw.githubusercontent.com/lilter96/tgslots/master/docs/media/nine-lives.webp)](https://lilter96.github.io/portfolio/#showreel)

**Nine Lives** — new flagship: cat-Reaper collection, cluster cascades and a carried bonus multiplier.  
**Ancient Dragon** — classic paylines, mystery symbols and free spins.  
**Woodland Whisper** — interactive card picks and independently calculated expected return.  
**Le Militare** — combat cascades, persistent multipliers and giant sticky WILDs.  
**X7 Club** — locked coin prizes, Hold & Spin and column boosters.

[Nine Lives · 1440p promo](https://lilter96.github.io/portfolio/media/slots/nine-lives-promo.mp4) ·
[LinkedIn edit](https://lilter96.github.io/portfolio/media/slots/nine-lives-linkedin.mp4) ·
[Original capture](https://github.com/lilter96/tgslots/releases/tag/nine-lives-media-2026-10-08).
Real normal-speed gameplay; 120 FPS landscape export from approximately 77 actual
captured frames/s. Licensed music, no game sound effects.

The showcase now includes all five games, with Nine Lives first. The source explains the RNG boundary,
weighted samplers, payline trie, cluster BFS, bonus states, wager normalization
and complete-round verification. Le Militare's verification uses held-out seed
streams on the actual engine; Woodland additionally has a separate Python
analytical reference. Test results, sampling estimates and analytical expectations
are identified individually.

[Watch the five-game promo](https://lilter96.github.io/portfolio/media/slots/tgslots-reel.mp4) ·
[Read the mathematics](https://github.com/lilter96/tgslots/blob/master/docs/mathematics.md) ·
[Review both X7 backend modes](https://github.com/lilter96/tgslots/blob/master/docs/x7-verification.md)

The games currently run locally with an API; the portfolio hosts videos.

## More engineering perspectives

- **C# + Go execution boundaries:** [Trading Systems Lab](https://github.com/lilter96/trading-systems-lab) — order state, protobuf/gRPC contracts, PostgreSQL audit immutability and an independent emergency watchdog. **151 .NET tests passed, one optional benchmark skipped**; Go watchdog tests passed.
- **Python + LLM/media orchestration:** [Signal Processing Lab](https://github.com/lilter96/signal-processing-lab) — async parsing, persisted campaigns, typed model output, dry-run execution and risk invariants. **340 offline tests**; live-provider acceptance remains separate.
- **BIM model integrity:** [ModelGuard](https://github.com/lilter96/model-guard-revit) — parameter contracts, transaction-safe mark updates and worksharing ownership. Shares AccessRoute's core/test suite; Revit-host execution remains unverified.
- **Enterprise integration:** [MekashronTest](https://github.com/lilter96/MekashronTest) — an older Umbraco / WCF / SOAP / SQL Server assignment.
- **Earlier application work:** [Realtime Chat](https://github.com/lilter96/realtime_chat) and [StatsHub](https://github.com/lilter96/statshub) — SignalR, React, CQRS and caching, with narrower demo scope.

## How I work

I use **AI-assisted development** with explicit constraints, architecture decisions,
verification artifacts and final review. Architecture, acceptance decisions and
engineering responsibility remain mine. I distinguish a passing contract test,
a synthetic benchmark, a mathematical expectation and a commercial result.

**Backend:** C# / F# · .NET / ASP.NET Core · PostgreSQL / SQL Server · Redis · Kafka / RabbitMQ · outbox / idempotency · Docker · CI/CD  
**Across the stack:** React / TypeScript · Blazor · Go · Python · Revit API · WPF/MVVM · probability models and deterministic simulation

<sub>Verification records span 2026-10-07–08; the linked reports define each suite's scope. Counts are not comparable project scores or production reliability guarantees.</sub>
