# spec.md — `leaders.yml`

Single source of truth for the Maldives health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Maldives Ministry of Health, Aasandha health insurance scheme (universal coverage), Maldives Food and Drug Authority (MFDA), Indira Gandhi Memorial Hospital (IGMH), and adjacent bodies.

The Maldives system has Aasandha universal coverage; MoH runs the public network across dispersed atolls; IGMH is the main referral.

## 2. Scope

In scope: President Mohamed Muizzu; Vice President; Minister of Health; State Ministers; Permanent Secretary; CEO Aasandha; CEO MFDA; CEO IGMH; Health Atoll-level coordinators; People's Majlis Social Affairs Committee; Maldives Medical and Dental Council.

## 3. Structure

Standard.

## 4. Field definitions

Party affiliation: `PNC` (People's National Congress — Muizzu), `MDP` (Maldivian Democratic Party — Solih), `JP` (Jumhooree Party). Titles in English / Dhivehi.

## 5. Provenance and dating

The Muizzu (PNC) government formed in November 2023. Health Minister Dr. Abdulla Khaleel served 2023-2024 then moved to Foreign Affairs. Abdulla Nazim Ibrahim served as Health Minister but resigned en masse with nine other cabinet ministers on 14 April 2026. Substantive Minister of Health post-14-April-2026 to be verified.

## 6. Update workflow

Verify against presidency.gov.mv, health.gov.mv, parliament.mv, Maldives Independent, Sun Online, Avas, Mihaaru.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Importing US framings — Maldives is universal coverage with significant private hospital sector and donor coordination.

## 9. Acronym glossary

- **Aasandha** — universal-coverage health-insurance scheme.
- **IGMH** — Indira Gandhi Memorial Hospital.
- **MFDA** — Maldives Food and Drug Authority.

## 10. Worked example

```yaml
      - Notes on Minister of Health:
          - Status: The Maldives Health Minister position has experienced rapid turnover in the Muizzu (PNC) government. Dr. Abdulla Khaleel served as Minister of Health 2023-2024 before moving to Foreign Affairs in 2024. Abdulla Nazim Ibrahim subsequently served as Health Minister but resigned en masse along with nine other cabinet ministers on 14 April 2026 in a political-instability episode. The substantive identity of the Minister of Health post-14-April-2026 should be verified against presidency.gov.mv and Maldivian media.
          - Implication: Engagement on the Maldives health portfolio should be routed via the Permanent Secretary, CEO Aasandha, and CEO IGMH until the substantive Minister identity is publicly confirmed.
```

## 11. Out-of-band notes

For roles unfilled or in transition.

## 12. Open questions

- Substantive identity of Minister of Health post-14-April-2026 cabinet resignations.
- Named State Ministers and Permanent Secretary under any new Minister.
- CEO Aasandha, CEO MFDA, CEO IGMH with currency verified.
- Health atoll-level coordinators for major atolls.
- People's Majlis Social Affairs Committee Chair with currency verified.
- President Maldives Medical and Dental Council with currency verified.
