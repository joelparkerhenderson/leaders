# spec.md — `leaders.yml`

Single source of truth for the Singaporean health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Singapore Ministry of Health (MOH), the three healthcare clusters (NHG, SingHealth, NUHS), Health Sciences Authority (HSA), Agency for Care Effectiveness (ACE), and adjacent bodies.

The Singaporean system is mixed: MOH steers; three regional clusters operate hospitals and primary care (Polyclinics, GPs); financing combines MediShield Life (compulsory insurance), MediSave (medical savings), CareShield Life (disability), and MediFund (safety net). Health Promotion Board leads prevention; Healthier SG (primary care registration) launched 2023 is a defining reform. HSA regulates medicines, devices, blood and transplantation.

## 2. Scope

In scope: Prime Minister; Deputy Prime Minister; Minister for Health (concurrently Coordinating Minister for Social Policies); Senior Minister of State and Ministers of State for Health; Permanent Secretary; CEO MOH Holdings; CEOs of the three clusters (NHG, SingHealth, NUHS); CEO HSA; CEO HPB; CEO ACE; CEO CPF Board (for MediShield/MediSave); Chair Government Parliamentary Committee on Health; SMC, SNB, SPC councils.

## 3. Structure

Standard 2/6/10/14. Ordering: PMO → MOH → MOH Holdings → 3 clusters (NHG, SingHealth, NUHS) → HSA → HPB → ACE → CPF Board → GPC Health → professional councils.

## 4. Field definitions

Party affiliation using canonical Singapore abbreviations: `PAP` (People's Action Party), `WP` (Workers' Party), `PSP` (Progress Singapore Party). Titles in English.

## 5. Provenance and dating

Mr Ong Ye Kung (PAP) has been Minister for Health since 2021; concurrently Coordinating Minister for Social Policies in the Lawrence Wong government formed May 2024 after Lee Hsien Loong's transition. Singapore had a general election in 2025 — Wong PAP government retained a strong majority. Ong continues as Minister for Health in the Wong cabinet.

## 6. Update workflow

Verify against moh.gov.sg, pmo.gov.sg, hsa.gov.sg, hpb.gov.sg, parliament.gov.sg, The Straits Times, Channel News Asia (CNA), Today, Business Times Singapore.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating MOH as the only purchaser — the three healthcare clusters and MOH Holdings together comprise the operational architecture.
- Importing US framings unmodified — Singapore is a highly distinctive 'co-payment plus compulsory savings' model that doesn't map to typical NHS / SHI / private patterns.

## 9. Acronym glossary

- **ACE** — Agency for Care Effectiveness (HTA).
- **CareShield Life** — disability insurance.
- **CPF Board** — Central Provident Fund Board.
- **GPC** — Government Parliamentary Committee.
- **Healthier SG** — primary-care registration and preventive-care initiative (2023).
- **HPB** — Health Promotion Board.
- **HSA** — Health Sciences Authority.
- **MediFund** — safety-net subsidy.
- **MediSave** — compulsory medical savings.
- **MediShield Life** — compulsory health insurance.
- **MOH** — Ministry of Health.
- **NHG** — National Healthcare Group.
- **NUHS** — National University Health System.
- **SingHealth** — Singapore Health Services.

## 10. Worked example

```yaml
      - Mr Ong Ye Kung (PAP):
          - Title: Minister for Health and Coordinating Minister for Social Policies (since 2021; retained in Wong PAP government 2024-)
          - Stakeholder engagement notes:
              - "Minister for Health since 2021 and Coordinating Minister for Social Policies in Lawrence Wong's PAP government (formed May 2024 after Lee Hsien Loong's transition; retained after the 2025 general election); PAP; previously Minister for Transport, Minister for Education and Minister for Manpower across multiple cabinets — senior PAP figure with broad portfolio experience."
              - "Active 2026: led Singapore's delegation to the 79th World Health Assembly in Geneva (May 2026); delivered Committee of Supply 2026 speech in Parliament (5 March 2026) covering MOH priorities; spoke at Singapore Health Quality Service Awards, 3rd Singapore Primary Care Conference (15 May 2026), and National Medical Research Council Awards Ceremony (22 May 2026); NHG Health Musculoskeletal Day Fiesta (28 March 2026)."
              - "Owns the implementation of Healthier SG (primary-care registration with family GPs since 2023), the three-cluster restructuring (NHG, SingHealth, NUHS), MediShield Life and CareShield Life premium policy, MOH Holdings governance, HSA regulation, HPB prevention, ACE HTA, ageing population services, the new Punggol General Hospital pipeline, the bilateral cooperation with WHO, ASEAN+3 and BRICS+ on health."
              - "Hook: Healthier SG implementation and impact, ageing population services, dementia care, MediShield Life policy, MOH Holdings governance, three-cluster reform, primary care, mental health, climate-and-health, healthtech and AI, and ASEAN cooperation land."
          - Tone advice:
              - "Open with Healthier SG, ageing, primary care, MediShield Life policy and ASEAN cooperation — these are his sustained 2021-2026 priorities and the PAP frame on health."
              - "Do not pitch as if MOH could authorise everything directly — three clusters and MOH Holdings retain operational authority; engagement on hospital programmes must include cluster CEOs."
```

## 11. Out-of-band notes

For roles unfilled or in transition.

## 12. Open questions

- Named Senior Minister of State and Ministers of State for Health under Ong with currency verified.
- Permanent Secretary MOH with currency verified.
- CEO MOH Holdings; CEOs NHG, SingHealth, NUHS with currency verified.
- CEO HSA, HPB, ACE with currency verified.
- Chair Government Parliamentary Committee on Health in the current 15th Parliament after the 2025 election.
- President SMC, SNB, SPC with currency verified.
