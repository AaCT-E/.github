# AaCT-E — Admissibility at Commit-Time

Commit-time governance for real systems.

---

## What this is

AaCT-E (Admissibility at Commit-Time Engine) is a runtime enforcement layer that determines whether an action should be allowed at the exact moment it becomes irreversible.

Most systems evaluate before execution or audit after.

AaCT-E governs at the point of commit.

---

## Core idea

An action is allowed only if it preserves the system’s ability to remain within a recoverable and governable state.

If that condition fails, the action is denied.

---

## Why this matters

Modern systems increasingly:
- act autonomously
- chain decisions
- operate under partial information

Without enforcement at the commit boundary, systems can:
- drift into unsafe states through individually valid steps
- lose the ability to recover before failure is detected

AaCT-E closes that gap.

---

## What we build

- AaCT-E Engine — runtime admissibility resolver
- Simulation demos — minimal, reproducible proofs
- Formal models — admissibility, recoverability, invariance
- Execution-layer tooling — integration into real systems

---

## Current status

- Minimal working prototype (2-aircraft simulation)
- Commit-time allow/deny enforcement
- Deterministic replay + trace output

---

## Roadmap

- Multi-agent scenarios
- Disturbance-aware models
- Formal proof integration (barrier functions / reachability)
- Real system integration points

---

## Contact / Collaboration

We are actively exploring:
- SBIR / government partnerships
- safety-critical system integration
- research collaboration

---

AaCT-E enforces one rule:

> If recovery is no longer possible, the action does not occur.
