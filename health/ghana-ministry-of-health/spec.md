# spec.md — `leaders.yml`

Single source of truth for the Ghanaian health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Ghanaian Ministry of Health (MoH), Ghana Health Service (GHS), National Health Insurance Authority (NHIA), Food and Drugs Authority (FDA), Pharmacy Council, and adjacent bodies.

The Ghanaian system has the NHIS covering ~50% of the population; MoH sets policy; GHS runs the public service through 16 Regional Health Directorates and 261 District Health Directorates and Christian Health Association of Ghana (CHAG)-affiliated mission facilities; FDA regulates medicines. The Mahama NDC government rolled out a Free Primary Healthcare policy starting 2026 with 150 districts in phase one.

## 2. Scope

In scope: President; Minister of Health; Deputy Ministers; Chief Director MoH; Director-General GHS; CEO NHIA; CEO FDA; Heads of major teaching hospitals (Korle Bu, Komfo Anokye, Tamale, Cape Coast, Ho); Regional Directors of Health Services (16); Chair Parliament Committee on Health; Ghana Medical Association; Ghana Registered Nurses and Midwives Association; Pharmaceutical Society of Ghana; Christian Health Association of Ghana (CHAG).

## 3. Structure

Standard. Ordering: Presidency → MoH → GHS → NHIA → FDA → Pharmacy Council → teaching hospitals → 16 Regional Directorates → CHAG → Parliament committee → professional associations.

## 4. Field definitions

Party affiliation using canonical Ghanaian abbreviations: `NDC` (National Democratic Congress), `NPP` (New Patriotic Party), `CPP`, `PNC`. Titles in English.

## 5. Provenance and dating

Hon. Kwabena Mintah Akandoh (NDC, MP Juaboso) was sworn in as Minister of Health by President John Dramani Mahama in February 2025, following the NDC's victory in the December 2024 election; previously Ranking Member on Parliament's Health Committee. Active 2026 on Free Primary Healthcare policy implementation.

## 6. Update workflow

Verify against moh.gov.gh, presidency.gov.gh, ghs.gov.gh, nhis.gov.gh, fda.gov.gh, parliament.gh, GhanaWeb, MyJoyOnline, Daily Graphic, Citi Newsroom, Modern Ghana, Ghana Health Nest.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating MoH as the operational owner — GHS runs delivery; CHAG covers significant rural and mission-affiliated provision.
- Importing NHS framings unmodified — Ghana has NHIS social insurance with mixed delivery and pioneering 1992 NHIS Act lineage.

## 9. Acronym glossary

- **CHAG** — Christian Health Association of Ghana.
- **FDA** — Food and Drugs Authority.
- **GHS** — Ghana Health Service.
- **NHIA** — National Health Insurance Authority.
- **NHIS** — National Health Insurance Scheme.

## 10. Worked example

```yaml
      - Hon. Kwabena Mintah Akandoh (NDC):
          - Title: Minister of Health (since February 2025, in the John Mahama NDC government)
          - Stakeholder engagement notes:
              - "Minister of Health sworn in by President John Dramani Mahama in February 2025, following the NDC's victory in the December 2024 presidential election; NDC; MP for Juaboso since 2013; previously Ranking Member on Parliament's Health Committee — extensive parliamentary health-portfolio background; Gavi board member representing Ghana / WHO Africa Region."
              - "Active 2026: announced government will roll out flagship Free Primary Healthcare policy in phases between 2026 and 2028 starting with 150 districts in phase one (Citi Newsroom April 2026; ModernGhana); pushed for global health equity at the 79th World Health Assembly in Geneva on 19 May 2026 (GhanaWeb); charged GHS to drive implementation."
              - "Owns Ministry policy and Free PHC rollout, NHIS expansion and financial sustainability under the renewed NDC mandate, GHS delivery oversight, FDA regulation, the Agenda 111 hospitals legacy (NPP-era programme inherited), Korle Bu and Komfo Anokye Teaching Hospitals, and Ghana's WHO Africa and ECOWAS health diplomacy."
              - "Hook: Free Primary Healthcare policy implementation, NHIS expansion, primary-care strengthening, NCDs, mental health, maternal-and-child health, vaccine self-reliance, climate-and-health, and CHAG partnership land."
          - Tone advice:
              - "Open with Free Primary Healthcare policy, NHIS expansion, primary-care strengthening and the NDC equity frame — these are Akandoh's authored 2026 priorities and the political signature of the Mahama administration."
              - "Do not pitch as if the NPP Agenda 111 programme were abandoned — the inheritance of unfinished hospitals is a complex political-management challenge; framings must respect both legacies."
```

## 11. Out-of-band notes

For roles unfilled or in transition.

## 12. Open questions

- Named Deputy Ministers of Health under Akandoh with currency verified.
- Chief Director Ministry of Health and Director-General GHS with currency verified.
- CEO NHIA, CEO FDA, Registrar Pharmacy Council with currency verified.
- Heads of Korle Bu, Komfo Anokye, Tamale, Cape Coast, Ho Teaching Hospitals with currency verified.
- Regional Directors of Health Services for all 16 regions with currency verified.
- Chair Parliament Committee on Health in the 9th Parliament.
- Presidents Ghana Medical Association, Ghana Registered Nurses and Midwives Association, Pharmaceutical Society of Ghana, Executive Director CHAG.
