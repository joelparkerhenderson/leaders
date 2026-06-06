# spec.md — `leaders.yml`

Single source of truth for the Sudanese health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Sudanese Federal Ministry of Health, state-level Ministries of Health (18 states), National Medical Supplies Fund (NMSF), and adjacent bodies. The Sudanese system is in deep crisis due to the SAF-RSF civil war since April 2023; major hospitals destroyed or non-functional; refugee and IDP populations exceed 12 million; cholera, dengue, hunger, measles outbreaks chronic.

## 2. Scope

In scope: Sovereignty Council Chairman (Gen. al-Burhan); PM (recently appointed); Federal Minister of Health; State-level Ministers of Health (18 states); DG NMSF; major hospital directors (Khartoum Teaching Hospital — non-functional, Port Sudan, Wad Madani, Kosti); WHO Sudan office head; UN OCHA Sudan; humanitarian-coordination bodies.

## 3. Structure

Standard.

## 4. Field definitions

Government is SAF / Sovereignty Council-aligned; RSF-controlled territories operate separate de facto health-services. Titles in English / Arabic.

## 5. Provenance and dating

Haitham Mohammed Ibrahim serves as Federal Minister of Health in the SAF / Sovereignty Council-aligned government; active 2026 on recovery, rehabilitation, international partnerships, joint coordination with South Sudan and Chad, Italian Emergency Agency cooperation, Darfur surveillance with WHO, UNFPA engagement.

## 6. Update workflow

Verify against fmoh.gov.sd, sudanhorizon.com, allAfrica Sudan section, Sudan Tribune, Radio Dabanga, WHO Sudan, AP Sudan, Reuters.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating Sudan as one unified system — RSF-controlled territories have separate de facto arrangements.
- Importing peace-time framings — Sudan is in active civil war.

## 9. Acronym glossary

- **NMSF** — National Medical Supplies Fund.
- **RSF** — Rapid Support Forces.
- **SAF** — Sudanese Armed Forces.

## 10. Worked example

```yaml
      - Haitham Mohammed Ibrahim:
          - Title: Federal Minister of Health of Sudan (in the SAF / Sovereignty Council-aligned government)
          - Stakeholder engagement notes:
              - "Federal Minister of Health of Sudan in the SAF / Sovereignty Council-aligned government during the ongoing civil war (April 2023-); operates from Port Sudan and partial-control territories."
              - "Active 2026: affirmed Sudan's steady progress toward recovery and rehabilitation of health institutions at WHA79 (allAfrica 20 May 2026); discussed strengthening HIV/AIDS support; urged international partners to support Sudan's health system; praised Al-Gezira State for rapid restoration of health system after RSF withdrawal; joint Sudan-South Sudan coordination meeting (22 May 2026); joint Sudan-Chad cross-border health cooperation; met Italian Emergency Agency Director; discussed Darfur surveillance with WHO delegation; met UNFPA Resident Representative; 'Health Assistance' Project evaluation."
              - "Owns Federal Ministry policy (within SAF-controlled areas), NMSF, state-level coordination, post-conflict reconstruction, Cholera and dengue outbreak response, HIV / TB / malaria continuity, mental-health and trauma response, cross-border coordination with South Sudan, Chad, Egypt, Ethiopia."
              - "Hook: post-conflict recovery, NMSF and pharmaceutical supply chains, cholera / dengue response, cross-border cooperation, international partner advocacy, mental-health and trauma response land."
          - Tone advice:
              - "Open with recovery, international-partner support, cross-border cooperation and humanitarian needs — these are sustained authored lines."
              - "Do not pitch as if Sudan were peacetime — the civil war is ongoing and RSF-controlled territories operate separately; engagement must respect war-context constraints."
```

## 11. Out-of-band notes

For roles unfilled or interim.

## 12. Open questions

- Named Deputy Minister and Senior Officials of the Federal Ministry under Ibrahim.
- DG NMSF with currency verified.
- State Ministers of Health for the 18 states with currency verified — priority Port Sudan, Al-Gezira, Sennar, Kassala, Red Sea, Blue Nile (SAF-controlled); separately track RSF-controlled de facto arrangements in Darfur and Khartoum.
- WHO Sudan Country Representative with currency verified.
- UN OCHA Sudan Humanitarian Coordinator.
