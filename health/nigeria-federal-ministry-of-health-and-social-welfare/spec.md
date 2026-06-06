# spec.md — `leaders.yml`

Single source of truth for the Nigerian health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Federal Ministry of Health and Social Welfare, NPHCDA, NAFDAC, NCDC, FMC and Federal teaching hospitals, the National Health Insurance Authority (NHIA), 36 State Ministries of Health plus FCT, and adjacent bodies.

Nigeria operates a tri-level system: federal sets policy and funds federal teaching/specialist hospitals; states own state hospitals and state primary healthcare boards; local governments run primary healthcare centres. The NHIA is the federal mandatory-insurance authority; State Health Insurance Schemes are being established under the 2022 NHI Act.

## 2. Scope

In scope: President; Vice-President; Coordinating Minister of Health and Social Welfare; Minister of State for Health; Permanent Secretary; DG NPHCDA; DG NAFDAC; DG NCDC; CEO NHIA; CMDs of major federal teaching hospitals (LUTH Lagos, UCH Ibadan, UNTH Enugu, ABUTH Zaria, NHA Abuja); State Commissioners for Health for the largest states (Lagos, Kano, Rivers, Kaduna, Oyo, Anambra, FCT); Chair Senate Committee on Health; Chair House Committee on Healthcare Services; NMA, NANNM, PSN, MDCN, PCN.

## 3. Structure

Standard 2/6/10/14. Ordering: Federal Government → MoHSW → NPHCDA → NAFDAC → NCDC → NHIA → Federal hospitals → State Ministries → Parliament committees → professional bodies.

## 4. Field definitions

Party affiliation: `APC` (All Progressives Congress — Tinubu), `PDP` (People's Democratic Party), `LP` (Labour Party), `NNPP` (New Nigeria Peoples Party), `APGA`, `ADC`, `SDP`. Titles in English.

## 5. Provenance and dating

Prof. Muhammad Ali Pate was appointed Coordinating Minister of Health and Social Welfare by President Bola Ahmed Tinubu in August 2023; Iziaq Adekunle Salako serves as Minister of State for Health; Daju Kachollom as Permanent Secretary. Pate previously was Minister of State for Health under Goodluck Jonathan; CEO of Gavi; senior World Bank Global Health head; Harvard professor — distinctive international-health background.

## 6. Update workflow

Verify against health.gov.ng, statehouse.gov.ng, nphcda.gov.ng, nafdac.gov.ng, ncdc.gov.ng, nhia.gov.ng, Vanguard, Premium Times, This Day, The Guardian Nigeria, Daily Trust, Punch.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating the federal MoHSW as the operational owner — states own state hospitals; LGAs own primary health centres.
- Importing US framings unmodified — Nigeria has mandatory insurance under the 2022 NHI Act with state-level implementation variability.

## 9. Acronym glossary

- **CMD** — Chief Medical Director.
- **LUTH** — Lagos University Teaching Hospital.
- **MDCN** — Medical and Dental Council of Nigeria.
- **NAFDAC** — National Agency for Food and Drug Administration and Control.
- **NANNM** — National Association of Nigerian Nurses and Midwives.
- **NCDC** — Nigeria Centre for Disease Control and Prevention.
- **NHIA** — National Health Insurance Authority.
- **NMA** — Nigerian Medical Association.
- **NPHCDA** — National Primary Health Care Development Agency.
- **PSN** — Pharmaceutical Society of Nigeria.

## 10. Worked example

```yaml
      - Prof. Muhammad Ali Pate (APC-affiliated technocrat):
          - Title: Coordinating Minister of Health and Social Welfare (since August 2023)
          - Stakeholder engagement notes:
              - "Coordinating Minister of Health and Social Welfare since August 2023, appointed by President Bola Ahmed Tinubu; previously Minister of State for Health under President Goodluck Jonathan 2011-2013; CEO of Gavi the Vaccine Alliance 2019-2021; Director, Global Health at the World Bank Group; professor at Harvard T.H. Chan School of Public Health — distinctive international-health background among Nigerian ministers."
              - "Iziaq Adekunle Salako serves as Minister of State for Health; Daju Kachollom is Permanent Secretary — administrative team configuration."
              - "January 2026: addressed National Traditional and Religious Leaders Summit on Health 'Crowning the Compact' at the Banquet Hall, Aso Rock Villa; March 2026: federal government to inject additional $346 million into HIV, TB and malaria programmes; introduced new long-acting HIV-prevention injection (WHO Africa coverage)."
              - "Owns the Nigeria Health Sector Renewal Investment Initiative (the Compact); NHIA implementation; PHC strengthening via NPHCDA; vaccination programmes; the local pharmaceutical manufacturing roadmap (Presidential Initiative for Unlocking the Healthcare Value Chain); response to insecurity-driven displacement health and humanitarian portfolios."
              - "Hook: NHIA implementation, PHC strengthening, local pharmaceutical manufacturing, HIV/TB/malaria co-financing, mpox and outbreak preparedness, vaccine self-reliance, climate-and-health, and reduced reliance on foreign aid land."
          - Tone advice:
              - "Open with the Compact (Health Sector Renewal Investment Initiative), local pharma manufacturing, NHIA, PHC strengthening and Tinubu-era self-reliance framing — these are Pate's sustained, internationally-credible public lines."
              - "Do not pitch as if the federal level were the operational buyer — states own state hospitals and have autonomous Commissioners for Health; framings that bypass States will be redirected."
```

## 11. Out-of-band notes

For roles unfilled or in transition.

## 12. Open questions

- DG NPHCDA, NAFDAC, NCDC, CEO NHIA with currency verified.
- CMDs of LUTH, UCH Ibadan, UNTH Enugu, ABUTH Zaria, National Hospital Abuja with currency verified.
- State Commissioners for Health for Lagos, Kano, Rivers, Kaduna, Oyo, Anambra, FCT with currency verified.
- Chair Senate Committee on Health and Chair House Committee on Healthcare Services in the current 10th National Assembly.
- President NMA, NANNM, PSN, MDCN, PCN with currency verified.
