# spec.md — `leaders.yml`

Single source of truth for the Yemeni health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around Yemen's Ministry of Public Health and Population (MoPHP). Yemen has two de facto governments: the internationally-recognised government (IRG, PLC-led, Aden-based) and the Houthi-controlled administration in Sana'a. Each operates a separate MoPHP. Yemen has experienced the world's worst humanitarian crisis with ongoing cholera, malnutrition, conflict-injury and reproductive-health emergencies.

## 2. Scope

In scope: For both governments — Presidential Leadership Council Chair (Rashad al-Alimi) for IRG; Houthi Supreme Political Council head for Sana'a; PM; Minister of Public Health and Population (each); Deputy Ministers; major hospital directors; WHO Yemen; UN OCHA Yemen; humanitarian-coordination bodies.

## 3. Structure

Standard. Document both governments separately.

## 4. Field definitions

IRG aligned with Saudi-led coalition; Houthi administration aligned with Iran. Titles in English / Arabic.

## 5. Provenance and dating

Dr. Qasim Buhaibeh serves as Minister of Public Health (medical specialist, led pandemic response) in the IRG following Presidential Decree No. 3 of 2026 that formed a new government with 35 ministers (Yeni Yemen, Yemen Monitor). Houthi administration Minister of Health to verify separately.

## 6. Update workflow

Verify against yemen-embassyat.de, yeniyemen.net, yemenmonitor.com, WHO Yemen, Sana'a Center for Strategic Studies, Houthi-controlled SABA News Agency.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating Yemen as unitary — two de facto health administrations.
- Ignoring humanitarian crisis scale.

## 9. Acronym glossary

- **IRG** — Internationally-Recognised Government.
- **MoPHP** — Ministry of Public Health and Population.
- **PLC** — Presidential Leadership Council.
- **SABA** — Houthi-controlled news agency.

## 10. Worked example

```yaml
      - Dr. Qasim Buhaibeh (IRG):
          - Title: Minister of Public Health and Population, Internationally-Recognised Government (since 2026 by Presidential Decree No. 3)
          - Stakeholder engagement notes:
              - "Minister of Public Health and Population in the new Yemeni IRG cabinet formed by Presidential Decree No. 3 of 2026 (35-minister comprehensive reshuffle per Yeni Yemen and Yemen Monitor); medical specialist; led national pandemic response."
              - "Owns IRG MoPHP policy, hospital network in IRG-controlled areas (Aden, Hadhramaut, Marib, Taiz, Mahra), pharmaceutical supply, cholera and dengue outbreak response, malnutrition response, conflict-injury services, and coordination with WHO Yemen, UNICEF, WFP, MSF, ICRC."
              - "Hook: cholera response, malnutrition, conflict-injury surgical care, GBV and reproductive-health emergencies, Aden hospital network reconstruction, cross-administration humanitarian coordination."
          - Tone advice:
              - "Open with cholera and outbreak response, malnutrition, hospital reconstruction in IRG areas, and humanitarian coordination — these are the war-context priorities."
              - "Do not assume single counterpart — Houthi-Sana'a-controlled territory has separate MoPHP administration."
```

## 11. Out-of-band notes

Document both governments separately. Houthi-controlled MoPHP based in Sana'a operates a separate administration with separate Health Minister to verify.

## 12. Open questions

- IRG Deputy Ministers and Senior Officials under Buhaibeh with currency verified.
- Houthi-administration MoPHP Minister of Health and Sana'a-based administration leadership.
- Hospital directors in Aden (Republican Teaching Hospital, Al-Naqib), Sana'a (Al-Thawra, Al-Kuwait), Taiz, Hodeidah.
- WHO Yemen Country Representative.
- UN OCHA Yemen Humanitarian Coordinator.
