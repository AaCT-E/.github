# Contributing to AaCT-E

Thank you for your interest in the Admissibility at Commit-Time Engine.

## Getting Started

1. **Clone the demo repo:**
   ```bash
   git clone https://github.com/AaCT-E/demo.git
   cd demo
   python verify_demo.py
   ```

2. **Read the spec:** [`DEMO_SPEC.md`](https://github.com/AaCT-E/demo/blob/main/DEMO_SPEC.md)

3. **Check the architecture:** [`aacte.architecture.json`](https://github.com/AaCT-E/demo/blob/main/aacte.architecture.json)

## Contribution Guidelines

- **Zero-dependency policy:** The demo uses only the Python standard library.
- **Verification required:** All changes must pass `verify_demo.py`.
- **Trace compatibility:** Scenario JSON format is stable — changes require schema version bump.
- **Ecosystem awareness:** Changes affecting StegDB hooks or Publisher integration need cross-repo coordination.

## Code of Conduct

Be respectful, constructive, and safety-focused. This project deals with aviation safety formalism — rigor matters.

## Questions?

Open an issue at [github.com/AaCT-E/demo/issues](https://github.com/AaCT-E/demo/issues).
