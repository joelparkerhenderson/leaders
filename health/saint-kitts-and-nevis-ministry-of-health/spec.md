# spec.md — `leaders.yml`

Single source of truth for the Saint Kitts and Nevis health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Saint Kitts and Nevis Ministry of Health and adjacent bodies.

Saint Kitts and Nevis is a federation of two islands, a Commonwealth realm under King Charles III. Nevis has its own Premier and Nevis Island Administration with substantial autonomy including in health. The Terrance Drew (SKNLP — Saint Kitts and Nevis Labour Party) government has been in office since August 2022. Smallest sovereign state in the Americas by both population and area.

## 2. Scope

In scope: Governor-General; Prime Minister; Minister of Health (federal); Premier of Nevis; Nevis Island Administration Minister of Health; Joseph N. France General Hospital; National Assembly.

Out of scope: parish health office heads.

## 3. Structure

Standard 2/6/10/14 indentation. Top-level key: `Saint Kitts and Nevis health stakeholders:`.

## 4. Field definitions

Party affiliation: `SKNLP` (Saint Kitts and Nevis Labour Party, ruling federally), `PAM` (People's Action Movement), `CCM` (Concerned Citizens Movement, governing Nevis), `NRP` (Nevis Reformation Party). Titles in English.

## 5. Provenance and dating

Anchor to year, month or date. Hon. Dr. Terrance Drew himself holds the Health portfolio as Prime Minister and Minister of Health since August 2022; verify against gov.kn.

## 6. Update workflow

Verify against gov.kn, sknnewsroom.com, ZIZ Broadcasting Corporation.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating the Federation as unitary — Nevis has substantial autonomy in health under the 1983 Constitution.
- Conflating with neighbouring OECS states — distinct sovereign.

## 9. Acronym glossary

- **CCM** — Concerned Citizens Movement.
- **PAM** — People's Action Movement.
- **SKNLP** — Saint Kitts and Nevis Labour Party.

## 10. Worked example

```yaml
      - Hon. Dr. Terrance Drew (SKNLP):
          - Title: Prime Minister and Minister of Health (since August 2022)
          - Stakeholder engagement notes:
              - "Prime Minister and Minister of Health in the SKNLP government since August 2022; medical doctor (internal medicine specialist with Caribbean-Cuban training); first PM to hold the health portfolio personally in many years."
              - "Owns federal MoH policy and budget, Joseph N. France General Hospital, coordination with Nevis Island Administration Minister of Health for Alexandra Hospital and Nevis health services, and CARICOM-OECS-CARPHA diplomacy."
              - "Hook: NCDs, mental health, sugar-tax policy (Saint Kitts has a notable industry legacy), CBI-financed health investments, federation health coordination, and CARPHA cooperation land."
          - Tone advice:
              - "Open with NCDs, mental health, sugar-tax policy, federation coordination and CARPHA cooperation."
              - "Recognise Nevis Island Administration's distinctness in health."
```

## 11. Out-of-band notes

For roles unfilled or interim.

## 12. Open questions

- Nevis Island Administration Minister of Health with currency verified.
- Permanent Secretary federal MoH.
