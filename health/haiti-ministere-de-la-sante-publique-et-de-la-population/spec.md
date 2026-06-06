# spec.md — `leaders.yml`

Source unique de vérité pour le registre du système de santé haïtien. Le YAML doit se conformer à cette spécification.

## 1. Purpose

Registre d'engagement des personnes nommées au sein du Ministère de la Santé Publique et de la Population (MSPP) de la République d'Haïti et corps adjacents.

Haïti opère un système de santé fragile, fortement dépendant des partenaires internationaux et des ONG (PAHO, USAID, MSF, ICRC, World Bank, EU, Canadian bilateral). Crise politique, sécuritaire et humanitaire majeure depuis l'assassinat du Président Jovenel Moïse (juillet 2021) et l'effondrement sécuritaire à Port-au-Prince avec contrôle de gangs (Viv Ansanm). Un Conseil Présidentiel de Transition (CPT) gouverne depuis avril 2024 avec Premier Ministre Alix Didier Fils-Aimé (depuis novembre 2024).

## 2. Scope

In scope: Conseil Présidentiel de Transition; Premier Ministre; Ministre de la Santé Publique et de la Population; Directeur Général MSPP; Directeur Hôpital Universitaire de l'État d'Haïti (HUEH); Coordination humanitaire.

Out of scope: directeurs départementaux; directeurs hospitaliers régionaux.

## 3. Structure

Standard 2/6/10/14 indentation. Top-level key: `Parties prenantes du système de santé haïtien:`. Ordre: CPT → Premier Ministre → MSPP → HUEH → Coordination humanitaire.

## 4. Field definitions

Affiliation partisane: dans le contexte CPT, les conseillers représentent plusieurs forces (Pitit Desalin, Fanmi Lavalas, EDE/RED, Collectif du 30 janvier, Accord du 21 décembre); le gouvernement Fils-Aimé est de type technocratique. Titres en français.

## 5. Provenance and dating

Anchor to year, month or date. Le Ministre de la Santé Publique sous le gouvernement Fils-Aimé (depuis novembre 2024) est à vérifier contre la Primature et l'Agence Haïtienne de Presse (AHP).

## 6. Update workflow

Verify against primature.gouv.ht, mspp.gouv.ht, AHP, Le Nouvelliste, Haiti Libre, Alterpresse, Le National.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Ignorer le contexte sécuritaire — Port-au-Prince est largement sous contrôle de gangs Viv Ansanm avec destruction de l'HUEH et de nombreux hôpitaux; framings qui supposent un accès stable sont inexacts.
- Importer des framings République Dominicaine — Haïti est un État souverain distinct avec sa propre architecture francophone-créolophone.
- Sous-estimer la dimension humanitaire — Haïti est en crise humanitaire aiguë avec famine, choléra, mpox.

## 9. Acronym glossary

- **AHP** — Agence Haïtienne de Presse.
- **CPT** — Conseil Présidentiel de Transition.
- **HUEH** — Hôpital Universitaire de l'État d'Haïti.
- **MSPP** — Ministère de la Santé Publique et de la Population.

## 10. Worked example

```yaml
      - Dr [Nom à vérifier]:
          - Title: Ministre de la Santé Publique et de la Population (Minister of Public Health and Population)
          - Stakeholder engagement notes:
              - "Ministre du MSPP sous le gouvernement de transition d'Alix Didier Fils-Aimé (depuis novembre 2024); vérifier contre la Primature et l'AHP."
              - "Owns la politique et le budget MSPP, l'HUEH (en partie détruit), le réseau des hôpitaux départementaux (Cap-Haïtien, Les Cayes, Jérémie), la coordination avec les partenaires (PAHO, OMS, UNICEF, MSF, ICRC, USAID), et la diplomatie CARICOM, OEA et Francophonie."
              - "Hook: choléra (réémergence), mpox, malnutrition aiguë sévère, blessures par armes à feu et chirurgie d'urgence, et reconstruction de l'HUEH atterrissent."
          - Tone advice:
              - "Ouvrir avec choléra, mpox, malnutrition, blessures et reconstruction."
              - "Ne pas ignorer le contexte sécuritaire ni importer des framings RD."
```

## 11. Out-of-band notes

Pour les postes vacants ou intérimaires.

## 12. Open questions

- Identité du Ministre de la Santé Publique en titre avec titularité vérifiée.
- Directeur Général MSPP.
- Directeur HUEH (en reconstruction).
