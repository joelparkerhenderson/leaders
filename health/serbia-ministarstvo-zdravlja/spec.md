# spec.md — `leaders.yml`

Single source of truth for the Serbian health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Ministarstvo zdravlja Republike Srbije (Ministry of Health), Republički fond za zdravstveno osiguranje (RFZO), Agencija za lekove i medicinska sredstva (ALIMS), Klinički centri (Belgrade, Niš, Kragujevac, Novi Sad), and adjacent bodies.

The Serbian system is statutory health insurance through RFZO; the Ministry sets policy; ALIMS regulates medicines; 4 University Clinical Centres and 17 regional general hospitals deliver tertiary and secondary care. EU integration accession negotiations frame regulatory alignment.

## 2. Scope

In scope: President; PM; Minister of Health; State Secretaries; Director RFZO; Director ALIMS; Directors of Klinički centri (UKC Beograd, UKC Niš, UKC Kragujevac, UKCV Novi Sad); Director Institute of Public Health 'Dr Milan Jovanović Batut'; National Assembly Health and Family Committee Chair; Serbian Medical Society; Serbian Medical Chamber.

## 3. Structure

Standard. Ordering: PM → Ministarstvo → RFZO → ALIMS → IPH Batut → 4 UKC → 17 OZH (regional general hospitals) → Parliament → Serbian Medical Chamber.

## 4. Field definitions

Party affiliation: `SNS` (Srpska Napredna Stranka — Vučić), `SPS` (Socialist), `Zavetnici`, `NPS`, `PUPS`, `JS`, opposition `SSP / Stranka slobode i pravde`, `NDB`, `ZLF`, `DS` and others. Titles in Serbian / English.

## 5. Provenance and dating

Dr. Zlatibor Lončar (SNS) has served as Minister of Health since 2 May 2024 in the Miloš Vučević / Đuro Macut government; previously Minister of Health 2014-2022; physician; familiar nickname 'Dr Život'. Met with World Bank delegation on a new project in 2026.

## 6. Update workflow

Verify against zdravlje.gov.rs, srbija.gov.rs, rfzo.rs, alims.gov.rs, parlament.gov.rs, Politika, Blic, RTS, N1 Srbija, Nova.rs, Danas.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating Ministarstvo as the buyer — RFZO is the statutory payer.
- Importing NHS framings unmodified — Serbia is Bismarckian SHI with state-dominated delivery.

## 9. Acronym glossary

- **ALIMS** — Agencija za lekove i medicinska sredstva.
- **IPH Batut** — Institut za javno zdravlje 'Dr Milan Jovanović Batut'.
- **RFZO** — Republički fond za zdravstveno osiguranje.
- **UKC** — Univerzitetski klinički centar.

## 10. Worked example

```yaml
      - Dr. Zlatibor Lončar (SNS):
          - Title: Minister of Health of the Republic of Serbia (since 2 May 2024; previously served 2014-2022)
          - Stakeholder engagement notes:
              - "Minister of Health since 2 May 2024 in the Vučević / Macut government; SNS; previously Minister of Health 2014-2022 — returning to the portfolio with extensive institutional memory; physician; familiar public nickname 'Dr Život' ('Dr Life')."
              - "Active 2026: met with World Bank delegation to discuss new project (Ministry of Health website); meeting with SEEHN (South-Eastern European Health Network)."
              - "Owns Ministarstvo policy, RFZO statutory insurance coordination, ALIMS regulation, IPH Batut public-health surveillance, 4 UKC and 17 OZH, healthtech investment (Pirot oncology center, Tirsova children's hospital reconstruction), EU acquis health alignment in accession negotiations, and Serbia's WHO Europe and SEEHN positioning."
              - "Hook: hospital infrastructure investment (Tirsova reconstruction is high-profile), EU health-acquis alignment, RFZO reform, oncology national programme, SEEHN cooperation."
          - Tone advice:
              - "Open with hospital infrastructure investment, EU accession alignment, and SEEHN — these are his sustained authored lines."
              - "Do not pitch with frames that ignore Serbia-Kosovo or Serbia-EU complexity — these contexts shape every health-policy decision; framings that bypass them will be politically tone-deaf."
```

## 11. Out-of-band notes

For roles unfilled or in transition.

## 12. Open questions

- Named State Secretaries under Lončar with currency verified.
- Director RFZO and Director ALIMS with currency verified.
- Directors of UKC Beograd, UKC Niš, UKC Kragujevac, UKCV Novi Sad with currency verified.
- Director Institute of Public Health 'Dr Milan Jovanović Batut' with currency verified.
- National Assembly Health and Family Committee Chair with currency verified.
- Serbian Medical Society and Serbian Medical Chamber leadership with currency verified.
