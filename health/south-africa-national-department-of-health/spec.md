# spec.md — `leaders.yml`

Single source of truth for the South African health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the South African National Department of Health (NDoH), nine provincial Departments of Health, South African Health Products Regulatory Authority (SAHPRA), National Institute for Communicable Diseases (NICD), Council for Medical Schemes (CMS), and adjacent bodies.

The South African system is constitutionally divided: NDoH sets national norms; the nine provincial Departments of Health own public-sector delivery; the private sector covers ~16% of the population via medical schemes regulated by CMS. The 2024 National Health Insurance (NHI) Act was signed into law as the framework for universal coverage; implementation is multi-year and politically contested by medical schemes and DA-led provinces.

## 2. Scope

In scope: President; Deputy President; Minister of Health; Deputy Minister of Health; Director-General Health; CEO SAHPRA; Executive Director NICD; CEO CMS; CEO Office of Health Standards Compliance (OHSC); CEO National Health Laboratory Service (NHLS); MECs (Member of the Executive Council) for Health in the nine provinces (Gauteng, KwaZulu-Natal, Western Cape, Eastern Cape, Limpopo, North West, Mpumalanga, Free State, Northern Cape); HoDs of provincial DoHs; Chair Portfolio Committee on Health in the National Assembly; Chair Select Committee on Health and Social Services NCOP; SA Medical Association; DENOSA; SA Pharmacy Council; Health Professions Council of SA (HPCSA).

## 3. Structure

Standard 2/6/10/14. Ordering: Presidency → NDoH → SAHPRA → NICD → CMS → OHSC → NHLS → 9 provincial DoHs → Parliament committees → professional bodies.

## 4. Field definitions

Party affiliation using canonical South African abbreviations: `ANC`, `DA` (Democratic Alliance), `MK` (uMkhonto we Sizwe), `EFF` (Economic Freedom Fighters), `IFP`, `PA` (Patriotic Alliance), `FF+` (Vryheidsfront Plus), `UDM`, `Rise Mzansi`, `ActionSA`, `ATM`, `Al Jama-ah`. Titles in English (or Afrikaans / Zulu where used).

## 5. Provenance and dating

Dr. Pakishe Aaron Motsoaledi (ANC) was appointed Minister of Health on 3 July 2024 in the Government of National Unity (GNU) following the May 2024 election that produced the ANC-DA-IFP-PA-led coalition; previously served as Minister of Health 2009-2019 and Minister of Home Affairs 2019-2024 — returning to the Health portfolio. In May 2026 he briefed Parliament on Hantavirus implications; on 5 June 2026 tabled the department's 2026/27 budget vote in the NCOP and revealed 11 infrastructure bids; on 6 February 2026 met newly appointed Provincial HoDs.

## 6. Update workflow

Verify against health.gov.za, gov.za, parliament.gov.za, news.gov.za, IOL, News24, Daily Maverick, Mail & Guardian, Bhekisisa, Spotlight, GroundUp.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating NDoH as the only counterparty — provincial DoHs own delivery and many provinces (especially WC under DA) have independent reform agendas.
- Importing US framings unmodified — South Africa has a constitutionally devolved system, private-medical-schemes market and the contested NHI Act framework.

## 9. Acronym glossary

- **CMS** — Council for Medical Schemes.
- **DENOSA** — Democratic Nursing Organisation of South Africa.
- **GNU** — Government of National Unity (post-2024 election).
- **HoD** — Head of Department (provincial).
- **HPCSA** — Health Professions Council of South Africa.
- **MEC** — Member of the Executive Council (provincial minister-equivalent).
- **NCOP** — National Council of Provinces.
- **NDoH** — National Department of Health.
- **NHI** — National Health Insurance Act (2024).
- **NHLS** — National Health Laboratory Service.
- **NICD** — National Institute for Communicable Diseases.
- **OHSC** — Office of Health Standards Compliance.
- **SAHPRA** — South African Health Products Regulatory Authority.
- **SAMA** — South African Medical Association.

## 10. Worked example

```yaml
      - Dr. Pakishe Aaron Motsoaledi (ANC):
          - Title: Minister of Health (since 3 July 2024, in the Government of National Unity)
          - Stakeholder engagement notes:
              - "Minister of Health since 3 July 2024 in the Government of National Unity (GNU) formed after the May 2024 election; ANC; medical doctor; returning to the Health portfolio he held 2009-2019 before serving as Minister of Home Affairs 2019-2024 — institutionally distinctive continuity."
              - "On 5 June 2026 tabled the 2026/27 budget vote for the National Department of Health in the NCOP, revealing 11 bids to enhance healthcare infrastructure (IOL coverage); on 6 May 2026 briefed Parliament on Hantavirus implications (TimesLIVE); on 6 February 2026 met the newly appointed Provincial HoDs of Health."
              - "Owns the implementation of the National Health Insurance Act (signed May 2024), the response to private-medical-schemes legal challenges to NHI, oversight of SAHPRA, NICD, OHSC, NHLS, and the post-2024-election GNU coalition negotiations on health-policy direction."
              - "Hook: NHI implementation, HIV / TB programmes (South Africa has the world's largest HIV cohort), Hantavirus and outbreak preparedness, infrastructure investment, healthcare workforce, mental health, NCDs and obesity, and BRICS+ health-cooperation land."
              - "Tradeoffs: DA holds Western Cape and is in coalition; DA-led provinces and medical-schemes industry have challenged NHI implementation in court — coalition politics are core to NHI rollout."
          - Tone advice:
              - "Open with NHI implementation, HIV / TB, outbreak preparedness, healthcare infrastructure and workforce — these are Motsoaledi's authored, sustained policy lines across his multi-term ministerial career."
              - "Do not pitch as if the GNU were a single-party government — the ANC-DA dynamic shapes every health-policy decision; framings that ignore coalition complexity will fail."
```

## 11. Out-of-band notes

For roles unfilled or in transition.

## 12. Open questions

- Named Deputy Minister of Health under Motsoaledi with currency verified.
- Director-General Health under Motsoaledi with currency verified.
- CEO SAHPRA, Executive Director NICD, CEO CMS, CEO OHSC, CEO NHLS with currency verified.
- MECs for Health in all nine provinces with currency verified (particularly Gauteng, KZN, WC, EC).
- HoDs of provincial Departments of Health.
- Chair Portfolio Committee on Health (National Assembly) and Chair Select Committee on Health and Social Services (NCOP).
- President SAMA, DENOSA, SA Pharmacy Council, HPCSA with currency verified.
