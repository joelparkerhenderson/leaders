# spec.md — `leaders.yml`

Single source of truth for the Gambian health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Gambian Ministry of Health (MoH), and adjacent bodies.

The Gambia is the smallest mainland African country, bordered on three sides by Senegal. The health system is public-dominant with the Edward Francis Small Teaching Hospital (EFSTH) in Banjul as the apex referral, supported by regional hospitals and minor health facilities. The country is under the Adama Barrow (NPP) government.

## 2. Scope

In scope: President; Minister of Health; Permanent Secretary; CEO EFSTH; Director Medical Services; Director Health Services; National Assembly Select Committee on Health.

Out of scope: regional health team leads.

## 3. Structure

Standard 2/6/10/14 indentation. Top-level key: `Gambian health stakeholders:`. Ordering: Presidency → MoH → EFSTH → National Assembly.

## 4. Field definitions

Party affiliation: `NPP` (National People's Party, ruling under Barrow), `UDP` (United Democratic Party, principal opposition), `GDC` (Gambia Democratic Congress), `PPP` (People's Progressive Party), `APRC` (Alliance for Patriotic Reorientation and Construction, legacy Jammeh party). Titles in English.

## 5. Provenance and dating

Anchor to year, month or date. Dr. Ahmadou Lamin Samateh has served as Minister of Health in the Barrow government; verify currency against the State House and the National Assembly.

## 6. Update workflow

Verify against statehouse.gov.gm, moh.gov.gm, national-assembly.gov.gm, The Standard, Foroyaa, The Point, GRTS.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating the Gambia as a sub-region of Senegal — despite the geographic enclave, the Gambia is a distinct sovereign state with its own MoH, healthcare architecture and English-language administrative tradition.
- Ignoring the Senegambia coordination — Senegambia health cooperation (transboundary disease control, ambulance evacuation, referral) is operationally significant and should be acknowledged.

## 9. Acronym glossary

- **EFSTH** — Edward Francis Small Teaching Hospital.
- **MoH** — Ministry of Health.
- **NPP** — National People's Party.
- **UDP** — United Democratic Party.

## 10. Worked example

```yaml
      - Dr. Ahmadou Lamin Samateh (NPP):
          - Title: Minister of Health
          - Stakeholder engagement notes:
              - "Minister of Health in the Adama Barrow government; medical doctor; long-serving in the portfolio under the post-Jammeh transition; verify currency against statehouse.gov.gm."
              - "Owns MoH policy and budget, Edward Francis Small Teaching Hospital (apex referral in Banjul), the regional hospital network, primary-care minor health centres, donor coordination (WHO, UNICEF, Global Fund, Gavi, World Bank, EU, FCDO, Saudi bilateral), and ECOWAS and OMVG health diplomacy."
              - "Hook: malaria control, maternal-and-child mortality reduction, NCDs, immunisation, and Senegambia transboundary cooperation land."
          - Tone advice:
              - "Open with malaria, MCH, NCDs, immunisation and Senegambia cooperation — durable MoH priorities."
              - "Do not treat the Gambia as a sub-region of Senegal — distinct sovereign state with its own architecture."
```

## 11. Out-of-band notes

For roles unfilled or interim.

## 12. Open questions

- Permanent Secretary, CEO EFSTH and Director Medical Services with currency verified.
- National Assembly Select Committee on Health Chair with currency verified.
