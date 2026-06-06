# spec.md — `leaders.yml`

Single source of truth for the Bangladeshi health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Bangladesh Ministry of Health and Family Welfare (MoHFW), Directorate General of Health Services (DGHS), Directorate General of Family Planning (DGFP), Directorate General of Drug Administration (DGDA), and adjacent bodies.

The Bangladeshi system is government-led with the MoHFW running the public health network through district-level facilities, Upazila Health Complexes, Union Sub-Centres, and Community Clinics. The 2024 interim government led by Chief Adviser Muhammad Yunus replaced the Sheikh Hasina era after the August 2024 student-led uprising; an Adviser of Health serves the equivalent ministerial function.

## 2. Scope

In scope: Chief Adviser; Health and Family Welfare Adviser; Senior Secretary Health Services Division; Senior Secretary Medical Education and Family Welfare Division; Director General DGHS; Director General DGFP; Director General DGDA; Director Institute of Epidemiology, Disease Control and Research (IEDCR); Directors of major medical college hospitals (Dhaka Medical, Bangabandhu Sheikh Mujib Medical University, Chattogram Medical, Rajshahi Medical); Parliament Standing Committee on MoHFW (when restored); Bangladesh Medical Association; Bangladesh Nursing and Midwifery Council.

## 3. Structure

Standard 2/6/10/14. Ordering: Chief Adviser's office → MoHFW (Health Services Division and Medical Education / Family Welfare Division) → DGHS → DGFP → DGDA → IEDCR → medical college hospitals → professional bodies → Parliament when restored.

## 4. Field definitions

Party affiliation note: the 2024 interim government is non-partisan / technocratic. Pre-2024 party affiliations: `AL` (Awami League), `BNP` (Bangladesh Nationalist Party), `JI` (Jamaat-e-Islami), `JP` (Jatiya Party). Titles in English with Bengali where used officially.

## 5. Provenance and dating

Nurjahan Begum has served as Adviser for Health and Family Welfare in the Muhammad Yunus interim government since August 2024 — the equivalent role to Minister of Health in the previous Hasina government (where Samanta Lal Sen had been Minister). The interim government is preparing for general elections; a referendum is also anticipated.

## 6. Update workflow

Verify against mohfw.gov.bd, cabinet.gov.bd, dghs.gov.bd, dgda.gov.bd, parliament.gov.bd, Daily Star, Prothom Alo, BSS, BD News24, New Age, Business Standard, Bangla Tribune.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating MoHFW as the only stakeholder — Bangladesh's NGO sector (BRAC, Grameen Kalyan, icddr,b) operates parallel large-scale health programmes.
- Importing NHS framings unmodified — Bangladesh is a low-middle-income country with high out-of-pocket spending (>60%) and predominantly public delivery for the lowest tiers.

## 9. Acronym glossary

- **BSMMU** — Bangabandhu Sheikh Mujib Medical University.
- **DGDA** — Directorate General of Drug Administration.
- **DGFP** — Directorate General of Family Planning.
- **DGHS** — Directorate General of Health Services.
- **icddr,b** — International Centre for Diarrhoeal Disease Research, Bangladesh.
- **IEDCR** — Institute of Epidemiology, Disease Control and Research.
- **MoHFW** — Ministry of Health and Family Welfare.

## 10. Worked example

```yaml
      - Nurjahan Begum (interim government appointee):
          - Title: Adviser for Health and Family Welfare (equivalent to Minister of Health) (since August 2024, in the Muhammad Yunus interim government)
          - Stakeholder engagement notes:
              - "Adviser for Health and Family Welfare in the Muhammad Yunus interim government since August 2024 — equivalent to the role of Minister of Health in the previous Sheikh Hasina Awami League government (where Samanta Lal Sen held the post until the August 2024 uprising); appointment as 'Adviser' reflects the interim-government structure."
              - "Public-policy lines 2026: urged doctors to refrain from political involvement and prioritise healthcare duties; participated as Chief Guest in national stakeholder consultations for landmark tobacco-control legislative reform; commented on the upcoming referendum and elections process."
              - "Owns federal coordination of public-health programmes through DGHS, DGFP and DGDA; oversees IEDCR; chairs national health-security committee; manages the MoHFW budget through both the Health Services Division and the Medical Education and Family Welfare Division."
              - "Hook: tobacco control (landmark 2026 legislation), maternal and neonatal mortality, dengue, cholera (icddr,b research base), primary care and community-clinic strengthening, BSMMU and tertiary-network reform, dengue and climate-health land."
          - Tone advice:
              - "Open with tobacco control, maternal and child health, dengue and climate health, and primary-care strengthening — these are her authored 2026 public lines."
              - "Do not assume political continuity beyond the interim transition — the political environment is fluid (referendum, election prospect); long-term commitments will be filtered."
```

## 11. Out-of-band notes

For roles unfilled or interim.

## 12. Open questions

- Identify the date of any post-election Minister of Health if the political transition completes during 2026.
- Senior Secretary Health Services Division and Senior Secretary Medical Education and Family Welfare Division under the interim government with currency verified.
- Director General DGHS, DGFP, DGDA, and Director IEDCR with currency verified.
- Directors of major medical college hospitals (Dhaka Medical, BSMMU, Chattogram Medical, Rajshahi Medical) with currency verified.
- Standing Committee Chair on MoHFW after Parliament is restored.
- President Bangladesh Medical Association, Bangladesh Nursing and Midwifery Council with currency verified.
