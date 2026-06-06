# spec.md — `leaders.yml`

Single source of truth for the Fijian health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Fiji Ministry of Health and Medical Services (MHMS) and adjacent bodies.

Fiji is a republic with President as Head of State. The Sitiveni Rabuka (People's Alliance — PAP) coalition government has been in office since December 2022. PIF, MSG, ACP and Commonwealth member; hosts the PIF Secretariat in Suva.

## 2. Scope

In scope: President; Prime Minister; Minister of Health and Medical Services; Permanent Secretary for Health; Director Colonial War Memorial Hospital; Parliamentary Standing Committee on Social Affairs.

Out of scope: divisional health office heads.

## 3. Structure

Standard 2/6/10/14 indentation. Top-level key: `Fijian health stakeholders:`.

## 4. Field definitions

Party affiliation: `PAP` (People's Alliance Party, ruling), `NFP` (National Federation Party, coalition partner), `SODELPA` (Social Democratic Liberal Party, coalition partner), `FijiFirst` (legacy Bainimarama party). Titles in English.

## 5. Provenance and dating

Anchor to year, month or date. Hon. Dr. Atonio Lalabalavu has served as Minister of Health in the Rabuka government since December 2022; verify against fiji.gov.fj.

## 6. Update workflow

Verify against health.gov.fj, fiji.gov.fj, parliament.gov.fj, Fiji Sun, Fiji Times, FBC News, FijiVillage.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating Fiji as small Pacific SIDS — Fiji is a regional hub with the PIF Secretariat and is the dominant health-system in the Central Pacific.
- Ignoring the iTaukei-Indo-Fijian community dynamics which can affect framing.

## 9. Acronym glossary

- **MHMS** — Ministry of Health and Medical Services.
- **NFP** — National Federation Party.
- **PAP** — People's Alliance Party.
- **PIF** — Pacific Islands Forum.

## 10. Worked example

```yaml
      - Hon. Dr. Atonio Lalabalavu (PAP):
          - Title: Minister of Health and Medical Services (since December 2022)
          - Stakeholder engagement notes:
              - "Minister of Health in the Rabuka coalition government; medical doctor; verify against fiji.gov.fj."
              - "Owns MHMS policy and budget, Colonial War Memorial Hospital (Suva), Lautoka Hospital, Labasa Hospital, divisional and sub-divisional hospital network, and PIF-MSG-WPRO diplomacy."
              - "Hook: NCDs (highest in WPRO), TB, dengue, climate-and-health (PIF chair), and PIF Secretariat hosting role land."
          - Tone advice:
              - "Open with NCDs, climate-and-health, TB and PIF cooperation."
              - "Recognise iTaukei-Indo-Fijian community dynamics."
```

## 11. Out-of-band notes

For roles unfilled or interim.

## 12. Open questions

- Permanent Secretary for Health with currency verified.
