# spec.md — `leaders.yml`

Single source of truth for the Zambian health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Zambia Ministry of Health, Zambia Medicines Regulatory Authority (ZAMRA), National Health Insurance Management Authority (NHIMA), and adjacent bodies.

The Zambian system has National Health Insurance Scheme (NHIS) administered by NHIMA from 2018; Ministry runs public facilities through Provincial Health Offices in 10 provinces; UTH Lusaka is the main tertiary referral.

## 2. Scope

In scope: President; VP; Minister of Health; Permanent Secretary Technical; Permanent Secretary Administration; DG NHIMA; DG ZAMRA; DG Zambia National Public Health Institute (ZNPHI); CEO UTH; Provincial Health Office Directors; National Assembly Health Committee Chair; Medical Council of Zambia; General Nursing Council.

## 3. Structure

Standard. Ordering: President → VP → Ministry → NHIMA → ZAMRA → ZNPHI → UTH → 10 Provincial Health Offices → Parliament → MCZ.

## 4. Field definitions

Party affiliation: `UPND` (United Party for National Development — Hichilema), `PF` (Patriotic Front), `Tonse Alliance`. Titles in English.

## 5. Provenance and dating

Hon. Dr. Alex Katakwe was appointed Minister of Health by President Hakainde Hichilema on 13 March 2026 and sworn in 14 March 2026 (Lusaka Times), succeeding Hon. Dr. Elijah Julaki Muchima who was relieved of his duties 18 February 2026; Solwezi East MP; UPND.

## 6. Update workflow

Verify against moh.gov.zm, sh.gov.zm, parliament.gov.zm, Lusaka Times, Mwebantu, Zambian Observer, Open Zambia, Mast Newspaper.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Importing US framings — Zambia is donor-financed transitioning to NHIS-based universal coverage.
- Ignoring PEPFAR / Global Fund flows — donor coordination is structurally embedded.

## 9. Acronym glossary

- **NHIMA** — National Health Insurance Management Authority.
- **NHIS** — National Health Insurance Scheme.
- **UTH** — University Teaching Hospital (Lusaka).
- **ZAMRA** — Zambia Medicines Regulatory Authority.
- **ZNPHI** — Zambia National Public Health Institute.

## 10. Worked example

```yaml
      - Hon. Dr. Alex Katakwe (UPND):
          - Title: Minister of Health of Zambia (since 13 March 2026)
          - Stakeholder engagement notes:
              - "Minister of Health appointed by President Hakainde Hichilema on 13 March 2026 (State House press release) and sworn in 14 March 2026 (Lusaka Times); UPND; MP for Solwezi East; succeeded Hon. Dr. Elijah Julaki Muchima who was relieved of his duties 18 February 2026."
              - "Owns Ministry policy, NHIMA NHIS rollout, ZAMRA medicines regulation, ZNPHI public-health institute, UTH and provincial hospital network coordination, drug-availability priority (President Hichilema specifically directed the new Minister of Health to ensure drug availability in hospitals per Mwebantu), and Zambia's WHO Africa, SADC and AU CDC positioning."
              - "Hook: drug-availability emergency response (presidential directive), NHIS expansion, mpox preparedness, HIV / TB / malaria post-PEPFAR-changes continuity, hospital modernisation, and SADC cooperation land."
          - Tone advice:
              - "Open with drug-availability, NHIS, HIV continuity post-PEPFAR and SADC cooperation — these are the priorities under presidential directive and the early-mandate focus."
              - "Do not assume political stability of the Health portfolio — the February 2026 dismissal suggests the role is under active political pressure; long-horizon commitments must be calibrated."
```

## 11. Out-of-band notes

For roles unfilled or in transition.

## 12. Open questions

- Named Permanent Secretaries Technical and Administration under Katakwe with currency verified.
- DG NHIMA, DG ZAMRA, DG ZNPHI with currency verified.
- CEO UTH Lusaka with currency verified.
- Provincial Health Office Directors of 10 provinces with currency verified.
- National Assembly Health Committee Chair with currency verified.
- President Medical Council of Zambia and General Nursing Council with currency verified.
