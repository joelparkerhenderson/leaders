# spec.md — `leaders.yml`

Source unique de vérité pour le registre des parties prenantes du système de santé de la République du Congo (Brazzaville). Le YAML doit se conformer à cette spécification.

## 1. Purpose

Registre d'engagement des personnes nommées au sein du Ministère de la Santé et de la Population (MSP) de la République du Congo et corps adjacents.

À ne pas confondre avec la République Démocratique du Congo (Kinshasa). La République du Congo est sous la présidence de Denis Sassou-Nguesso (PCT — Parti Congolais du Travail, au pouvoir 1979-1992 puis depuis 1997).

## 2. Scope

In scope: Président; Premier Ministre; Ministre de la Santé et de la Population; Directeur Général CHU de Brazzaville; Directeur Général CHU de Pointe-Noire; Assemblée Nationale Commission Santé.

Out of scope: directeurs départementaux; chefs de service.

## 3. Structure

Standard 2/6/10/14 indentation. Top-level key: `Parties prenantes du système de santé congolais (Brazzaville):`. Ordre: Présidence → Premier Ministre → MSP → CHU → Assemblée.

## 4. Field definitions

Affiliation partisane: `PCT` (Parti Congolais du Travail, parti dominant), `UPADS` (Union Panafricaine pour la Démocratie Sociale), `MCDDI`. Titres en français.

## 5. Provenance and dating

Anchor to year, month or date. Le Ministre de la Santé et de la Population sous Sassou-Nguesso est à vérifier contre la Présidence et l'ACI (Agence Congolaise d'Information).

## 6. Update workflow

Verify against presidence.cg, sante.gouv.cg, ACI, Les Dépêches de Brazzaville, Vox Congo.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Confondre Congo-Brazzaville (République du Congo) et Congo-Kinshasa (RDC) — deux États souverains distincts; la confusion est très fréquente et embarrassante.
- Ignorer le bassin du Congo et One Health — Congo-Brazzaville est un acteur clé pour la surveillance forestière, Ebola, Marburg, mpox.

## 9. Acronym glossary

- **ACI** — Agence Congolaise d'Information.
- **CHU** — Centre Hospitalier Universitaire.
- **MSP** — Ministère de la Santé et de la Population.
- **PCT** — Parti Congolais du Travail.

## 10. Worked example

```yaml
      - Dr [Nom à vérifier] (PCT):
          - Title: Ministre de la Santé et de la Population (Minister of Health and Population)
          - Stakeholder engagement notes:
              - "Ministre du MSP sous Sassou-Nguesso; vérifier contre la Présidence et l'ACI."
              - "Owns la politique et le budget MSP, le CHU de Brazzaville, le CHU de Pointe-Noire, les hôpitaux des douze départements, et la diplomatie OMS AFRO, CEMAC, CEEAC et OIF."
              - "Hook: paludisme, mpox (le Congo est dans la zone de transmission active), Ebola et Marburg en surveillance one-health, MCH, NCDs et VIH atterrissent."
          - Tone advice:
              - "Ouvrir avec paludisme, mpox, Ebola/Marburg, MCH et One Health."
              - "Ne jamais confondre avec la RDC; reconnaître le rôle one-health du bassin du Congo."
```

## 11. Out-of-band notes

Pour les postes vacants ou intérimaires.

## 12. Open questions

- Identité du Ministre de la Santé et de la Population en titre avec titularité vérifiée.
- Directeur Général CHU de Brazzaville.
- Président Commission Santé Assemblée Nationale.
