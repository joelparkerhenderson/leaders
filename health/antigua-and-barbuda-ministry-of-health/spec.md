# spec.md — `leaders.yml`

Single source of truth for the Antigua and Barbuda health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Antigua and Barbuda Ministry of Health, Wellness and the Environment and adjacent bodies.

Antigua and Barbuda is a Commonwealth realm under King Charles III with the Gaston Browne (ABLP — Antigua and Barbuda Labour Party) government in office. CARICOM, OECS, ECCB and Commonwealth member.

## 2. Scope

In scope: Governor-General; Prime Minister; Minister of Health, Wellness and the Environment; Permanent Secretary; CEO Sir Lester Bird Medical Centre; House of Representatives Standing Committee on Social Services.

Out of scope: parish health office heads.

## 3. Structure

Standard 2/6/10/14 indentation. Top-level key: `Antigua and Barbuda health stakeholders:`.

## 4. Field definitions

Party affiliation: `ABLP` (Antigua and Barbuda Labour Party, ruling), `UPP` (United Progressive Party, opposition), `BPM` (Barbuda People's Movement). Titles in English.

## 5. Provenance and dating

Anchor to year, month or date. Sir Molwyn Joseph has served as Minister of Health and Wellness in the Gaston Browne ABLP government; verify currency against ab.gov.ag.

## 6. Update workflow

Verify against ab.gov.ag, parliament.gov.ag, Antigua Observer, Antigua Newsroom, ZDK News.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating Antigua and Barbuda as single-island — Barbuda is administratively distinct (BPM-administered Barbuda Council).
- Conflating with neighbouring OECS states — distinct sovereign.

## 9. Acronym glossary

- **ABLP** — Antigua and Barbuda Labour Party.
- **ECCB** — Eastern Caribbean Central Bank.
- **OECS** — Organisation of Eastern Caribbean States.

## 10. Worked example

```yaml
      - Sir Molwyn Joseph (ABLP):
          - Title: Minister of Health, Wellness and the Environment
          - Stakeholder engagement notes:
              - "Minister of Health in the Gaston Browne ABLP government; verify against ab.gov.ag."
              - "Owns MoH policy and budget, Sir Lester Bird Medical Centre, polyclinics, and CARICOM-CARPHA, OECS and PAHO diplomacy."
              - "Hook: NCDs, mental health, sargassum-and-health, hurricane preparedness, and Barbuda post-Irma reconstruction land."
          - Tone advice:
              - "Open with NCDs, mental health, climate-and-health and CARPHA cooperation."
              - "Recognise the Barbuda administrative distinctness."
```

## 11. Out-of-band notes

For roles unfilled or interim.

## 12. Open questions

- Permanent Secretary and CEO SLBMC with currency verified.
