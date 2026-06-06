# spec.md — `leaders.yml`

Single source of truth for the Dominican (Commonwealth of Dominica) health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Commonwealth of Dominica Ministry of Health, Wellness and Social Services. Not to be confused with the Dominican Republic.

Dominica is a republic with President as Head of State; the Roosevelt Skerrit (DLP — Dominica Labour Party) government has been in office since 2004 (long-serving). CARICOM, OECS, ECCB, Commonwealth member.

## 2. Scope

In scope: President; Prime Minister; Minister of Health, Wellness and Social Services; Permanent Secretary; CEO Dominica China Friendship Hospital; House of Assembly Public Accounts Committee.

Out of scope: parish health office heads.

## 3. Structure

Standard 2/6/10/14 indentation. Top-level key: `Dominican (Commonwealth of Dominica) health stakeholders:`.

## 4. Field definitions

Party affiliation: `DLP` (Dominica Labour Party, ruling), `UWP` (United Workers' Party, principal opposition). Titles in English.

## 5. Provenance and dating

Anchor to year, month or date. Hon. Dr. Cassanni Laville has served as Minister of Health, Wellness and Social Services in the Roosevelt Skerrit DLP government; verify against dominica.gov.dm.

## 6. Update workflow

Verify against dominica.gov.dm, parliament.gov.dm, Dominica News Online, Dominica Vibes, GIS Dominica.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Confusing with the Dominican Republic — radically different sovereign state, language, system.
- Ignoring the Citizenship by Investment funding architecture which is significant for the Ministry.

## 9. Acronym glossary

- **DLP** — Dominica Labour Party.
- **OECS** — Organisation of Eastern Caribbean States.
- **UWP** — United Workers' Party.

## 10. Worked example

```yaml
      - Hon. Dr. Cassanni Laville (DLP):
          - Title: Minister of Health, Wellness and Social Services
          - Stakeholder engagement notes:
              - "Minister of Health in the Roosevelt Skerrit DLP government; verify against dominica.gov.dm."
              - "Owns MoH policy and budget, Dominica China Friendship Hospital (Chinese-built), polyclinics, and CARICOM-OECS-CARPHA diplomacy."
              - "Hook: NCDs, mental health, climate-and-health (Hurricane Maria 2017 legacy), CBI-financed health investments and resilience reconstruction land."
          - Tone advice:
              - "Open with NCDs, mental health, climate-and-health and resilience reconstruction."
              - "Never confuse with the Dominican Republic."
```

## 11. Out-of-band notes

For roles unfilled or interim.

## 12. Open questions

- Permanent Secretary with currency verified.
