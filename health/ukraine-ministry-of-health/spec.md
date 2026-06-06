# spec.md — `leaders.yml`

Single source of truth for the Ukrainian health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Ukrainian Ministry of Health (Міністерство охорони здоров'я України, MOZ), National Health Service of Ukraine (NHSU — the single payer), State Medicines and Drug Control Service, Public Health Centre, and adjacent bodies.

The Ukrainian system underwent reform from 2017 separating financing from delivery: NHSU is the single payer; providers (state, communal, private) contract with NHSU on a capitation and DRG-equivalent basis; the Programme of Medical Guarantees defines covered services. Ongoing Russian aggression since February 2022 has caused massive damage to health infrastructure and substantial population displacement.

## 2. Scope

In scope: President; Prime Minister; Minister of Health; Deputy Ministers; Director-General Directorate; Head NHSU; Head State Medicines Service; Director Public Health Centre; Heads of oblast Health Departments (Kyiv, Lviv, Kharkiv, Odesa, Dnipropetrovsk, Donetsk, Zaporizhzhia); Director Ohmatdyt; Verkhovna Rada Health Committee Chair; WHO Ukraine Office head (key partner); Ministry of Health partners (USAID, WHO, EU4Health).

## 3. Structure

Standard. Ordering: President / PM → MOZ → NHSU → State Medicines Service → Public Health Centre → oblasts → Verkhovna Rada Health Committee.

## 4. Field definitions

Party affiliation using canonical Ukrainian abbreviations: `Sluha Narodu` (Servant of the People — Zelenskyy), `YeS` (European Solidarity), `Batkivshchyna`, `Holos`, `OPZZ` (banned). Titles in English (with Ukrainian where useful).

## 5. Provenance and dating

Viktor Liashko has served as Minister of Health since 20 May 2021 in the Shmyhal government; reappointed 17 July 2025 in a Cabinet reorganisation under President Zelenskyy. Previously Chief State Sanitary Doctor (Chief Sanitary Doctor) during the early Covid-19 response. Continues active through 2026, working closely with WHO Europe on humanitarian response.

## 6. Update workflow

Verify against moz.gov.ua, kmu.gov.ua, president.gov.ua, nszu.gov.ua, rada.gov.ua, Ukrinform, Interfax-Ukraine, Kyiv Independent, Ukrainska Pravda, Babel.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating MOZ as the buyer — NHSU is the single payer for guaranteed services.
- Ignoring the war context — health infrastructure damage, displaced populations and mental-health needs are central.

## 9. Acronym glossary

- **MOZ** — Ministry of Health (Міністерство охорони здоров'я).
- **NHSU / НСЗУ** — National Health Service of Ukraine (single payer).
- **Ohmatdyt** — National Specialized Children's Hospital, Kyiv.
- **PMG** — Programme of Medical Guarantees.
- **VRU** — Verkhovna Rada of Ukraine (parliament).

## 10. Worked example

```yaml
      - Viktor Liashko / Віктор Ляшко (Sluha Narodu / technocratic):
          - Title: Minister of Health of Ukraine (since 20 May 2021; reappointed 17 July 2025)
          - Stakeholder engagement notes:
              - "Minister of Health since 20 May 2021 in the Denys Shmyhal government, reappointed 17 July 2025 in a Cabinet reorganisation under President Volodymyr Zelenskyy; previously Chief State Sanitary Doctor of Ukraine during the early Covid-19 pandemic response; physician-epidemiologist."
              - "Active 2026: met WHO Europe and WHO Ukraine representatives on strategic priorities for humanitarian response in 2026 (Cabinet of Ministers); working visit to Donetsk region (February 2026) — visible field presence in the war-affected territories."
              - "Owns wartime health system continuity, EHR rollout and digital integration, NHSU programme of medical guarantees, post-Ohmatdyt-bombing rebuilding (the Kyiv children's hospital was attacked in July 2024), pharmaceutical supply, mental-health-and-PTSD national response (a focus given war), prosthetics and rehabilitation, and EU-accession alignment of health legislation."
              - "International partners: USAID (Health Reform Support), WHO Europe, EU4Health, World Bank, Global Fund; Liashko's bilateral diplomacy is dense and continuous."
              - "Hook: wartime health-system continuity, Ohmatdyt rebuilding, mental health and PTSD, prosthetics and rehabilitation, NHSU programme of medical guarantees, pharmaceutical supply, EU-accession health legislation land."
          - Tone advice:
              - "Open with wartime continuity, Ohmatdyt rebuilding, mental health, prosthetics, and EU-accession alignment — these are Liashko's sustained authored lines and the priority files of the Zelenskyy-Shmyhal government."
              - "Do not pitch as if peace conditions were normal — every health-policy decision is shaped by ongoing aggression, infrastructure damage, occupied territories and population displacement."
```

## 11. Out-of-band notes

For roles unfilled or in transition.

## 12. Open questions

- Named Deputy Ministers of Health under Liashko with currency verified.
- Head NHSU with currency verified.
- Head State Medicines Service, Director Public Health Centre with currency verified.
- Heads of oblast Health Departments for Kyiv, Lviv, Kharkiv, Odesa, Dnipropetrovsk, Donetsk, Zaporizhzhia with currency verified.
- Director Ohmatdyt with currency verified (post-July-2024 reconstruction context).
- VRU Health Committee Chair with currency verified.
- WHO Ukraine Office head and key bilateral partners (USAID Mission Director, EU Delegation health attaché).
