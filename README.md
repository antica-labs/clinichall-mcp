# ClinicHall — Plugin Google Antigravity & MCP

Connectez **ClinicHall** (`https://clinichall.com`), le moteur de recherche scientifique et encyclopédique en biochimie (taxonomie LOINC), physiologie de l'exercice (`VO2max`, `HRV RMSSD`), modèles mathématiques de longévité et vérification cryptographique SHA-256, directement à votre agent IA.

## Installation & Authentification OAuth 2.1

1. **OAuth 2.1 + PKCE (`S256`) + CIMD** : À la première requête, votre client IA ouvre l'écran sécurisé `https://clinichall.com/api/oauth/authorize`.
2. **Clé API MCP** : Authentifiez-vous avec votre compte de recherche ClinicHall ou une clé `ch_live_...`.

## Les 12 Outils MCP (`readOnlyHint: true`)

- `get_longevity_research_overview`, `list_loinc_biomarker_benchmarks`, `list_physiology_telemetry_benchmarks`, `list_longevity_index_formulas`, `list_micronutrition_reference_compounds`, `list_research_cohorts_and_studies`, `list_research_fellows_directory`, `list_scientific_publications`, `search_scientific_literature`, `verify_document_seal`, `search`, `fetch`.
