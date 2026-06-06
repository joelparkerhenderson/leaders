# spec.md — `leaders.yml`

Single source of truth for the Uzbek health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Uzbekistan Ministry of Health, State Sanitary and Epidemiological Welfare Service, Republican Clinical Hospitals, Tashkent Medical Academy hospitals, and adjacent bodies.

The Uzbek system is undergoing reform under Mirziyoyev's modernisation programme; State Health Insurance Fund piloting; significant donor and BRICS+ partnerships.

## 2. Scope

In scope: President Mirziyoyev; PM; Minister of Health; Deputy Ministers; DG State Sanitary and Epidemiological Welfare Service; Heads of Republican Clinical Hospitals (Tashkent, Republican Cancer Center, Republican Cardiac Center); Heads of 14 oblast Health Departments; Oliy Majlis Health Committee; Uzbekistan Medical Association.

## 3. Structure

Standard.

## 4. Field definitions

Party affiliation: `UzLiDeP` (Uzbekistan Liberal-Democratic Party — Mirziyoyev), `O'zMTDP`, others. Titles in English / Uzbek.

## 5. Provenance and dating

Eldor Adilov appointed Minister of Health in May 2026 (UzDaily, Gazeta.uz, Zamin.uz coverage), succeeding Asilbek Khudayarov who led the Ministry from November 2024 (acting from January 2024) before being transferred to another position; substantive cabinet reshuffle in the Mirziyoyev government.

## 6. Update workflow

Verify against gov.uz, hukumat.uz, ssv.uz, gazeta.uz, uzdaily.uz, zamin.uz, Daryo, Kun.uz.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Importing US framings — Uzbekistan is reform-orientated mandatory-insurance-piloting with significant Russia / China / Korea / Turkey bilateral partnerships.

## 9. Acronym glossary

- **Oliy Majlis** — Uzbek parliament.
- **UzLiDeP** — Uzbekistan Liberal-Democratic Party.

## 10. Worked example

```yaml
      - Eldor Adilov:
          - Title: Minister of Health of the Republic of Uzbekistan (since May 2026)
          - Stakeholder engagement notes:
              - "Minister of Health appointed in May 2026 (UzDaily) succeeding Asilbek Khudayarov who led the Ministry from November 2024 (acting from January 2024) and was transferred to another position (Gazeta.uz; Zamin.uz reshuffle coverage); part of the Mirziyoyev modernisation cabinet reform direction."
              - "Owns Ministry policy, State Sanitary and Epidemiological Welfare Service oversight, Republican Clinical Hospitals coordination (Tashkent, Republican Cancer Center, Republican Cardiac Center, Republican Children's Hospital), 14 oblast Health Departments, State Health Insurance Fund piloting and rollout, and Uzbekistan's WHO Europe, SCO, ECO and CIS health diplomacy."
              - "Hook: State Health Insurance Fund rollout, Mirziyoyev modernisation reform implementation, oncology and cardiology centres of excellence, primary-care strengthening, SCO and BRICS+ cooperation, and Aral Sea legacy health programmes."
          - Tone advice:
              - "Open with State Health Insurance Fund, modernisation reform, SCO cooperation and Aral Sea programmes — these are sustained Uzbek priorities."
              - "Do not pitch with single-bloc framings — Uzbekistan pragmatically balances Russia / China / EU / US / Korea / Türkiye / Iran partnerships."
```

## 11. Out-of-band notes

For roles unfilled or in transition.

## 12. Open questions

- Confirm Eldor Adilov's biographical detail, prior roles, and exact decree of appointment.
- Named Deputy Ministers under Adilov with currency verified.
- DG State Sanitary and Epidemiological Welfare Service with currency verified.
- Heads of Republican Clinical Hospitals with currency verified.
- Heads of 14 oblast Health Departments with currency verified.
- Oliy Majlis Health Committee Chair with currency verified.
- President Uzbekistan Medical Association with currency verified.
