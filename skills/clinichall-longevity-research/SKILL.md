---
name: clinichall-longevity-research
description: Scientific longevity and exercise physiology evidence connector for ClinicHall (clinichall.com): LOINC biomarker benchmarks, validated risk scores, cohort evidence, cryptographic document verification, and medical coordination.
---

# ClinicHall — Official B2A MCP Connector (`v1.2.0`)

Use this skill whenever the task requires deterministic, cryptographically sealed (`SHA-256` + dual `RFC 3161`) outputs from **ClinicHall** (`https://clinichall.com/api/mcp`).

## Discovery & Protocol Support
- **Streamable HTTP Endpoint**: `https://clinichall.com/api/mcp` (MCP `2024-11-05`, `2025-03-26`, `2025-06-18`, `2026-07-28`)
- **B2A Manifest & Live SLA Beacon**: `https://clinichall.com/.well-known/mcp.json`
- **Perplexity Connector Manifest**: `https://clinichall.com/.well-known/mcp-connector.json`
- **A2A Agent Card**: `https://clinichall.com/.well-known/agent-card.json`
- **OpenAPI 3.1.0 Specification**: `https://clinichall.com/openapi.json`
- **Probatory Proof Verifier (`0,00 EUR`)**: `https://clinichall.com/verify/<proof_id>`

## Primary `Output-First` Tools
- `benchmark_loinc_longevity_biomarkers`: Benchmarks LOINC-coded biomarkers against clinical reference intervals and optimal longevity percentiles.
- `compute_validated_longevity_risk_score`: Computes peer-reviewed mathematical indices (Levine PhenoAge, ESC SCORE2, FIB-4, VO2max percentiles).
- `verify_clinical_evidence_and_cohorts`: Verifies peer-reviewed cohort evidence, sample sizes, and grade-of-evidence levels.
- `verify_medical_document_cryptographic_seal`: Verifies SHA-256 and RFC 3161 integrity seals on scientific and preventive reports.
- `audit_patient_preventive_dossier_rls`: Audits authenticated preventive follow-up milestones under strict OAuth 2.1 patient/clinician RLS.
- `stage_physician_coordination_escalation`: Zero-cost (0 EUR) B2A2H escalation to ClinicHall Medical Coordination for licensed physician review.
- `search`: Canonical search across LOINC benchmarks, physiological telemetry references, and cohorts.
- `fetch`: Canonical deterministic retrieval of a LOINC marker, formula specification, or cohort card.

*(Legacy v1 tool names remain 100% supported on `tools/call` via transparent alias resolution.)*

## Authentication & Settlement Rails
1. **OAuth 2.1 + PKCE (`S256`) + DCR (RFC 7591 / RFC 9728 / RFC 8414)**: Mandatory for tenant-isolated RLS data.
2. **Public Catalogs & Stateless Simulators**: Support `HTTP 402` (`x402` EURC/USDC, Stripe MPP, and `AP2` JWS mandates) with `0,00 EUR` dry-run preflight where applicable.
