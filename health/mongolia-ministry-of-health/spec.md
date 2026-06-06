# spec.md — `leaders.yml`

Single source of truth for the Mongolian health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Mongolia Ministry of Health (Эрүүл мэндийн яам), Health Insurance General Agency, National Center for Communicable Diseases (NCCD), Central Hospitals, and adjacent bodies.

The Mongolian system has compulsory health insurance through the Health Insurance General Agency; MoH runs public network; significant rural-urban disparity given sparse population over vast territory.

## 2. Scope

In scope: President; PM; Minister of Health; State Secretaries; DG NCCD; CEOs of Central Hospitals (First Central Hospital, State First Central, Third Central, National Cancer Centre); 21 Aimag and Ulaanbaatar district Health Offices; Health Committee in State Great Khural; Mongolian Medical Association.

## 3. Structure

Standard.

## 4. Field definitions

Party affiliation: `MPP` (Mongolian People's Party), `DP` (Democratic Party), `HUN` (HUN — Mongolian New Right Party), others. Titles in English.

## 5. Provenance and dating

Munkhsaikhan Togtmol serves as Minister of Health in the current Mongolian cabinet (Prime Minister Oyun-Erdene Luvsannamsrai or successor); met WHO Representative in Mongolia per Montsame.

## 6. Update workflow

Verify against moh.gov.mn, mongolia.gov.mn, parliament.mn, Montsame, Mongolian Economy, News.MN.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Importing US framings — Mongolia is mandatory insurance with state-dominated delivery and substantial donor coordination.

## 9. Acronym glossary

- **MPP** — Mongolian People's Party.
- **NCCD** — National Center for Communicable Diseases.

## 10. Worked example

```yaml
      - Munkhsaikhan Togtmol (MPP):
          - Title: Minister of Health, Mongolia
          - Stakeholder engagement notes:
              - "Minister of Health of Mongolia in the current cabinet; met with WHO Representative in Mongolia (Montsame)."
              - "Owns MoH policy, Health Insurance General Agency coordination, NCCD outbreak surveillance, Central Hospitals network, 21 Aimag and Ulaanbaatar district Health Offices, telemedicine programmes (UNFPA Telemedicine Project on Maternal and Newborn Health), and Mongolia's WHO WPRO, SCO and OSCE health cooperation."
              - "Hook: Health Insurance reform, telemedicine for nomadic and remote populations, NCDs (high alcohol-related disease burden), mpox preparedness, traditional Mongolian medicine integration, and SCO cooperation."
          - Tone advice:
              - "Open with telemedicine, NCDs, traditional medicine and SCO cooperation — distinctive Mongolian priorities."
              - "Do not pitch as if Mongolia were small — vast territory, nomadic populations and geo-strategic position between Russia and China make engagement distinctive."
```

## 11. Out-of-band notes

For roles unfilled or in transition.

## 12. Open questions

- Named State Secretaries under Togtmol with currency verified.
- DG NCCD, CEO Health Insurance General Agency with currency verified.
- CEOs of First, State First, Third Central Hospitals, National Cancer Centre.
- Health Committee Chair in State Great Khural.
- President Mongolian Medical Association with currency verified.
