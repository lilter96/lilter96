# Terentiy Gatsukov

**Senior .NET Backend Engineer · Distributed Systems · iGaming · BIM Automation**

I build backend services and engineering tools with C# and .NET. My public work focuses on explicit architecture, performance, testable domain logic, and repeatable delivery.

[Engineering portfolio](https://lilter96.github.io/portfolio/) · [LinkedIn](https://www.linkedin.com/in/terentiy-gatsukov-048694224/)

### Selected engineering work

| Project | What to review |
| --- | --- |
| **[.NET Engineering Portfolio](https://github.com/lilter96/portfolio)** | .NET 10 / React 19 monorepo; PostgreSQL, Redis, Testcontainers, API versioning, ADRs, and backend/frontend CI. |
| **[AccessRoute for Revit](https://github.com/lilter96/access-route-revit)** | Cable routing with a BVH spatial index and Dijkstra; versioned storage; Revit 2021–2025 adapters; WPF/MVVM. |
| **[ModelGuard for Revit](https://github.com/lilter96/model-guard-revit)** | BIM parameter contracts, equipment references, and mark updates with transaction and worksharing ownership checks. |
| **[Realtime Chat](https://github.com/lilter96/realtime_chat)** | ASP.NET Core / SignalR / React; strongly typed hub, rooms, reconnect, WebSocket/SSE fallback, and Azure deployment configuration. |
| **[StatsHub](https://github.com/lilter96/statshub)** | Revenue dashboard with CQRS/MediatR, EF Core/PostgreSQL, Redis caching, SignalR updates, and React. |

### Evidence and boundaries

- **Modern .NET delivery:** the portfolio includes isolated integration tests, Docker, CI, coverage collection, and architecture decision records.
- **Routing performance:** on a synthetic benchmark of 7,080 segments and 1,500 nearest-segment queries, AccessRoute recorded **4.85 ms indexed vs 68.41 ms full scan**. Routing for 500 devices took **115 ms** in the core. [Method and raw results](https://github.com/lilter96/access-route-revit/blob/main/docs/evidence/benchmark.json).
- **BIM portfolio experience:** AccessRoute and ModelGuard share a core and ViewModel suite of **68 tests**. These are portfolio previews; **execution inside Revit and production deployment are not yet verified**. They demonstrate Revit API work, not commercial Tekla experience.
- **Enterprise integration:** [MekashronTest](https://github.com/lilter96/MekashronTest) is an older test assignment showing Umbraco and WCF/SOAP integration.

### How I work

I use AI-assisted development, with architecture, constraints, verification, and final review remaining my responsibility. I value reviewable changes, documented trade-offs, and tests that establish behavior rather than repeat implementation details.

**Core stack:** C# · .NET · ASP.NET Core · PostgreSQL · Redis · SignalR · Docker · GitHub Actions  
**Additional engineering:** React / TypeScript · Revit API · WPF / MVVM
