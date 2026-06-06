# spec.md — `leaders.yml`

Single source of truth for the Nepalese health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Nepal Ministry of Health and Population (MoHP), Department of Health Services (DoHS), Department of Drug Administration (DDA), Health Insurance Board, and adjacent bodies.

The Nepalese system devolved health delivery to seven Provinces and 753 Local Levels under the 2015 Constitution; federal MoHP retains policy, vertical programmes, and tertiary referral. Health Insurance Board manages the National Health Insurance Programme. Substantial NGO and donor presence (USAID, UK FCDO, WHO, UNICEF, Gavi).

## 2. Scope

In scope: President; PM; Minister of Health and Population; State Minister; Secretary; Director-General DoHS; Director-General DDA; Director Health Insurance Board; Heads of provincial Ministries of Social Development / Health (seven provinces); Director Bir Hospital, Tribhuvan University Teaching Hospital; Federal Parliament Social Committee Chair (Health); Nepal Medical Association.

## 3. Structure

Standard. Ordering: PM → MoHP → DoHS → DDA → Health Insurance Board → seven provinces → Bir / TUTH → Federal Parliament Social Committee → Nepal Medical Association.

## 4. Field definitions

Party affiliation in Nepal frequently shifts; major parties: `NC` (Nepali Congress), `CPN (UML)`, `CPN (Maoist Centre)`, `RSP` (Rastriya Swatantra Party), `RPP` (Rastriya Prajatantra Party), `JSP` (Janata Samajwadi Party), independents. Titles in English with Devanagari where useful.

## 5. Provenance and dating

Nisha Mehta has been confirmed as Nepal's Minister of Health and Population in the Balendra Shah Cabinet finalised in March 2026 (Kathmandu Post coverage); AIIMS New Delhi alumna; Master's degree in nursing from University of Gwalior; previously worked at Birat Teaching Hospital, Biratnagar.

## 6. Update workflow

Verify against mohp.gov.np, opmcm.gov.np, dohs.gov.np, dda.gov.np, parliament.gov.np, Kathmandu Post, The Annapurna Express, MyRepublica, Online Khabar, Setopati.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating MoHP as the operational owner — Provinces and Local Levels run delivery.
- Importing US framings — Nepal is low-middle-income with federalised devolution and substantial donor coordination.

## 9. Acronym glossary

- **DDA** — Department of Drug Administration.
- **DoHS** — Department of Health Services.
- **MoHP** — Ministry of Health and Population.
- **NHIP** — National Health Insurance Programme.
- **TUTH** — Tribhuvan University Teaching Hospital.

## 10. Worked example

```yaml
      - Hon. Nisha Mehta (Balendra Shah Cabinet):
          - Title: Minister of Health and Population, Federal Democratic Republic of Nepal
          - Stakeholder engagement notes:
              - "Minister of Health and Population in the Balendra Shah Cabinet finalised in March 2026 (Kathmandu Post 27 March 2026); AIIMS New Delhi alumna; Master's degree in nursing from University of Gwalior, India; previously worked at Birat Teaching Hospital in Biratnagar — clinical-academic profile rare among Nepali health ministers."
              - "Owns federal MoHP policy, vertical programmes (immunisation, TB, HIV, malaria), DoHS coordination with provinces, DDA pharmaceutical regulation, Health Insurance Board administration of NHIP, and Nepal's WHO SEARO and SAARC health diplomacy."
              - "Hook: NHIP expansion, federal-provincial coordination, immunisation including Covid legacy, TB and HIV programmes, mental health, climate-and-health (Nepal is highly climate-vulnerable), donor coordination (USAID, UK FCDO, WHO, UNICEF, Gavi)."
          - Tone advice:
              - "Open with NHIP, federal-provincial coordination, climate-and-health and donor coordination — these are the priority files of MoHP in the 2026 context."
              - "Do not pitch as if MoHP were the operational buyer — Provinces and 753 Local Levels run delivery under the 2015 Constitution; framings must include provincial and local-government dimensions."
```

## 11. Out-of-band notes

For roles unfilled or in transition.

## 12. Open questions

- Confirm Nisha Mehta's swearing-in date and party affiliation within the Balendra Shah Cabinet.
- Named State Minister and Secretary MoHP with currency verified.
- Director-General DoHS, Director-General DDA, Director Health Insurance Board with currency verified.
- Heads of provincial Ministries of Social Development / Health for all seven provinces.
- Director Bir Hospital and TUTH with currency verified.
- Federal Parliament Social Committee Chair with currency verified.
- President Nepal Medical Association with currency verified.
