# spec.md — `leaders.yml`

Single source of truth for the Philippine health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Philippine Department of Health (DOH), Philippine Health Insurance Corporation (PhilHealth), Food and Drug Administration (FDA), Department of Science and Technology – Philippine Council for Health Research and Development (PCHRD), and adjacent bodies.

The Philippine system is operationally devolved to Local Government Units (LGUs) since 1991 but is being recentralised under the Universal Health Care (UHC) Law of 2019. DOH sets policy; PhilHealth administers the National Health Insurance Program (NHIP) as single payer; FDA regulates medicines; LGUs run public hospitals and rural health units. The transition under UHC includes Province-wide and City-wide Integrated Health Systems.

## 2. Scope

In scope: President; Department of Health Secretary; Undersecretaries; Assistant Secretaries; Director-General Food and Drug Administration; President and CEO PhilHealth; Director Bureau of Quarantine; Director Research Institute for Tropical Medicine; Heads of DOH Centers for Health Development (17 regions); Chair House Committee on Health; Chair Senate Committee on Health and Demography; President Philippine Medical Association; President Philippine Nurses Association; President Integrated Pharmacists Association.

## 3. Structure

Standard 2/6/10/14. Ordering: Office of the President → DOH → PhilHealth → FDA → RITM / BoQ → DOH CHD regions → Congress committees → professional associations.

## 4. Field definitions

Party affiliation using canonical Philippine abbreviations: `PFP` (Partido Federal ng Pilipinas — Marcos), `Lakas-CMD`, `PDP-Laban`, `NPC`, `NUP`, `Liberal Party`, `Akbayan`, `Makabayan`. Titles in English.

## 5. Provenance and dating

Dr. Teodoro 'Ted' J. Herbosa was appointed Secretary of Health by President Bongbong Marcos on 5 June 2023, took oath the following day. Continues in 2026; in January 2026 he dismissed rumours of his replacement. In July 2025 he and five other DOH officials were charged with corruption cases over P44.6 million worth of mental-health drugs at the Office of the Ombudsman; matter ongoing.

## 6. Update workflow

Verify against doh.gov.ph, op.gov.ph, philhealth.gov.ph, fda.gov.ph, congress.gov.ph, senate.gov.ph, Philippine Daily Inquirer, Manila Bulletin, Rappler, ABS-CBN, GMA News, Manila Times.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Ignoring LGU operational autonomy — even under UHC, LGUs retain significant authority over local health delivery.
- Importing US framings unmodified — the Philippines has single-payer NHIP via PhilHealth with mixed delivery, large OFW remittance health-financing flows, and a substantial private hospital sector.

## 9. Acronym glossary

- **CHD** — Center for Health Development (DOH regional office).
- **DOH** — Department of Health.
- **FDA** — Food and Drug Administration.
- **HFEP** — Health Facilities Enhancement Program.
- **LGU** — Local Government Unit.
- **NHIP** — National Health Insurance Program.
- **PCHRD** — Philippine Council for Health Research and Development.
- **PhilHealth / PHIC** — Philippine Health Insurance Corporation.
- **RITM** — Research Institute for Tropical Medicine.
- **UHC** — Universal Health Care Act (2019).

## 10. Worked example

```yaml
      - Dr. Teodoro 'Ted' J. Herbosa (PFP-aligned, technocrat):
          - Title: Secretary of Health (since 6 June 2023)
          - Stakeholder engagement notes:
              - "Secretary of Health appointed by President Bongbong Marcos on 5 June 2023; took oath 6 June 2023; physician (general surgery and emergency medicine background); previously DOH-Officer-in-Charge during the early Covid-19 pandemic and Senior Adviser on Covid-19 response."
              - "In January 2026 dismissed rumours of his replacement ('there's no truth to that'; no Cabinet revamp per Manila Bulletin and Inquirer); maintained position through political-cycle speculation."
              - "Faced corruption charges July 2025 with five other DOH officials over alleged irregularities in P44.6 million of mental-health drug allocations to the Rotary Club of Quezon City; case proceedings before the Office of the Ombudsman are ongoing and have not removed him from office."
              - "Owns UHC implementation (Province- and City-wide Integrated Health Systems), PhilHealth premium and benefits design, FDA regulation, the national vaccine programme (post-Dengvaxia trust-rebuilding), HFEP infrastructure investment, and Philippine WHO WPRO and ASEAN positioning."
              - "Hook: UHC implementation, PhilHealth benefits expansion, mental health (the Bayanihan to Heal as One context), Universal Mental Health Act implementation, climate and health, dengue, HIV / AIDS, and pharmacy access aterrissent."
          - Tone advice:
              - "Open with UHC implementation, PhilHealth benefits, mental health, vaccine confidence rebuilding and climate-health — these are Herbosa's sustained 2025-2026 priorities."
              - "Do not assume LGU compliance — even with UHC the LGUs retain significant operational discretion; framings that bypass LGUs at scale will be redirected."
```

## 11. Out-of-band notes

For roles unfilled or in transition.

## 12. Open questions

- Named Undersecretaries and Assistant Secretaries of Health under Herbosa with currency verified.
- Director-General FDA and President-CEO PhilHealth with currency verified.
- Director Bureau of Quarantine, Director RITM with currency verified.
- Heads of DOH Centers for Health Development for NCR, Calabarzon, Central Luzon, Western Visayas, Central Visayas, Davao with currency verified.
- Chair House Committee on Health and Chair Senate Committee on Health and Demography with currency verified.
- President Philippine Medical Association, Philippine Nurses Association, Integrated Pharmacists Association with currency verified.
