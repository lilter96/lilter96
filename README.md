# Terentiy Gatsukov

### Senior .NET Backend Engineer

**Durable workflows · Real-time systems · Game mathematics · BIM automation**

I build services and engineering tools with C# and .NET. My work focuses on the boundaries where software becomes difficult: state that survives a process crash, concurrent streams with bounded memory, reproducible probability models, and geometry inside engineering applications.

[Portfolio website](https://lilter96.github.io/portfolio/) · [LinkedIn](https://www.linkedin.com/in/terentiy-gatsukov-048694224/) · [Engineering walkthroughs](docs/ENGINEERING.md)

## Six projects, six engineering perspectives

| Project | What it demonstrates | Verified evidence |
| --- | --- | --- |
| **[JobFinder](https://github.com/lilter96/jobfinder-showcase)** | .NET 10 / PostgreSQL / Wolverine / Blazor. Durable workflows, transactional outbox, revision witnesses, typed LLM recipes, and reconciliation when an external outcome is unknown. | **939 selected tests**, including PostgreSQL transport and process-termination recovery; [verification](https://github.com/lilter96/jobfinder-showcase/blob/main/docs/PUBLICATION-VERIFICATION.md). |
| **[Slot Math Lab](https://github.com/lilter96/slot-math-lab)** | Exact rational and Monte Carlo interpreters, deterministic RNG streams, graph compilation and a React editor. | **704 core tests** passed locally. Research prototype; full CI still needs follow-up. |
| **[Realtime Primitives](https://github.com/lilter96/dotnet-realtime-primitives)** | Circuit breakers, typed HTTP failures, retained audio replay and a bounded, nonblocking flight recorder. Extracted from a larger personal application. | **89 offline tests**, public CI; [contracts and limits](https://github.com/lilter96/dotnet-realtime-primitives#readme). |
| **[AccessRoute for Revit](https://github.com/lilter96/access-route-revit)** | BVH spatial search, Dijkstra routing, versioned storage, Revit 2021–2025 adapters and WPF/MVVM. | **68 core/ViewModel tests**; indexed queries **~11.2× faster** on a synthetic benchmark. [Raw results](https://github.com/lilter96/access-route-revit/blob/main/docs/evidence/benchmark-2026-10-07.json). |
| **[TGSlots](https://github.com/lilter96/tgslots)** | TypeScript / Bun / Elysia / PixiJS 8 / React. Modular game math, rendering and Monte Carlo tooling. | **736 tests** and lint passed locally. Simulation-runner typecheck needs follow-up. |
| **[Engineering Portfolio](https://github.com/lilter96/portfolio)** | Versioned .NET 10 content API, PostgreSQL/Redis, React 19, Testcontainers, Docker, ADRs and CI. This profile's delivery monorepo. | **56 backend + 43 frontend tests**, isolated database fixtures; [architecture decisions](https://github.com/lilter96/portfolio/tree/main/docs/adr). |

## More breadth, with clear boundaries

- **C# + Go systems:** [Trading Systems Lab](https://github.com/lilter96/trading-systems-lab) covers order state, protobuf/gRPC contracts, PostgreSQL audit immutability and an independent emergency watchdog. **151 .NET tests passed, 1 optional benchmark skipped**; Go watchdog tests passed. No live exchange or profitability claim.
- **Python + LLM/media:** [Signal Processing Lab](https://github.com/lilter96/signal-processing-lab) shows async parsing, persisted campaigns, dry-run execution and risk invariants. **340 offline tests passed**; live providers and screener acceptance were not verified.

- **BIM model integrity:** [ModelGuard](https://github.com/lilter96/model-guard-revit) covers parameter contracts, transactional mark updates and worksharing ownership. It shares the AccessRoute core/test suite. **Revit-host execution is not yet verified** for either plugin; this is practical portfolio experience, not commercial Tekla experience.
- **Enterprise integration:** [MekashronTest](https://github.com/lilter96/MekashronTest) is an older assignment with Umbraco and WCF/SOAP integration.
- **Earlier real-time work:** [Realtime Chat](https://github.com/lilter96/realtime_chat) shows SignalR and React integration; [StatsHub](https://github.com/lilter96/statshub) adds CQRS, caching and a dashboard. These are supporting demos, with narrower scope than the projects above.

## How I work

I use AI-assisted development. Architecture, constraints, verification and final review remain my responsibility. I document trade-offs and distinguish a passing test, a synthetic benchmark and a production result.

**Core:** C# · .NET · ASP.NET Core · PostgreSQL · Redis · Wolverine · Docker · GitHub Actions  
**Across the stack:** React / TypeScript · Blazor · Revit API · WPF / MVVM · deterministic simulation

<sub>Verification recorded on 2026-10-07. Test counts describe different suites, not comparable project scores or production reliability guarantees.</sub>
