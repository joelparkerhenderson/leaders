# spec.md — `leaders.yml`

Single source of truth for the Thai health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Thai Ministry of Public Health (กระทรวงสาธารณสุข, Krasuang Sathannasuk), National Health Security Office (NHSO), Thai Food and Drug Administration (Thai FDA), Comptroller General's Department (CGD) Civil Servant Medical Benefit Scheme, Social Security Office Health Insurance, and adjacent bodies.

The Thai system delivers universal coverage through three schemes: Universal Coverage Scheme (UCS, ~76% of population) administered by NHSO; Social Security Scheme (SSS, ~16%) administered by SSO; Civil Servant Medical Benefit Scheme (CSMBS, ~7%) administered by CGD. Ministry of Public Health (MoPH) owns ~70% of hospitals; the Bangkok Metropolitan Administration and Ministry of Defence also operate public hospitals; the private sector is significant.

## 2. Scope

In scope: Prime Minister; Minister of Public Health; Deputy Minister; Permanent Secretary MoPH; Director-General each department (Disease Control, Medical Services, Health Service Support, Mental Health, Health, Medical Sciences, Thai Traditional and Alternative Medicine, Health Department); Secretary-General Thai FDA; Secretary-General NHSO; Director Social Security Office Health Insurance; Director-General Department of Disease Control; Directors of major hospitals (Siriraj, Chulalongkorn, Ramathibodi, Rajavithi, King Chulalongkorn Memorial); Chair House Health Committee; Chair Senate Health and Sports Committee; President Thai Medical Council; President Thailand Nursing and Midwifery Council.

## 3. Structure

Standard 2/6/10/14. Ordering: PM Office → MoPH → NHSO → Thai FDA → SSO Health Insurance → CGD Civil Servant Scheme → major hospitals → Parliament committees → professional councils.

## 4. Field definitions

Party affiliation using canonical Thai abbreviations: `Bhumjaithai` (BJT — Anutin), `Pheu Thai` (PT), `People's Party` (PP — successor to Move Forward), `United Thai Nation` (UTN), `Palang Pracharath` (PPRP), `Democrat`, `Chartthaipattana`, `Klatham`. Titles in English with Thai where useful.

## 5. Provenance and dating

Anutin Charnvirakul (Bhumjaithai) was re-elected as 32nd Prime Minister on 19 March 2026 with 293 votes after the February 2026 snap election; his second cabinet was royally endorsed and sworn in on 6 April 2026 at Dusit Palace. The Bhumjaithai-Pheu Thai coalition allocates cabinet seats with Bhumjaithai holding the larger share. The Minister of Public Health in the second Anutin cabinet should be verified; Somsak Thepsuthin had been Minister of Public Health in the earlier Pheu Thai-led government.

## 6. Update workflow

Verify against thaigov.go.th, moph.go.th, nhso.go.th, fda.moph.go.th, parliament.go.th, Bangkok Post, The Nation Thailand, Thai PBS World, Khaosod, Matichon, Thairath, Prachatai English.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating MoPH as the only health buyer — NHSO, SSO and CGD are three distinct purchasers in the universal-coverage architecture.
- Importing NHS framings unmodified — Thailand has three statutory schemes and a substantial private market; reform asks must engage all three.

## 9. Acronym glossary

- **CGD** — Comptroller General's Department (administers CSMBS).
- **CSMBS** — Civil Servant Medical Benefit Scheme.
- **MoPH** — Ministry of Public Health.
- **NHSO** — National Health Security Office (UCS administrator).
- **SSO** — Social Security Office (SSS administrator).
- **Thai FDA** — Thai Food and Drug Administration.
- **UCS** — Universal Coverage Scheme.

## 10. Worked example

```yaml
      - Notes on Minister of Public Health:
          - Status: The second Anutin Charnvirakul (Bhumjaithai) cabinet was royally endorsed and sworn in on 6 April 2026 following Anutin's re-election as 32nd Prime Minister on 19 March 2026 with 293 votes. Cabinet seat allocations are shared between Bhumjaithai (the larger partner) and Pheu Thai (the junior coalition partner) with 35 cabinet members across 16 backing parties. The substantive identity of the Minister of Public Health in the second Anutin cabinet should be verified against thaigov.go.th and Bangkok Post coverage. Somsak Thepsuthin (Pheu Thai) had been Minister of Public Health under the earlier Srettha Thavisin and Paetongtarn Shinawatra governments; with Bhumjaithai now the senior partner, the portfolio likely transitioned to a Bhumjaithai or other coalition appointee.
          - Implication: Engagement should be routed through the Permanent Secretary MoPH, Secretary-General NHSO and Department-level Director-Generals until the substantive Minister is publicly confirmed and added to this register; coalition arithmetic suggests political volatility on Health-related decisions during the early Anutin II period.
```

## 11. Out-of-band notes

For roles unfilled or in transition. The Notes block above is used because the substantive Minister of Public Health identity in the second Anutin cabinet is not yet verifiable in this register as of June 2026.

## 12. Open questions

- Confirm identity and party affiliation of the Minister of Public Health in the second Anutin cabinet (sworn in 6 April 2026).
- Named Deputy Minister of Public Health with currency verified.
- Permanent Secretary MoPH and Director-Generals of MoPH departments with currency verified.
- Secretary-General Thai FDA and Secretary-General NHSO with currency verified.
- Director Social Security Office Health Insurance and Director CGD Civil Servant Scheme with currency verified.
- Directors of Siriraj, Chulalongkorn Hospital, Ramathibodi, Rajavithi with currency verified.
- Chair House Health Committee and Chair Senate Health and Sports Committee.
- President Thai Medical Council and Thailand Nursing and Midwifery Council with currency verified.
