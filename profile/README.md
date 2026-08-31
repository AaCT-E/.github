# AaCT-E

**AaCT-E develops evaluator- and procurement-facing executable evidence for admissibility at the point where a proposed action would become consequential.**

The organization packages narrow, reproducible scenarios that let reviewers inspect how commit-time evaluation, recoverability, and fail-closed behavior work without requiring them to trust a narrative description.

## Current focus

The public **demo** repository provides executable scenarios and verification around commit-time safety enforcement, including aviation-oriented examples. **telemetry** supports observation and evidence about those runs.

The core pattern is:

```text
candidate action
-> current governed state
-> admissibility / recoverability evaluation
-> ALLOW / DENY / FAIL_CLOSED
-> trace / receipt / verification
```

## Relationship to GCAT/BCAT and StegVerse

AaCT-E is an applied evidence surface downstream of GCAT/BCAT research and related StegVerse tooling. It translates formal concepts into runnable cases for independent inspection.

A passing demonstration is evidence about the frozen case. It does not create regulatory approval, procurement award, operational authority, third-party endorsement, or authority beyond the scope explicitly represented in the result.
