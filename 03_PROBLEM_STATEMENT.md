# Problem Statement

## The operational problem

In professional broadcast operations, the real system is rarely represented in one authoritative place.

A typical answer to the question “Where does this signal go?” may require combining:

- a vendor manual;
- a console configuration;
- a DSP engine route;
- an AoIP channel assignment;
- a processor preset;
- a physical patch;
- a relay or GPIO relationship;
- an old incident log;
- a shift engineer’s memory.

This creates five structural failures.

## 1. Knowledge fragmentation

Information exists, but in incompatible forms:

- PDF manuals;
- web interfaces;
- configuration backups;
- screenshots;
- spreadsheets;
- handwritten notes;
- logs;
- email threads;
- personal memory.

## 2. Capability/configuration confusion

Manuals say what a device *can* do. Engineers need to know what the installed device *is doing*.

This distinction is often lost in informal documentation and generic AI workflows.

## 3. Institutional memory loss

When experienced engineers leave, the reasons behind many design decisions disappear:

- why this route exists;
- why a backup is intentionally disabled;
- why a GPIO contact must not be reused;
- why an old processor remains in the chain;
- why a specific latency or QoS setting was chosen.

## 4. Unsafe automation pressure

Once an AI system is connected to infrastructure, there is pressure to make it “do things.” In broadcast environments, autonomous action can be unacceptable. A wrong route, firmware action, reboot, preset change, or failover activation can create immediate on-air consequences.

## 5. Lack of evidence-aware reasoning

Most current AI systems are optimized for plausibility. Engineering operations require traceability.

The system must be able to say:

- “This is proven by an exported configuration.”
- “This is known only from the manual.”
- “This is an operator observation.”
- “This remains unknown.”
- “This recommendation cannot be made until a station policy or telemetry source is available.”

## Required outcome

BKE should create a working engineering memory that:

1. preserves evidence;
2. distinguishes fact from inference;
3. identifies unknown parameters systematically;
4. produces safe acquisition plans;
5. supports human engineers during diagnosis;
6. incrementally reconstructs station topology;
7. remains safe by default.

## Example

A processor manual confirms that a device supports analog, AES, AoIP, backup inputs, presets, alarms, GPIO, and SNMP.

That does **not** prove:

- which input is active;
- whether backup is armed;
- what preset is loaded;
- whether alarms are present;
- whether AoIP is in use;
- whether the signal path is on-air.

BKE must preserve this difference.
