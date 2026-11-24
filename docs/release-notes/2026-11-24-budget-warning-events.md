---
date: 2026-11-24
feature: Budget warning thresholds for policy usage and observability
scope: feat
packages: ["@vegaforge/tollway-core", "@vegaforge/tollway-client", "@vegaforge/tollway-observability"]
scenario-impact: none
---

# Budget warning events

Policies can now configure integer basis-point warning thresholds on daily, lifetime, per-service, and per-resource spend limits. The agent emits `budget:warning` once per threshold crossing per limit period, re-arms after a period rollover, and bridges matching events to the observability hub as `budget.warning` without blocking `pay()`.
