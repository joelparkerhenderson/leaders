# spec.md — `leaders.yml`

Single source of truth for the Armenian health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Armenia Ministry of Healthcare (Հայաստանի Հանրապետության առողջապահության նախարարություն), the National Center for Disease Control and Prevention, the Scientific Center for Pharmacology, the National Health Insurance system rolling out, and adjacent bodies.

The Armenian system is transitioning to mandatory health insurance (announced for 2026 launch by Health Minister Avanesyan after years of delay). The Ministry sets policy; State Health Agency administers state-financed services; Yerevan State Medical University runs major academic hospitals; large diaspora-funded private hospitals (Wigmore Clinic, Erebouni, Astghik) operate in parallel.

## 2. Scope

In scope: President; PM; Minister of Healthcare; Deputy Ministers; Director Scientific Centre of Drug and Medical Technology Expertise; Director NCDCP; CEO State Health Agency; Heads of major hospitals (Yerevan State Medical University, Wigmore Clinic, Erebouni, Astghik); National Assembly Standing Committee on Health Care, Maternity and Childhood Chair; Armenian Medical Association.

## 3. Structure

Standard. Ordering: PM → Ministry → SHA → NCDCP → SCDMTE → major hospitals → National Assembly Committee → Armenian Medical Association.

## 4. Field definitions

Party affiliation: `Civil Contract` (Pashinyan), `Hayastan` (Kocharyan-aligned), `I Have Honor`, `Republic` and others. Titles in English with Armenian where useful.

## 5. Provenance and dating

Anahit Avanesyan has served as Minister of Healthcare of the Republic of Armenia since 18 January 2021 in the Nikol Pashinyan (Civil Contract) government. Active 2026 on mandatory health insurance launch.

## 6. Update workflow

Verify against moh.am, gov.am, parliament.am, Armenpress, ArmInfo, Civilnet, EVN Report, The Armenian Report.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Importing US framings — Armenia is transitioning to mandatory insurance.
- Ignoring diaspora dimension — significant diaspora-funded health infrastructure.

## 9. Acronym glossary

- **MoH** — Ministry of Healthcare.
- **NCDCP** — National Center for Disease Control and Prevention.
- **SHA** — State Health Agency.

## 10. Worked example

```yaml
      - Anahit Avanesyan (Civil Contract):
          - Title: Minister of Healthcare of the Republic of Armenia (since 18 January 2021)
          - Stakeholder engagement notes:
              - "Minister of Healthcare since 18 January 2021 in the Nikol Pashinyan (Civil Contract) government; previously Deputy Minister and Acting Minister; physician-administrator background."
              - "Confirmed 2026: Armenia to launch mandatory health insurance in 2026 after years of delay (The Armenian Report); discussed healthcare reforms and joint programmes with EU Ambassador (Armenpress); active on EU-Armenia partnership agenda."
              - "Owns Ministry policy, mandatory health insurance rollout, SHA programmes, NCDCP surveillance, diaspora-cooperation programmes, post-2023-Artsakh-displaced-persons health response, and Armenia's WHO Europe and EU bilateral health diplomacy."
              - "Hook: mandatory health insurance launch 2026, post-Artsakh-displaced-persons health, oncology national programme, mental health, EU bilateral cooperation, and Armenia-diaspora-medical partnerships land."
          - Tone advice:
              - "Open with mandatory health insurance launch, post-Artsakh health response, EU bilateral cooperation and diaspora partnerships — these are her sustained authored priorities."
              - "Do not pitch with Russia-aligned framings as default — the Pashinyan government has pivoted toward EU and Western partnerships; pre-2022 Russia-aligned defaults will be politically misaligned."
```

## 11. Out-of-band notes

For roles unfilled or in transition.

## 12. Open questions

- Named Deputy Ministers under Avanesyan with currency verified.
- Director Scientific Centre of Drug and Medical Technology Expertise and Director NCDCP with currency verified.
- CEO State Health Agency with currency verified.
- Heads of Yerevan State Medical University Hospital, Wigmore Clinic, Erebouni, Astghik with currency verified.
- National Assembly Standing Committee on Health Care, Maternity and Childhood Chair with currency verified.
- President Armenian Medical Association with currency verified.
