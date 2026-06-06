# spec.md — `leaders.yml`

Single source of truth for the Egyptian health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Egyptian Ministry of Health and Population (MoHP), Universal Health Insurance Authority (UHIA), Egyptian Drug Authority (EDA), Egyptian Authority for Unified Procurement, Medical Supply and Health Technology Management (UPA), General Authority for Health Care (GAHC), and adjacent bodies.

The Egyptian system is undergoing the Universal Health Insurance (UHI) Law implementation since 2018 — a phased transition from segmented public delivery (MoHP, military health, MoHE university hospitals) to a single-payer UHIA model with GAHC as public provider. Implementation is rolling out by governorate, starting with Port Said and Luxor.

## 2. Scope

In scope: President; Prime Minister; Minister of Health and Population (concurrently Deputy Prime Minister); Deputy Ministers; Head UHIA; Head EDA; Head UPA; Head GAHC; Head Central Administration for Preventive Affairs; Heads of governorate health directorates (Cairo, Alexandria, Giza, Qalyubia, Daqahlia, Sharqia, Beheira); Chair House of Representatives Health Committee; Chair Senate Health Committee; Egyptian Medical Syndicate; Egyptian Pharmacist Syndicate; Egyptian Nurses Syndicate.

## 3. Structure

Standard 2/6/10/14. Ordering: Presidency → PM Cabinet → MoHP → UHIA → EDA → UPA → GAHC → governorate health directorates → Parliament committees → professional syndicates.

## 4. Field definitions

Party affiliation in Egypt is dominated by `Mostaqbal Watan` (Nation's Future), `Wafd`, `Republican People's Party`, `Reform and Development Party`, plus various coalitions; technocratic appointments are common. Titles in English with Arabic transliteration.

## 5. Provenance and dating

Dr. Khaled Abdel Ghaffar continues as Minister of Health and Population following the 4 February 2026 cabinet reshuffle; also serves as Deputy Prime Minister of Egypt; oral-and-dental-medicine academic background; ex-Minister of Higher Education and Scientific Research before transferring to Health. State targets raising healthy life expectancy to 75 years by 2030; recent Hantavirus and other surveillance signals.

## 6. Update workflow

Verify against mohp.gov.eg, presidency.eg, eda.mohp.gov.eg, uhia.gov.eg, dostor.org, parliament.gov.eg, Egypt Today, Al-Ahram (English), Daily News Egypt, Egypt Independent, Mada Masr.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating the MoHP as the only buyer — UHIA is the single payer in UHI-implemented governorates.
- Importing US framings unmodified — Egypt is undergoing a transition from segmented public to single-payer-public-provider model under UHI Law 2018.

## 9. Acronym glossary

- **EDA** — Egyptian Drug Authority.
- **GAHC** — General Authority for Health Care (public provider under UHI Law).
- **MoHP** — Ministry of Health and Population.
- **UHI** — Universal Health Insurance Law (2018).
- **UHIA** — Universal Health Insurance Authority (single payer).
- **UPA** — Egyptian Authority for Unified Procurement, Medical Supply and Health Technology Management.

## 10. Worked example

```yaml
      - Dr. Khaled Abdel Ghaffar:
          - Title: Minister of Health and Population and Deputy Prime Minister of Egypt (continuing after 4 February 2026 cabinet reshuffle)
          - Stakeholder engagement notes:
              - "Minister of Health and Population and Deputy Prime Minister of Egypt; continued in role after the 4 February 2026 cabinet reshuffle (Egypt Today); previously Minister of Higher Education and Scientific Research before transferring to Health; oral-and-dental-medicine academic; widely regarded as one of Egypt's leading academic figures in his field."
              - "Public lines 2026: state targets raising healthy life expectancy to 75 years by 2030; called for stronger local drug manufacturing (Daily News Egypt, May 2026); reported on Egypt's 'red zones' shrinking and the birth rate decline as part of public-health success indicators."
              - "Owns MoHP policy and the Universal Health Insurance Law implementation (since 2018; phased rollout starting with Port Said, Luxor, others); UHIA contracting; EDA medicines regulation; UPA unified-procurement reforms; GAHC public provider build-out; the Cancer-Free Egypt initiative; presidential Decent Life initiative health components; and Egypt's WHO EMRO, AU, BRICS+ health diplomacy."
              - "Hook: UHI rollout governorate-by-governorate, local pharmaceutical manufacturing and EDA fast-track, oncology and chronic-disease national programmes, maternal-and-child mortality reduction, Cancer-Free Egypt, Decent Life and digital-health (My Health) land."
          - Tone advice:
              - "Open with UHI rollout, local pharmaceutical manufacturing, Cancer-Free Egypt and Decent Life — these are the strategic priorities and his sustained public lines."
              - "Do not assume that the entire country has migrated to UHI — the rollout is governorate-phased; pitches must align with the specific phase of the targeted geography."
```

## 11. Out-of-band notes

For roles unfilled or in transition.

## 12. Open questions

- Named Deputy Ministers of Health and Population under Abdel Ghaffar with currency verified.
- Head UHIA, Head EDA, Head UPA, Head GAHC with currency verified.
- Head Central Administration for Preventive Affairs with currency verified.
- Heads of governorate health directorates of major governorates (Cairo, Alexandria, Giza, Qalyubia, Daqahlia, Sharqia, Beheira).
- Chair House of Representatives Health Committee and Chair Senate Health Committee in the current parliamentary cycle.
- Heads of Egyptian Medical Syndicate, Egyptian Pharmacist Syndicate, Egyptian Nurses Syndicate with currency verified.
