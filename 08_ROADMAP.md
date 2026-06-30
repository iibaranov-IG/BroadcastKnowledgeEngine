# Roadmap

## Phase 0 — Foundation

**Status:** substantially underway

Deliverables:
- asset inventory;
- documentation domains;
- manual mapping;
- engineering profiles;
- knowledge coverage reports;
- manual-to-asset gap audits;
- safety-scoped acquisition profiles.

Success criterion:
- every known critical asset can be classified as known, partially known, unknown, or blocked for key engineering fields.

## Phase 1 — Evidence ingestion and parsers

Deliverables:
- artifact registry with checksums and provenance;
- vendor backup/config parser framework;
- parser contract tests;
- import dry-run mode;
- configuration-delta reports;
- redaction rules for secrets.

Priority targets:
- console/engine exports;
- AoIP node reports;
- processor configs;
- telephony configuration;
- workstation evidence.

Success criterion:
- imported artifacts produce structured station facts without leaking secrets.

## Phase 2 — Livewire / AoIP catalog

Deliverables:
- station source catalog;
- destinations/subscriptions model;
- source naming normalization;
- collision detection;
- unconsumed-source detection;
- unresolved-subscription report.

Success criterion:
- the system can identify candidate signal relationships across critical AoIP assets.

## Phase 3 — Signal-path reconstruction

Deliverables:
- graph-based main and backup paths;
- confidence scoring by evidence type;
- path gaps;
- device-to-device route explanations;
- diagram generation.

Success criterion:
- an engineer can ask “what is the evidence-backed path from source X to output Y?” and receive a traceable answer.

## Phase 4 — Vendor configuration intelligence

Deliverables:
- device-family parsers;
- profile-specific config reports;
- firmware/version inventory;
- preset and failover visibility;
- GPIO mapping model;
- station-policy comparison framework.

Success criterion:
- manuals and real configuration can be compared parameter by parameter.

## Phase 5 — Read-only telemetry

Deliverables:
- telemetry source catalog;
- polling policy;
- passive discovery design;
- health evidence model;
- event correlation;
- audio-presence integration where technically available.

Success criterion:
- system can distinguish configuration facts from current operational facts.

## Phase 6 — Incident investigations

Deliverables:
- incident evidence bundle;
- time-correlated event timeline;
- deterministic hypothesis generation;
- operator checklists;
- post-incident knowledge capture.

Success criterion:
- each incident produces reusable engineering knowledge rather than disappearing into chat history.

## Phase 7 — Continuous topology and documentation

Deliverables:
- generated station diagrams;
- topology change detection;
- evidence freshness reporting;
- stale-document warnings;
- human review workflow.

Success criterion:
- station architecture becomes easier to maintain than to ignore.

## Phase 8 — External validation and industry collaboration

Deliverables:
- anonymized case studies;
- reproducible demo data;
- vendor documentation coverage matrix;
- partner-facing research brief;
- deployment blueprint for other broadcasters.

Success criterion:
- an external engineering team can understand, evaluate, and pilot the approach without access to the original station.
