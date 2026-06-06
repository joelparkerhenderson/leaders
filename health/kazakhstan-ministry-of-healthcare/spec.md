# spec.md — `leaders.yml`

Single source of truth for the Kazakh health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Ministry of Healthcare of the Republic of Kazakhstan (Қазақстан Республикасы Денсаулық сақтау министрлігі), the Social Health Insurance Fund (FSMS), the National Centre for Health Information, the Scientific Centre for Pediatrics and Pediatric Surgery, and adjacent bodies.

The Kazakh system implemented mandatory social health insurance (FSMS) from 2020 covering ~80% of the population. The Ministry sets policy; FSMS purchases; 14 oblast Health Departments plus Almaty and Astana cities and Shymkent run delivery; major specialised centres (cardiology, oncology, pediatrics) provide tertiary care. Vision 2050 frames reform.

## 2. Scope

In scope: President; PM; Minister of Healthcare; Deputy Ministers; Chair FSMS; Director-General Republican Centre for Health Development; Director Scientific Centres for Cardiology, Oncology, Pediatrics; Heads of oblast Health Departments (Almaty Oblast, Astana, Almaty City, Shymkent, Karaganda, Kostanay, Pavlodar); Majilis Committee on Social and Cultural Development Chair; Senate Committee on Social Development Chair; Kazakh Medical Association.

## 3. Structure

Standard. Ordering: President → PM → Minzdrav → FSMS → Republican Centre → Scientific Centres → oblast Departments → Parliament committees → Kazakh Medical Association.

## 4. Field definitions

Party affiliation: `Amanat` (dominant party, formerly Nur Otan), `Auyl`, `Aq Jol`, `Respublica`, `OSDP`, `People's Party of Kazakhstan`. Titles in English with Kazakh / Russian.

## 5. Provenance and dating

Akmaral Alnazarova (Aqmaral Älnazarova) has served as Minister of Healthcare of Kazakhstan since February 2024 in the Olzhas Bektenov government under President Tokayev. Pediatrician; born 16 February 1971 in Kyzylorda; degrees from Almaty State Institute of Medicine and Korkyt Ata Kyzylorda University; received by President Tokayev in 2026.

## 6. Update workflow

Verify against gov.kz/memleket/entities/dsm, primeminister.kz, akorda.kz, parlam.kz, Qazinform, KazTAG, El.kz, SilkwayTV.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating Minzdrav as the buyer — FSMS is the single payer.
- Importing US framings — Kazakhstan is mandatory social health insurance with state-dominated delivery and emerging private sector.

## 9. Acronym glossary

- **FSMS** — Social Health Insurance Fund (Қазақстан халықтық денсаулық сақтау қоры).
- **Minzdrav** — Ministry of Healthcare.

## 10. Worked example

```yaml
      - H.E. Dr. Akmaral Alnazarova (Amanat-aligned):
          - Title: Minister of Healthcare of the Republic of Kazakhstan (since February 2024)
          - Stakeholder engagement notes:
              - "Minister of Healthcare since February 2024 in the Olzhas Bektenov government under President Kassym-Jomart Tokayev; pediatrician; born 16 February 1971 in Kyzylorda; degrees from Almaty State Institute of Medicine (pediatrics) and Korkyt Ata Kyzylorda University (economics); senior career in oblast health administration before ministerial role; received by President Tokayev in 2026 (silkwaytv.kz)."
              - "Owns Minzdrav policy, FSMS single-payer governance, the Republican Centre for Health Development and Scientific Centres network, digital health and UNDP collaboration (UNDP Kazakhstan on digitalisation strengthened cooperation), Vision 2050 health-sector implementation, and Kazakhstan's WHO Europe, SCO and CSTO health diplomacy."
              - "Hook: FSMS reform, digital health and AI integration, Scientific Centres expansion (Cardiology Centre Astana is internationally cited), oncology national programme, primary-care strengthening through 'Salamatti Qazaqstan' programme, and SCO / CSTO cooperation land."
          - Tone advice:
              - "Open with FSMS, digital health, Scientific Centres and Salamatti Qazaqstan — these are her sustained 2024-2026 priorities."
              - "Do not pitch as if engagement could bypass FSMS — the single-payer logic is structural and any provider-financing arrangement must include FSMS as counterparty."
```

## 11. Out-of-band notes

For roles unfilled or in transition.

## 12. Open questions

- Named Deputy Ministers under Alnazarova with currency verified.
- Chair FSMS with currency verified.
- Directors of Republican Centre for Health Development and Scientific Centres for Cardiology, Oncology, Pediatrics with currency verified.
- Heads of oblast Health Departments (priority: Almaty Oblast, Astana, Almaty City, Shymkent, Karaganda).
- Chairs of Majilis Committee on Social and Cultural Development and Senate Committee on Social Development.
- President Kazakh Medical Association with currency verified.
