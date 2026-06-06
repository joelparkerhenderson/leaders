# spec.md — `leaders.yml`

Source unique de vérité pour le registre des parties prenantes du système de santé tchadien. Le YAML doit se conformer à cette spécification.

## 1. Purpose

Registre d'engagement des personnes nommées au sein du Ministère de la Santé Publique (MSP) de la République du Tchad et corps adjacents.

Le Tchad est sous la présidence de Mahamat Idriss Déby Itno (MPS — Mouvement Patriotique du Salut, élu en mai 2024 après transition militaire 2021-2024 succédant à son père Idriss Déby Itno). Pays sahélien membre de la CEMAC, CEEAC, OCI; touché par les crises soudanaise (afflux massif de réfugiés au Ouaddaï, Sila, Wadi Fira), libyenne et nord-nigériane.

## 2. Scope

In scope: Président; Premier Ministre; Ministre de la Santé Publique; Secrétaire Général; Directeur Général Hôpital Général de Référence Nationale; Assemblée Nationale Commission Santé.

Out of scope: directeurs provinciaux; chefs de service.

## 3. Structure

Standard 2/6/10/14 indentation. Top-level key: `Parties prenantes du système de santé tchadien:`. Ordre: Présidence → Premier Ministre → MSP → HGRN → Assemblée.

## 4. Field definitions

Affiliation partisane: `MPS` (Mouvement Patriotique du Salut, parti dominant), `Les Transformateurs` (opposition principale, Succès Masra), `RNDT-Le Réveil`. Titres en français.

## 5. Provenance and dating

Anchor to year, month or date. Le Ministre de la Santé sous Mahamat Idriss Déby est à vérifier contre la Présidence et l'ATPE (Agence Tchadienne de Presse et d'Édition).

## 6. Update workflow

Verify against presidence.td, sante-tchad.org, ATPE, Tchadinfos, Alwihda Info, Tchad One.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Ignorer la crise des réfugiés soudanais — depuis 2023, plus d'un million de Soudanais ont fui au Tchad oriental; la dimension humanitaire-santé est centrale.
- Anchorer aux framings sahéliens uniformes — le Tchad est sahélien dans le nord et soudanien-équatorial dans le sud, avec une diversité épidémiologique très importante.

## 9. Acronym glossary

- **ATPE** — Agence Tchadienne de Presse et d'Édition.
- **HGRN** — Hôpital Général de Référence Nationale.
- **MPS** — Mouvement Patriotique du Salut.
- **MSP** — Ministère de la Santé Publique.

## 10. Worked example

```yaml
      - Dr [Nom à vérifier] (MPS):
          - Title: Ministre de la Santé Publique (Minister of Public Health)
          - Stakeholder engagement notes:
              - "Ministre du MSP sous Mahamat Idriss Déby Itno; vérifier contre la Présidence et l'ATPE."
              - "Owns la politique et le budget MSP, l'Hôpital Général de Référence Nationale à N'Djamena, l'Hôpital de la Mère et de l'Enfant, les hôpitaux provinciaux des 23 provinces, et la diplomatie CEMAC, CEEAC, CILSS, OCI et UA."
              - "Hook: crise sanitaire soudanaise à l'Est, paludisme, MCH, malnutrition aiguë, choléra, polio, mpox et coopération CEMAC atterrissent."
          - Tone advice:
              - "Ouvrir avec crise soudanaise, paludisme, MCH, malnutrition, choléra et polio."
              - "Ne pas ignorer la crise soudanaise ni assumer une homogénéité épidémiologique nord-sud."
```

## 11. Out-of-band notes

Pour les postes vacants ou intérimaires.

## 12. Open questions

- Identité du Ministre de la Santé Publique en titre avec titularité vérifiée.
- Directeur Général HGRN.
- Président Commission Santé Assemblée Nationale.
