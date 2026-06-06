# spec.md — `leaders.yml`

Single source of truth for the Trinidad and Tobago health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Trinidad and Tobago Ministry of Health, the five Regional Health Authorities (NWRHA, NCRHA, ERHA, SWRHA, TRHA), the Pan American Health Organization country office, and adjacent bodies.

The TT system is tax-funded universal with low user fees through the five RHAs operating public hospitals and primary care. The Children's Life Fund supplements complex care. CARICOM and CARPHA frame regional health cooperation.

## 2. Scope

In scope: President; PM; Minister of Health; Parliamentary Secretary; Permanent Secretary; CMO; CEO NWRHA, NCRHA, ERHA, SWRHA; CEO TRHA (Tobago); CEO National Insurance Property Development Company (for hospital construction); Chair Joint Select Committee on Social Services and Public Administration; Medical Board of Trinidad and Tobago; T&T Medical Association.

## 3. Structure

Standard. Ordering: PM → Ministry → CMO → 5 RHAs → Children's Life Fund → Parliament committee → Medical Board.

## 4. Field definitions

Party affiliation: `PNM` (People's National Movement), `UNC` (United National Congress), `Patriotic Front`. Titles in English.

## 5. Provenance and dating

Dr. Lackram Bodoe is Minister of Health, MP for Oropouche West; medical doctor by profession. Confirmed in role as of February 2026.

## 6. Update workflow

Verify against health.gov.tt, opm.gov.tt, ttparliament.org, Trinidad Guardian, Trinidad Express, Newsday, Loop Trinidad.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating Ministry as the operational owner — RHAs run delivery.
- Importing US framings — TT is tax-funded universal with low user fees.

## 9. Acronym glossary

- **CARPHA** — Caribbean Public Health Agency.
- **ERHA** — Eastern Regional Health Authority.
- **NCRHA** — North Central Regional Health Authority.
- **NWRHA** — North West Regional Health Authority.
- **SWRHA** — South West Regional Health Authority.
- **TRHA** — Tobago Regional Health Authority.

## 10. Worked example

```yaml
      - Dr. Lackram Bodoe (UNC):
          - Title: Minister of Health, Trinidad and Tobago
          - Stakeholder engagement notes:
              - "Minister of Health, Trinidad and Tobago; MP for Oropouche West; medical doctor by profession; confirmed in role as of February 2026 (Ministry of Health official Facebook coverage of his feature address)."
              - "Owns Ministry policy, the five Regional Health Authorities (NWRHA, NCRHA, ERHA, SWRHA, TRHA), Children's Life Fund, primary-care strengthening, CARICOM and CARPHA cooperation; US bilateral health-cooperation announced US$6 million in health support to advance US health priorities in Trinidad and Tobago (US Embassy)."
              - "Hook: RHA modernisation, primary-care strengthening, NCDs, mental health, CARPHA cooperation, US bilateral health-cooperation, and oil-and-gas-revenue-funded health infrastructure land."
          - Tone advice:
              - "Open with RHA modernisation, primary care, NCDs and CARPHA cooperation — these are the political-priorities of the Ministry."
              - "Do not pitch as if Ministry could direct RHAs — RHAs operate with operational autonomy under statutory mandates."
```

## 11. Out-of-band notes

For roles unfilled or in transition.

## 12. Open questions

- Named Parliamentary Secretary and Permanent Secretary with currency verified.
- CMO Trinidad and Tobago with currency verified.
- CEOs of NWRHA, NCRHA, ERHA, SWRHA, TRHA with currency verified.
- Chair Joint Select Committee on Social Services and Public Administration with currency verified.
- President T&T Medical Association with currency verified.
