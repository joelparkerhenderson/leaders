# spec.md — `leaders.yml`

Source unique de vérité pour le registre des parties prenantes du système de santé comorien. Le YAML doit se conformer à cette spécification.

## 1. Purpose

Registre d'engagement des personnes nommées au sein du Ministère de la Santé, de la Solidarité, de la Protection sociale et de la Promotion du Genre (MSSPSPG) de l'Union des Comores et corps adjacents.

L'Union des Comores est une fédération de trois îles (Ngazidja-Grande Comore, Ndzuwani-Anjouan, Mwali-Mohéli) avec une présidence tournante. Le système de santé combine un MSSPSPG fédéral, des structures insulaires (Direction de la Santé pour chaque île), et un fort appui des partenaires (OMS, UNICEF, AFD, Banque Mondiale, Gavi).

## 2. Scope

In scope: Président de l'Union; Ministre de la Santé; Secrétaire Général MSSPSPG; Directeurs de la Santé de chaque île; Assemblée de l'Union — Commission Santé.

Out of scope: directeurs hospitaliers; chefs de service.

## 3. Structure

Standard 2/6/10/14 indentation. Top-level key: `Parties prenantes du système de santé comorien:`. Ordre: Présidence → MSSPSPG → Directions insulaires → Assemblée.

## 4. Field definitions

Affiliation partisane: `CRC` (Convention pour le Renouveau des Comores, parti du Président Azali), `Juwa` (parti Juwa), `Orange`, `RDC`. Titres en français.

## 5. Provenance and dating

Anchor to year, month or date. Le portefeuille de la santé a été remanié au sein du gouvernement de l'Union; vérifier la titularité actuelle contre la Présidence de l'Union et l'Agence Comores-Presse.

## 6. Update workflow

Verify against beit-salam.km (Présidence), gouv.km, hayba.fm, Comores Infos, Al-Watwan, Agence Comores Presse.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Traiter les Comores comme une entité unique sans tenir compte des trois îles — chaque île a son gouverneur et sa Direction de la Santé.
- Confondre l'Union des Comores avec Mayotte — Mayotte est un département français, hors souveraineté comorienne dans le statut français mais revendiqué par l'Union.

## 9. Acronym glossary

- **AFD** — Agence Française de Développement.
- **CRC** — Convention pour le Renouveau des Comores.
- **MSSPSPG** — Ministère de la Santé, de la Solidarité, de la Protection sociale et de la Promotion du Genre.

## 10. Worked example

```yaml
      - Dr [Nom à vérifier] (CRC):
          - Title: Ministre de la Santé, de la Solidarité, de la Protection sociale et de la Promotion du Genre (Minister of Health)
          - Stakeholder engagement notes:
              - "Ministre de la Santé du gouvernement de l'Union des Comores sous la présidence d'Azali Assoumani; vérifier la titularité contre la Présidence beit-salam.km."
              - "Owns la politique et le budget santé fédéral, l'Hôpital El-Maarouf à Moroni (référence nationale), les hôpitaux insulaires de Anjouan et Mohéli, la coordination avec les Directions de la Santé des trois îles, l'achat de médicaments, et la diplomatie sanitaire OMS AFRO, UA et Ligue Arabe."
              - "Hook: paludisme (les Comores ont fait des progrès vers l'élimination), santé maternelle et infantile, nutrition, NCDs, coordination inter-îles, et appui des partenaires (Gavi, OMS, AFD, Banque Mondiale) atterrissent."
          - Tone advice:
              - "Ouvrir avec paludisme, santé maternelle et infantile, nutrition, NCDs et coordination inter-îles — priorités durables."
              - "Ne pas négliger la structure à trois îles ni confondre avec Mayotte."
```

## 11. Out-of-band notes

Pour les postes vacants ou intérimaires.

## 12. Open questions

- Identité du Ministre de la Santé en titre avec titularité vérifiée.
- Secrétaire Général MSSPSPG et Directeurs de la Santé insulaires.
- Président Commission Santé Assemblée de l'Union.
