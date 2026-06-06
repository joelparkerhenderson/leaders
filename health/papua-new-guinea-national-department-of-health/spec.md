# spec.md — `leaders.yml`

Single source of truth for the Papua New Guinea (PNG) health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the PNG National Department of Health (NDoH), Provincial Health Authorities (PHAs) and adjacent bodies.

PNG is the most populous Pacific Island state (~10 million), a Commonwealth realm under King Charles III. James Marape (Pangu Pati) has been Prime Minister since 2019. Member of PIF, MSG, ACP and Commonwealth.

## 2. Scope

In scope: Governor-General; Prime Minister; Minister for Health; Secretary NDoH; CEO Port Moresby General Hospital; Parliamentary Permanent Committee on Health.

Out of scope: PHA CEOs.

## 3. Structure

Standard 2/6/10/14 indentation. Top-level key: `Papua New Guinea health stakeholders:`.

## 4. Field definitions

Party affiliation: `Pangu Pati`, `PNC` (People's National Congress), `URP` (United Resources Party), `NA` (National Alliance Party). Titles in English.

## 5. Provenance and dating

Anchor to year, month or date. Hon. Elias Kapavore has served as Minister for Health in the Marape government; verify against pmnec.gov.pg.

## 6. Update workflow

Verify against health.gov.pg, pmnec.gov.pg, parliament.gov.pg, Post-Courier, The National (PNG), EMTV Online, NBC PNG.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating PNG as small Pacific SIDS — PNG is the largest Pacific state with continental-scale geography, diverse epidemiology and a strongly decentralised PHA architecture.
- Ignoring PHA decentralisation — Provincial Health Authorities have substantial operational authority.

## 9. Acronym glossary

- **MSG** — Melanesian Spearhead Group.
- **NDoH** — National Department of Health.
- **PHA** — Provincial Health Authority.
- **PIF** — Pacific Islands Forum.

## 10. Worked example

```yaml
      - Hon. Elias Kapavore (Pangu Pati):
          - Title: Minister for Health
          - Stakeholder engagement notes:
              - "Minister for Health in the Marape Pangu Pati-led coalition; verify against pmnec.gov.pg."
              - "Owns NDoH policy and budget, Port Moresby General Hospital, Provincial Hospitals, Provincial Health Authorities, and PIF-MSG-WPRO diplomacy."
              - "Hook: TB and MDR-TB (high burden), MCH, NCDs, malaria, HIV, polio surveillance, and PHA decentralisation land."
          - Tone advice:
              - "Open with TB-MDR, MCH, NCDs, malaria, HIV and PHA decentralisation."
              - "Recognise PNG's continental scale and PHA architecture."
```

## 11. Out-of-band notes

For roles unfilled or interim.

## 12. Open questions

- Secretary NDoH with currency verified.
- Parliamentary Permanent Committee on Health Chair.
