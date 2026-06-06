# spec.md — `leaders.yml`

Single source of truth for the Guyanese health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around Guyana's Ministry of Health, the Guyana Public Hospital Corporation, Regional Health Authorities, and adjacent bodies.

Guyana operates a tax-funded universal Beveridgean system with the Ministry of Health setting policy and the Guyana Public Hospital Corporation (Georgetown) as the national referral hospital. Ten Regional Democratic Councils have devolved primary-care responsibility through Regional Health Authorities. The Food and Drug Department within MoH regulates medicines.

## 2. Scope

In scope: President; Minister of Health; Permanent Secretary; CEO Guyana Public Hospital Corporation; Director Food and Drug Department; Chief Medical Officer; Regional Health Officers; Chair Public Hospital Corporation; Chair Parliamentary Sectoral Committee on Social Services (Health); President Guyana Medical Association; President Guyana Nurses Association.

Out of scope: operational staff below directorate level; vendors; historical post-holders.

## 3. Structure

```
Guyana health stakeholders:
  - {Organisation}:
      - {Person}:
          - Title: ...
          - Stakeholder engagement notes: [...]
          - Tone advice: [...]
```

Standard indentation. Ordering: Cabinet → Ministry of Health → Guyana Public Hospital Corporation → Regional Health Authorities → Food and Drug Department → Parliament → professional bodies.

## 4. Field definitions

Standard. Party affiliation using canonical Guyanese abbreviations: `PPP/C` (People's Progressive Party / Civic), `APNU+AFC` (A Partnership for National Unity + Alliance for Change). Titles in English.

## 5. Provenance and dating

Anchor facts to year, month or exact date. Dr. Frank C. S. Anthony has been Minister of Health since 2020 in the PPP/C government of President Irfaan Ali. Re-elected in PPP/C-won 2025 general election.

## 6. Update workflow

Verify against health.gov.gy, op.gov.gy, parliament.gov.gy, Stabroek News, Guyana Chronicle, Demerara Waves, Kaieteur News.

## 7. Invariants

Standard.

## 8. Anti-patterns

Importing US framings unmodified — Guyana is tax-funded universal Beveridgean.
Importing high-volume country frames — Guyana's population (~800k) and geography (interior settlements) make scale and access the operational levers.

## 9. Acronym glossary

- **CARICOM** — Caribbean Community (Guyana is the headquarters).
- **GPHC** — Guyana Public Hospital Corporation.
- **MoH** — Ministry of Health.
- **PAHO/WHO** — Pan American Health Organization / WHO.

## 10. Worked example

```yaml
      - Dr. Frank C. S. Anthony (PPP/C):
          - Title: Minister of Health (since 2020)
          - Stakeholder engagement notes:
              - "Minister of Health since 2020 in the People's Progressive Party / Civic (PPP/C) government of President Irfaan Ali, retained after the PPP/C-won 2025 general election."
              - "Medical doctor by training; long-running parliamentary career; previously Minister of Culture, Youth and Sport; recognised regionally — was elected Chair of a CARICOM-coordinated health initiative."
              - "Owns Guyana's universal health-coverage agenda, oil-revenue-funded health infrastructure investments (hospital construction in Region 3, 4, 5, 6 and 10), oncology and cardiology centres, telemedicine to interior regions, and the Caribbean health-cooperation portfolio."
              - "Hook: oil-revenue health infrastructure, oncology and cardiology centres, telemedicine to hinterland, CARICOM cooperation, NCD prevention, maternal-and-child health land."
          - Tone advice:
              - "Lead with oil-revenue infrastructure investments, NCD prevention, telemedicine and CARICOM cooperation — these are Guyana's policy priorities reflecting the oil-boom fiscal context."
              - "Do not pitch as if Guyana were resource-poor — substantial oil revenues since 2020 have changed the health-financing environment significantly."
```

## 11. Out-of-band notes

For roles unfilled or interim.

## 12. Open questions

- Named Permanent Secretary, CEO GPHC, Chief Medical Officer with currency verified.
- Director Food and Drug Department.
- Regional Health Officers of the ten Regions.
- Chair Parliamentary Sectoral Committee on Social Services (Health).
- Presidents Guyana Medical Association, Guyana Nurses Association.
