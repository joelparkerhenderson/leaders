# spec.md — `leaders.yml`

Single source of truth for the Malagasy health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Madagascar Ministère de la Santé Publique (MINSANP), Agence du Médicament de Madagascar, Institut Pasteur de Madagascar, Centres Hospitaliers Universitaires, and adjacent bodies.

The Malagasy system is donor-coordinated with low public health spending; MINSANP runs the public network through 22 Directions Régionales de la Santé Publique; the Institut Pasteur de Madagascar is a regional reference; UMC (Universal Medical Coverage) implementation underway.

## 2. Scope

In scope: Président; Premier Ministre; Ministre de la Santé Publique; Secrétaire Général; Directeur Général Santé; DG Agence du Médicament de Madagascar; Directeur Institut Pasteur de Madagascar; Directeurs CHU (HJRA Antananarivo, JRB Befelatanana, Soavinandriana, Joseph Ravoahangy Andrianavalona, etc.); Directeurs Régionaux 22 régions; Assemblée Nationale Commission Santé; Ordre des Médecins.

## 3. Structure

Standard. Ordering: Présidence → Primature → MINSANP → AMM → IPM → CHU → 22 DRSP → Assemblée → Ordre.

## 4. Field definitions

Party affiliation: `IRD` (Isika Rehetra miaraka amin'i Andry Rajoelina), `TIM` (Tiako i Madagasikara — Ravalomanana). Titles in Malagasy / French / English.

## 5. Provenance and dating

Prof. Zely Arivelo Randriamanantany serves as Ministre de la Santé Publique (per msanp.gov.mg) in the Rajoelina / Rajaonarison government per Wikipedia Gouvernement Rajaonarison article.

## 6. Update workflow

Verify against sante.gov.mg, msanp.gov.mg, primature.gov.mg, presidence.gov.mg, diplomatie.gouv.fr/madagascar, Midi Madagasikara, L'Express Madagascar, Madagascar Tribune.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Importing US framings — Madagascar is donor-coordinated with major French and EU partnerships.
- Ignoring Pasteur Institute role — IPM is a regional centre of excellence.

## 9. Acronym glossary

- **AMM** — Agence du Médicament de Madagascar.
- **CHU** — Centre Hospitalier Universitaire.
- **DRSP** — Direction Régionale de la Santé Publique.
- **IPM** — Institut Pasteur de Madagascar.
- **MINSANP** — Ministère de la Santé Publique.

## 10. Worked example

```yaml
      - Prof. Zely Arivelo Randriamanantany:
          - Title: Ministre de la Santé Publique de Madagascar (Gouvernement Rajaonarison, sous le Président Andry Rajoelina)
          - Stakeholder engagement notes:
              - "Ministre de la Santé Publique de Madagascar sous le Président Andry Rajoelina; perfil officiel disponible sur msanp.gov.mg / index.php/ministre; profil académique-clinique avec parcours d'enseignement universitaire."
              - "Owns la politique du MINSANP, la coordination avec les 22 DRSP, l'Agence du Médicament de Madagascar, l'Institut Pasteur de Madagascar (centre de référence régional pour le paludisme, la peste, la fièvre de la vallée du Rift et autres pathologies), le réseau des CHU à Antananarivo (HJRA, JRB Befelatanana, Soavinandriana, JRA, Anjanamasina, etc.), la réponse aux épidémies (peste annuelle, paludisme, cholera occasionnel), et la diplomatie sanitaire de Madagascar à l'OMS Afrique, COI (Commission de l'océan Indien) et SADC."
              - "Hook: peste et paludisme endemiques, Institut Pasteur de Madagascar programmes, Couverture Médicale Universelle (UMC) rollout, formation de quadros de santé, coopération COI et SADC."
          - Tone advice:
              - "Ouvrir avec peste / paludisme endémiques, IPM, UMC et COI — sont les axes structurants du portfolio."
              - "Ne pas pitcher en framings purement français — Madagascar a diversifié ses partenariats vers la Chine, l'Inde et les BRICS+; framings exclusivement franco-occidentaux ne reflèteront pas la diplomatie actuelle."
```

## 11. Out-of-band notes

For roles unfilled or in transition.

## 12. Open questions

- Confirm Prof. Zely Arivelo Randriamanantany's date de nomination et profil partidaire.
- Named Secrétaire Général et Directeur Général Santé du MINSANP.
- DG Agence du Médicament de Madagascar et Directeur IPM with currency verified.
- Directeurs des CHU HJRA, JRB Befelatanana, Soavinandriana, JRA.
- Directeurs des 22 Directions Régionales de la Santé Publique.
- Président Commission Santé de l'Assemblée Nationale et Sénat.
- Président Ordre des Médecins de Madagascar with currency verified.
