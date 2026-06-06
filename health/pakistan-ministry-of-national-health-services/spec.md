# spec.md — `leaders.yml`

Single source of truth for the Pakistani health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Ministry of National Health Services, Regulations and Coordination (NHSRC) at federal level, provincial Health Departments, DRAP (Drug Regulatory Authority of Pakistan), and adjacent bodies.

The Pakistani system is constitutionally devolved since the 18th Amendment (2010): Health is principally a provincial subject. The federal Ministry of NHSRC retains national coordination, immunisation, regulatory functions (DRAP), and Islamabad delivery. Provincial Departments of Health own delivery in Punjab, Sindh, Khyber Pakhtunkhwa and Balochistan; AJK and Gilgit-Baltistan have their own structures. Sehat Sahulat Programme provides social-health-insurance-style coverage in several provinces.

## 2. Scope

In scope: Prime Minister; Federal Minister NHSRC; Minister of State NHSRC; Secretary NHSRC; CEO DRAP; Director General Health; Federal Director of Health (Islamabad); Provincial Health Ministers and Secretaries of Punjab, Sindh, KP, Balochistan; AJK and GB Health Ministers; Chair National Assembly Standing Committee on NHSRC; Chair Senate Standing Committee on NHSRC; President Pakistan Medical Association (PMA); President Pakistan Nursing Council.

## 3. Structure

Standard 2/6/10/14. Ordering: PM Office → NHSRC → DRAP → Provincial Health Departments (Punjab, Sindh, KP, Balochistan) → AJK and GB → Parliament committees → professional bodies.

## 4. Field definitions

Party affiliation using canonical Pakistani abbreviations: `PML-N` (Pakistan Muslim League — Nawaz), `PPP` (Pakistan People's Party), `PTI` (Pakistan Tehreek-e-Insaf), `MQM-P`, `JUI-F`, `BAP`, `IPP`, `PML-Q`, `ANP`, `BNP-M`, `GDA`. Titles in English (or Urdu where used officially).

## 5. Provenance and dating

Syed Mustafa Kamal serves as Federal Minister for National Health Services, Regulations and Coordination in the Shehbaz Sharif (PML-N) coalition government formed after the February 2024 general election.

## 6. Update workflow

Verify against nhsrc.gov.pk, pmo.gov.pk, dra.gov.pk, na.gov.pk, senate.gov.pk, Dawn, Express Tribune, The News International, Geo, ARY, Pakistan Today.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating Health as a federally controlled subject — the 18th Amendment devolved health principally to provinces.
- Importing NHS framings unmodified — Pakistan has a mixed system with strong provincial autonomy, large private sector (~70% out-of-pocket spending), and emerging Sehat Sahulat insurance scheme.

## 9. Acronym glossary

- **18th Amendment** — 2010 constitutional amendment that devolved many subjects, including health, to provinces.
- **AJK** — Azad Jammu and Kashmir.
- **DRAP** — Drug Regulatory Authority of Pakistan.
- **GB** — Gilgit-Baltistan.
- **NHSRC** — Ministry of National Health Services, Regulations and Coordination.
- **PMA** — Pakistan Medical Association.
- **Sehat Sahulat Programme** — provincial / federal social-health-insurance-style coverage programme.

## 10. Worked example

```yaml
      - Syed Mustafa Kamal (MQM-P):
          - Title: Federal Minister for National Health Services, Regulations and Coordination (in the Shehbaz Sharif PML-N coalition government)
          - Stakeholder engagement notes:
              - "Federal Minister for National Health Services, Regulations and Coordination in the Shehbaz Sharif (PML-N) coalition government formed after the February 2024 general election; MQM-Pakistan; previously Mayor of Karachi 2005-2010 and founder of Pak Sarzameen Party before its merger back into MQM-P."
              - "Owns federal-level coordination of immunisation (EPI), Polio Eradication Programme, DRAP regulatory functions, Islamabad Capital Territory health delivery, and federal-provincial coordination through the Council of Common Interests on cross-cutting health issues."
              - "Hook: Polio Eradication (Pakistan and Afghanistan remain the last two endemic countries), EPI strengthening, Sehat Sahulat federal continuation, DRAP reform, climate-health (post-2022 floods), maternal-and-child health, and Karachi-specific urban-health programmes land."
          - Tone advice:
              - "Lead with Polio Eradication, EPI, DRAP and Karachi urban-health — these are federally meaningful levers given the 18th-Amendment devolution and Mustafa Kamal's MQM-P / Karachi political base."
              - "Do not pitch as if delivery decisions were federal — provincial Health Departments own delivery; Punjab and Sindh in particular have independent reform agendas."
```

## 11. Out-of-band notes

For roles unfilled or in transition.

## 12. Open questions

- Confirm Mustafa Kamal's date of appointment and any changes in the coalition cabinet through 2026.
- Named Minister of State NHSRC and Secretary NHSRC under Mustafa Kamal with currency verified.
- CEO DRAP and Director General Health with currency verified.
- Provincial Health Ministers and Secretaries of Punjab, Sindh, KP, Balochistan with currency verified.
- AJK and GB Health Ministers with currency verified.
- Chair National Assembly Standing Committee on NHSRC and Chair Senate Standing Committee on NHSRC.
- President PMA, Pakistan Nursing Council, and Pakistan Pharmacists Association.
