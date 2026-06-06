# spec.md — `leaders.yml`

Single source of truth for the Azerbaijani health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Azerbaijani Ministry of Health (Səhiyyə Nazirliyi), State Agency on Mandatory Health Insurance (TƏBİB), Analytical Expertise Center, and adjacent bodies.

The Azerbaijani system implemented mandatory health insurance through TƏBİB from 2020-2021 with a single-payer model purchasing services from public and private providers; the Ministry sets policy; oil-revenue-funded SOFAZ-financed major hospital and primary-care investments support reform. Post-Karabakh recovery in regions retaken in 2020 and 2023 shapes reconstruction priorities.

## 2. Scope

In scope: President; PM; Minister of Health; Deputy Ministers; Chair TƏBİB; Director Analytical Expertise Center for Medicines; Heads of major hospitals (Central Clinical Hospital, Republican Children's Hospital, Mərdəkan COVID Hospital, Karabakh modular hospital network); Milli Məclis Health Committee Chair; Azerbaijani Medical Association.

## 3. Structure

Standard. Ordering: PM → Ministry → TƏBİB → Analytical Expertise Center → major hospitals → Milli Məclis → Azerbaijani Medical Association.

## 4. Field definitions

Party affiliation: `Yeni Azərbaycan` (YAP — ruling), and several opposition parties. Titles in English with Azerbaijani.

## 5. Provenance and dating

Teymur Yusif oghlu Musayev was appointed Minister of Health by President Ilham Aliyev; confirmed in 2026 attending Regional Ecological Summit in Astana (AZERTAC). Continues active in role.

## 6. Update workflow

Verify against sehiyye.gov.az, president.az, parliament.az, AZERTAC, APA, Report.az, Trend, Caspian News.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating Ministry as the buyer — TƏBİB is the single payer for mandatory insurance.
- Importing US framings — Azerbaijan is mandatory insurance with state-dominated delivery and significant oil-revenue investment.

## 9. Acronym glossary

- **TƏBİB** — State Agency on Mandatory Health Insurance.

## 10. Worked example

```yaml
      - Teymur Yusif oghlu Musayev:
          - Title: Minister of Health of the Republic of Azerbaijan (under President Ilham Aliyev)
          - Stakeholder engagement notes:
              - "Minister of Health appointed by President Ilham Aliyev; confirmed in 2026 by attendance at Regional Ecological Summit in Astana (AZERTAC); previously Acting Minister, then substantive Minister appointment."
              - "Active 2026: participated in Regional Ecological Summit Astana; coordinates Karabakh-region health-services reconstruction after the 2020 and 2023 Azerbaijani recovery of Karabakh territories; modular hospitals and primary-care centres deployed in Karabakh region."
              - "Owns Ministry policy, TƏBİB single-payer governance, Analytical Expertise Center for medicines regulation, Karabakh reconstruction health programmes, SOCAR / SOFAZ-funded health infrastructure, oncology and cardiology centres, COP29 host-country health-and-climate legacy programmes, and Azerbaijan's WHO Europe and Organisation of Turkic States health diplomacy."
              - "Hook: Karabakh-region reconstruction, TƏBİB mandatory-insurance refinement, COP29 health-and-climate legacy, oncology and cardiology centres of excellence, Organisation of Turkic States cooperation, and BRICS+ engagement land."
          - Tone advice:
              - "Open with Karabakh reconstruction, TƏBİB refinement and Organisation of Turkic States cooperation — these are the political-priorities of the Aliyev government."
              - "Do not pitch through Western-default framings — Azerbaijan operates multi-vector diplomacy and framings should accommodate that pluralism."
```

## 11. Out-of-band notes

For roles unfilled or in transition.

## 12. Open questions

- Named Deputy Ministers under Musayev with currency verified.
- Chair TƏBİB and Director Analytical Expertise Center with currency verified.
- Heads of major hospitals (Central Clinical Hospital, Republican Children's Hospital, Karabakh modular hospital network) with currency verified.
- Milli Məclis Health Committee Chair with currency verified.
- President Azerbaijani Medical Association with currency verified.
