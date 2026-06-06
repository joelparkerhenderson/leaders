# spec.md — `leaders.yml`

Source unique de vérité pour le registre des parties prenantes du système de santé djiboutien. Le YAML doit se conformer à cette spécification.

## 1. Purpose

Registre d'engagement des personnes nommées au sein du Ministère de la Santé (MSP) de Djibouti, de la Centrale d'Achat des Médicaments et Matériels Essentiels (CAMME), et corps adjacents.

Djibouti est un petit État stratégique de la Corne de l'Afrique avec accueil de bases militaires multinationales (US Camp Lemonnier, France, Chine, Japon, Italie). Le système de santé public est centré sur l'Hôpital Général Peltier et complété par l'Hôpital Bouffard (français). Le Ministre est nommé par le Président Ismaïl Omar Guelleh (RPP, au pouvoir depuis 1999).

## 2. Scope

In scope: Président; Ministre de la Santé; Secrétaire Général MSP; Directeur de la CAMME; Directeur INSPD (Institut National de Santé Publique de Djibouti); Commission Santé de l'Assemblée Nationale.

Out of scope: directeurs régionaux; chefs de service hospitaliers.

## 3. Structure

Standard 2/6/10/14 indentation. Top-level key: `Parties prenantes du système de santé djiboutien:`. Ordre: Présidence → MSP → CAMME → INSPD → Assemblée → associations professionnelles.

## 4. Field definitions

Affiliation partisane: `RPP` (Rassemblement Populaire pour le Progrès, parti au pouvoir au sein de l'UMP — Union pour la Majorité Présidentielle), `UDJ` (Union pour la Démocratie et la Justice, opposition). Titres en français avec gloses anglaises.

## 5. Provenance and dating

Anchor to year, month or date. Dr Ahmed Robleh Abdilleh occupe le poste de Ministre de la Santé du gouvernement de Djibouti; vérifier la titularité actuelle contre le Secrétariat Général du Gouvernement.

## 6. Update workflow

Verify against presidence.dj, sante.gouv.dj, assemblee.dj, La Nation (quotidien), ADI (Agence Djiboutienne d'Information).

## 7. Invariants

Standard.

## 8. Anti-patterns

- Ignorer la géopolitique des bases militaires — Djibouti accueille des bases multinationales et la santé doit être lue dans ce contexte stratégique.
- Importer des framings Éthiopie ou Somalie — Djibouti est sovereignement distinct et sa politique sanitaire suit une trajectoire propre.

## 9. Acronym glossary

- **CAMME** — Centrale d'Achat des Médicaments et Matériels Essentiels.
- **IGAD** — Intergovernmental Authority on Development.
- **INSPD** — Institut National de Santé Publique de Djibouti.
- **MSP** — Ministère de la Santé.
- **RPP** — Rassemblement Populaire pour le Progrès.
- **UMP** — Union pour la Majorité Présidentielle.

## 10. Worked example

```yaml
      - Dr Ahmed Robleh Abdilleh (RPP-UMP):
          - Title: Ministre de la Santé (Minister of Health)
          - Stakeholder engagement notes:
              - "Ministre de la Santé du gouvernement de Djibouti sous la présidence d'Ismaïl Omar Guelleh; médecin; vérifier la titularité contre le Secrétariat Général du Gouvernement et le journal La Nation."
              - "Owns la politique et le budget du MSP, l'Hôpital Général Peltier, l'Hôpital Cheiko, les centres de santé communautaires des cinq régions (Ali Sabieh, Arta, Dikhil, Obock, Tadjourah) plus Djibouti-Ville, la CAMME, l'INSPD, et la diplomatie sanitaire IGAD, UA et Ligue Arabe."
              - "Hook: paludisme, tuberculose, VIH, santé maternelle et infantile, urgences sanitaires de la Corne de l'Afrique, et coopération avec les bases militaires alliées sur la sécurité sanitaire atterrissent."
          - Tone advice:
              - "Ouvrir avec paludisme, TB, VIH, santé maternelle et infantile, et urgences régionales — priorités durables du MSP."
              - "Ne pas importer des framings éthiopiens ou somaliens — Djibouti est sovereignement distinct avec sa propre trajectoire."
```

## 11. Out-of-band notes

Pour les postes vacants ou intérimaires.

## 12. Open questions

- Secrétaire Général MSP, Directeur CAMME et Directeur INSPD avec titularité vérifiée.
- Président de la Commission Santé de l'Assemblée Nationale avec titularité vérifiée.
