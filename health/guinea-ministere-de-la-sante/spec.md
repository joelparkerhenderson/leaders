# spec.md — `leaders.yml`

Source unique de vérité pour le registre des parties prenantes du système de santé guinéen. Le YAML doit se conformer à cette spécification.

## 1. Purpose

Registre d'engagement des personnes nommées au sein du Ministère de la Santé et de l'Hygiène Publique de la République de Guinée (Conakry) et corps adjacents.

La Guinée est sous transition militaire depuis le coup d'État du 5 septembre 2021 mené par le Colonel Mamadi Doumbouya (CNRD — Comité National du Rassemblement pour le Développement). Le système de santé public est centré sur l'Hôpital National Donka et l'Hôpital Ignace Deen à Conakry. Pays touché par Ebola (2014-2016) puis par les épidémies récurrentes (Marburg 2021, Lassa).

## 2. Scope

In scope: Président de la Transition; Ministre de la Santé et de l'Hygiène Publique; Secrétaire Général; Directeur ANSS (Agence Nationale de Sécurité Sanitaire); Directeur DNPL (pharmacie); Conseil National de la Transition Commission Santé.

Out of scope: directeurs régionaux; chefs de service.

## 3. Structure

Standard 2/6/10/14 indentation. Top-level key: `Parties prenantes du système de santé guinéen:`. Ordre: Présidence de la Transition → MSHP → ANSS → DNPL → CNT.

## 4. Field definitions

Affiliation: la transition CNRD a suspendu les partis dans l'exécutif, donc affiliation `CNRD/Transition` ou `Indépendant/technocrate`. Titres en français.

## 5. Provenance and dating

Anchor to year, month or date. Le Ministre de la Santé sous la transition est nommé par le Colonel Mamadi Doumbouya; vérifier la titularité contre la Présidence et l'AGP (Agence Guinéenne de Presse).

## 6. Update workflow

Verify against presidence.gov.gn, sante.gov.gn, anss-guinee.org, AGP, Guinéenews, Mediaguinee.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Ignorer le contexte de transition — la Guinée est sous gouvernement de transition militaire CNRD; le calendrier électoral et la légitimité des engagements à long terme dépendent du processus de retour à l'ordre constitutionnel.
- Anchrer aux framings Ebola exclusivement — l'épidémie 2014-2016 est mémoire institutionnelle mais les priorités actuelles sont PHC, paludisme, NCDs et préparation aux urgences (Marburg, Lassa, mpox).

## 9. Acronym glossary

- **AGP** — Agence Guinéenne de Presse.
- **ANSS** — Agence Nationale de Sécurité Sanitaire.
- **CNRD** — Comité National du Rassemblement pour le Développement.
- **CNT** — Conseil National de la Transition.
- **DNPL** — Direction Nationale de la Pharmacie et du Laboratoire.
- **MSHP** — Ministère de la Santé et de l'Hygiène Publique.

## 10. Worked example

```yaml
      - Dr [Nom à vérifier] (CNRD/Transition):
          - Title: Ministre de la Santé et de l'Hygiène Publique (Minister of Health and Public Hygiene)
          - Stakeholder engagement notes:
              - "Ministre de la Santé sous la transition CNRD du Colonel Mamadi Doumbouya; vérifier la titularité contre la Présidence et l'AGP."
              - "Owns la politique et le budget MSHP, l'Hôpital National Donka, l'Hôpital Ignace Deen, les hôpitaux régionaux des huit régions administratives, l'ANSS, la DNPL, et la diplomatie OMS AFRO, CEDEAO (statut Guinée actuel) et UA."
              - "Hook: paludisme, santé maternelle et infantile, NCDs, préparation aux urgences (Marburg, Lassa, mpox), et reconstruction post-Ebola atterrissent; framings de long terme filtrés par le calendrier de transition."
          - Tone advice:
              - "Ouvrir avec paludisme, MCH, NCDs, préparation aux urgences et reconstruction post-Ebola."
              - "Ne pas ignorer le contexte de transition ni s'anchorer exclusivement à Ebola."
```

## 11. Out-of-band notes

Pour les postes vacants ou intérimaires sous la transition.

## 12. Open questions

- Identité du Ministre de la Santé en titre avec titularité vérifiée.
- Directeur ANSS et Directeur DNPL avec titularité vérifiée.
- Président Commission Santé du CNT.
