# spec.md — `leaders.yml`

Single source of truth for the Bhutanese health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Bhutanese Ministry of Health (MoH), and adjacent bodies.

Bhutan operates a constitutional Buddhist monarchy under King Jigme Khesar Namgyel Wangchuck and a parliamentary government. The health system is constitutionally free at point of use and centred on the Jigme Dorji Wangchuck National Referral Hospital (JDWNRH) in Thimphu and the Eastern Regional Referral Hospital in Mongar. The country is known for the Gross National Happiness (GNH) framework which informs policy. The Tshering Tobgay (People's Democratic Party — PDP) government has been in office since January 2024.

## 2. Scope

In scope: King; Prime Minister; Minister of Health; Health Secretary; President JDWNRH; Director General of Health Services; National Assembly Social and Cultural Affairs Committee.

Out of scope: dzongkhag health office heads.

## 3. Structure

Standard 2/6/10/14 indentation. Top-level key: `Bhutanese health stakeholders:`. Ordering: Monarchy → Cabinet → MoH → JDWNRH → Parliament.

## 4. Field definitions

Party affiliation: `PDP` (People's Democratic Party, ruling), `DTT` (Druk Thuendrel Tshogpa), `DPT` (Druk Phuensum Tshogpa). Bhutanese honorifics: `Dasho` (Sir, honorific title), `Lyonpo` (Minister). Titles in English.

## 5. Provenance and dating

Anchor to year, month or date. Lyonpo Tandin Wangchuk has served as Minister of Health since the formation of the Tshering Tobgay PDP government in January 2024 following the 9 January 2024 National Assembly election.

## 6. Update workflow

Verify against moh.gov.bt, gov.bt, na.gov.bt, Kuensel (national newspaper), Bhutan Broadcasting Service (BBS), The Bhutanese.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Importing Indian framings — Bhutan is a sovereign monarchy with a distinct constitutional, cultural and Buddhist-philosophical orientation; framings that import Indian-system patterns will be politely corrected.
- Ignoring Gross National Happiness — the GNH framework is constitutionally embedded and shapes health-policy framing; framings that ignore it miss a central lens.
- Ignoring referral to India — Bhutanese patients with conditions exceeding domestic capacity are referred to Indian tertiary centres under government-funded arrangements; this is structural.

## 9. Acronym glossary

- **DTT** — Druk Thuendrel Tshogpa.
- **GNH** — Gross National Happiness.
- **JDWNRH** — Jigme Dorji Wangchuck National Referral Hospital.
- **PDP** — People's Democratic Party.

## 10. Worked example

```yaml
      - Lyonpo Tandin Wangchuk (PDP):
          - Title: Minister of Health (since January 2024)
          - Stakeholder engagement notes:
              - "Minister of Health in the Tshering Tobgay (People's Democratic Party) government since January 2024 following the 9 January 2024 National Assembly election; engineer by training; long-serving public official."
              - "Owns MoH policy and budget, JDWNRH in Thimphu, Eastern Regional Referral Hospital in Mongar, Central Regional Referral Hospital in Gelephu, dzongkhag and basic health unit network across the twenty dzongkhags, the constitutional free-at-point-of-use commitment, the GNH-informed health-policy framing, and SAARC and BIMSTEC health diplomacy."
              - "Hook: GNH-aligned health-system framing, mental health, NCDs, mother and child health, traditional Sowa Rigpa medicine integration, climate-and-health (Bhutan is a carbon-negative country with active climate-health agenda), digital health, and referral-to-India coordination land."
          - Tone advice:
              - "Open with GNH-aligned framing, mental health, NCDs, MCH, traditional medicine, climate-and-health and digital health — these are Bhutanese signature lines."
              - "Do not import Indian-system framings or ignore the constitutional free-at-point-of-use commitment and GNH lens — both will be politely corrected."
```

## 11. Out-of-band notes

For roles unfilled or interim.

## 12. Open questions

- Health Secretary and Director General of Health Services with currency verified.
- President JDWNRH with currency verified.
- National Assembly Social and Cultural Affairs Committee Chair with currency verified.
