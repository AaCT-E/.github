# Security Policy

## Supported Versions

| Version | Supported |
|---------|-----------|
| 0.1.x   | ✅ Active |

## Reporting a Vulnerability

Given the safety-critical nature of this project's domain (aviation decision support), security concerns are taken seriously even at the demo stage.

**Please do not open public issues for security vulnerabilities.**

Instead, contact maintainers privately:
- Via GitHub Security Advisory (preferred)
- Or email security [at] aacte.org (if configured)

## What We Consider In Scope

- Deterministic execution guarantees
- Trace tampering / integrity
- CI pipeline integrity
- Dependency injection (though we have zero external dependencies)

## What Is Out of Scope

This is a research demo, not operational software:
- No live aircraft control
- No real-time data feeds
- No certified safety claims

## Response Timeline

| Severity | Acknowledgment | Fix Target |
|----------|---------------|------------|
| Critical | 24 hours | 7 days |
| High | 48 hours | 14 days |
| Medium | 72 hours | 30 days |
| Low | 1 week | Next release |
