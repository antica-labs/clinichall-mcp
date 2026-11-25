---
description: Règles de rigueur scientifique et de traçabilité LOINC / SHA-256 lors de l'utilisation du serveur MCP ClinicHall.
---

# Règles d'utilisation du connecteur MCP ClinicHall

1. **Rigueur Taxonomique LOINC** : Lors de toute requête sur un marqueur biochimique via `list_loinc_biomarker_benchmarks`, mentionnez systématiquement son code LOINC officiel, son unité et la distinction entre intervalle standard et cible optimale issue de la littérature sur la longévité.
2. **Modèles Physiologiques & Bibliographie** : Appuyez chaque synthèse de physiologie de l'exercice (`VO2max`, `HRV RMSSD`, sommeil) sur les outils `list_physiology_telemetry_benchmarks`, `list_longevity_index_formulas` et `search_scientific_literature`.
3. **Vérification Cryptographique SHA-256** : Utilisez `verify_document_seal` pour contrôler l'empreinte SHA-256 des monographies et rapports certifiés sur `https://clinichall.com/verifier`.
