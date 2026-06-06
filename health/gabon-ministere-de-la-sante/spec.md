# spec.md — `leaders.yml`

Source unique de vérité pour le registre des parties prenantes du système de santé gabonais. Le YAML doit se conformer à cette spécification.

## 1. Purpose

Registre d'engagement des personnes nommées au sein du Ministère de la Santé de la République Gabonaise et corps adjacents.

Le Gabon est sous un régime de transition depuis le coup d'État du 30 août 2023 mené par le Général Brice Clotaire Oligui Nguema (CTRI — Comité pour la Transition et la Restauration des Institutions), avec un retour à l'ordre constitutionnel programmé. Le Général Oligui Nguema a remporté l'élection présidentielle d'avril 2025 et est devenu Président élu. Le système est public-dominant; CNAMGS (assurance maladie obligatoire) couvre une large part formelle.

## 2. Scope

In scope: Président; Premier Ministre; Ministre de la Santé; Secrétaire Général; Directeur Général CHUL (CHU de Libreville); Directeur CNAMGS; Assemblée Nationale Commission Santé.

Out of scope: directeurs régionaux; chefs de service.

## 3. Structure

Standard 2/6/10/14 indentation. Top-level key: `Parties prenantes du système de santé gabonais:`. Ordre: Présidence → Premier Ministre → MS → CHUL → CNAMGS → Assemblée.

## 4. Field definitions

Affiliation partisane: `UDB` (Union Démocratique des Bâtisseurs, parti d'Oligui Nguema créé en 2025), `PDG` (Parti Démocratique Gabonais, ancien parti unique sous les Bongo), `RPM`. Titres en français.

## 5. Provenance and dating

Anchor to year, month or date. Le Ministre de la Santé sous le gouvernement Oligui Nguema (post-transition, depuis l'élection d'avril 2025) est à vérifier contre la Présidence et l'AGP (Agence Gabonaise de Presse).

## 6. Update workflow

Verify against presidence.ga, sante.gouv.ga, assemblee-nationale.ga, AGP, Gabonreview, L'Union (quotidien).

## 7. Invariants

Standard.

## 8. Anti-patterns

- Anchorer aux framings Bongo — la transition CTRI a recomposé l'architecture politique; framings basés sur la doctrine PDG des Bongo seront désalignés.
- Ignorer la CNAMGS — la couverture obligatoire est une caractéristique structurelle distinctive du Gabon en Afrique centrale.

## 9. Acronym glossary

- **AGP** — Agence Gabonaise de Presse.
- **CHUL** — Centre Hospitalier Universitaire de Libreville.
- **CNAMGS** — Caisse Nationale d'Assurance Maladie et de Garantie Sociale.
- **CTRI** — Comité pour la Transition et la Restauration des Institutions.
- **MS** — Ministère de la Santé.
- **UDB** — Union Démocratique des Bâtisseurs.

## 10. Worked example

```yaml
      - Dr [Nom à vérifier] (UDB):
          - Title: Ministre de la Santé (Minister of Health)
          - Stakeholder engagement notes:
              - "Ministre de la Santé sous le gouvernement post-transition d'Oligui Nguema; vérifier contre la Présidence et l'AGP."
              - "Owns la politique et le budget MS, le CHU de Libreville, le CHU d'Owendo, l'hôpital régional de Port-Gentil, le réseau provincial des neuf provinces, la CNAMGS, et la diplomatie OMS AFRO, CEMAC, CEEAC et OIF."
              - "Hook: CNAMGS et CUS, paludisme, MCH, NCDs, mpox (le Gabon a connu des flambées), et restructuration post-transition atterrissent."
          - Tone advice:
              - "Ouvrir avec CNAMGS-CUS, paludisme, MCH, NCDs et préparation aux urgences."
              - "Ne pas s'anchorer aux framings PDG-Bongo ni ignorer la CNAMGS."
```

## 11. Out-of-band notes

Pour les postes vacants ou intérimaires.

## 12. Open questions

- Identité du Ministre de la Santé en titre avec titularité vérifiée.
- Directeur Général CHUL et Directeur CNAMGS.
- Président Commission Santé Assemblée Nationale.
