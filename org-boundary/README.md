# AaCT-E Organizational Boundary

AaCT-E/.github is the canonical specification and bootstrap home for the AaCT-E organizational ingress/egress boundary.

## Boundary rule

All cross-organization requests or results are represented as governed InTr envelopes at this boundary. Individual AaCT-E repositories expose endpoint profiles; they do not each redefine organization-level transport, provenance, routing, or crossing receipts.

## Processing path

```
HB or HB-derived carrier
  -> InTr envelope
  -> org ingress validation
  -> destination/profile resolution
  -> internal dispatch
  -> endpoint consumption
  -> result/evidence binding
  -> org egress packaging
  -> InTr envelope
  -> carrier
```

HB and derived carriers provide synchronization/carrier capability only. They do not grant admission, execution, credential, routing, transition, or receiving authority.

## Responsibilities

Ingress:
- validate envelope schema/version;
- preserve packet and carrier references;
- establish origin and provenance references;
- resolve destination service/profile;
- bind transition context without hard-coding authority;
- emit ingress evidence.

Internal dispatch:
- resolve registered AaCT-E services;
- pass only the normalized governed payload and required context;
- distinguish dispatch from consumption;
- preserve request identity across the boundary.

Egress:
- accept endpoint result plus application evidence;
- bind consumption/result evidence to the original request;
- resolve destination organization/endpoint;
- construct a governed response envelope;
- emit egress evidence.

## Runtime independence

This repository defines the boundary contract. GitHub Actions may validate source and evidence artifacts, but GitHub is not runtime authority and workflow success is not runtime execution proof. A resident AaCT-E boundary process may consume these definitions locally without PyPI, CDN, GitHub-runtime, or third-party package authority.

## Current endpoints

See `registry/services.json` and `profiles/`.
