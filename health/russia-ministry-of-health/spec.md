# spec.md — `leaders.yml`

Single source of truth for the Russian Federation health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Russian Ministry of Health (Минздрав России), Rospotrebnadzor (Federal Service for Surveillance on Consumer Rights Protection and Human Wellbeing), Roszdravnadzor (Federal Service for Surveillance in Healthcare), the Federal Medical-Biological Agency (FMBA), the FOMS (Federal Compulsory Medical Insurance Fund), federal medical institutes, and adjacent bodies.

The Russian system combines federal stewardship with regional implementation. The Compulsory Medical Insurance (OMS) is the financing mechanism; territorial health funds purchase from public and private providers. Rospotrebnadzor handles public health and consumer-health surveillance; Roszdravnadzor regulates medical activities; FMBA covers strategic-industry workers and nuclear-medicine functions. Federal medical research centres (Pirogov, Bakulev, Burdenko, Blokhin, Mechnikov) operate as the academic-tertiary backbone.

## 2. Scope

In scope: President; Deputy Prime Minister with social-block portfolio; Minister of Health; Deputy Ministers; Head Rospotrebnadzor; Head Roszdravnadzor; Director FMBA; Chair FOMS; Chair State Duma Committee on Health Protection; Chair Federation Council Committee on Social Policy; Directors of major federal centres; Heads of regional Health Ministries of the major subjects (Moscow, St Petersburg, Moscow Oblast, Tatarstan, Sverdlovsk Oblast); President National Medical Chamber.

## 3. Structure

Standard 2/6/10/14. Ordering: Presidency → Government social block → Minzdrav → Rospotrebnadzor → Roszdravnadzor → FMBA → FOMS → federal centres → regional ministries → State Duma → professional bodies.

## 4. Field definitions

Standard. Party affiliation typically `United Russia` for senior officials; opposition parties: `CPRF` (KPRF), `LDPR`, `Just Russia`, `New People`. Names in Cyrillic / Latinised. Titles in Russian or English with glosses.

## 5. Provenance and dating

Mikhail Murashko has served as Minister of Health since 21 January 2020 in the Mishustin government, retained through the 2024 presidential cycle and the Putin V term.

## 6. Update workflow

Verify against minzdrav.gov.ru, government.ru, kremlin.ru, rospotrebnadzor.ru, roszdravnadzor.gov.ru, fmba.gov.ru, ffoms.gov.ru, duma.gov.ru, RIA Novosti, TASS, Kommersant, Vedomosti, Meduza, Novaya Gazeta Europe.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating Russia as a Western-style multi-payer market — the system is state-dominated with OMS as a single statutory financing mechanism.
- Importing US framings unmodified — Russia is post-Soviet centralised with strong vertical chains of command from federal to regional levels.
- Ignoring sanctions context — international pharmaceutical and device supply has been reshaped since 2022.

## 9. Acronym glossary

- **FMBA** — Federal Medical-Biological Agency (Федеральное медико-биологическое агентство).
- **FOMS** — Federal Compulsory Medical Insurance Fund.
- **Minzdrav (Минздрав)** — Ministry of Health.
- **OMS** — Obligatory Medical Insurance (Обязательное медицинское страхование).
- **Rospotrebnadzor** — Federal Service for Surveillance on Consumer Rights Protection and Human Wellbeing.
- **Roszdravnadzor** — Federal Service for Surveillance in Healthcare.

## 10. Worked example

```yaml
      - Mikhail Murashko / Михаил Мурашко:
          - Title: Minister of Health of the Russian Federation (since 21 January 2020)
          - Stakeholder engagement notes:
              - "Minister of Health of the Russian Federation since 21 January 2020 in the Mikhail Mishustin government; retained across the 2024 presidential cycle and into Putin's V term; physician by training; previously Head of Roszdravnadzor 2015-2020."
              - "Active throughout 2026: working meetings with President Putin (April 2026), addressed 79th World Health Assembly in Geneva (May 2026) defending Russia's position on global health, official three-day visits to Sri Lanka (4-7 May 2026) and Ethiopia (March 2026)."
              - "Public-policy line: announced Russia has groundwork for vaccine against new Ebola strain (May 2026 to African Initiative news agency) — signal of biomedical-sovereignty agenda and Russian-vaccine export ambition."
              - "Owns federal Minzdrav, coordination with Rospotrebnadzor and Roszdravnadzor, FMBA, federal centres, national projects 'Healthcare' and 'Demography', OMS governance through FOMS, post-sanctions pharmaceutical localisation, and Russian medical-cooperation portfolio in BRICS, Africa and CIS."
              - "Hook: Russian vaccine and biomedical sovereignty, national projects, BRICS / Africa cooperation, pharmaceutical localisation, oncology and cardiology national networks, paediatric centres land."
          - Tone advice:
              - "Lead with national projects, biomedical sovereignty, BRICS-Africa cooperation and federal-regional integration — these are the Murashko / Putin V-era public lines."
              - "Do not pitch via Western multilateral frames or sanctions-bypass language — engagement is politically calibrated and Western-framed proposals will be filtered or rebuffed."
```

## 11. Out-of-band notes

For roles unfilled or in transition.

## 12. Open questions

- Named Deputy Prime Minister for social block (typically held by senior figure in Mishustin government).
- Named Deputy Ministers of Minzdrav under Murashko with currency verified.
- Heads of Rospotrebnadzor, Roszdravnadzor, FMBA, Chair FOMS with currency verified.
- Chairs of State Duma Committee on Health Protection and Federation Council Committee on Social Policy.
- Heads of regional Health Ministries of Moscow, St Petersburg, Moscow Oblast, Tatarstan, Sverdlovsk Oblast.
- Directors of major federal centres (Pirogov, Bakulev, Burdenko, Blokhin, Mechnikov).
- President National Medical Chamber with currency verified.
