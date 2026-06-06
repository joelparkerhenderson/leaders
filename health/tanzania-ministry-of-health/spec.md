# spec.md — `leaders.yml`

Single source of truth for the Tanzanian health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Ministry of Health (Wizara ya Afya), President's Office Regional Administration and Local Government (PORALG) which oversees primary care, Tanzania Medicines and Medical Devices Authority (TMDA), Tanzania Food and Drugs Authority successor TMDA, Muhimbili National Hospital and other Referral Hospitals, and adjacent bodies.

The Tanzanian system has tax-funded universal access through MoH and PORALG networks; the iCHF community-based insurance and the National Health Insurance Fund (NHIF) provide insurance options; Tanzania Mainland and Zanzibar have distinct administrations. The post-2025-election Hassan cabinet (announced 17 November 2025) reorganised ministerial portfolios.

## 2. Scope

In scope: President; PM; Minister of Health; Deputy Minister; Permanent Secretary MoH; Permanent Secretary PORALG; Director-General TMDA; Director-General NHIF; CEO Muhimbili National Hospital, KCMC Moshi, Bugando Medical Centre, Mbeya Zonal Referral Hospital; Zanzibar Minister of Health; Tanzania National Assembly Health and Social Welfare Committee; Medical Association of Tanzania.

## 3. Structure

Standard. Ordering: President → PM → MoH → PORALG → TMDA → NHIF → Referral Hospitals → Zanzibar → Parliament Committee → MAT.

## 4. Field definitions

Party affiliation: `CCM` (Chama Cha Mapinduzi — dominant), `CHADEMA`, `ACT-Wazalendo`, `CUF`. Titles in English / Kiswahili.

## 5. Provenance and dating

Mohamed Mchengerwa took office as Minister of Health on 17 November 2025 after President Samia Suluhu Hassan's post-election cabinet reshuffle (following CCM landslide win at 29 October 2025 election); replaced Jenista Mhagama (who was dropped and subsequently died 11 December 2025); 46 years old; MP for Rufiji Constituency in Pwani Region; CCM; relation as son-in-law of President Hassan reported in international press.

## 6. Update workflow

Verify against moh.go.tz, ikulu.go.tz, parliament.go.tz, Daily News Tanzania, The Citizen, Mwananchi, The Guardian Tanzania, EastAfrican, Africanews.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating MoH as only operational owner — PORALG holds primary-care delivery operationally; Zanzibar has separate Ministry.
- Importing US framings — Tanzania has mixed financing with strong donor coordination.

## 9. Acronym glossary

- **iCHF** — improved Community Health Fund.
- **NHIF** — National Health Insurance Fund.
- **PORALG** — President's Office Regional Administration and Local Government.
- **TMDA** — Tanzania Medicines and Medical Devices Authority.

## 10. Worked example

```yaml
      - Hon. Mohamed Mchengerwa (CCM):
          - Title: Minister of Health, United Republic of Tanzania (since 17 November 2025)
          - Stakeholder engagement notes:
              - "Minister of Health since 17 November 2025 in President Samia Suluhu Hassan's post-election Cabinet reshuffle following the 29 October 2025 General Election that returned CCM with a landslide majority; CCM; 46 years old; MP for Rufiji Constituency in the Pwani Region; replaced Jenista Mhagama who was dropped from Cabinet in the reshuffle and subsequently died on 11 December 2025."
              - "Family connection reported in international press: son-in-law of President Hassan — politically distinctive context."
              - "Inherits the 2025/26 Health Budget priorities: 28,000 health workers recruitment, 9 referral hospitals investment, AI investment, local drug and ARV manufacturing, amid donor-policy shifts (per TanzaniaInvest coverage); ongoing engagement with international medical tourism positioning."
              - "Owns Ministry policy, coordination with PORALG on primary-care delivery, TMDA medicines regulation, NHIF and iCHF insurance reform, referral hospital network (Muhimbili, KCMC, Bugando, Mbeya), and Tanzania's WHO Africa and SADC health positioning; coordination with Zanzibar Ministry of Health."
              - "Hook: 28,000 health-worker recruitment, referral hospital investment, ARV local manufacturing, AI in health, NHIF reform, mpox and outbreak preparedness, post-donor-shift self-reliance, and SADC cooperation land."
          - Tone advice:
              - "Open with health-worker recruitment, referral hospital investment, NHIF reform and SADC cooperation — these are the 2025/26 budget priorities."
              - "Do not assume single-actor framing — PORALG holds primary-care delivery operationally; framings must include PORALG-level partners."
```

## 11. Out-of-band notes

For roles unfilled or in transition.

## 12. Open questions

- Named Deputy Minister of Health under Mchengerwa with currency verified.
- Permanent Secretary MoH and Permanent Secretary PORALG under the new arrangements with currency verified.
- Director-General TMDA, Director-General NHIF with currency verified.
- CEOs of Muhimbili National Hospital, KCMC Moshi, Bugando Medical Centre, Mbeya Zonal Referral Hospital with currency verified.
- Zanzibar Minister of Health with currency verified.
- National Assembly Health and Social Welfare Committee Chair with currency verified.
- President Medical Association of Tanzania with currency verified.
