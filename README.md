# AaCT-E — Admissibility at Commit-Time Engine

> **Executable procurement evidence for the GCAT/BCAT safety formalism.**

[![Ecosystem](https://img.shields.io/badge/ecosystem-GCAT%2FBCAT-blue)](https://github.com/GCAT-BCAT-Engine)
[![License](https://img.shields.io/badge/license-Apache--2.0-green)](https://github.com/AaCT-E/demo/blob/main/LICENSE)

---

## What is AaCT-E?

**AaCT-E** (Admissibility at Commit-Time Engine) is the procurement-facing demonstration layer of the GCAT/BCAT research ecosystem. It translates formal safety proofs into **runnable, verifiable artifacts** that FAA/TSSC reviewers and SBIR evaluators can execute in seconds.

### The Core Claim

> At the exact moment an action would become operationally real, the system can evaluate whether recovery remains available and **deny** the action if it would push the system into an unrecoverable or separation-violating state.

This is **commit-time safety enforcement** — not pre-approved authority, not post-hoc audit, but governance at the boundary between decision and effect.

---

## Repositories

| Repo | Purpose | Status |
|------|---------|--------|
| **[`demo`](https://github.com/AaCT-E/demo)** | Minimal runnable prototype — Phase I evidence | 🟢 Active |

---

## Ecosystem

AaCT-E sits between **theory** and **operations** in the GCAT/BCAT pipeline:

```
┌─────────────────────┐     ┌─────────────────────┐     ┌─────────────────────┐
│  GCAT-BCAT-Engine   │────▶│  GCAT-BCAT-Engine   │────▶│    AaCT-E/demo      │
│  (Formal Theory)    │     │  /Publisher           │     │  (Executable Demo)    │
│  Proofs, Metrics    │     │  Papers, Submissions  │     │  Procurement Evidence │
└─────────────────────┘     └─────────────────────┘     └─────────────────────┘
            │                                               │
            └───────────────────────────────────────────────┘
                              StegVerse Ecosystem
                    ┌─────────┐    ┌─────────┐    ┌─────────┐
                    │ StegDB  │    │  SDK    │    │  Site   │
                    │ Monitor │    │ Validate│    │ Publish │
                    └─────────┘    └─────────┘    └─────────┘
```

- **Upstream theory:** [GCAT-BCAT-Engine](https://github.com/GCAT-BCAT-Engine)
- **Paper publishing & social media:** [GCAT-BCAT-Engine/Publisher](https://github.com/GCAT-BCAT-Engine/Publisher)
- **Entity sandbox & monitoring:** [StegVerse-Labs/StegDB](https://github.com/StegVerse-Labs/StegDB)
- **User-facing validation:** [StegVerse-Labs/SDK](https://github.com/StegVerse-Labs/SDK)

---

## Quick Start

```bash
git clone https://github.com/AaCT-E/demo.git
cd demo
python run_demo.py      # Execute scenarios
python verify_demo.py   # Verify assertions
```

**Zero dependencies. Zero configuration. One command.**

---

## For Reviewers

- **FAA / TSSC:** See [`docs/PROCUREMENT.md`](https://github.com/AaCT-E/demo/blob/main/docs/PROCUREMENT.md)
- **SBIR Evaluators:** See [`docs/PROCUREMENT.md`](https://github.com/AaCT-E/demo/blob/main/docs/PROCUREMENT.md) → Commercialization Path
- **Academic Researchers:** See [`CITATION.cff`](https://github.com/AaCT-E/demo/blob/main/CITATION.cff) and upstream [Publisher](https://github.com/GCAT-BCAT-Engine/Publisher)

---

## Contact

- Issues: [github.com/AaCT-E/demo/issues](https://github.com/AaCT-E/demo/issues)
- Discussions: [github.com/GCAT-BCAT-Engine](https://github.com/GCAT-BCAT-Engine)
- Security: See [`SECURITY.md`](https://github.com/AaCT-E/.github/blob/main/SECURITY.md) (if available)

---

*AaCT-E is maintained by the GCAT/BCAT research group and integrated with the StegVerse ecosystem.*
