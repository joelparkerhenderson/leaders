# spec.md — `leaders.yml`

Single source of truth for the structure, semantics, and update rules of `leaders.yml` for the Republic of Korea (South Korea) health system. The YAML must conform to this spec; if they disagree, the spec wins and the YAML is fixed.

## 1. Purpose

`leaders.yml` is an engagement register of named individuals in and around the Korean health system. Each entry helps a reader inside the Ministry of Health and Welfare (Bogeonbokjibu / 보건복지부), Korea Disease Control and Prevention Agency (KDCA / 질병관리청), National Health Insurance Service (NHIS / 국민건강보험공단), Health Insurance Review and Assessment Service (HIRA / 건강보험심사평가원), Ministry of Food and Drug Safety (MFDS / 식품의약품안전처), or an adjacent body decide who to engage, how, and where.

The Korean system is single-payer National Health Insurance (NHI) financed through wage-based contributions and general subsidies, administered by NHIS. HIRA reviews and prices claims. MOHW sets policy; KDCA handles infectious disease and public health (post-2020 elevation from the former KCDC). MFDS regulates medicines and devices. The 2024 doctor-strike crisis around medical-school admission expansions reshaped political dynamics around medical workforce policy.

## 2. Scope

**In scope:** Daetongnyeong (President); Gukmuchongri (Prime Minister); Bogeonbokji Buchangwan (Minister of Health and Welfare); Cha-gwan (Vice Ministers); Cheongjang KDCA (Commissioner KDCA); Cheojang MFDS (Commissioner MFDS); Wonjang NHIS; Wonjang HIRA; Wonjang KIHASA (Korea Institute for Health and Social Affairs); Wonjang National Medical Center; Chair NAS Standing Committee on Health and Welfare; Chair Korean Medical Association (KMA / 대한의사협회); Chair Korean Hospital Association (KHA); Chair Korean Nurses Association (KNA); Chair Korean Pharmaceutical Association (KPA).

**Out of scope:** operational staff below kwanjang (director-general) level; vendors; historical post-holders.

## 3. Structure

```
대한민국 보건의료 이해관계자 / Republic of Korea health stakeholders:
  - {Organisation}:
      - {Person}:
          - Title: ...
          - Stakeholder engagement notes: [...]
          - Tone advice: [...]
```

Indentation 2/6/10/14 spaces. Ordering: Cheongwadae → MOHW → KDCA → MFDS → NHIS → HIRA → KIHASA → National Medical Center → KMA/KHA/KNA/KPA → NAS Standing Committee.

## 4. Field definitions

Standard family conventions. Party affiliation using canonical Korean abbreviations: `Minjudang` (더불어민주당, Democratic Party of Korea), `Gukmin-ui Him` (국민의힘, People Power Party), `Saemiraedang` (Future Party), `Jeong-uidang` (Justice Party), `Saerounmiraedang` (Rebuilding Korea Party), `Sangsik`, etc. Titles in English with Korean (Hangul) where useful; person names in family-name-first order following Korean convention.

## 5. Provenance and dating

Anchor facts to year, month or exact date. Following the December 2024 martial-law / impeachment cycle that ended Yoon Suk-yeol's presidency and the subsequent presidential election in 2025, the Korean political landscape underwent significant change. Jeong Eun-kyeong (Chung Eun-kyung) — the former KDCA Commissioner who led the Covid-19 response — became Minister of Health and Welfare in 2026 (delivered the 2026 New Year's Address as Minister).

## 6. Update workflow

1. Identify the change. 2. Verify against korea.kr, mohw.go.kr, kdca.go.kr, nhis.or.kr, hira.or.kr, mfds.go.kr, assembly.go.kr, Yonhap, Hankyoreh, Chosun Ilbo, JoongAng Ilbo, Korea Times, Korea Herald, Korea Biomedical Review. 3. Apply minimum diff. 4. Confirm structure. 5. Re-validate cross-references.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating NHIS as a Ministry sub-unit — NHIS is the single payer with autonomous statutory authority over benefit administration.
- Importing NHS or US framings unmodified — Korea is single-payer NHI with universal coverage, predominantly private providers, fee-for-service with HIRA review, and a distinct medical-workforce political economy.

## 9. Acronym glossary

- **HIRA / 건강보험심사평가원** — Health Insurance Review and Assessment Service.
- **KDCA / 질병관리청** — Korea Disease Control and Prevention Agency.
- **KHA / 대한병원협회** — Korean Hospital Association.
- **KIHASA / 한국보건사회연구원** — Korea Institute for Health and Social Affairs.
- **KMA / 대한의사협회** — Korean Medical Association.
- **KNA / 대한간호협회** — Korean Nurses Association.
- **KPA / 대한약사회** — Korean Pharmaceutical Association.
- **MFDS / 식품의약품안전처** — Ministry of Food and Drug Safety.
- **MOHW / 보건복지부** — Ministry of Health and Welfare.
- **NHIS / 국민건강보험공단** — National Health Insurance Service.

## 10. Worked example

```yaml
      - Jeong Eun-kyeong / 정은경 (party affiliation to verify):
          - Title: Minister of Health and Welfare (보건복지부 장관 Bogeonbokji Buchangwan) (in office in 2026)
          - Stakeholder engagement notes:
              - "Minister of Health and Welfare in 2026, having delivered the '2026 New Year's Address as Minister of Health and Welfare' in early January 2026; nationally recognised public-health figure as the former Commissioner of KDCA (then KCDC) who led the South Korean Covid-19 response 2020-2022."
              - "Public-health physician by background; KDCA Commissioner credibility translates into unusual institutional capital at MOHW — particularly on infectious-disease preparedness, vaccination, and public-health workforce policy."
              - "Public mandate priorities for 2026: expanding regional and essential healthcare reforms (Korea Biomedical Review January 2026); strengthening state responsibility for care, particularly essential medical specialties (Seoul Economic Daily); managing the post-2024 doctor-strike workforce settlement."
              - "Hook: regional essential medical-care, pediatrics and emergency-medicine workforce, infectious-disease preparedness, NHI benefit reform, drug pricing, dementia and ageing care, and digital health (My Health Way) land."
          - Tone advice:
              - "Open with regional essential healthcare, infectious-disease preparedness, public-health workforce and the post-doctor-strike settlement — these are her authored priorities and the political flashpoints of the 2024-2026 cycle."
              - "Do not propose framings that bypass NHIS as the single payer — Korea's NHI is the structural axis and pitches that assume direct MOHW commissioning will be redirected."
```

## 11. Out-of-band notes

For roles unfilled or interim.

## 12. Open questions

- Confirm Jeong Eun-kyeong's exact swearing-in date and party affiliation in the post-Yoon presidency configuration.
- Named Vice Ministers (1st and 2nd) under Jeong with currency verified.
- Cheongjang KDCA, Cheojang MFDS, Wonjang NHIS, Wonjang HIRA, Wonjang KIHASA with currency verified.
- Wonjang National Medical Center with currency verified.
- Chair NAS Standing Committee on Health and Welfare in the current National Assembly.
- Chair KMA, KHA, KNA, KPA with currency verified following the 2024-2026 medical-workforce political cycle.
