# spec.md — `leaders.yml`

Single source of truth for the Belize health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around Belize's Ministry of Health and Wellness, the Karl Heusner Memorial Hospital Authority (KHMHA, the national referral hospital), regional health authorities, and adjacent bodies.

The Belizean system is tax-funded universal with primary-care delivered through health centres, four regional hospitals, and KHMH as the tertiary referral facility. Belize has hosted Cuban medical brigades for decades.

## 2. Scope

In scope: Prime Minister; Minister of Health and Wellness; CEO Ministry; Director General Health Services; CEO KHMHA; Regional Managers (Western, Northern, Southern, Central Health Regions); Chair Public Health Committee in Parliament; President Belize Medical and Dental Association; President Nurses Association of Belize.

## 3. Structure

Standard. Ordering: Cabinet → MoH&W → KHMHA → Regional Health Authorities → Parliament → professional bodies.

## 4. Field definitions

Party affiliation using canonical Belizean abbreviations: `PUP` (People's United Party), `UDP` (United Democratic Party). Titles in English.

## 5. Provenance and dating

Anchor facts to year, month or exact date. The John Briceño PUP government has been in office since 2020 and won re-election in March 2025. Hon. Kevin Emmanuel Bernard has been Minister of Health and Wellness through both terms.

## 6. Update workflow

Verify against health.gov.bz, op.gov.bz, nationalassembly.gov.bz, Channel 5 Belize, Breaking Belize News, Caribbean National Weekly.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating Belize as a single-hospital system — KHMH dominates tertiary but four regional networks operate distinct service models.
- Importing US framings unmodified — Belize is tax-funded universal Beveridgean with Cuban-mission cooperation.

## 9. Acronym glossary

- **CARICOM** — Caribbean Community (Belize is a member).
- **KHMH** — Karl Heusner Memorial Hospital.
- **KHMHA** — Karl Heusner Memorial Hospital Authority.
- **MoH&W** — Ministry of Health and Wellness.

## 10. Worked example

```yaml
      - Hon. Kevin Emmanuel Bernard (PUP):
          - Title: Minister of Health and Wellness (in the second John Briceño PUP government, since March 2025)
          - Stakeholder engagement notes:
              - "Minister of Health and Wellness in the second John Briceño (PUP) government after re-election in March 2025; retained the portfolio from the first Briceño term (2020-2025) — continuous tenure across two electoral cycles."
              - "At the 79th World Health Assembly (May 2026) Belize called for global health solidarity and supported Taiwan's participation in international health discussions — Bernard delivered the national statement, indicating Belize's distinctive foreign-policy alignment within Central America."
              - "Defended the Cuban medical missions publicly — a long-standing PUP policy that brings Cuban doctors and nurses to support service delivery in remote and underserved areas."
              - "Owns universal health coverage agenda, KHMH and regional hospitals, primary-care strengthening, Cuban-mission cooperation, climate-and-health, Belize's CARICOM and PAHO positioning."
              - "Hook: universal health coverage, KHMH modernisation, Cuban-mission cooperation, climate and health, NCDs, primary care land."
          - Tone advice:
              - "Lead with universal coverage, KHMH, Cuban-mission cooperation and climate health — these are sustained PUP policy lines."
              - "Do not pitch in US-aligned framings — Belize's foreign-policy stance, including support for Taiwan and defence of Cuban missions, makes US-aligned framings politically incongruent."
```

## 11. Out-of-band notes

For roles unfilled or interim.

## 12. Open questions

- Named CEO and Director General Health Services with currency verified.
- CEO KHMHA with currency verified.
- Regional Managers of the four Health Regions.
- Chair Public Health Committee in the current National Assembly.
- President Belize Medical and Dental Association, Nurses Association of Belize.
