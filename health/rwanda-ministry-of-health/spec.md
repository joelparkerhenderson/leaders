# spec.md — `leaders.yml`

Single source of truth for the Rwandan health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Rwanda Ministry of Health, Rwanda Biomedical Centre (RBC), Rwanda Food and Drugs Authority (Rwanda FDA), Mutuelles de Santé / Community-Based Health Insurance (CBHI), Rwanda Social Security Board (RSSB) health, and adjacent bodies.

The Rwandan system has near-universal coverage through Mutuelles de Santé / CBHI administered by RSSB; the Ministry sets policy and RBC operates national programmes; 30 district hospitals plus national referral facilities provide care. Rwanda is internationally recognised for its health-system reforms.

## 2. Scope

In scope: President; PM; Minister of Health; Permanent Secretary; DG RBC; DG Rwanda FDA; DG RSSB; CEOs of CHUK, CHUB, King Faisal, Rwanda Military Hospital; Parliament Committee on Social Affairs; Rwanda Medical and Dental Council.

## 3. Structure

Standard. Ordering: President → PM → Ministry → RBC → Rwanda FDA → RSSB → CHUK/CHUB/KFH/RMH → Parliament Committee → RMDC.

## 4. Field definitions

Party affiliation: `RPF` (Rwandan Patriotic Front — Kagame). Titles in English with Kinyarwanda.

## 5. Provenance and dating

Dr. Sabin Nsanzimana has served as Minister of Health since November 2022; epidemiologist; PhD Epidemiology Basel; ex-DG Rwanda Biomedical Centre; ex-Director University Teaching Hospital Butare; re-elected Co-Chair Pandemic Fund Board; TIME100 Health 2026 honouree; 230+ scientific publications.

## 6. Update workflow

Verify against moh.gov.rw, gov.rw, parliament.gov.rw, RBC.gov.rw, KT Press, New Times Rwanda, IGIHE.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Importing US framings — Rwanda is universal-coverage through CBHI / Mutuelles with a highly centralised state-management model.

## 9. Acronym glossary

- **CBHI** — Community-Based Health Insurance.
- **CHUK / CHUB** — Centre Hospitalier Universitaire de Kigali / Butare.
- **RBC** — Rwanda Biomedical Centre.
- **RSSB** — Rwanda Social Security Board.

## 10. Worked example

```yaml
      - Dr. Sabin Nsanzimana (RPF):
          - Title: Minister of Health of the Republic of Rwanda (since November 2022)
          - Stakeholder engagement notes:
              - "Minister of Health since November 2022 in the Kagame government; epidemiologist; PhD Epidemiology University of Basel; previously led the Rwanda Biomedical Centre, the University Teaching Hospital of Butare, and Rwanda's national HIV and hepatitis programmes; 230+ scientific publications."
              - "Re-elected Co-Chair of the Pandemic Fund Board (RBC SPPROHRWANDA); named to TIME100 Health 2026 — international recognition of his leadership."
              - "Active 2026: reassured Rwandans as Ebola cases rise in neighbouring countries (IGIHE); led the 3rd annual Health Research & Policy Conference; addressed Marburg virus 2024 outbreak legacy."
              - "Owns Ministry policy, RBC operational programmes, Rwanda FDA medicines regulation, RSSB CBHI / Mutuelles administration, the 30 district hospitals plus King Faisal, CHUK, CHUB, RMH referral network, and Rwanda's WHO Africa, AU CDC, EAC and Commonwealth health diplomacy."
              - "Hook: CBHI / Mutuelles refinement, AU CDC and pandemic preparedness, Ebola / Marburg / mpox preparedness, BioNTech Africa mRNA hub Kigali, Rwanda Cancer Centre and oncology national programme, AU CDC leadership cooperation land."
          - Tone advice:
              - "Open with CBHI, AU CDC pandemic preparedness, BioNTech Africa mRNA hub Kigali and Rwanda Cancer Centre — these are his sustained 2022-2026 priorities and his international research-profile assets."
              - "Do not pitch as if Rwanda were donor-dependent — Rwanda's self-reliance framing under Kagame is structural; pitches must respect Rwandan ownership of strategic decisions."
```

## 11. Out-of-band notes

For roles unfilled or in transition.

## 12. Open questions

- Named Permanent Secretary, DG RBC (post-Nsanzimana), DG Rwanda FDA, DG RSSB with currency verified.
- CEOs of CHUK Kigali, CHUB Butare, King Faisal, Rwanda Military Hospital with currency verified.
- Parliament Committee on Social Affairs Chair with currency verified.
- President Rwanda Medical and Dental Council with currency verified.
