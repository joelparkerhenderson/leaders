# spec.md — `leaders.yml`

Single source of truth for the Barbadian health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Barbados Ministry of Health and Wellness (MoHW), Queen Elizabeth Hospital and adjacent bodies.

Barbados became a republic on 30 November 2021 (transitioning from Commonwealth realm to republic within the Commonwealth) with President Sandra Mason then Sir Carl Springer; the Mia Mottley (BLP) government has been in office since 2018. CARICOM and CARPHA member.

## 2. Scope

In scope: President; Prime Minister; Minister of Health and Wellness; Permanent Secretary; CEO Queen Elizabeth Hospital; Senate and House of Assembly Joint Committee on Social Affairs and Health.

Out of scope: parish health office heads.

## 3. Structure

Standard 2/6/10/14 indentation. Top-level key: `Barbadian health stakeholders:`. Ordering: President → Prime Minister → MoHW → QEH → Parliament.

## 4. Field definitions

Party affiliation: `BLP` (Barbados Labour Party, ruling), `DLP` (Democratic Labour Party, principal opposition). Titles in English.

## 5. Provenance and dating

Anchor to year, month or date. Hon. Jerome Walcott has served as Minister of Health and Wellness in the Mia Mottley BLP government (cabinet reshuffles have occurred); verify currency against gov.bb.

## 6. Update workflow

Verify against gov.bb, parliament.gov.bb, Barbados Today, Nation News, Loop News Barbados, Barbados Government Information Service.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating Barbados as still a Commonwealth realm — Barbados is a republic since 30 November 2021.
- Conflating with Jamaica or Trinidad — distinct CARICOM sovereign with its own architecture.

## 9. Acronym glossary

- **BLP** — Barbados Labour Party.
- **DLP** — Democratic Labour Party.
- **MoHW** — Ministry of Health and Wellness.
- **QEH** — Queen Elizabeth Hospital.

## 10. Worked example

```yaml
      - Hon. Jerome Walcott (BLP):
          - Title: Minister of Health and Wellness
          - Stakeholder engagement notes:
              - "Minister of Health and Wellness in the Mia Mottley BLP government; senior BLP cabinet member; verify current portfolio holder against gov.bb."
              - "Owns MoHW policy and budget, Queen Elizabeth Hospital, the polyclinic network across the eleven parishes, and CARICOM-CARPHA and PAHO diplomacy."
              - "Hook: NCDs, mental health, climate-and-health (Bridgetown Initiative leadership), maternal-and-child health, and CARPHA cooperation land."
          - Tone advice:
              - "Open with NCDs, mental health, Bridgetown Initiative climate-and-health, MCH and CARPHA cooperation."
              - "Recognise republican status and CARICOM distinctness."
```

## 11. Out-of-band notes

For roles unfilled or interim.

## 12. Open questions

- Permanent Secretary and CEO QEH with currency verified.
