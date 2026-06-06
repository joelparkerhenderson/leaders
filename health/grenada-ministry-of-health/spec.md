# spec.md — `leaders.yml`

Single source of truth for the Grenadian health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Grenada Ministry of Health, Wellness and Religious Affairs and adjacent bodies.

Grenada is a Commonwealth realm under King Charles III. The Dickon Mitchell (NDC — National Democratic Congress) government has been in office since June 2022. CARICOM, OECS, ECCB, Commonwealth member.

## 2. Scope

In scope: Governor-General; Prime Minister; Minister of Health; Permanent Secretary; CEO General Hospital St. George's; House of Representatives Standing Committee.

Out of scope: parish health office heads.

## 3. Structure

Standard 2/6/10/14 indentation. Top-level key: `Grenadian health stakeholders:`.

## 4. Field definitions

Party affiliation: `NDC` (National Democratic Congress, ruling), `NNP` (New National Party, principal opposition). Titles in English.

## 5. Provenance and dating

Anchor to year, month or date. Hon. Philip Telesford has served as Minister of Health in the Dickon Mitchell NDC government; verify against gov.gd.

## 6. Update workflow

Verify against gov.gd, parliament.gd, NOW Grenada, Grenada Informer, GIS Grenada.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating Grenada as single-island — Carriacou and Petite Martinique are administratively distinct (Carriacou and Petite Martinique District).
- Conflating with OECS peers — distinct sovereign.

## 9. Acronym glossary

- **NDC** — National Democratic Congress.
- **NNP** — New National Party.
- **OECS** — Organisation of Eastern Caribbean States.

## 10. Worked example

```yaml
      - Hon. Philip Telesford (NDC):
          - Title: Minister of Health, Wellness and Religious Affairs
          - Stakeholder engagement notes:
              - "Minister of Health in the Dickon Mitchell NDC government since June 2022; verify against gov.gd."
              - "Owns MoH policy and budget, General Hospital St. George's, Princess Alice Hospital (Carriacou), polyclinics, and CARICOM-OECS-CARPHA diplomacy."
              - "Hook: NCDs, mental health, Hurricane Beryl 2024 reconstruction (Carriacou and Petite Martinique devastated), CBI-financed health investments, and CARPHA cooperation land."
          - Tone advice:
              - "Open with NCDs, mental health, Hurricane Beryl reconstruction and CARPHA cooperation."
              - "Recognise Carriacou and Petite Martinique distinctness."
```

## 11. Out-of-band notes

For roles unfilled or interim.

## 12. Open questions

- Permanent Secretary with currency verified.
