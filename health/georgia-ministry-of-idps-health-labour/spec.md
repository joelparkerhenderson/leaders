# spec.md — `leaders.yml`

Single source of truth for the Georgian health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Georgian Ministry of Internally Displaced Persons from the Occupied Territories, Labour, Health and Social Affairs (MOILHSA), the State Regulation Agency for Medical and Pharmaceutical Activities, National Center for Disease Control and Public Health (NCDC), and adjacent bodies.

The Georgian system implemented universal health coverage from 2013 (UHC programme) through a state-funded contracted-provider model. MOILHSA combines multiple social-protection and health responsibilities. The Georgian Dream government has been in office since 2012; post-2024-election tensions and EU-accession suspension shape the political environment.

## 2. Scope

In scope: President; PM; Minister of IDPs, Labour, Health and Social Affairs; First Deputy and Deputy Ministers; CEO State Regulation Agency for Medical and Pharmaceutical Activities; Director NCDC; CEO Social Service Agency; Heads of major hospitals (Tbilisi State Medical University Hospital, MediClub, Aversi Clinic, Republican Hospital Tbilisi); Parliament Health Care and Social Affairs Committee Chair; Georgian Medical Association.

## 3. Structure

Standard. Ordering: PM → MOILHSA → State Regulation Agency → NCDC → SSA → major hospitals → Parliament Committee → Georgian Medical Association.

## 4. Field definitions

Party affiliation: `Georgian Dream` (KO — Kartuli Otsneba), `UNM` (United National Movement, Saakashvili), `For Georgia` (Gakharia), `Lelo for Georgia`, `Strategy Aghmashenebeli`, `Conservatives for Georgia`. Titles in English with Georgian where useful.

## 5. Provenance and dating

Mikheil Sarjveladze was appointed Minister of Internally Displaced Persons, Labour, Health and Social Affairs in March 2024 under the Georgian Dream government; continuity through 2025-2026 to verify against current MOILHSA listing given the political volatility following the 2024 parliamentary election and EU accession suspension.

## 6. Update workflow

Verify against moh.gov.ge, gov.ge, parliament.ge, Civil Georgia, Agenda.ge, JAM News, 1TV, OC Media.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating Ministry as small — MOILHSA combines major IDP, labour, health and social-affairs responsibilities.
- Importing US framings — Georgia is contracted-provider model with state purchase of services from public and private providers.

## 9. Acronym glossary

- **MOILHSA** — Ministry of Internally Displaced Persons from the Occupied Territories, Labour, Health and Social Affairs.
- **NCDC** — National Center for Disease Control and Public Health.
- **SSA** — Social Service Agency.
- **UHC** — Universal Health Coverage Programme (2013-).

## 10. Worked example

```yaml
      - Mikheil Sarjveladze (Georgian Dream):
          - Title: Minister of IDPs, Labour, Health and Social Affairs (since March 2024; verify currency)
          - Stakeholder engagement notes:
              - "Minister of Internally Displaced Persons from the Occupied Territories, Labour, Health and Social Affairs since March 2024 under the Georgian Dream government; continuity through 2025-2026 to be verified given political volatility following the 2024 parliamentary election and EU accession suspension."
              - "Owns MOILHSA policy combining IDP affairs (Abkhazia, South Ossetia), labour and social protection, the UHC Programme contracted-provider arrangements, NCDC public-health surveillance, State Regulation Agency for medicines and pharmacies, and Georgia's WHO Europe positioning."
              - "Hook: UHC programme refinement, NCDC public-health surveillance, IDP health, social-protection integration, post-Covid recovery, EU-accession-suspended cooperation context."
          - Tone advice:
              - "Open with UHC programme, NCDC and social-protection integration — these are the operational policy levers."
              - "Do not assume EU-aligned framings — the EU accession process has been suspended; framings should respect the political-context constraints."
```

## 11. Out-of-band notes

For roles unfilled or in transition.

## 12. Open questions

- Confirm continuity of Mikheil Sarjveladze as Minister in 2026 against current MOILHSA listing.
- Named Deputy Ministers under MOILHSA with currency verified.
- CEO State Regulation Agency for Medical and Pharmaceutical Activities and Director NCDC with currency verified.
- CEO Social Service Agency with currency verified.
- Heads of major hospitals (Tbilisi State Medical University Hospital, MediClub, Aversi Clinic, Republican Hospital).
- Parliament Health Care and Social Affairs Committee Chair with currency verified.
- President Georgian Medical Association with currency verified.
