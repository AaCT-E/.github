# AACT_E_ORG_BOUNDARY_MIRROR_HANDOFF.md

Status: ACTIVE
Updated: 2026-08-31

## Purpose
This repository is the canonical organizational ingress/egress definition for AaCT-E.

## Current task authority
1. Establish AaCT-E/.github as the organization-level Interlock/InTr boundary definition.
2. Consolidate reusable ingress, normalization, routing, registry, evidence, and egress contracts here rather than rebuilding them per repository.
3. Keep GitHub Actions as validation/evidence transport only; the resident boundary implementation must not depend on GitHub runtime authority.
4. Preserve AaCT-E/demo as an application endpoint with a profile, not a second organization boundary.
5. Require deterministic ingress, dispatch, consumption, egress, and reconstruction evidence for cross-organization work.

## Canonical layering
HB or HB-derived carrier -> InTr organizational boundary -> ingestion -> core-lite routing/registry -> repository/runtime profile.
Return path reverses through core-lite/evidence -> organization egress -> InTr -> carrier.

## Immediate implementation
- org-boundary/README.md
- org-boundary/schemas/intr-envelope.schema.json
- org-boundary/registry/services.json
- org-boundary/profiles/demo.json
- org-boundary/evidence/receipt-chain.schema.json

## Non-claims
Source presence, CI success, merge, or deployment do not establish runtime activation, request consumption, observation, or reconstruction.

## Next
After AaCT-E boundary skeleton is established, continue smallest organizations first. Triad-Test currently lacks an organization .github repository and needs that repository created before its canonical boundary can be installed.


## Canonical resident-runtime activation rule — 2026-08-31
- Every AaCT-E resident runtime activation surface MUST be kept in `AaCT-E/.github`.
- No application repository is the organization resident-runtime activation authority.
- Application repositories expose capabilities/endpoints to the organizational boundary; the organization `.github` owns activation, ingress, egress, and organization-crossing transport behavior.
- All communication crossing the AaCT-E organizational boundary MUST be generated through this `.github` boundary using Interlock/InTr semantics.
- Ingress responsibilities: carrier observation, InTr envelope validation, provenance binding, transition-context binding, destination/profile resolution, dispatch evidence.
- Egress responsibilities: result/evidence validation, destination-org resolution, InTr envelope generation, egress evidence, reconstruction linkage.
- HB/HB-derived carrier presence remains non-authorizing. Authority is determined by applicable transition elements.
- GitHub Actions may validate or transport evidence, but GitHub-hosted workflow execution is not required as sovereign runtime authority.
- Canonical implementation paths: `org-boundary/runtime/`, `org-boundary/registry/`, `org-boundary/schemas/`, `org-boundary/evidence/`, `resident-runtime/`.
- Any legacy resident activation implementation outside `AaCT-E/.github` becomes an endpoint/provider to this boundary or must be migrated here; it must not remain a competing organizational activation point.
