# spec.md — `leaders.yml`

Single source of truth for the Qatari health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Qatar Ministry of Public Health (MoPH), Hamad Medical Corporation (HMC), Primary Health Care Corporation (PHCC), Sidra Medicine, Qatar Investment Authority (QIA — for context given the new minister's background), and adjacent bodies.

The Qatari system delivers universal coverage for citizens free at point of use, with HMC running tertiary hospital services, PHCC running primary care, Sidra serving women and children, and a substantial private sector. National Health Strategy 2024-2030 frames reform.

## 2. Scope

In scope: Emir; Prime Minister; Minister of Public Health; Undersecretary; CEO HMC; CEO PHCC; CEO Sidra Medicine; CEO Qatar Red Crescent; Director Qatar Council for Healthcare Practitioners (QCHP); CEO Qatar Cancer Society; Chair Shura Council Health Committee; Qatar Medical Association.

## 3. Structure

Standard. Ordering: Emir → PM → MoPH → HMC → PHCC → Sidra → QCHP → Shura Council → QMA.

## 4. Field definitions

Qatar does not have political parties. Titles in English; H.E. for Ministers.

## 5. Provenance and dating

H.E. Mansoor bin Ebrahim bin Saad Al Mahmoud was appointed Minister of Public Health on 12 November 2024 by Emiri Decree, succeeding H.E. Dr. Hanan Mohamed Al Kuwari (who held the role 2016-2024 and now serves as Advisor to the Prime Minister for Public Health Affairs); Al Mahmoud previously served as Chief Executive Officer of Qatar Investment Authority (QIA) from September 2018 to November 2024; prior roles include CEO Qatar Museums, CEO Qatar Development Bank, and Director Investment Affairs Office for the Prime Minister and Minister of Foreign Affairs — an investment-and-finance background unusual for a health-portfolio appointee.

## 6. Update workflow

Verify against moph.gov.qa, gco.gov.qa, hamad.qa, phcc.gov.qa, sidra.org, shura.qa, Qatar Tribune, The Peninsula, Doha News, Gulf Times.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating MoPH as the operational delivery owner — HMC, PHCC and Sidra are major statutorily distinct providers.
- Importing US framings unmodified — Qatar combines universal-for-citizens public delivery, expatriate-specific private and insurance arrangements, and substantial sovereign-wealth-funded investment.

## 9. Acronym glossary

- **HMC** — Hamad Medical Corporation.
- **MoPH** — Ministry of Public Health.
- **PHCC** — Primary Health Care Corporation.
- **QCHP** — Qatar Council for Healthcare Practitioners.
- **QIA** — Qatar Investment Authority.
- **Sidra** — Sidra Medicine.

## 10. Worked example

```yaml
      - H.E. Mansoor bin Ebrahim bin Saad Al Mahmoud:
          - Title: Minister of Public Health (since 12 November 2024)
          - Stakeholder engagement notes:
              - "Minister of Public Health since 12 November 2024 by Emiri Decree, succeeding H.E. Dr. Hanan Mohamed Al Kuwari (who served 2016-2024 and now serves as Advisor to the Prime Minister for Public Health Affairs); Mansoor Al Mahmoud previously served as Chief Executive Officer of Qatar Investment Authority (QIA) from September 2018 to November 2024; prior roles include CEO Qatar Museums, CEO Qatar Development Bank, and Director Investment Affairs Office for the Prime Minister and Minister of Foreign Affairs — an investment-and-finance background unusual for a health-portfolio appointee."
              - "Active 2025-2026: announced comprehensive reforms (Qatar Tribune); leads the National Health Strategy 2024-2030 implementation; maintains the elevated international standing of MoPH in WHO Executive Board engagement initiated by Dr. Al Kuwari (Qatar Chaired the WHO Executive Board)."
              - "Owns MoPH policy and the WHO Executive Board / WHO Eastern Mediterranean engagement; HMC, PHCC and Sidra coordination; QCHP licensing; Qatar Red Crescent humanitarian-health partnership; Qatar's WHO EMRO, GCC, BRICS+ and ASEAN-GCC health diplomacy; National Health Strategy 2024-2030 implementation."
              - "Hook: National Health Strategy 2024-2030, healthtech and AI integration in HMC and Sidra, primary-care expansion via PHCC, health financing innovation, WHO multilateral diplomacy, and BRICS+ / GCC cooperation land."
          - Tone advice:
              - "Open with National Health Strategy 2024-2030, healthtech and AI, primary care, WHO multilateral and BRICS+ cooperation — these align with his investment background and Qatar's strategic-investment-in-health framing."
              - "Do not pitch as if Qatar were resource-constrained — sovereign-wealth-backed health investment provides distinctive options; framings that assume resource scarcity will be politically discordant."
```

## 11. Out-of-band notes

For roles unfilled or in transition.

## 12. Open questions

- Named Undersecretary MoPH under Al Mahmoud with currency verified.
- CEO HMC, CEO PHCC, CEO Sidra Medicine with currency verified.
- Director QCHP, CEO Qatar Red Crescent, CEO Qatar Cancer Society with currency verified.
- Chair Shura Council Health Committee with currency verified.
- President Qatar Medical Association with currency verified.
