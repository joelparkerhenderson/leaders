# spec.md — `leaders.yml`

Single source of truth for the Belarusian health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Ministry of Health of the Republic of Belarus (Министерство здравоохранения), the State Centre for Hygiene, Epidemiology and Public Health, the Belarusian Medical Academy of Postgraduate Education, and adjacent bodies.

The Belarusian system is centralised state-managed Beveridgean: free at point of use, financed via general taxation, with Soviet-inheritance polyclinic and hospital network. Sanctions and economic constraints since 2020 have shaped pharmaceutical supply.

## 2. Scope

In scope: President; PM; Minister of Health; First Deputy and Deputy Ministers; Directors of major institutions (Centre for Hygiene, BelMAPO, Centre for Medical Rehabilitation and Balneology, Republican Scientific and Practical Centres for Cardiology, Oncology, Tuberculosis); Heads of oblast Health Departments (Minsk, Brest, Vitebsk, Gomel, Grodno, Mogilev); National Assembly Health Committee Chair; Belarusian Medical Society.

## 3. Structure

Standard. Ordering: Presidency → PM → Minzdrav → Centres → oblast departments → Assembly → professional body.

## 4. Field definitions

Party affiliation: independents and pro-government coalitions (Belaya Rus). Titles in English with Russian / Belarusian.

## 5. Provenance and dating

Alexander Khodzhayev has been Minister of Health since 26 January 2024 in the Roman Golovchenko (now Aleksandr Turchin) government under President Lukashenko. Active 2026 on healthcare quality accessibility, BelarusMedica forum, healthcare exhibitions, international partnerships.

## 6. Update workflow

Verify against minzdrav.gov.by, government.by, president.gov.by, BelTA, BelaPAN, Nasha Niva, Reform.by.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Importing US framings — Belarus is fully state-managed Beveridgean.
- Ignoring sanctions context — Western pharmaceutical and equipment supply is reshaped post-2020.

## 9. Acronym glossary

- **BelMAPO** — Belarusian Medical Academy of Postgraduate Education.
- **MinZdrav** — Ministry of Health.

## 10. Worked example

```yaml
      - Alexander Khodzhayev:
          - Title: Minister of Health of the Republic of Belarus (since 26 January 2024)
          - Stakeholder engagement notes:
              - "Minister of Health since 26 January 2024 in the Lukashenko-aligned government; previously held senior roles in the Belarusian health system; physician background."
              - "Active 2026 public lines: 'quality healthcare must be accessible across Belarus' (BelTA); healthcare exhibition helps Belarus find new partners from abroad (BelTA); BelarusMedica forum as crucial for shaping national strategy."
              - "Owns Minzdrav policy, state pharmaceutical supply (Belmedpreparaty, Borisov Plant of Medical Preparations), Republican Scientific and Practical Centres network, primary-care polyclinics, BRICS+ and CSTO/EAEU health cooperation, China-Belarus medical cooperation, Russia-Belarus Union State health programmes."
              - "Hook: pharmaceutical localisation (Belmedpreparaty, Borisov), Russia-Belarus Union State health programmes, BelarusMedica forum, China cooperation, primary-care polyclinic modernisation."
          - Tone advice:
              - "Open with pharmaceutical localisation, Union State and BRICS+ cooperation — these are the geopolitical-economic frames of Belarusian healthcare under Lukashenko."
              - "Do not pitch through Western multilateral framings — engagement is calibrated to Russia-Belarus-China alignment and Western-framed proposals will be filtered."
```

## 11. Out-of-band notes

For roles unfilled or in transition.

## 12. Open questions

- Named Deputy Ministers under Khodzhayev with currency verified.
- Heads of Republican Scientific and Practical Centres for Cardiology, Oncology, Tuberculosis, and BelMAPO.
- Heads of oblast Health Departments (Minsk, Brest, Vitebsk, Gomel, Grodno, Mogilev).
- National Assembly Health Committee Chair with currency verified.
- President Belarusian Medical Society with currency verified.
