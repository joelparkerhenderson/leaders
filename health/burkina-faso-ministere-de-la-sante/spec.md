# spec.md — `leaders.yml`

Single source of truth for the Burkinabè health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Burkina Faso Ministère de la Santé et de l'Hygiène Publique, Caisse Nationale d'Assurance Maladie Universelle (CNAMU), Agence Nationale de Régulation Pharmaceutique (ANRP), CHU Yalgado Ouédraogo, and adjacent bodies.

The Burkinabè system has Gratuité des soins for under-5s and pregnant women, and Couverture Maladie Universelle implementation; donor-coordinated with significant insecurity-related health-service disruption in northern and eastern regions. The Traoré transition government emphasises souveraineté sanitaire.

## 2. Scope

In scope: Président Capitaine Ibrahim Traoré; Premier Ministre; Ministre de la Santé et de l'Hygiène Publique; Secrétaire Général; Directeurs Centraux; DG CNAMU; DG ANRP; DG Centre Hospitalier Universitaire Yalgado Ouédraogo; Directeurs Régionaux Santé (13 régions); Assemblée Législative de Transition Commission Santé; Ordre des Médecins du Burkina Faso.

## 3. Structure

Standard. Ordering: Présidence → Premier Ministre → MSHP → CNAMU → ANRP → CHU YO → 13 DRS → ALT → Ordre.

## 4. Field definitions

Transition government — no formal party affiliations; military and technocratic appointments. Titles in French / English.

## 5. Provenance and dating

Dr. Robert Lucien Jean-Claude Kargougou serves as Ministre de la Santé et de l'Hygiène Publique in the transition government under Capitaine Ibrahim Traoré; active 2026 on consolidation of 2025 gains, FONAFIS (Forum National sur le Financement de la Santé) March 2026, priorities 2026-2030 strategy.

## 6. Update workflow

Verify against sante.gov.bf, presidencefaso.bf, primature.gov.bf, leFaso.net, Sidwaya, Burkina24, Faso7, Agence d'Information du Burkina, BurkinaInfo.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Importing Western framings — Traoré transition has emphasised souveraineté and Sahel alliance over Western partnerships.
- Ignoring insurgency context — north and east regions face JNIM and ISGS attacks affecting health services.

## 9. Acronym glossary

- **ALT** — Assemblée Législative de Transition.
- **ANRP** — Agence Nationale de Régulation Pharmaceutique.
- **CNAMU** — Caisse Nationale d'Assurance Maladie Universelle.
- **DRS** — Direction Régionale de la Santé.
- **MSHP** — Ministère de la Santé et de l'Hygiène Publique.

## 10. Worked example

```yaml
      - Dr. Robert Lucien Jean-Claude Kargougou:
          - Title: Ministre de la Santé et de l'Hygiène Publique (in the Traoré transition government)
          - Stakeholder engagement notes:
              - "Ministre de la Santé et de l'Hygiène Publique dans le gouvernement de transition sous le Capitaine Ibrahim Traoré; biographie sur sante.gov.bf; médecin de profession; cérémonie d'installation médiatisée."
              - "Active 2026: évaluation des performances 2025 et tracé des priorités 2026-2030 (leFaso.net, Pravda BF mars 2026); a déclaré 2026 comme l'année de consolidation des acquis 2025; FONAFIS (Forum National sur le Financement de la Santé) à Ouagadougou 18 mars 2026 — première édition; accueil du premier bébé de 2026 au CHU de Bogodogo (1er janvier 2026, Faso7, Pravda BF)."
              - "Owns MSHP policy, CNAMU CMU rollout, ANRP pharmaceutical regulation, Gratuité des soins pour les enfants de moins de 5 ans et les femmes enceintes, CHU Yalgado Ouédraogo et CHU Bogodogo, 13 Directions Régionales Santé, insurgency-affected northern and eastern regions health response, et la diplomatie sanitaire AES (Alliance des États du Sahel — Burkina Faso, Mali, Niger) et CEDEAO-retirée."
              - "Hook: Gratuité, CMU rollout, FONAFIS financing, AES sanitaire cooperation, north/east regions insurgency-affected health response."
          - Tone advice:
              - "Ouvrir avec souveraineté sanitaire, FONAFIS, CMU et AES — sont les lignes autoréais du gouvernement de transition."
              - "Ne pas pitcher en framings français / CEDEAO — le Burkina s'est retiré de la CEDEAO et reformulé autour de l'AES; les framings ouest-africains traditionnels ne reflèteront pas la nouvelle diplomatie."
```

## 11. Out-of-band notes

For roles unfilled or in transition.

## 12. Open questions

- Named Secrétaire Général et Directeurs Centraux du MSHP.
- DG CNAMU, DG ANRP, DG CHU YO, DG CHU Bogodogo.
- Directeurs Régionaux Santé des 13 régions — priorité Sahel, Est, Centre-Nord, Boucle du Mouhoun (insurgency-affected).
- ALT Commission Santé Chair.
- Président Ordre des Médecins du Burkina Faso with currency verified.
