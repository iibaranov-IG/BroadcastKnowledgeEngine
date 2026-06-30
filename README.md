# Broadcast Knowledge Engine

**Engineering memory for broadcast infrastructure.**

Broadcast Knowledge Engine (BKE) is a safety-first architecture for preserving, validating, and applying engineering knowledge in professional broadcast environments.

It is not an autonomous control system. It does not change production equipment. It does not collect or store passwords. It does not treat a vendor manual as proof of station configuration.

Instead, BKE creates a traceable chain:

```text
Evidence → normalization → knowledge model → deterministic reasoning → engineer-reviewed action
```

The project is being developed from real operational workflows in a commercial broadcast environment. Specific organization, geography, asset names, IP addresses, credentials, and production configurations are intentionally omitted from the public materials.

## The problem

Broadcast plants often outlive their original documentation and the engineers who built them. A signal path may be operational but poorly understood. The result is slow troubleshooting, unsafe change decisions, and institutional knowledge loss.

## The thesis

AI becomes useful in production engineering only when it is constrained by evidence, safety boundaries, and human validation.

> **Deterministic first. AI second.**

## Current prototype capabilities

- asset inventory and manual asset mapping;
- vendor documentation coverage;
- engineering profiles by device family;
- manual-to-asset gap audits;
- safety-scoped knowledge acquisition plans;
- deterministic reasoning templates;
- signal-path and station-architecture models;
- report generation for known vs. unknown configuration facts.

## Non-goals

- autonomous routing changes;
- autonomous firmware upgrades;
- storage of passwords, API tokens, SIP credentials, or admin secrets;
- unaudited device login or network probing;
- declaring live signal state without telemetry or explicit operator evidence.

## Repository map

- `01_EXECUTIVE_SUMMARY.md` — concise project overview
- `02_RESEARCH_BRIEF.md` — research and design rationale
- `03_PROBLEM_STATEMENT.md` — the engineering problem being addressed
- `04_ARCHITECTURE.md` — system architecture and data model
- `05_KNOWLEDGE_ACQUISITION.md` — evidence acquisition framework
- `06_SAFETY_MODEL.md` — safety model and operating boundaries
- `07_CODEX_COLLABORATION.md` — human–Codex collaboration model
- `08_ROADMAP.md` — staged delivery roadmap
- `09_OPENAI_LETTER.md` — draft partnership inquiry
- `10_ENGINEERING_PHILOSOPHY.md` — principles and decision rules
- `diagrams/` — Mermaid source diagrams
- `docs/` — supporting technical notes
- `examples/` — anonymized case formats

## Team model

| Role | Responsibility |
|---|---|
| Project owner / technical director | Operational truth, strategy, acceptance criteria |
| Broadcast validation engineer | Shift-level validation, real-world workflow review, evidence collection |
| ChatGPT | Architecture, technical writing, specification, analysis support |
| Codex | Code implementation, reports, tests, deterministic tooling |

## Status

Early technical prototype. The project has a working evidence-and-gap-analysis layer; live telemetry and production integration remain future work.

## License

Draft materials only. Select an appropriate license before public release.
