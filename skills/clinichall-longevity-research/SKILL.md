---
name: clinichall-longevity-research
description: Moteur de recherche scientifique et encyclopédique en biochimie (taxonomie LOINC), physiologie de l'exercice (VO2max, HRV), modèles mathématiques de longévité et vérification cryptographique SHA-256 via le serveur MCP de ClinicHall (clinichall.com).
---

# ClinicHall — Recherche Scientifique en Biochimie, Physiologie & Longévité (MCP)

Utilisez cette compétence académique et éducative pour interroger les référentiels scientifiques de biochimie (nomenclature LOINC), les jeux de données de référence en physiologie de l'exercice (VO2max, variabilité RMSSD, cycles de sommeil), les modèles mathématiques de longévité publiés dans la littérature scientifique et la vérification cryptographique SHA-256 des monographies sur **ClinicHall** (`https://clinichall.com`).

## Authentification & Lecture Seule

Le serveur MCP ClinicHall (`https://clinichall.com/api/mcp`) supporte :
1. **OAuth 2.1 + PKCE (`S256`) + CIMD** via `https://clinichall.com/.well-known/oauth-authorization-server`.
2. **Bearer Token (`ch_live_...`)** généré depuis l'espace de recherche ClinicHall.
L'ensemble des 12 outils sont en **lecture seule stricte** (`readOnlyHint: true`, `destructiveHint: false`, `openWorldHint: false`) et portent exclusivement sur des référentiels scientifiques et éducatifs.

## Les 12 Outils MCP ClinicHall (`readOnlyHint: true`)

- `get_longevity_research_overview` : Synthèse des référentiels scientifiques de longévité, biochimie LOINC et physiologie de l'exercice indexés dans ClinicHall.
- `list_loinc_biomarker_benchmarks` : Référentiel taxonomique LOINC des marqueurs biochimiques avec unités et valeurs de référence issues de la littérature scientifique (ApoB, Lp(a), HbA1c, hs-CRP, HOMA-IR, Vitamine D3, DFG, Oméga-3).
- `list_physiology_telemetry_benchmarks` : Séries de référence en physiologie de l'exercice (variabilité RMSSD, architecture des cycles de sommeil, capacité aérobie VO2max).
- `list_longevity_index_formulas` : Modèles mathématiques et équations de référence publiés sur la longévité et la physiologie (modèle Levine PhenoAge, quartiles de VO2max, indices métaboliques).
- `list_micronutrition_reference_compounds` : Base documentaire des micronutriments, acides gras essentiels et cofacteurs biochimiques étudiés en recherche sur la longévité.
- `list_research_cohorts_and_studies` : Répertoire des études longitudinales, cohortes académiques et séminaires de recherche en physiologie.
- `list_research_fellows_directory` : Annuaire académique des chercheurs, physiologistes et auteurs scientifiques référencés.
- `list_scientific_publications` : Métadonnées des monographies techniques et rapports scientifiques scellés SHA-256.
- `search_scientific_literature` : Recherche par mots-clés dans le corpus bibliographique interne de ClinicHall sur la biochimie et la physiologie.
- `verify_document_seal` : Vérification cryptographique SHA-256 d'un rapport ou document certifié (`clinichall.com/verifier`).
- `search` : Recherche documentaire unifiée par mots-clés dans les référentiels LOINC, modèles physiologiques, chercheurs et publications.
- `fetch` : Détail structuré d'une référence scientifique ClinicHall par identifiant (`biomarker:<id>`, `score:<id>`, `practitioner:<id>`, `evidence:<id>`).
