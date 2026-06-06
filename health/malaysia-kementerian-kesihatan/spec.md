# spec.md — `leaders.yml`

Single source of truth for the Malaysian health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around Kementerian Kesihatan Malaysia (KKM, Ministry of Health), National Pharmaceutical Regulatory Agency (NPRA), Institute for Medical Research (IMR), state Jabatan Kesihatan Negeri, and adjacent bodies.

The Malaysian system is dual: a tax-funded universal public sector run by KKM with low user fees, complemented by a substantial private sector that operates in parallel and increasingly outpaces public-sector spending. State and Federal Territory Health Departments implement nationally. Universiti Malaya Medical Centre and HSAJB, HKL serve as referral backbones.

## 2. Scope

In scope: PM; Minister of Health; Deputy Minister of Health; Director-General of Health; Deputy Directors-General (Public Health; Medical; Research and Technical Support); Director NPRA; Director IMR; CEOs of Federal Hospitals (HKL, HSAJB, Hospital Pulau Pinang); State Health Directors (Selangor, Johor, Penang, Sabah, Sarawak, Kelantan, Kedah); Chair Dewan Rakyat Special Select Committee on Health; Malaysian Medical Association; Malaysian Pharmaceutical Society; Malaysian Nurses Association.

## 3. Structure

Standard 2/6/10/14. Ordering: PM Office → KKM → NPRA → IMR → Federal Hospitals → State Jabatan Kesihatan → Dewan Rakyat Committee → professional bodies.

## 4. Field definitions

Party affiliation using canonical Malaysian abbreviations: `PH` (Pakatan Harapan — Anwar coalition including PKR, DAP, AMANAH); `BN` (Barisan Nasional — UMNO et al.); `PN` (Perikatan Nasional — BERSATU, PAS); `GPS` (Gabungan Parti Sarawak); `GRS` (Gabungan Rakyat Sabah); `MUDA`. Titles in English / Bahasa Malaysia.

## 5. Provenance and dating

Dato' Dr. Dzulkefly Ahmad (PH/AMANAH) has served as Minister of Health since 12 December 2023 in the Anwar Ibrahim unity government, replacing Dr Zaliha Mustafa. Previously Minister of Health 2018-2020 under Mahathir's Pakatan Harapan government — returning to the portfolio.

## 6. Update workflow

Verify against moh.gov.my, pmo.gov.my, npra.gov.my, parliment.gov.my, The Star, New Straits Times, Free Malaysia Today, Malaysiakini, CodeBlue, The Edge Malaysia.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating KKM as the only buyer — Malaysia has a substantial parallel private hospital and clinic sector with private insurance contributors.
- Ignoring state-level health planning — particularly Sabah and Sarawak under their distinct constitutional arrangements.

## 9. Acronym glossary

- **HKL** — Hospital Kuala Lumpur.
- **HSAJB** — Hospital Sultanah Aminah Johor Bahru.
- **IMR** — Institute for Medical Research.
- **KKM** — Kementerian Kesihatan Malaysia (Ministry of Health).
- **MMC** — Malaysian Medical Council.
- **NPRA** — National Pharmaceutical Regulatory Agency.

## 10. Worked example

```yaml
      - Dato' Dr. Dzulkefly Ahmad (PH / AMANAH):
          - Title: Minister of Health (since 12 December 2023, in the Anwar Ibrahim unity government)
          - Stakeholder engagement notes:
              - "Minister of Health since 12 December 2023 in the Anwar Ibrahim Pakatan Harapan-led unity government; AMANAH; previously Minister of Health 2018-2020 under the Mahathir PH government — returning to the portfolio with institutional memory; medical doctor by training."
              - "Active 2026: marked 2026 as year for implementing health-system reforms including further digitalisation (Malaysian Business 'Know Your Minister'); expects 10% cut to Health Ministry's budget (CodeBlue, May 2026); Ministry to submit counter-proposal on budget cuts (FMT, May 2026); stated Malaysia's private healthcare spending to surpass public 'soonest' (CodeBlue, January 2026)."
              - "Owns KKM policy and budget; oversight of NPRA, IMR, MMC and KEMENTAH liaison on Defence Health; primary-care reform; hospital-based EMR rollout (HIS expansion to 16 hospitals); state-coordination via State Health Departments (Selangor, Johor, Penang, Sabah, Sarawak prominent)."
              - "Hook: budget defence and health-financing reform, private-public balance, EMR / HIS expansion, primary-care strengthening, dialysis and NCD programmes, dengue and infectious disease, climate-and-health, and ASEAN health-cooperation land."
          - Tone advice:
              - "Open with budget-defence, private-public balance, EMR / HIS expansion, primary-care reform and ASEAN cooperation — these are the live 2026 issues and his sustained authored lines."
              - "Do not assume Sabah and Sarawak align with peninsular Malaysia on health planning — under MA63 / IGC the two East Malaysian states retain distinct constitutional health-policy autonomy."
```

## 11. Out-of-band notes

For roles unfilled or in transition.

## 12. Open questions

- Named Deputy Minister of Health and Director-General of Health under Dzulkefly with currency verified.
- Director NPRA, Director IMR with currency verified.
- CEOs of HKL, HSAJB, Hospital Pulau Pinang with currency verified.
- State Health Directors for Selangor, Johor, Penang, Sabah, Sarawak, Kelantan, Kedah.
- Chair Dewan Rakyat Special Select Committee on Health in the current Parliament.
- Malaysian Medical Association, Malaysian Pharmaceutical Society, Malaysian Nurses Association presidents with currency verified.
