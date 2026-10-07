# A technical reading guide

The repositories demonstrate different kinds of engineering. Start with a problem, follow the implementation, then read the tests and the stated limits. The counts below are verification records, not measures of professional seniority.

## Backend reliability and AI workflows — JobFinder

[Source and architecture](https://github.com/lilter96/jobfinder-showcase) · [Publication verification](https://github.com/lilter96/jobfinder-showcase/blob/main/docs/PUBLICATION-VERIFICATION.md)

A workflow can survive a restart and still make the wrong decision if it acts on an outdated draft or retries an external action with an unknown result. This project makes those boundaries explicit through revision witnesses, durable feature state, transactional outbox and reconciliation. LLM work uses typed task contracts and versioned recipes rather than treating generated text as an unconditional action.

For a 15-minute review: read the README architecture, follow a workflow's state transitions and its external-outcome boundary, then inspect `WolverineIntegrationTests`. The publication ran 929 core/LLM/recorded-source tests and 10 actual PostgreSQL/process-boundary tests. The historical larger suite is described separately; it was not rerun in full for publication. The public snapshot excludes personal subscriptions, accounts and working history.

## Streaming, concurrency and failure contracts — Realtime Primitives

[Source and test map](https://github.com/lilter96/dotnet-realtime-primitives)

Read the circuit breaker's failure domains and half-open probe rules, retained audio acquisition/replay semantics, then the bounded flight recorder's behavior when a sink blocks or fails. The 89 tests cover these extracted contracts with local doubles and controllable time. The extraction is not the full application, a published NuGet package, or a throughput benchmark.

## Probability and deterministic computation — Slot Math Lab

[Source and documented limitations](https://github.com/lilter96/slot-math-lab)

Compare exact rational interpretation with sampling; trace deterministic random streams into graph compilation. The interesting engineering is the semantic contract between representations and execution modes. The 704 locally passing core tests do not establish complete frontend/E2E acceptance or casino certification. The existing full CI requires follow-up.

## Geometry and host integration — AccessRoute + ModelGuard

[AccessRoute](https://github.com/lilter96/access-route-revit) · [ModelGuard](https://github.com/lilter96/model-guard-revit) · [Fresh benchmark](https://github.com/lilter96/access-route-revit/blob/main/docs/evidence/benchmark-2026-10-07.json)

Trace a nearest-segment query through the BVH and a route through Dijkstra. Then inspect versioned storage and the Revit boundary: transactions, ownership and model parameters. The pair shares 55 core and 13 presentation tests, so these are not two independent 68-test achievements.

On 2026-10-07, a synthetic 7,080-segment/1,500-query run measured 5.3273 ms indexed versus 59.873 ms exhaustive, with zero distance error; 500 device routes succeeded in 134.8231 ms. Timings depend on machine and input. The benchmark runs outside Revit. Host execution, production deployment and Tekla API experience are not established by these results.

## Product implementation and game tooling — TGSlots

[Source and verification notes](https://github.com/lilter96/tgslots)

Review the modular game packages, state transitions and Monte Carlo tooling, then the PixiJS rendering boundary. The actual stack is TypeScript/Bun/Elysia/PixiJS/React. It is not evidence of an ASP.NET/SignalR/Hangfire casino platform. Locally, 736 tests, all workspace typechecks and lint passed after explicitly supplying Node worker typings. The API uses prototype in-memory state.

## Full-stack delivery — Portfolio

[Source](https://github.com/lilter96/portfolio) · [ADRs](https://github.com/lilter96/portfolio/tree/main/docs/adr) · [Website](https://lilter96.github.io/portfolio/)

Read versioned endpoints, cache/health boundaries and the integration fixtures. The content API and React website demonstrate delivery discipline, not casino mathematics. On 2026-10-07, 56 backend tests and 43 frontend tests passed; endpoint smoke tests now use isolated PostgreSQL/Redis fixtures. GitHub Pages serves curated content without depending on a separately deployed API. Contact remains a real email/LinkedIn link in that mode.

## Cross-language execution systems and Python signal processing

[Trading Systems Lab](https://github.com/lilter96/trading-systems-lab) adds C#/Go and shared protobuf contracts. Read order state and audit immutability, then compare the engine with the independent watchdog. The public suite requires a disposable PostgreSQL database: 151 tests passed, one optional memory benchmark skipped. The fixture loads the actual deployment trigger and verifies both EF and direct SQL mutation rejection. Go watchdog tests passed. The complete deployed system and live exchange behavior remain unverified.

[Signal Processing Lab](https://github.com/lilter96/signal-processing-lab) adds Python async orchestration, typed LLM/media parsing, SQLite campaign persistence, risk rules and dry-run execution. Its sanitized snapshot passed 340 offline tests. Personal account configuration, harvested corpus, provider recordings and performance exports are excluded. Neither profitable signal quality nor real-provider acceptance is claimed.

## Supporting older work

- [MekashronTest](https://github.com/lilter96/MekashronTest): CMS and WCF/SOAP integration in an assignment.
- [Realtime Chat](https://github.com/lilter96/realtime_chat): older SignalR/React integration demo; review its authentication, room isolation and in-memory concurrency limits before treating it as a reference architecture.
- [StatsHub](https://github.com/lilter96/statshub): a smaller CQRS/cache/dashboard example.
- [TestJob](https://github.com/lilter96/TestJob): focused parsing/API/encryption assignment; 19 tests passed during the audit.

AI-assisted implementation is part of the workflow. The useful evidence is the explicit architecture, constraints, tests and review artifacts—not an unmeasured percentage of generated code.
