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

## Playable games, probability models and cross-language execution — TGSlots

[Source and screenshots](https://github.com/lilter96/tgslots) ·
[Mathematical walkthrough](https://github.com/lilter96/tgslots/blob/master/docs/mathematics.md) ·
[Backend verification](https://github.com/lilter96/tgslots/blob/master/docs/x7-verification.md) ·
[Real gameplay promos](https://lilter96.github.io/portfolio/#showreel)

Five games expose different mathematical and state-management problems: classic
paylines, interactive picks, combat cascades with giant sticky WILDs, and Hold &
Spin with column boosters, plus Nine Lives collector cascades. The runtime stack is TypeScript/Bun/Elysia/PixiJS 8/
GSAP, with a React marketing frontend. X7 additionally supports Go + RabbitMQ.

For a 15-minute review:

1. Read the mathematical walkthrough's separation of probability sampling,
   deterministic evaluation, feature state and paid-result accounting.
2. Trace the shared payline trie or cluster BFS, then Le Militare's position
   weights: a five-row giant connects across five cells but counts as one symbol.
3. Compare Woodland's actual game with the separate Python analytical reference.
   The first repeated weighted draw and free-spin retriggers both affect expected
   return; the report derives approximately 96.0006% normal-round RTP.
4. Inspect X7's common seeded executor, Bun local server and Go/RabbitMQ path.
   The math worker never owns the wallet; request identity, revision and pending
   seed preserve an outcome across retries.
5. Watch the matching gameplay and inspect the API tests for duplicate charges,
   complete bought bonuses, stale revisions and unavailable upstreams.

Nine Lives adds shared-engine collector cascades and a common revisioned Bun
session client. Its stored 10M base + 1M purchase audit reports 97.3574% normal
and 96.0103% purchase return; the base 95% interval excludes the 96% target.
[Verification and limits](https://github.com/lilter96/tgslots/blob/master/docs/nine-lives-verification.md).

On 2026-10-08, **812 workspace tests**, typechecks and lint passed; the web-client
production build and **7 Go tests under the race detector** passed. Live smoke
checks completed X7 bonuses through the full API in both backend modes. All
three other games passed state + spin checks on both API instances.

Le Militare's **81.6M complete verification rounds** use seed streams separate
from calibration while executing the actual game engine. This is held-out Monte
Carlo verification, not a separately implemented cluster/combat evaluator.
Woodland's Python reference is independent of its RNG and evaluator. X7's stored
report separates 5M normal rounds from 1M purchases and normalizes purchase return
by its actual cost. Alias sampling has documented finite-precision thresholds;
RTP intervals and point estimates are not exact probability claims.

The website hosts videos; interactive play currently requires a running API.
Both X7 modes retain in-memory demo sessions. They do not provide durable wallet
accounting across process restarts or a certified real-money deployment.

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
