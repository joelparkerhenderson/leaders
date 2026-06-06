# spec.md — `leaders.yml`

Single source of truth for the Bahraini health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Bahrain Ministry of Health (وزارة الصحة), Supreme Council of Health (SCH), National Health Regulatory Authority (NHRA), Salmaniya Medical Complex (SMC), Bahrain Defence Force Royal Medical Services, and adjacent bodies.

The Bahraini system provides universal coverage for citizens free at point of use through MoH facilities; expatriates have separate insurance under the Sehati / mandatory health insurance reform underway. NHRA regulates; the SCH coordinates strategy.

## 2. Scope

In scope: King; Crown Prince and PM; Minister of Health; Undersecretary; CEO Supreme Council of Health; CEO NHRA; CEO Salmaniya Medical Complex; CEO King Hamad University Hospital; Director Primary Health Care; Parliamentary Council of Representatives Health, Environment and Population Committee Chair; Bahrain Medical Society.

## 3. Structure

Standard 2/6/10/14. Ordering: Royal Court → PM → MoH → SCH → NHRA → SMC → KHUH → Parliament Health Committee → Bahrain Medical Society.

## 4. Field definitions

Bahrain does not have political parties. Titles in English; H.E. for Ministers.

## 5. Provenance and dating

Dr. Jaleela bint Sayed Jawad Hassan has served as Minister of Health since June 2022; medical doctor; active 2026 on Bahrainisation of primary-care workforce, sickle-cell programmes, and PM Fellowship Programme participation.

## 6. Update workflow

Verify against moh.gov.bh, pmo.gov.bh, nhra.bh, newsofbahrain.com, gulfnews.com Bahrain section, Bahrain News Agency (BNA).

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating MoH as only counterparty — NHRA regulates separately and Royal Medical Services is parallel.
- Importing US framings — Bahrain is tax-funded for citizens with mandatory insurance for expatriates rolling out.

## 9. Acronym glossary

- **KHUH** — King Hamad University Hospital.
- **MoH** — Ministry of Health.
- **NHRA** — National Health Regulatory Authority.
- **SCH** — Supreme Council of Health.
- **Sehati** — mandatory health insurance reform.
- **SMC** — Salmaniya Medical Complex.

## 10. Worked example

```yaml
      - H.E. Dr. Jaleela bint Sayed Jawad Hassan:
          - Title: Minister of Health of the Kingdom of Bahrain (since June 2022)
          - Stakeholder engagement notes:
              - "Minister of Health of Bahrain since June 2022 by Royal Decree of HM King Hamad bin Isa Al Khalifa; medical doctor; first female Minister of Health in Bahrain; recognised in international fora including Abu Dhabi Global Health Week."
              - "Active 2026: met Prime Minister's Fellowship Programme participants (January 2026); cited 100% Bahrainisation in primary care amid doctor-hiring discussion (Daily Tribune); reaffirmed commitment to youth empowerment; strengthened partnership with Bahrain Sickle Cell Society."
              - "Owns MoH policy, Sehati mandatory health insurance rollout coordination with SCH, NHRA regulation oversight, SMC public-hospital network, KHUH joint governance, primary-care strengthening, sickle-cell national programme (high prevalence in Bahrain), and Bahrain's WHO EMRO and GCC health diplomacy."
              - "Hook: Sehati mandatory insurance rollout, primary-care Bahrainisation, sickle-cell programme, SMC modernisation, KHUH centre-of-excellence model, and GCC cooperation land."
          - Tone advice:
              - "Open with Sehati rollout, sickle-cell, primary-care Bahrainisation and GCC cooperation — these are her 2026 sustained priorities."
              - "Do not assume Bahrainisation is a soft policy — workforce nationalisation in healthcare is a political priority and pitches must address it directly."
```

## 11. Out-of-band notes

For roles unfilled or in transition.

## 12. Open questions

- Named Undersecretary, CEO Supreme Council of Health, CEO NHRA, CEO SMC, CEO KHUH with currency verified.
- Director Primary Health Care with currency verified.
- Chair Council of Representatives Health, Environment and Population Committee.
- President Bahrain Medical Society with currency verified.
