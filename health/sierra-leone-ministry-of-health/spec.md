# spec.md — `leaders.yml`

Single source of truth for the Sierra Leonean health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Sierra Leone Ministry of Health (MoH — renamed from Ministry of Health and Sanitation in 2024), the Pharmacy Board of Sierra Leone (PBSL), the National Medical Supplies Agency (NMSA), and adjacent bodies.

Sierra Leone operates a public, primarily PHC-oriented system with significant donor partnership (World Bank, Global Fund, Gavi, WHO, USAID/PEPFAR), recovering institutionally from the 2014–2016 Ebola outbreak and subsequent shocks; the country runs a Free Healthcare Initiative (FHCI) for pregnant women, lactating mothers and children under five. The Ministry serves under President Julius Maada Bio (SLPP, second term).

## 2. Scope

In scope: President; Vice President; Minister of Health; Deputy Minister; Chief Medical Officer; Permanent Secretary; Registrar PBSL; Director NMSA; Parliamentary Committee on Health; Sierra Leone Medical and Dental Association (SLMDA); Sierra Leone Nurses Association (SLNA).

Out of scope: District Health Management Team leads; hospital medical superintendents.

## 3. Structure

Standard 2/6/10/14 indentation. Top-level key: `Sierra Leonean health stakeholders:`. Ordering: Presidency → MoH → PBSL → NMSA → Parliament → professional associations.

## 4. Field definitions

Party affiliation: `SLPP` (Sierra Leone People's Party, ruling), `APC` (All People's Congress, principal opposition). Independent for non-aligned. Titles in English.

## 5. Provenance and dating

Anchor to year, month or date. Dr. Austin Demby has served as Minister of Health since 2022 (continued through President Bio's second term); previously Sierra Leone field-station Director for the US Centers for Disease Control and Prevention and Acting Director of the Office of Global Health at HRSA; PhD and MPH credentials; widely cited as a technocratic appointment.

## 6. Update workflow

Verify against mohs.gov.sl, statehouse.gov.sl, parliament.gov.sl, Sierra Leone Telegraph, Awoko, Concord Times, Politico SL.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Anchoring framings to Ebola — the 2014–2016 outbreak is part of institutional memory but framings that reduce Sierra Leone health to Ebola will be politely corrected; the Ministry's current priorities are PHC, FHCI sustainability, mpox preparedness, and NCDs.
- Ignoring the Free Healthcare Initiative — the FHCI for pregnant women, lactating mothers and children under five is the most politically protected health programme and must be acknowledged; framings that imply user fees for these groups are politically toxic.

## 9. Acronym glossary

- **APC** — All People's Congress.
- **FHCI** — Free Healthcare Initiative.
- **MoH** — Ministry of Health (renamed from MoHS in 2024).
- **NMSA** — National Medical Supplies Agency.
- **PBSL** — Pharmacy Board of Sierra Leone.
- **SLPP** — Sierra Leone People's Party.

## 10. Worked example

```yaml
      - Dr. Austin Demby (SLPP-aligned, technocrat):
          - Title: Minister of Health (since 2022, continued through President Bio's second term)
          - Stakeholder engagement notes:
              - "Minister of Health since 2022, continued through President Julius Maada Bio's second term; PhD, MPH; previously Sierra Leone field-station Director for the US Centers for Disease Control and Prevention and Acting Director of the Office of Global Health at HRSA; widely cited as a technocratic appointment with strong US public-health institutional ties."
              - "Owns MoH policy and budget, Connaught Hospital and the regional referral hospital network (Bo, Kenema, Makeni), district hospitals and primary-care unit network, the Free Healthcare Initiative (FHCI), the Community Health Worker programme, PBSL oversight, NMSA supply-chain coordination, and donor engagement (World Bank, Global Fund, Gavi, WHO, PEPFAR, FCDO)."
              - "Hook: FHCI sustainability and expansion, PHC strengthening, mpox and outbreak preparedness (Sierra Leone has invested in surveillance since Ebola), CHW programme, maternal-and-child mortality reduction, health-financing reform, and donor-coordination architecture land."
          - Tone advice:
              - "Open with FHCI, PHC, CHW programme, outbreak preparedness, maternal-and-child health and donor coordination — these are Demby's signature lines and the Bio government's health priorities."
              - "Do not anchor exclusively to Ebola — the 2014–2016 outbreak is part of institutional memory but the Ministry's current agenda is PHC, FHCI sustainability and NCDs; framings that reduce Sierra Leone to Ebola will be politely redirected."
```

## 11. Out-of-band notes

For roles unfilled or interim.

## 12. Open questions

- Named Deputy Minister, Chief Medical Officer and Permanent Secretary with currency verified.
- Registrar PBSL and Director NMSA with currency verified.
- Parliamentary Committee on Health Chair with currency verified.
