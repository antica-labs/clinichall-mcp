# ClinicHall — Official B2A & Enterprise MCP Connector (`v1.2.0`)

Scientific longevity and exercise physiology evidence connector for ClinicHall (clinichall.com): LOINC biomarker benchmarks, validated risk scores, cohort evidence, cryptographic document verification, and medical coordination.

## Sovereign Endpoints & Discovery
| Surface | URL |
| :--- | :--- |
| **MCP Streamable HTTP** | `https://clinichall.com/api/mcp` |
| **MCP Discovery & SLA Beacon** | `https://clinichall.com/.well-known/mcp.json` |
| **Perplexity Connector Manifest** | `https://clinichall.com/.well-known/mcp-connector.json` |
| **A2A Agent Card** | `https://clinichall.com/.well-known/agent-card.json` |
| **OAuth 2.1 Protected Resource (RFC 9728)** | `https://clinichall.com/.well-known/oauth-protected-resource` |
| **OAuth 2.1 Authorization Server (RFC 8414)** | `https://clinichall.com/.well-known/oauth-authorization-server` |
| **OpenAPI 3.1.0 Spec** | `https://clinichall.com/openapi.json` |
| **Agent Index (`llms.txt`)** | `https://clinichall.com/llms.txt` |

## Primary `Output-First` Tools
- `benchmark_loinc_longevity_biomarkers`: Benchmarks LOINC-coded biomarkers against clinical reference intervals and optimal longevity percentiles.
- `compute_validated_longevity_risk_score`: Computes peer-reviewed mathematical indices (Levine PhenoAge, ESC SCORE2, FIB-4, VO2max percentiles).
- `verify_clinical_evidence_and_cohorts`: Verifies peer-reviewed cohort evidence, sample sizes, and grade-of-evidence levels.
- `verify_medical_document_cryptographic_seal`: Verifies SHA-256 and RFC 3161 integrity seals on scientific and preventive reports.
- `audit_patient_preventive_dossier_rls`: Audits authenticated preventive follow-up milestones under strict OAuth 2.1 patient/clinician RLS.
- `stage_physician_coordination_escalation`: Zero-cost (0 EUR) B2A2H escalation to ClinicHall Medical Coordination for licensed physician review.
- `search`: Canonical search across LOINC benchmarks, physiological telemetry references, and cohorts.
- `fetch`: Canonical deterministic retrieval of a LOINC marker, formula specification, or cohort card.

## Guarantees
- **Zero Data Retention (`ZDR`)**: `X-Data-Retention: zero`, `X-Training-On-Payloads: false`, EU sovereign processing (`EU-FR-LU`).
- **AST Prompt-Injection Defense**: 6-layer deterministic sanitizer (`X-Prompt-Injection-Sanitized: ast-v2`).
- **Cryptographic Opposability**: `SHA-256` payload digest + dual qualified `RFC 3161` timestamps + `0,00 EUR` counterparty verification at `https://clinichall.com/verify/<proof_id>`.
