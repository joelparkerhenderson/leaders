# spec.md — `leaders.yml`

Single source of truth for the Ugandan health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Ugandan Ministry of Health, the National Drug Authority (NDA), Uganda Virus Research Institute (UVRI), National Health Laboratory and Diagnostic Services (NHLDS), Central Public Health Laboratories (CPHL), Mulago National Referral Hospital, and adjacent bodies.

The Ugandan system is tax-funded universal access through MoH and the District Health Office system; the National Health Insurance Scheme is at pilot phase. PEPFAR / Global Fund / Gavi donor coordination is structural; the Aceng-era Ministry has prominent ebola, mpox, HIV response programmes.

## 2. Scope

In scope: President; PM; Minister of Health; Ministers of State (Primary Health Care; General Duties); Permanent Secretary; Director-General Health Services; CEO NDA; Director UVRI; Director NHLDS / CPHL; CEO Mulago National Referral Hospital; CEO Butabika National Referral Mental Hospital; District Health Officers; Parliament Health Committee Chair; Uganda Medical Association.

## 3. Structure

Standard. Ordering: President → PM → MoH → NDA → UVRI → NHLDS/CPHL → Mulago/Butabika → District Health Offices → Parliament Committee → UMA.

## 4. Field definitions

Party affiliation: `NRM` (National Resistance Movement — Museveni), `NUP` (National Unity Platform — Bobi Wine), `FDC`, `DP`, `PFF`, `UPC`, `JEEMA`. Titles in English.

## 5. Provenance and dating

Hon. Dr. Jane Ruth Aceng Ocero has served as Minister of Health since 2016 across two NRM terms; reaffirmed in 2026 elections context (launched re-election campaign for parliamentary seat November 2025); senior consultant pediatrician; MBChB, MMED (Pediatrics), MPH.

## 6. Update workflow

Verify against health.go.ug, statehouse.go.ug, parliament.go.ug, New Vision, Daily Monitor, Nile Post, Independent Uganda, NTV Uganda, Observer.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Importing US framings — Uganda is donor-funded universal access with HIV / TB / malaria vertical programmes structurally embedded.
- Ignoring district-level autonomy — District Health Offices manage substantial primary-care delivery.

## 9. Acronym glossary

- **CPHL** — Central Public Health Laboratories.
- **NDA** — National Drug Authority.
- **NHLDS** — National Health Laboratory and Diagnostic Services.
- **UVRI** — Uganda Virus Research Institute.

## 10. Worked example

```yaml
      - Hon. Dr. Jane Ruth Aceng Ocero (NRM):
          - Title: Minister of Health of the Republic of Uganda (since 2016)
          - Stakeholder engagement notes:
              - "Minister of Health since 2016 in the Museveni (NRM) government; across two consecutive terms — one of the longest-serving Ugandan ministers; pediatrician (Senior Consultant Pediatrician); MBChB, MMED (Pediatrics), MPH, Diploma in Public Administration and Management; born and politically based in Lira; launched re-election bid for parliamentary seat November 2025 (faces two opponents per New Vision)."
              - "Active 2026: announced Lubowa Specialized Hospital on track to open by end of 2026 (Nilepost); blocked UVRI from Ebola testing (Monitor) — controversial managerial intervention; applauded NHLDS for driving Uganda's diagnostic excellence; provided public Ebola updates."
              - "Led Uganda's pioneering Ebola Sudan virus response 2022; subsequent mpox and SARS-CoV-2 responses; Lubowa Specialised Hospital long-running tertiary-investment programme."
              - "Owns Ministry policy, NDA medicines regulation, UVRI / NHLDS / CPHL public-health laboratory network, Mulago National Referral Hospital, Butabika Mental Hospital, District Health Office coordination, NHIS pilot expansion, and Uganda's WHO Africa, EAC and AU CDC positioning."
              - "Hook: Ebola and Marburg outbreak preparedness, NHIS rollout, Lubowa Specialised Hospital, mental-health expansion (Butabika modernisation), HIV / TB / malaria vertical programmes, pharmaceutical localisation, and AU CDC / WHO Africa cooperation land."
          - Tone advice:
              - "Open with Ebola / Marburg preparedness, NHIS rollout, Lubowa Specialised Hospital and AU CDC cooperation — these are her sustained authored lines."
              - "Do not assume single-actor Ministry framing — District Health Offices and PEPFAR / Global Fund / Gavi donor coordination are structurally embedded; framings must include district-level and donor partners."
```

## 11. Out-of-band notes

For roles unfilled or in transition.

## 12. Open questions

- Named Ministers of State for Primary Health Care and General Duties under Aceng with currency verified.
- Permanent Secretary MoH and Director-General Health Services with currency verified.
- CEO NDA, Director UVRI, Director NHLDS / CPHL with currency verified.
- CEO Mulago National Referral Hospital and CEO Butabika National Referral Mental Hospital with currency verified.
- District Health Officers of major districts (Kampala, Wakiso, Mbarara, Gulu, Lira, Mbale).
- Parliament Health Committee Chair in the 11th Parliament.
- President Uganda Medical Association with currency verified.
