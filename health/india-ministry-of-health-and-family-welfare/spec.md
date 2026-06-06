# spec.md — `leaders.yml`

Single source of truth for the structure, semantics, and update rules of `leaders.yml` for the Indian Union Ministry of Health and Family Welfare (MoHFW) and the broader health system. The YAML must conform to this spec; if they disagree, the spec wins and the YAML is fixed.

## 1. Purpose

`leaders.yml` is an engagement register of named individuals in and around the Indian health system. Each entry helps a reader inside MoHFW, the Department of Health Research, the National Health Authority (NHA, runs PM-JAY / Ayushman Bharat), ICMR, AIIMS New Delhi, a state Department of Health, or an adjacent body decide who to engage, how, and where.

India's health system is constitutionally devolved — Health is a State subject under the Seventh Schedule. The Union MoHFW runs national programmes (PM-JAY / Ayushman Bharat, National Health Mission, immunisation), AIIMS hospitals and central tertiary institutes, and the regulatory ecosystem through CDSCO. Each State and Union Territory has its own Department of Health, Director of Health Services, and public-hospital network. AIIMS New Delhi and other AIIMS act as national teaching-and-research backbones. NHA administers PM-JAY (the world's largest public-funded health insurance scheme). ICMR is the apex biomedical research body.

## 2. Scope

**In scope:** Pradhan Mantri (Prime Minister); Union Minister of Health and Family Welfare; Ministers of State (MoS) for Health and Family Welfare; Secretary MoHFW (Department of Health and Family Welfare); Secretary Department of Health Research; CEO National Health Authority; Director-General ICMR; Drugs Controller General of India (CDSCO); Director AIIMS New Delhi and Directors of other AIIMS; Director General of Health Services (DGHS); Chairperson NMC (National Medical Commission); Chair Standing Committee on Health and Family Welfare (Lok Sabha and Rajya Sabha); State Health Ministers of the largest states (Uttar Pradesh, Maharashtra, Bihar, West Bengal, Madhya Pradesh, Tamil Nadu, Rajasthan, Karnataka, Gujarat, Andhra Pradesh, Telangana, Kerala); President Indian Medical Association (IMA); President Federation of Indian Chambers of Commerce and Industry (FICCI) Health Services Committee.

**Out of scope:** operational staff below Joint Secretary; vendors; historical post-holders.

## 3. Structure

```
India Ministry of Health and Family Welfare stakeholders:
  - {Organisation}:
      - {Person}:
          - Title: ...
          - Stakeholder engagement notes: [...]
          - Tone advice: [...]
```

Indentation 2/6/10/14 spaces. Ordering: Union Cabinet → MoHFW → Department of Health Research → National Health Authority → ICMR → CDSCO → AIIMS New Delhi → other AIIMS → NMC → DGHS → 12 largest states → Standing Committees → IMA / FICCI.

## 4. Field definitions

Standard family conventions. Party affiliation using canonical Indian abbreviations: `BJP`, `INC` (Indian National Congress), `JD(U)`, `JD(S)`, `TMC` (Trinamool Congress), `DMK`, `AIADMK`, `SP` (Samajwadi Party), `BSP`, `RJD`, `NCP(SP)`, `Shiv Sena`, `BJD`, `BRS`, `YSRCP`, `TDP`, `AAP`, `CPI`, `CPI(M)`. Titles in English.

## 5. Provenance and dating

Anchor facts to year, month or exact date. J. P. Nadda took dual charge of MoHFW and the Ministry of Chemicals and Fertilizers on 9 June 2024 in the Modi III government. MoS arrangements include Anupriya Patel (Apna Dal-S) and Prataprao Ganpatrao Jadhav (Shiv Sena).

## 6. Update workflow

1. Identify the change. 2. Verify against india.gov.in, mohfw.gov.in, nha.gov.in, icmr.gov.in, cdsco.gov.in, aiims.edu, pib.gov.in, sansad.in, NDTV, The Hindu, The Indian Express, Times of India, Mint, Economic Times. 3. Apply minimum diff. 4. Confirm structure. 5. Re-validate cross-references.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating the Union Ministry as the operational owner of health delivery — Health is constitutionally a State subject; the Union sets framework and runs central programmes.
- Importing NHS or US framings unmodified — India is a mixed system with strong private-sector dominance in outpatient care, PM-JAY public insurance for hospitalisation for the bottom 40%, and minimal universal coverage outside that.

