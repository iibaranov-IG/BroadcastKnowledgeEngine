# Research Brief

## Title

**Broadcast Knowledge Engine: An Evidence-First Architecture for Engineering Memory in Professional Broadcast Infrastructure**

## Abstract

Professional broadcast systems combine specialist hardware, legacy design decisions, proprietary protocols, physical signal paths, networked audio, timing systems, vendor-specific interfaces, and human operational practices. While individual devices are documented, the real configuration of a working station is often fragmented across manuals, handwritten notes, web interfaces, backups, informal knowledge, and the memories of engineers.

Broadcast Knowledge Engine (BKE) explores an alternative to generic “manuals + chatbot” approaches. It proposes an evidence-first architecture in which vendor knowledge, station configuration, and live telemetry remain distinct layers. AI may assist with interpretation, planning, and explanation, but the evidence model remains deterministic and traceable.

The project investigates how an engineering assistant can become useful without becoming unsafe: no autonomous writes, no implicit assumptions, no secret retention, and no claim of operational truth without supporting evidence.

## 1. Background

Broadcast infrastructure is unusually difficult to document because it is both technical and historical. A modern station may contain equipment from different vendors and eras, including IP consoles, DSP engines, AoIP nodes, codecs, audio processors, software workstations, encoders, phone hybrids, timing services, and relay logic.

Each subsystem may be understandable in isolation. The real challenge is the relationship between them:

- which source feeds which destination;
- what constitutes the main and backup paths;
- where audio is converted, processed, delayed, mixed, encoded, or distributed;
- which GPIO event triggers which operational behavior;
- which device owns clocking and timing;
- which settings are inherited, local, obsolete, or critical.

## 2. Why generic RAG is insufficient

A generic retrieval system can quote a manual. It cannot safely distinguish between:

- “the device supports AES67” and “AES67 is active in this station”;
- “this model has a backup input” and “this input is configured as the active failover path”;
- “DSCP 56 exists as an option” and “DSCP 56 is correct for this network”;
- “a firmware feature exists” and “this installed device runs a version containing it.”

For engineering use, these distinctions are essential. Incorrect certainty is more dangerous than uncertainty.

## 3. Research question

Can a production-grade engineering assistant be constructed around deterministic evidence acquisition, explicit confidence boundaries, and human approval—while still using advanced AI to accelerate analysis, documentation, and troubleshooting?

## 4. Design hypothesis

The proposed hypothesis is:

> An AI-assisted engineering system becomes more trustworthy when it reasons over an explicit evidence graph instead of treating all available text as equivalent truth.

BKE therefore uses:

- provenance-aware records;
- device-family engineering profiles;
- known / partially known / unknown / blocked states;
- acquisition plans tied to required evidence;
- deterministic reports before AI interpretation;
- human approval gates for any station interaction.

## 5. Evidence hierarchy

| Evidence class | Example | Permitted conclusion |
|---|---|---|
| Vendor documentation | User manual, release notes | Device capability |
| Station inventory | Asset IP, hardware identity | Device presence / identity |
| Exported configuration | Backup, official report, config file | Station configuration |
| Operator observation | Verified manual entry | Visible state at observation time |
| Log / alarm artifact | Syslog, event export | Historical operational event |
| Read-only telemetry | SNMP, status endpoint, passive feed | Current operational state |
| Inference | Architecture hypothesis | Candidate explanation only |

## 6. Prototype lessons

The initial prototype demonstrated that the biggest early gain is not “diagnosis.” It is honest visibility into ignorance.

A gap audit can reveal that a device is known by identity and documentation domain, but that its active input, output, firmware, presets, subscriptions, or failover state remain unknown. This is valuable because it converts vague discomfort into an actionable evidence collection plan.

## 7. Technical direction

BKE is expected to evolve around:

- structured evidence ingestion;
- vendor-specific parsers;
- AoIP and Livewire cataloging;
- configuration delta analysis;
- station topology reconstruction;
- passive read-only telemetry;
- incident correlation;
- explainable engineering recommendations.

## 8. Evaluation criteria

The system should be evaluated not only by answer quality, but by engineering safety:

- provenance completeness;
- rate of unsupported claims;
- time-to-understand for incidents;
- percentage of critical assets with configuration evidence;
- percentage of signal paths validated;
- reduction in repeated manual discovery;
- operator trust and correction rate.

## 9. Limitations

BKE cannot replace a competent broadcast engineer. It cannot infer live audio presence from manuals. It cannot validate QoS, PTP, or signal-path correctness without station-specific evidence. It cannot safely act on equipment without explicit approval and a formally designed control model.

## 10. Conclusion

The project is not primarily about making an LLM sound knowledgeable. It is about building a disciplined memory system for technical operations—one that knows what it knows, what it does not know, and what evidence is required next.
