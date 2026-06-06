# spec.md — `leaders.yml`

Source unique de vérité pour le registre du système de santé monégasque. Le YAML doit se conformer à cette spécification.

## 1. Purpose

Registre d'engagement des personnes nommées au sein du Département des Affaires Sociales et de la Santé (DASS) de la Principauté de Monaco, et corps adjacents.

Monaco est une monarchie constitutionnelle sous le Prince Albert II avec un système de santé public-dominant centré sur le Centre Hospitalier Princesse Grace (CHPG) à Monaco-Ville. Membre de l'OMS, du Conseil de l'Europe et de l'ONU; relations privilégiées avec la France (convention sanitaire).

## 2. Scope

In scope: Prince; Ministre d'État; Conseiller-Ministre de l'Intérieur et des Affaires Sociales et de la Santé (selon découpage); Directeur DASS; Directeur CHPG; Conseil National (Parlement) Commission Affaires Sociales et Diverses.

Out of scope: chefs de service hospitaliers.

## 3. Structure

Standard 2/6/10/14 indentation. Top-level key: `Parties prenantes du système de santé monégasque:`. Ordre: Prince → Ministre d'État → Conseiller-Ministre → DASS → CHPG → Conseil National.

## 4. Field definitions

Monaco utilise un système de listes électorales (Primo!, Union Monégasque, HMC). Titres en français.

## 5. Provenance and dating

Anchor to year, month or date. Christophe Robino a été Conseiller de Gouvernement-Ministre des Affaires Sociales et de la Santé sous le Ministre d'État Pierre Dartout; verifier la titularité contre le Gouvernement Princier.

## 6. Update workflow

Verify against gouv.mc, palais.mc, conseilnational.mc, Monaco-Matin, Monaco Info.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Confondre Monaco et France — Monaco est un État souverain bien que la convention sanitaire et l'usage du CHU Pasteur de Nice pour services hautement spécialisés créent une interdépendance.
- Ignorer la dimension assurance-maladie — la Caisse de Compensation des Services Sociaux gère la couverture; framings NHS-pur seront corrigés.

## 9. Acronym glossary

- **CCSS** — Caisse de Compensation des Services Sociaux.
- **CHPG** — Centre Hospitalier Princesse Grace.
- **DASS** — Direction de l'Action Sanitaire.

## 10. Worked example

```yaml
      - Christophe Robino:
          - Title: Conseiller de Gouvernement-Ministre des Affaires Sociales et de la Santé (Government Councillor-Minister of Social Affairs and Health)
          - Stakeholder engagement notes:
              - "Conseiller-Ministre des Affaires Sociales et de la Santé sous le Ministre d'État; vérifier titularité contre gouv.mc."
              - "Owns la politique sanitaire monégasque, le CHPG, la Direction de l'Action Sanitaire (DASS), la CCSS, la convention sanitaire avec la France, et la diplomatie OMS Europe et Conseil de l'Europe."
              - "Hook: NCDs, oncologie (le CHPG a une réputation oncologique), longévité, salut mentale, recherche et CHPG-IMR, et coopération franco-monégasque atterrissent."
          - Tone advice:
              - "Ouvrir avec NCDs, oncologie CHPG, recherche, et coopération avec la France."
              - "Ne pas confondre avec la France ni ignorer la CCSS."
```

## 11. Out-of-band notes

Pour les postes vacants ou intérimaires.

## 12. Open questions

- Directeur DASS et Directeur CHPG avec titularité vérifiée.
- Président Commission Affaires Sociales du Conseil National.
