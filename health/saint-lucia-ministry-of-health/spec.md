# spec.md — `leaders.yml`

Single source of truth for the Saint Lucian health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Saint Lucia Ministry of Health, Wellness and Elderly Affairs and adjacent bodies.

Saint Lucia is a Commonwealth realm under King Charles III. The Philip J. Pierre (SLP — Saint Lucia Labour Party) government has been in office since July 2021. CARICOM, OECS, ECCB, OIF (Saint Lucia is a Francophone-Creole observer) and Commonwealth member.

## 2. Scope

In scope: Governor-General; Prime Minister; Minister of Health; Permanent Secretary; CEO Owen King EU Hospital; House of Assembly.

Out of scope: parish health office heads.

## 3. Structure

Standard 2/6/10/14 indentation. Top-level key: `Saint Lucian health stakeholders:`.

## 4. Field definitions

Party affiliation: `SLP` (Saint Lucia Labour Party, ruling), `UWP` (United Workers Party, principal opposition). Titles in English.

## 5. Provenance and dating

Anchor to year, month or date. Hon. Moses Jn. Baptiste has served as Minister of Health in the Philip J. Pierre SLP government since July 2021; verify against govt.lc.

## 6. Update workflow

Verify against govt.lc, parliament.gov.lc, Saint Lucia Times, St. Lucia News Online, NTN (National Television Network).

## 7. Invariants

Standard.

## 8. Anti-patterns

- Conflating with neighbouring OECS states — distinct sovereign.
- Ignoring the OKEU Hospital story — the Owen King EU Hospital replaced Victoria Hospital in 2017 and has been a central policy frame.

## 9. Acronym glossary

- **OKEU** — Owen King EU Hospital.
- **OECS** — Organisation of Eastern Caribbean States.
- **SLP** — Saint Lucia Labour Party.
- **UWP** — United Workers Party.

## 10. Worked example

```yaml
      - Hon. Moses Jn. Baptiste (SLP):
          - Title: Minister of Health, Wellness and Elderly Affairs (since July 2021)
          - Stakeholder engagement notes:
              - "Minister of Health in the Philip J. Pierre SLP government since July 2021; verify against govt.lc."
              - "Owns MoH policy and budget, Owen King EU Hospital, St. Jude Hospital (Vieux Fort), polyclinics, and CARICOM-OECS-CARPHA diplomacy."
              - "Hook: NCDs, mental health, elderly affairs, OKEU operationalisation, St. Jude Hospital reconstruction, and CARPHA cooperation land."
          - Tone advice:
              - "Open with NCDs, mental health, elderly affairs, OKEU and St. Jude, and CARPHA cooperation."
              - "Recognise OECS distinctness."
```

## 11. Out-of-band notes

For roles unfilled or interim.

## 12. Open questions

- Permanent Secretary with currency verified.
