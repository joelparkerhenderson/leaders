# spec.md — `leaders.yml`

Single source of truth for the Omani health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Omani Ministry of Health (وزارة الصحة), Sultan Qaboos University Hospital (SQUH), Oman Medical Specialty Board (OMSB), Royal Hospital, and adjacent bodies.

The Omani system delivers universal coverage for citizens free at point of use through MoH public hospitals, polyclinics and primary health centres; expatriate medical care is mostly private and insurance-financed. Vision 2040 frames national reform; the Health Care Management and Regulation Committee oversees regulatory development.

## 2. Scope

In scope: Sultan Haitham bin Tariq; Deputy PM; Minister of Health; Undersecretary; CEO Royal Hospital; CEO SQUH; CEO Khoula Hospital; CEO Al Nahdha Hospital; Executive President OMSB; CEO Oman Medical Association; Director-General Primary Healthcare; Health Affairs Director-Generals of major Governorates (Muscat, Dhofar, Al Batinah, Al Dakhiliyah); Health Care Management and Regulation Committee Chair; State Council Health Committee Chair; Majlis Al-Shura Health Committee Chair.

## 3. Structure

Standard. Ordering: Sultan → PM Office → MoH → Royal Hospital → SQUH → other hospitals → OMSB → Health Care Management Regulation Committee → Majlis Al-Shura / State Council → Oman Medical Association.

## 4. Field definitions

Oman does not have political parties. Titles in English; H.E. for Ministers.

## 5. Provenance and dating

H.E. Dr. Hilal bin Ali bin Hilal Al Sabti has served as Minister of Health since 16 June 2022 following a Royal Decree by HM Sultan Haitham bin Tariq; cardiothoracic surgeon; previously Senior Consultant Cardiothoracic Surgeon at SQUH; Executive President of the Oman Medical Specialty Board (OMSB) from May 2015 until ministerial appointment.

## 6. Update workflow

Verify against moh.gov.om, gov.om, omannews.gov.om, Times of Oman, Oman Observer, OERLive, MededgeMEA.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating MoH as the only provider — SQUH is independently operated under the Sultan Qaboos University (Diwan of Royal Court oversight), Royal Hospital under MoH but with its own governance.
- Importing US framings unmodified — Oman is tax-funded universal for citizens with significant private sector for expatriates.

## 9. Acronym glossary

- **MoH** — Ministry of Health.
- **OMSB** — Oman Medical Specialty Board.
- **SQUH** — Sultan Qaboos University Hospital.

## 10. Worked example

```yaml
      - H.E. Dr. Hilal bin Ali bin Hilal Al Sabti:
          - Title: Minister of Health of the Sultanate of Oman (since 16 June 2022)
          - Stakeholder engagement notes:
              - "Minister of Health since 16 June 2022 by Royal Decree of HM Sultan Haitham bin Tariq; cardiothoracic surgeon; Senior Consultant Cardiothoracic Surgeon at Sultan Qaboos University Hospital (SQUH); Executive President of the Oman Medical Specialty Board (OMSB) from May 2015 until ministerial appointment; aged 49 at appointment — clinical-academic credibility unusual for the political appointments tradition."
              - "Active 2026: Health Care Management and Regulation Committee held first meeting of 2026 (Times of Oman February 2026); welcomed Dr Hanan Balkhy, WHO EMRO Regional Director, at MoH (WHO Oman Office); led high-level meetings on health-sector boost (MededgeMEA)."
              - "Owns MoH policy and budget, public hospital network, primary health centre programme, OMSB residency / training continuity, SQUH coordination, Royal Hospital governance, Vision 2040 health-sector implementation, and Oman's WHO EMRO, GCC and Indian Ocean Rim health diplomacy."
              - "Hook: Vision 2040 health implementation, cardiothoracic and oncology specialist programmes (his clinical specialty), primary-care strengthening, healthtech and AI, OMSB residency expansion, regional GCC health cooperation, and WHO EMRO partnership land."
          - Tone advice:
              - "Open with Vision 2040 implementation, cardiothoracic / oncology specialist programmes, OMSB residency, primary care and GCC cooperation — these are his sustained authored 2022-2026 lines and clinical-academic frame."
              - "Do not pitch as if SQUH were under direct MoH control — SQUH operates under Sultan Qaboos University governance; pitches involving SQUH must include the SQU and Diwan of the Royal Court."
```

## 11. Out-of-band notes

For roles unfilled or in transition.

## 12. Open questions

- Named Undersecretary MoH under Al Sabti with currency verified.
- CEO Royal Hospital, CEO SQUH, CEO Khoula Hospital, CEO Al Nahdha Hospital with currency verified.
- Executive President OMSB after Al Sabti's move to the ministerial role.
- Director-General Primary Healthcare and Governorate Health Affairs DGs for Muscat, Dhofar, Al Batinah, Al Dakhiliyah.
- Chair Health Care Management and Regulation Committee with currency verified.
- Chairs of State Council and Majlis Al-Shura Health Committees with currency verified.
