# spec.md — `leaders.yml`

Single source of truth for the Ethiopian health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Ethiopian Ministry of Health (MoH), Ethiopian Pharmaceuticals Supply Service (EPSS), Ethiopian Food and Drug Authority (EFDA), Ethiopian Public Health Institute (EPHI), and adjacent bodies.

The Ethiopian system is decentralised across the federal MoH and 12 Regional Health Bureaux (RHBs) under the federal arrangement; further devolution to woredas (districts). The Health Extension Program (HEP) places trained Health Extension Workers in every kebele. Health insurance combines Community-Based Health Insurance (CBHI) for the informal sector and Social Health Insurance (SHI) for formal-sector workers. The country has faced significant disruption from the Tigray (2020-2022) and ongoing Amhara/Oromia conflicts.

## 2. Scope

In scope: Prime Minister; Minister of Health; State Ministers (Health Programs; Medical Services); Director-General EPHI; Director-General EFDA; Director-General EPSS; Heads of Regional Health Bureaux of Addis Ababa, Oromia, Amhara, Tigray, SNNPR (now multiple regions including South Ethiopia and Sidama), Somali, Afar; CMD Tikur Anbessa Specialized Hospital; House of Peoples' Representatives Health Standing Committee Chair; Ethiopian Medical Association.

## 3. Structure

Standard 2/6/10/14. Ordering: PM Office → MoH → EPHI → EFDA → EPSS → RHBs → Tikur Anbessa → House Standing Committee → Ethiopian Medical Association.

## 4. Field definitions

Party affiliation: `Prosperity Party` (PP — Abiy Ahmed), `Ezema`, others. Titles in English; H.E. for ministers per Ethiopian convention. Names typically two given names without family name; use "Dr." and ministry-specific honorifics.

## 5. Provenance and dating

Dr. Mekdes Daba Feyssa MD MPH has served as Minister of Health since 2024 (after the broader cabinet refresh during Abiy Ahmed's second term); OB/GYN by training (Hawassa University); ex-Team Lead at the WHO Deputy Director-General's Office in Geneva and various WHO HQ positions before returning to Ethiopia for the ministerial role.

## 6. Update workflow

Verify against moh.gov.et, pmo.gov.et, ephi.gov.et, efda.gov.et, hprestoffice.gov.et, ENA (Ethiopian News Agency), Addis Standard, Capital Ethiopia, Ethiopia Insider, Reuters Africa.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating the federal MoH as the operational owner — RHBs and woredas run delivery.
- Ignoring the conflict-affected zones — Tigray, Amhara and parts of Oromia have specific health-recovery needs.

## 9. Acronym glossary

- **CBHI** — Community-Based Health Insurance.
- **EFDA** — Ethiopian Food and Drug Authority.
- **EPHI** — Ethiopian Public Health Institute.
- **EPSS** — Ethiopian Pharmaceuticals Supply Service.
- **HEP** — Health Extension Program.
- **HEW** — Health Extension Worker.
- **MoH** — Ministry of Health.
- **RHB** — Regional Health Bureau.
- **SHI** — Social Health Insurance.

## 10. Worked example

```yaml
      - H.E. Dr. Mekdes Daba Feyssa, MD, MPH (PP):
          - Title: Minister of Health, Federal Democratic Republic of Ethiopia (since 2024)
          - Stakeholder engagement notes:
              - "Minister of Health since 2024 in the Abiy Ahmed (Prosperity Party) government; obstetrician and gynaecologist; medical degree from Hawassa University; OB/GYN residency at Addis Ababa University; Master of Public Health; immediately prior to the ministerial role served as Team Lead at the WHO Deputy Director-General's Office in Geneva and held positions at WHO HQ — distinctive WHO-Geneva background among African health ministers."
              - "Active 2026: implementing new innovation initiatives for Universal Health Coverage (ENA, late June 2026); met EU Delegation on strengthening Ethiopia's health system and supporting Marburg response efforts (MoH news, 2026); spoke at Ethiopian Red Cross Society events on government-partner collaboration (28 May 2026)."
              - "Attended the IAEA General Conference 2026 (delegation as Minister of Public Health); represented Ethiopia at the joint meeting of Ministers of Health of the African and Caribbean Regions (African Union)."
              - "Owns the post-conflict reconstruction of Tigray, Amhara and Oromia health infrastructure; UHC roadmap toward 2030; HEP modernisation; CBHI / SHI integration; EPSS supply chain reform; EFDA medicines regulation; Marburg and other VHF outbreak preparedness; cooperation with WHO Africa, AU and BRICS+."
              - "Hook: post-conflict health reconstruction, UHC innovation, HEP modernisation, CBHI / SHI integration, Marburg and other outbreak preparedness, local pharmaceutical manufacturing, climate-and-health, and WHO Africa multilateral diplomacy land."
          - Tone advice:
              - "Open with UHC innovation, HEP modernisation, post-conflict reconstruction and Marburg preparedness — these are her sustained authored 2026 public lines and her WHO-Geneva-background frame."
              - "Do not pitch as if Ethiopia were uniform — conflict-affected regions (Tigray, Amhara, Oromia) require specific reconstruction framings distinct from stable regions like Addis Ababa, Sidama or South Ethiopia."
```

## 11. Out-of-band notes

For roles unfilled or in transition.

## 12. Open questions

- Named State Ministers (Health Programs; Medical Services) under Daba with currency verified.
- Director-General EPHI, EFDA, EPSS with currency verified.
- Heads of Regional Health Bureaux of Addis Ababa, Oromia, Amhara, Tigray, South Ethiopia, Sidama, Somali, Afar, Benishangul-Gumuz, Gambela, Harari, Dire Dawa.
- CMD of Tikur Anbessa Specialized Hospital and other major referral hospitals.
- House of Peoples' Representatives Health Standing Committee Chair.
- Ethiopian Medical Association President with currency verified.
