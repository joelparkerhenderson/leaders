# spec.md — `leaders.yml`

Source unique de vérité pour le registre des parties prenantes du système de santé togolais. Le YAML doit se conformer à cette spécification.

## 1. Purpose

Registre d'engagement des personnes nommées au sein du Ministère de la Santé et de l'Hygiène Publique (MSHP) de la République Togolaise et corps adjacents.

Le Togo est sous la présidence de Faure Gnassingbé (UNIR) — depuis 2005 — et a transitionné en 2024-2025 vers un régime parlementaire avec la 5ème République où Gnassingbé est devenu Président du Conseil des Ministres. Membre de la CEDEAO, de l'UEMOA, de la Francophonie.

## 2. Scope

In scope: Président de la République; Président du Conseil des Ministres; Ministre de la Santé et de l'Hygiène Publique; Secrétaire Général; Directeur Général CHU Sylvanus Olympio; Directeur Pharmacie; Assemblée Nationale Commission Santé.

Out of scope: directeurs régionaux; chefs de service.

## 3. Structure

Standard 2/6/10/14 indentation. Top-level key: `Parties prenantes du système de santé togolais:`. Ordre: Présidence → MSHP → CHU → Pharmacie → Assemblée.

## 4. Field definitions

Affiliation partisane: `UNIR` (Union pour la République, au pouvoir Gnassingbé), `ANC` (Alliance Nationale pour le Changement, opposition Fabre), `DMK` (Dynamique pour la Majorité du Peuple). Titres en français.

## 5. Provenance and dating

Anchor to year, month or date. Le Ministre de la Santé sous le gouvernement Gnassingbé/régime parlementaire 5ème République est à vérifier contre la Présidence et l'ATOP (Agence Togolaise de Presse).

## 6. Update workflow

Verify against presidence.gouv.tg, sante.gouv.tg, assemblee-nationale.tg, ATOP, Togo Tribune, Republicoftogo.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Ignorer la transition vers la 5ème République — la nouvelle architecture avec Président du Conseil des Ministres a recomposé les centres de décision; framings basés sur l'ancienne 4ème République seront désalignés.
- Anchrer aux framings ghanéens — le Togo a une identité francophone et institutionnelle distincte du Ghana voisin anglophone.

## 9. Acronym glossary

- **ATOP** — Agence Togolaise de Presse.
- **CHU** — Centre Hospitalier Universitaire.
- **MSHP** — Ministère de la Santé et de l'Hygiène Publique.
- **UNIR** — Union pour la République.

## 10. Worked example

```yaml
      - Dr [Nom à vérifier] (UNIR):
          - Title: Ministre de la Santé et de l'Hygiène Publique (Minister of Health and Public Hygiene)
          - Stakeholder engagement notes:
              - "Ministre de la Santé sous le gouvernement de la 5ème République togolaise dirigé par le Président du Conseil des Ministres Faure Gnassingbé; vérifier contre la Présidence et l'ATOP."
              - "Owns la politique et le budget MSHP, le CHU Sylvanus Olympio à Lomé, le CHU Campus, l'hôpital régional de Kara, les hôpitaux des cinq régions (Maritime, Plateaux, Centrale, Kara, Savanes), la pharmacie centrale, l'INAM (assurance maladie), et la diplomatie OMS AFRO, CEDEAO, UEMOA et Francophonie."
              - "Hook: paludisme, santé maternelle et infantile, NCDs, couverture santé universelle via INAM, et préparation aux urgences atterrissent."
          - Tone advice:
              - "Ouvrir avec paludisme, MCH, NCDs, CUS-INAM et préparation aux urgences."
              - "Ne pas ignorer la 5ème République ni importer des framings ghanéens."
```

## 11. Out-of-band notes

Pour les postes vacants ou intérimaires.

## 12. Open questions

- Identité du Ministre de la Santé en titre avec titularité vérifiée.
- Directeur Général CHU Sylvanus Olympio.
- Président Commission Santé Assemblée Nationale.