## 9. Acronym glossary

- **AB-PMJAY** — Ayushman Bharat Pradhan Mantri Jan Arogya Yojana (the world's largest publicly funded health insurance scheme).
- **AIIMS** — All India Institute of Medical Sciences.
- **CDSCO** — Central Drugs Standard Control Organisation.
- **DGHS** — Directorate General of Health Services.
- **DHR** — Department of Health Research (Ministry of Health and Family Welfare).
- **ICMR** — Indian Council of Medical Research.
- **IMA** — Indian Medical Association.
- **MoHFW** — Ministry of Health and Family Welfare.
- **MoS** — Minister of State.
- **NHA** — National Health Authority.
- **NHM** — National Health Mission.
- **NMC** — National Medical Commission (replaced Medical Council of India in 2020).
- **PIB** — Press Information Bureau.
- **PMJAY** — Pradhan Mantri Jan Arogya Yojana.

## 10. Worked example

```yaml
      - Shri Jagat Prakash Nadda (BJP):
          - Title: Union Minister of Health and Family Welfare and Minister of Chemicals and Fertilizers (from 9 June 2024)
          - Stakeholder engagement notes:
              - "Union Minister of Health and Family Welfare and Minister of Chemicals and Fertilizers from 9 June 2024 in the Modi III government; BJP National President 2020-2024; previously Union Minister of Health and Family Welfare 2014-2019 in Modi I."
              - "Twin pasta: combined Health and Pharmaceuticals (Chemicals and Fertilizers) gives him the regulatory and pricing levers over a $100bn+ Indian pharma sector and over PM-JAY's public-funded insurance population (~500 million)."
              - "Launched SAHI and BODH initiatives at the India AI Impact Summit 2026 to strengthen 'responsible health AI ecosystem' — Health AI is a definitional theme of the second Nadda mandate; addressed 8th edition of 'Advantage Health Care – India 2026'."
              - "Owns the National Health Mission, Ayushman Bharat PM-JAY expansion, the post-Covid health infrastructure (PM-ABHIM), the CDSCO regulatory file, ICMR research portfolio, NMC reforms, and India's WHO-PAHO multilateral positioning."
              - "MoS team: Anupriya Patel (Apna Dal-S) and Prataprao Ganpatrao Jadhav (Shiv Sena) — coalition-balancing MoS appointments."
              - "Hook: PM-JAY expansion, Health AI (SAHI / BODH), pharma export and bulk-drug parks, medical-value-travel (Heal in India), digital public infrastructure for health (ABDM), and NMC reforms land; State-bypassing framings on delivery do not land."
          - Tone advice:
              - "Lead with PM-JAY, Health AI (SAHI/BODH), pharma export, medical-value-travel and Ayushman Bharat Digital Mission — these are Nadda's authored sustained policy lines."
              - "Do not pitch as if Union Health were operational delivery — State Health Ministers run delivery; framings must respect federal-State competence and Nadda's institutional politeness about it."
```

## 11. Out-of-band notes

For roles unfilled or interim.

## 12. Open questions

- Confirm full MoS responsibilities under Nadda in Modi III with currency verified.
- Secretary Department of Health and Family Welfare and Secretary Department of Health Research with currency verified.
- CEO National Health Authority, Director-General ICMR, Drugs Controller General of India, Director AIIMS New Delhi with currency verified.
- Chairperson National Medical Commission with currency verified.
- Chair Lok Sabha Standing Committee on Health and Family Welfare and Chair Rajya Sabha Standing Committee with currency verified.
- State Health Ministers of the 12 largest states (UP, MH, BR, WB, MP, TN, RJ, KA, GJ, AP, TS, KL) with currency verified.
- Director General of Health Services (DGHS) under MoHFW with currency verified.
- President Indian Medical Association and FICCI Health Services Committee with currency verified.
