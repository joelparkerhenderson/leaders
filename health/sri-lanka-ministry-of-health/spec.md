# spec.md — `leaders.yml`

Single source of truth for the Sri Lankan health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Sri Lankan Ministry of Health and Mass Media, the National Medicines Regulatory Authority (NMRA), the State Pharmaceutical Corporation (SPC), the Family Health Bureau, and adjacent bodies.

The Sri Lankan system is tax-funded universal: the Ministry runs a national network of teaching, provincial, district and divisional hospitals plus primary medical care units (PMCUs) and Medical Officer of Health (MOH) divisions for community health. Provincial Departments of Health Services administer regionally. Sri Lanka has historically achieved strong health outcomes despite low spending, but the 2022-2023 economic crisis severely strained the system.

## 2. Scope

In scope: President; Prime Minister; Minister of Health and Mass Media; State Minister of Health; Secretary Ministry of Health; Director-General Health Services; Deputy Directors-General; Director NMRA; Chairman SPC; Director Family Health Bureau; Provincial Directors of Health Services; Director National Hospital Sri Lanka (NHSL); CMO Lady Ridgeway Hospital; Chair Parliamentary Sectoral Oversight Committee on Health; Sri Lanka Medical Association; College of Pharmacists; Sri Lanka Nurses Association.

## 3. Structure

Standard 2/6/10/14. Ordering: Presidency → Ministry of Health → NMRA → SPC → Family Health Bureau → Provincial Departments → NHSL and tertiary hospitals → Parliament Sectoral Committee → professional bodies.

## 4. Field definitions

Party affiliation using canonical Sri Lankan abbreviations: `NPP` (National People's Power — Dissanayake; includes JVP / Janatha Vimukthi Peramuna), `SJB` (Samagi Jana Balawegaya), `SLPP` (Sri Lanka Podujana Peramuna), `UNP` (United National Party), `TNA`, `ITAK`, `EPDP`. Titles in English (with Sinhala / Tamil where used).

## 5. Provenance and dating

Dr. Nalinda Jayatissa (NPP / JVP) has served as Minister of Health and Mass Media, Chief Government Whip and Cabinet Spokesperson since November 2024 in the Anura Kumara Dissanayake (NPP) government formed after the September 2024 presidential election and the subsequent November 2024 parliamentary election that gave the NPP a supermajority. Medical doctor; long-time JVP figure; MP for Kalutara District.

## 6. Update workflow

Verify against health.gov.lk, presidentsoffice.gov.lk, nmra.gov.lk, spc.gov.lk, parliament.lk, Daily Mirror, Daily FT, Sunday Times, NewsFirst, Ada Derana, Lanka Mission to UN Geneva.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Importing NHS framings unmodified — Sri Lanka is tax-funded universal Beveridgean but with provincial administrative structures.
- Ignoring the post-2022-economic-crisis context — Sri Lanka's recovery is shaping every health-policy decision.

## 9. Acronym glossary

- **JVP** — Janatha Vimukthi Peramuna (People's Liberation Front; the historical core of NPP).
- **MOH** — Medical Officer of Health.
- **NHSL** — National Hospital of Sri Lanka.
- **NMRA** — National Medicines Regulatory Authority.
- **NPP** — National People's Power (Dissanayake-led coalition).
- **PMCU** — Primary Medical Care Unit.
- **SPC** — State Pharmaceuticals Corporation.

## 10. Worked example

```yaml
      - Dr. Nalinda Jayatissa (NPP / JVP):
          - Title: Minister of Health and Mass Media, Chief Government Whip and Cabinet Spokesperson (since November 2024)
          - Stakeholder engagement notes:
              - "Minister of Health and Mass Media, Chief Government Whip and Cabinet Spokesperson since November 2024 in the Anura Kumara Dissanayake (NPP) government formed after the September 2024 presidential election and the November 2024 parliamentary election that gave the NPP a supermajority; NPP / JVP; medical doctor; MP for Kalutara District; long-time JVP figure with parliamentary and public-policy experience."
              - "Delivered the national statement at the General Discussion of the 79th World Health Assembly in Geneva on 19 May 2026 — first major international-platform appearance as Minister, articulating the NPP government's health-policy direction including universal health coverage, prevention and equity."
              - "Active in international engagement: attended Tarique Rahman's oath ceremony in Bangladesh (February 2026); maintains visible posture on the Mass Media portfolio alongside Health, dual brief unusual for a Health Minister."
              - "Owns the post-2022-economic-crisis reconstruction of medicine supply, the NMRA reform agenda, SPC stabilisation, restoration of cancer-care services, oncology drugs procurement, maternal-and-child health continuation, NCD strategy, and the JVP / NPP equity-focused public-health framing."
              - "Hook: medicine supply restoration, oncology drugs, NCDs, maternal-and-child health continuation, primary-care strengthening, NMRA reform, climate-and-health, and South Asian / SAARC cooperation land."
          - Tone advice:
              - "Open with medicine supply restoration, oncology drugs and equity-focused public health — these are post-crisis priorities and the NPP / JVP frame."
              - "Do not pitch with private-sector-led framings as the default — the NPP government's emerging public-health line emphasises public provision and equity; private-led framings will be politically discounted."
```

## 11. Out-of-band notes

For roles unfilled or in transition.

## 12. Open questions

- Named State Minister of Health and Secretary Ministry of Health under Jayatissa with currency verified.
- Director-General Health Services and Deputy Directors-General with currency verified.
- Director NMRA, Chairman SPC, Director Family Health Bureau with currency verified.
- Provincial Directors of Health Services for the nine provinces.
- Director NHSL and CMO Lady Ridgeway Hospital with currency verified.
- Chair Parliamentary Sectoral Oversight Committee on Health in the current 10th Parliament.
- Sri Lanka Medical Association, College of Pharmacists, Sri Lanka Nurses Association presidents with currency verified.
