# spec.md — `leaders.yml`

Source unique de vérité pour le registre des parties prenantes du système de santé centrafricain. Le YAML doit se conformer à cette spécification.

## 1. Purpose

Registre d'engagement des personnes nommées au sein du Ministère de la Santé Publique et de la Population (MSPP) de la République Centrafricaine (RCA) et corps adjacents.

La RCA est sous la présidence de Faustin-Archange Touadéra (MCU — Mouvement Cœurs Unis), avec un système de santé fragile, affecté par le conflit, fortement dépendant des partenaires (OMS, UNICEF, MSF, ICRC, Fonds Mondial, Banque Mondiale, UE) et de la présence russe Wagner/Africa Corps. Mpox (clade I et Ib) y est en circulation active.

## 2. Scope

In scope: Président; Premier Ministre; Ministre de la Santé Publique et de la Population; Secrétaire Général; Directeur Hôpital Communautaire de Bangui; Assemblée Nationale Commission Santé.

Out of scope: directeurs préfectoraux; chefs de service.

## 3. Structure

Standard 2/6/10/14 indentation. Top-level key: `Parties prenantes du système de santé centrafricain:`. Ordre: Présidence → Premier Ministre → MSPP → Hôpitaux → Assemblée.

## 4. Field definitions

Affiliation partisane: `MCU` (Mouvement Cœurs Unis, mouvance Touadéra), `KNK` (Kwa Na Kwa, mouvance Bozizé), `URCA`. Titres en français.

## 5. Provenance and dating

Anchor to year, month or date. Le Ministre de la Santé sous Touadéra est à vérifier contre la Présidence et l'ACAP (Agence Centrafricaine de Presse).

## 6. Update workflow

Verify against presidence-rca.cf, sante.gouv.cf, ACAP, Corbeau News Centrafrique, RJDH (Réseau des Journalistes pour les Droits Humains).

## 7. Invariants

Standard.

## 8. Anti-patterns

- Ignorer le contexte sécuritaire — vaste contrôle territorial partagé entre gouvernement, groupes armés et présence russe; framings qui assument l'accès universel sont inexacts.
- Anchorer aux framings RDC — la RCA est un État souverain distinct avec son propre MSPP malgré la frontière partagée.

## 9. Acronym glossary

- **ACAP** — Agence Centrafricaine de Presse.
- **MCU** — Mouvement Cœurs Unis.
- **MSPP** — Ministère de la Santé Publique et de la Population.
- **RCA** — République Centrafricaine.

## 10. Worked example

```yaml
      - Dr [Nom à vérifier] (MCU):
          - Title: Ministre de la Santé Publique et de la Population (Minister of Public Health and Population)
          - Stakeholder engagement notes:
              - "Ministre du MSPP sous Touadéra; vérifier contre la Présidence et l'ACAP."
              - "Owns la politique et le budget MSPP, l'Hôpital Communautaire de Bangui, l'Hôpital de l'Amitié, le Complexe Pédiatrique, les hôpitaux préfectoraux, et la diplomatie OMS AFRO, CEEAC, CEMAC et CIRGL."
              - "Hook: mpox (clade I/Ib en circulation), conflit-blessures, malnutrition aiguë, MCH, paludisme et coordination humanitaire (OMS, MSF, UNICEF, ICRC) atterrissent."
          - Tone advice:
              - "Ouvrir avec mpox, conflit-blessures, MCH, malnutrition, paludisme et coordination humanitaire."
              - "Ne pas ignorer le contexte sécuritaire ni anchorer aux framings RDC."
```

## 11. Out-of-band notes

Pour les postes vacants ou intérimaires.

## 12. Open questions

- Identité du Ministre de la Santé en titre avec titularité vérifiée.
- Directeur Hôpital Communautaire de Bangui.
- Président Commission Santé Assemblée Nationale.
