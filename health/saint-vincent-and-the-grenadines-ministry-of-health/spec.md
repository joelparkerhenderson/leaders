# spec.md — `leaders.yml`

Single source of truth for the Vincentian health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Saint Vincent and the Grenadines Ministry of Health, Wellness and the Environment and adjacent bodies.

Saint Vincent and the Grenadines is a Commonwealth realm under King Charles III. The Ralph Gonsalves (ULP — Unity Labour Party) government has been in office since 2001 — one of the longest-serving Caribbean Prime Ministers. CARICOM, OECS, ECCB, ALBA, CELAC and Commonwealth member.

## 2. Scope

In scope: Governor-General; Prime Minister; Minister of Health; Permanent Secretary; CEO Milton Cato Memorial Hospital; House of Assembly.

Out of scope: parish health office heads.

## 3. Structure

Standard 2/6/10/14 indentation. Top-level key: `Vincentian health stakeholders:`.

## 4. Field definitions

Party affiliation: `ULP` (Unity Labour Party, ruling), `NDP` (New Democratic Party, principal opposition). Titles in English.

## 5. Provenance and dating

Anchor to year, month or date. Hon. St. Clair Prince has served as Minister of Health in the Ralph Gonsalves ULP government; verify against gov.vc.

## 6. Update workflow

Verify against gov.vc, parliament.gov.vc, iWitness News, Searchlight, NBC Radio.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating SVG as single-island — the Grenadines (Bequia, Mustique, Canouan, Mayreau, Union Island, Palm Island, Petit St Vincent) require inter-island health architecture.
- Ignoring volcanic and Cuban-Venezuelan engagement — La Soufrière 2021 eruption is operational memory; ALBA membership shapes Cuban medical mission and Venezuelan engagement.

## 9. Acronym glossary

- **ALBA** — Bolivarian Alliance for the Peoples of Our America.
- **NDP** — New Democratic Party.
- **ULP** — Unity Labour Party.

## 10. Worked example

```yaml
      - Hon. St. Clair Prince (ULP):
          - Title: Minister of Health, Wellness and the Environment
          - Stakeholder engagement notes:
              - "Minister of Health in the Ralph Gonsalves ULP government; verify against gov.vc."
              - "Owns MoH policy and budget, Milton Cato Memorial Hospital, Grenadines polyclinics, Cuban-medical-brigade coordination, and CARICOM-OECS-ALBA-CARPHA diplomacy."
              - "Hook: NCDs, mental health, La Soufrière 2021 eruption legacy, Cuban medical brigade, inter-island Grenadines architecture, and CARPHA cooperation land."
          - Tone advice:
              - "Open with NCDs, mental health, La Soufrière legacy, Cuban medical brigade and Grenadines architecture."
              - "Recognise ALBA-Cuban engagement which is distinctive in OECS."
```

## 11. Out-of-band notes

For roles unfilled or interim.

## 12. Open questions

- Permanent Secretary with currency verified.
