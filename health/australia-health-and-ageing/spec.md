# spec.md — `leaders.yml`

Single source of truth for the structure, semantics, and update rules of `leaders.yml` for the Australian health and ageing portfolio. The YAML must conform to this spec; if they disagree, the spec wins and the YAML is fixed.

## 1. Purpose

`leaders.yml` is an engagement register of named individuals in and around the Australian health system. Each entry helps a reader inside the Department of Health, Disability and Ageing (DHDA), Services Australia (Medicare), the Therapeutic Goods Administration (TGA), the Pharmaceutical Benefits Scheme (PBS) advisory committee, the National Disability Insurance Agency (NDIA), a State/Territory Department of Health, or a Local Health District / Hospital Network decide who to engage, how, and where.

The Australian system is a mixed Medicare-Beveridgean-and-Bismarckian model: the Commonwealth funds Medicare (universal medical-services insurance) and the PBS; the States and Territories run public hospitals via Local Health Districts / Local Health Networks; private health insurance covers ~45% of the population through community-rated premium products. The Australian Commission on Safety and Quality in Health Care (ACSQHC) sets national standards; AHPRA regulates 16 professions through national boards.

## 2. Scope

**In scope:** Prime Minister; Federal Minister for Health and Ageing; Minister for Aged Care; Minister for Disability and the NDIS; Assistant Ministers; Secretary of DHDA; Chief Medical Officer of Australia; CEO TGA; Chair PBAC (Pharmaceutical Benefits Advisory Committee); CEO NDIA; CEO Services Australia; CEO ACSQHC; CEO AHPRA; State and Territory Ministers for Health for the eight jurisdictions; Chief Health Officers of NSW, Vic, Qld, WA, SA, Tas, ACT, NT; Chair Standing Committee on Health, Aged Care and Sport (House); Chair Senate Community Affairs References Committee; Presidents of AMA, ANMF, RACGP, RACS, PSA, RDAA.

**Out of scope:** operational staff below First Assistant Secretary federally; vendors; historical post-holders.

## 3. Structure

```
Australian health and ageing stakeholders:
  - {Organisation}:
      - {Person}:
          - Title: ...
          - Stakeholder engagement notes: [...]
          - Tone advice: [...]
```

Indentation 2/6/10/14 spaces. Ordering: Commonwealth Government → DHDA → TGA → PBAC → ACSQHC → AHPRA → Services Australia (Medicare) → NDIA → 8 States/Territories → Parliamentary Committees → professional bodies.

## 4. Field definitions

Standard family conventions. Party affiliation using canonical Australian abbreviations: `ALP` (Australian Labor Party), `LIB` (Liberal Party of Australia), `NAT` (National Party of Australia), `LNP` (Liberal National Party of Queensland), `GRN` (Australian Greens), `JLN` (Jacqui Lambie Network), `ON` (One Nation), `IND` (Independent). Titles in English.

## 5. Provenance and dating

Anchor facts to year, month or exact date. The second Albanese (ALP) Government was sworn in after the 2025 federal election. Mark Butler MP (ALP, Hindmarsh) was retained as Minister for Health and Ageing and also took on Disability and the NDIS portfolio.

## 6. Update workflow

1. Identify the change. 2. Verify against health.gov.au, pm.gov.au, services.gov.au, tga.gov.au, pbs.gov.au, ndis.gov.au, ahpra.gov.au, aph.gov.au, ABC News, Sydney Morning Herald, The Age, The Australian, Guardian Australia, Croakey, NewsGP. 3. Apply minimum diff. 4. Confirm structure. 5. Re-validate cross-references.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating the system as federally directed — public-hospital delivery is States and Territories.
- Importing NHS framings unmodified — Australia is a Medicare+PBS mixed model with significant private-health-insurance penetration.

## 9. Acronym glossary

- **ACSQHC** — Australian Commission on Safety and Quality in Health Care.
- **AHPRA** — Australian Health Practitioner Regulation Agency.
- **AMA** — Australian Medical Association.
- **ANMF** — Australian Nursing and Midwifery Federation.
- **DHDA** — Department of Health, Disability and Ageing.
- **LHD / LHN** — Local Health District (NSW, Tas, NT) / Local Health Network (Vic, Qld, SA, ACT, WA).
- **MBS** — Medicare Benefits Schedule.
- **NDIA** — National Disability Insurance Agency.
- **NDIS** — National Disability Insurance Scheme.
- **PBAC** — Pharmaceutical Benefits Advisory Committee.
- **PBS** — Pharmaceutical Benefits Scheme.
- **PHN** — Primary Health Network (commissioning entity, 31 nationally).
- **RACGP** — Royal Australian College of General Practitioners.
- **RACS** — Royal Australasian College of Surgeons.
- **RDAA** — Rural Doctors Association of Australia.
- **TGA** — Therapeutic Goods Administration.

## 10. Worked example

```yaml
      - Mark Butler MP (ALP):
          - Title: Federal Minister for Health and Ageing, and Minister for Disability and the National Disability Insurance Scheme (after the 2025 federal election; second Albanese ministry)
          - Stakeholder engagement notes:
              - "Federal Minister for Health and Ageing and Minister for Disability and the NDIS in the second Albanese ministry after the 2025 federal election; ALP; Member for Hindmarsh (and previously Port Adelaide) since 2007 — one of the longest-serving ALP health spokespeople and Ministers."
              - "Retained the Health portfolio across the 2025 election cycle (newsGP confirmation) and absorbed the NDIS portfolio, signalling consolidated political accountability for the disability scheme alongside health."
              - "Active media cadence in 2026: multiple press conferences in Newcastle, Canberra and Melbourne May 2026; visible commitment to bulk-billing reform, PBS listings, mental-health funding and NDIS sustainability."
              - "Owns Medicare reform (bulk-billing, MBS), PBS listings and the National Medicines Policy, the Strengthening Medicare programmes, Aged Care Reform follow-through after the 2024 Aged Care Act, NDIS reform and the new NDIA arrangements."
              - "Hook: Medicare and bulk-billing, PBS listings, Strengthening Medicare, Aged Care reform, NDIS reform and digital health (My Health Record reform, electronic medication management) land; State-bypassing framings on hospital delivery do not."
          - Tone advice:
              - "Lead with Medicare bulk-billing, PBS access, Strengthening Medicare, Aged Care reform and NDIS sustainability — these are Butler's authored, sustained policy lines."
              - "Do not pitch hospital-service delivery as a federal lever — States and Territories own public-hospital delivery; Butler will redirect to State Ministers."
```

## 11. Out-of-band notes

For roles unfilled or interim.

## 12. Open questions

- Named Minister for Aged Care and Assistant Ministers under Butler with currency verified.
- Secretary DHDA, Chief Medical Officer of Australia, CEO TGA, Chair PBAC, CEO ACSQHC, CEO AHPRA with currency verified.
- CEO NDIA and CEO Services Australia with currency verified.
- State and Territory Ministers for Health for NSW, Vic, Qld, WA, SA, Tas, ACT, NT with currency verified.
- Chief Health Officers of NSW, Vic, Qld, WA, SA, Tas, ACT, NT with currency verified.
- Chair Standing Committee on Health, Aged Care and Sport (House) and Chair Senate Community Affairs References Committee with currency verified.
- Presidents AMA, ANMF, RACGP, RACS, PSA, RDAA with currency verified.
