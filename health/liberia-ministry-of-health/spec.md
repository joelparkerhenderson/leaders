# spec.md — `leaders.yml`

Single source of truth for the Liberian health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Liberian Ministry of Health (MoH), the Liberia Medicines and Health Products Regulatory Authority (LMHRA), the National Public Health Institute of Liberia (NPHIL), and adjacent bodies.

Liberia operates a primarily public, donor-supported system rebuilt after the 1989–2003 civil wars and the 2014–2016 Ebola outbreak. The Ministry serves under President Joseph N. Boakai (Unity Party, since January 2024).

## 2. Scope

In scope: President; Vice President; Minister of Health; Deputy Ministers; Chief Medical Officer; Director-General NPHIL; CEO LMHRA; Parliamentary Health Committee; Liberia Medical and Dental Association (LMDA); Liberia National Nurses Association.

Out of scope: county-health-team leads; hospital medical superintendents.

## 3. Structure

Standard 2/6/10/14 indentation. Top-level key: `Liberian health stakeholders:`. Ordering: Presidency → MoH → NPHIL → LMHRA → Parliament → professional associations.

## 4. Field definitions

Party affiliation: `UP` (Unity Party, ruling), `CDC` (Coalition for Democratic Change, principal opposition — former ruling party under Weah), `ALP` (All Liberian Party), `LP` (Liberty Party). Independent for non-aligned. Titles in English.

## 5. Provenance and dating

Anchor to year, month or date. Dr. Louise Mapleh Kpoto has served as Minister of Health under the Boakai administration since 2024; elected 3rd Vice-President of the 78th World Health Assembly (May 2025); recognised by WHO with the World No Tobacco Day Award 2026 for tobacco-control leadership.

## 6. Update workflow

Verify against moh.gov.lr, emansion.gov.lr (Executive Mansion), legislature.gov.lr, FrontPage Africa, The New Dawn, Daily Observer, Liberian Observer.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Anchoring framings to Ebola — the 2014–2016 outbreak is part of institutional memory but framings that reduce Liberia health to Ebola will be politely corrected; the Ministry's current priorities are PHC, maternal and child health, NCDs and tobacco control.
- Ignoring the donor architecture — Liberia's health system is materially co-financed by USAID/PEPFAR, World Bank, Global Fund, Gavi, WHO, EU and FCDO; framings that assume Treasury-only financing are inaccurate.

## 9. Acronym glossary

- **CDC** — Coalition for Democratic Change (note: not the US Centers for Disease Control).
- **LMDA** — Liberia Medical and Dental Association.
- **LMHRA** — Liberia Medicines and Health Products Regulatory Authority.
- **MoH** — Ministry of Health.
- **NPHIL** — National Public Health Institute of Liberia.
- **UP** — Unity Party.

## 10. Worked example

```yaml
      - Dr. Louise Mapleh Kpoto (UP-aligned):
          - Title: Minister of Health (since 2024)
          - Stakeholder engagement notes:
              - "Minister of Health under the Joseph N. Boakai administration since 2024; elected 3rd Vice-President of the 78th World Health Assembly (Geneva, May 2025) — a strong signal of African and Liberian standing in multilateral health diplomacy; awarded the WHO World No Tobacco Day certificate 2026 for tobacco-control leadership."
              - "Owns MoH policy and budget, the John F. Kennedy Medical Center (apex referral in Monrovia) and the county-hospital network across the fifteen counties, the primary-care clinic network, the Community Health Assistant programme, NPHIL outbreak surveillance, LMHRA regulation, and donor coordination (USAID/PEPFAR, World Bank, Global Fund, Gavi, WHO)."
              - "Hook: PHC strengthening, Community Health Assistant programme expansion, maternal and child health, tobacco control (a Kpoto signature), NCDs, mpox and outbreak preparedness, health-financing reform and donor coordination land."
          - Tone advice:
              - "Open with PHC, CHA programme, maternal and child health, tobacco control, outbreak preparedness and donor coordination — these are Kpoto's signature lines and the Boakai government's health priorities."
              - "Do not anchor exclusively to Ebola — it is part of institutional memory but the Ministry's current agenda is PHC, MCH, tobacco control and NCDs; framings that reduce Liberia to Ebola will be politely redirected."
```

## 11. Out-of-band notes

For roles unfilled or interim.

## 12. Open questions

- Named Deputy Ministers and Chief Medical Officer with currency verified.
- Director-General NPHIL and CEO LMHRA with currency verified.
- Parliamentary Health Committee Chairs (House and Senate) with currency verified.
