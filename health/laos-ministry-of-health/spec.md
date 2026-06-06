# spec.md — `leaders.yml`

Single source of truth for the Lao PDR health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Lao PDR Ministry of Health, National Health Insurance Bureau, Food and Drug Department, Mahosot Hospital, Mittaphab (Friendship) Hospital, and adjacent bodies.

The Lao PDR system has National Health Insurance scheme; MoH runs the public network across 18 provinces; significant Vietnam, China, Thailand, Japan, Korea bilateral cooperation; ASEAN integration ongoing.

## 2. Scope

In scope: President; PM; Minister of Health; Vice-Ministers; DG Department of Healthcare; DG Food and Drug Department; DG National Center for Laboratory and Epidemiology; CEOs of Mahosot, Mittaphab and Setthathirath Hospitals; Heads of 18 Provincial Health Departments; National Assembly Social and Cultural Committee.

## 3. Structure

Standard.

## 4. Field definitions

Party affiliation: `LPRP` (Lao People's Revolutionary Party, single ruling party). Titles in English / Lao.

## 5. Provenance and dating

Dr. Bounfeng Phoummalaysith has served as Minister of Health of Lao PDR since March 2021; Gavi Board member representing the Asia constituency; engaged with WHO Lao PDR's new Country Representative (July 2024); statement at 57th Session of UN Commission on Population and Development (CPD57); continued cooperation with Vietnam (PM Chính bilateral 2024) and ASEAN Digital Public Health Conference.

## 6. Update workflow

Verify against moh.gov.la, laogov.gov.la, na.gov.la, KPL News (Lao News Agency), Vientiane Times, Laotian Times.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Importing US framings — Lao PDR is single-party socialist with substantial Chinese and Vietnamese bilateral cooperation.

## 9. Acronym glossary

- **LPRP** — Lao People's Revolutionary Party.

## 10. Worked example

```yaml
      - H.E. Dr. Bounfeng Phoummalaysith (LPRP):
          - Title: Minister of Health, Lao PDR (since March 2021)
          - Stakeholder engagement notes:
              - "Minister of Health of Lao PDR since March 2021 (Nagoya University Asian Satellite Campuses Institute inauguration coverage); LPRP; Gavi Board member representing Asia constituency; medical professional with academic linkages."
              - "Active 2024-2026: PM Chinh Vietnam pledged Vietnam's support for Laos' health sector (Vietnam News, Vietnam Plus); UNICEF 'Impressive progress on health challenges, but much work remains' on Bokeo tour; ASEAN Digital Public Health Conference; statement at CPD57; met WHO Lao PDR's new Country Representative; US bilateral partnership on Maternal and Child Health and Nutrition launched (US Embassy Laos); Lao health ministry advocates greater use of traditional medicine."
              - "Owns MoH policy, NHIS coordination, Food and Drug Department, National Center for Laboratory and Epidemiology, Mahosot / Mittaphab / Setthathirath Hospitals, 18 Provincial Health Departments, Vietnam / China / Thailand / Korea / Japan / EU bilateral cooperation, ASEAN integration and WHO WPRO positioning."
              - "Hook: NHIS expansion, maternal-and-child health, immunisation, traditional Lao medicine integration, ASEAN Digital Public Health, Vietnam-Laos cooperation, US MCH/N partnership."
          - Tone advice:
              - "Open with NHIS, MCH, traditional medicine, ASEAN digital health and Vietnam-Laos cooperation — sustained authored lines."
              - "Do not pitch with single-bloc framings — Laos pragmatically balances ASEAN, China-Vietnam, Japan-Korea and US partnerships."
```

## 11. Out-of-band notes

For roles unfilled or in transition.

## 12. Open questions

- Named Vice-Ministers under Phoummalaysith with currency verified.
- DG Department of Healthcare, DG Food and Drug Department, DG NCLE with currency verified.
- CEOs of Mahosot, Mittaphab, Setthathirath Hospitals with currency verified.
- Heads of 18 Provincial Health Departments with currency verified.
- National Assembly Social and Cultural Committee Chair with currency verified.
