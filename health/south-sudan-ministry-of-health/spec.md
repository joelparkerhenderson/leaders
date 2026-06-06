# spec.md — `leaders.yml`

Single source of truth for the South Sudanese health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the South Sudanese Ministry of Health (MoH), and adjacent bodies under the Revitalised Agreement on the Resolution of the Conflict in South Sudan (R-ARCSS) framework that established a transitional government of national unity.

South Sudan's health system is fragile, heavily donor-dependent, and shaped by the prolonged civil-war legacy, large displaced populations and recurring outbreaks (cholera, hepatitis E, mpox, measles). The Ministry serves under the President Salva Kiir-led Revitalised Transitional Government of National Unity (R-TGoNU).

## 2. Scope

In scope: President; Vice Presidents (the R-ARCSS provides for multiple); Minister of Health; Undersecretary; National Transitional Legislative Assembly Specialised Committee on Health; State Ministers of Health (the ten states each have one).

Out of scope: county health department heads.

## 3. Structure

Standard 2/6/10/14 indentation. Top-level key: `South Sudanese health stakeholders:`. Ordering: Presidency → MoH → State Ministers → Legislative Assembly.

## 4. Field definitions

Party affiliation: `SPLM` (Sudan People's Liberation Movement, Kiir-led), `SPLM-IO` (SPLM-In Opposition, Riek Machar-led), `SSOA` (South Sudan Opposition Alliance), `OPP` (Other Political Parties). Titles in English.

## 5. Provenance and dating

Anchor to year, month or date. Hon. Yolanda Awel Deng Juach has served as Minister of Health in the Salva Kiir government; verify currency against the Office of the President.

## 6. Update workflow

Verify against moh.gov.ss (may have intermittent availability), gurtong.net, Eye Radio, Radio Tamazuj, Sudan Tribune, City Review.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Conflating South Sudan with (former) Sudan — South Sudan seceded in July 2011 and is a distinct sovereign state with its own MoH; framings that bundle them are inaccurate.
- Ignoring the donor architecture — South Sudan's health system is materially co-financed by USAID/PEPFAR, World Bank, Global Fund, Gavi, WHO, UNICEF, EU and FCDO; the Health Pooled Fund mechanism is a central structure.
- Assuming a stable transition timeline — the R-ARCSS has been repeatedly extended; framings that assume a fixed political-transition end-date risk being out of date.

## 9. Acronym glossary

- **R-ARCSS** — Revitalised Agreement on the Resolution of the Conflict in South Sudan.
- **R-TGoNU** — Revitalised Transitional Government of National Unity.
- **SPLM** — Sudan People's Liberation Movement.
- **SPLM-IO** — SPLM-In Opposition.

## 10. Worked example

```yaml
      - Hon. Yolanda Awel Deng Juach (SPLM):
          - Title: Minister of Health
          - Stakeholder engagement notes:
              - "Minister of Health in the Salva Kiir-led Revitalised Transitional Government of National Unity (R-TGoNU); verify currency against the Office of the President."
              - "Owns MoH policy and budget, Juba Teaching Hospital, the state-hospital and primary-care network across the ten states (Central Equatoria, Eastern Equatoria, Jonglei, Lakes, Northern Bahr el Ghazal, Unity, Upper Nile, Warrap, Western Bahr el Ghazal, Western Equatoria) plus the three administrative areas (Abyei, Pibor, Ruweng), donor coordination through the Health Pooled Fund, and IGAD and AU diplomacy."
              - "Hook: cholera, hepatitis E and mpox outbreak response, maternal-and-child mortality reduction, measles immunisation, conflict-injury surgical services, and humanitarian-development nexus framing land."
          - Tone advice:
              - "Open with outbreak response, MCH, immunisation, conflict-injury services and humanitarian-development nexus — operational priorities in the R-TGoNU context."
              - "Do not bundle with Sudan or assume a stable transition timeline — secession was 2011 and the R-ARCSS has been repeatedly extended."
```

## 11. Out-of-band notes

For roles unfilled or interim under the R-TGoNU framework.

## 12. Open questions

- Named Undersecretary with currency verified.
- State Ministers of Health for the ten states with currency verified.
- National Transitional Legislative Assembly Specialised Committee on Health Chair with currency verified.
