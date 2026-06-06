# spec.md — `leaders.yml`

Single source of truth for the Eswatini health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Eswatini Ministry of Health (MoH), the Eswatini Medicines Regulatory Authority (EMRA), the National Emergency Response Council on HIV/AIDS (NERCHA), and adjacent bodies.

Eswatini operates a public health system led by MoH, complemented by mission-hospital partners (Good Shepherd in Siteki, Raleigh Fitkin Memorial in Manzini) and private providers. The country is a recognised HIV/AIDS-response success case (it became one of the first sub-Saharan countries to achieve 95-95-95). Eswatini is a monarchy: King Mswati III is Head of State and appoints the Prime Minister.

## 2. Scope

In scope: King; Prime Minister; Minister of Health; Principal Secretary; Director of Health Services; CEO EMRA; Director NERCHA; House of Assembly Portfolio Committee on Health; Eswatini Medical and Dental Association.

Out of scope: hospital matrons; regional health management team leads.

## 3. Structure

Standard 2/6/10/14 indentation. Top-level key: `Eswatini health stakeholders:`. Ordering: Monarchy → Cabinet → MoH → EMRA → NERCHA → Parliament → professional associations.

## 4. Field definitions

Eswatini operates a non-party Tinkhundla electoral system; party affiliations are not used in official contexts. Titles in English. Honorific `Hon.` (Honourable) is standard for ministers.

## 5. Provenance and dating

Anchor to year, month or date. Hon. Mduduzi Matsebula has served as Minister of Health, was elected Chair of the East, Central and Southern Africa Health Community (ECSA-HC) Council of Health Ministers for 2026, and previously served as a civil servant in Eswatini Customs for ~17 years before entering politics.

## 6. Update workflow

Verify against gov.sz, parliament.gov.sz, Eswatini Observer, Times of Eswatini, Eswatini News Agency.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Using the legacy name "Swaziland" in formal engagement — the country was renamed Eswatini in April 2018 by royal proclamation; use of "Swaziland" will be politely corrected.
- Importing party-political framings — Eswatini operates a Tinkhundla non-party electoral system; party-aligned framings will be filtered.
- Ignoring the mission-hospital sub-system — Good Shepherd (Siteki) and Raleigh Fitkin Memorial (Manzini) provide a substantial share of secondary care under MoU with MoH.

## 9. Acronym glossary

- **ECSA-HC** — East, Central and Southern Africa Health Community.
- **EMRA** — Eswatini Medicines Regulatory Authority.
- **MoH** — Ministry of Health.
- **NERCHA** — National Emergency Response Council on HIV/AIDS.
- **Tinkhundla** — non-party electoral system of Eswatini.

## 10. Worked example

```yaml
      - Hon. Mduduzi Matsebula:
          - Title: Minister of Health
          - Stakeholder engagement notes:
              - "Minister of Health under the King Mswati III government; elected Chair of the East, Central and Southern Africa Health Community (ECSA-HC) Council of Health Ministers for 2026 — a recognised signal of Eswatini's standing in regional health diplomacy; previously served as a civil servant in Eswatini Customs for ~17 years before entering politics."
              - "Owns MoH policy and budget, Mbabane Government Hospital, Raleigh Fitkin Memorial Hospital, Good Shepherd Mission Hospital, the regional and primary-care network across the four regions (Hhohho, Lubombo, Manzini, Shiselweni), EMRA oversight, NERCHA programmes, and SADC and ECSA-HC health diplomacy."
              - "Hook: HIV/AIDS continuity and sustainability (Eswatini is a recognised 95-95-95 success case), TB and TB/HIV coinfection, NCDs, cervical cancer, maternal and child health, mission-hospital partnerships, and ECSA-HC regional cooperation land."
          - Tone advice:
              - "Open with HIV continuity, TB, NCDs, cervical cancer, mission-hospital partnerships and ECSA-HC cooperation — these are MoH's priorities and Matsebula's chair-line for 2026."
              - "Do not use 'Swaziland' or import party-political framings — the country was renamed Eswatini in 2018 and operates the non-party Tinkhundla electoral system; both will be politely corrected."
```

## 11. Out-of-band notes

For roles unfilled or interim.

## 12. Open questions

- Named Principal Secretary and Director of Health Services with currency verified.
- CEO EMRA and Director NERCHA with currency verified.
- House of Assembly Portfolio Committee on Health Chair with currency verified.
