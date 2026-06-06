# spec.md — `leaders.yml`

Single source of truth for the Iraqi health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Iraqi Ministry of Health (وزارة الصحة, Wizarat al-Sihha), Kurdistan Regional Government Ministry of Health (separately), Iraqi Drug Regulatory Authority, Iraqi Centre for Disease Control, governorate Health Directorates, and adjacent bodies.

The Iraqi system is tax-funded universal but heavily challenged by years of conflict, sanctions, sectarian division and infrastructure damage. The federal Ministry of Health operates 15 federal governorate health systems; the Kurdistan Regional Government has its own Ministry of Health for the three KRG governorates (Erbil, Sulaymaniyah, Duhok plus Halabja). The recent digital health insurance Dhamani platform is a flagship reform.

## 2. Scope

In scope: President; Prime Minister; Minister of Health; KRG Minister of Health; Deputy Ministers; Director-General Iraqi Drug Regulatory Authority; Director-General Iraqi Centre for Disease Control; Director-Generals of Governorate Health Directorates (Baghdad, Basra, Nineveh, Diyala, Anbar, Najaf, Karbala); Council of Representatives Health Committee; Iraqi Medical Association; Iraqi Pharmacists Syndicate.

## 3. Structure

Standard. Ordering: President / PM → MoH federal → KRG MoH → Drug Authority → CDC → governorate directorates → Council of Representatives → professional bodies.

## 4. Field definitions

Party affiliation by major coalition: `State of Law` (Maliki Da'wa), `Sairoon` (Sadrist, when active), `Fatah` (Iran-aligned), `Taqaddum` (Halbousi), `Sovereignty`, `Kurdistan Democratic Party` (KDP, Barzani), `Patriotic Union of Kurdistan` (PUK, Talabani). Titles in English (with Arabic transliteration).

## 5. Provenance and dating

Dr. Saleh Mahdi al-Hasnawi serves as Minister of Health since 28 October 2022 in the Mohammed Shia' al-Sudani government formed after the prolonged government-formation crisis post-October-2021 election; psychiatrist, public-health expert, and academic at the University of Kufa; independent politician. Active 2026 on Dhamani digital health insurance platform launch and drug-control programmes.

## 6. Update workflow

Verify against moh.gov.iq, pmo.iq, gov.krd, presidency.iq, parliament.iq, INA (Iraqi News Agency), Rudaw (KRG), Al-Mada, Al-Sabaah, Iraqi News.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating Iraq as unitary — KRG operates a separate health system within constitutional federalism.
- Importing US framings unmodified — Iraqi system has been shaped by sanctions, conflict and reconstruction-aid coordination.

## 9. Acronym glossary

- **Dhamani** — Iraqi digital health insurance platform launched 2025-2026.
- **KRG** — Kurdistan Regional Government.

## 10. Worked example

```yaml
      - Dr. Saleh Mahdi al-Hasnawi (independent):
          - Title: Minister of Health of Iraq (since 28 October 2022, in the al-Sudani government)
          - Stakeholder engagement notes:
              - "Minister of Health since 28 October 2022 in the Mohammed Shia' al-Sudani government formed after the prolonged government-formation crisis following the October 2021 election; psychiatrist; professor and public-health expert at the University of Kufa; independent politician; previously served as Minister of Health 2010-2014 in the Maliki government — returning to the portfolio."
              - "Operates in a continuing-recovery context: war-damaged infrastructure, displaced populations, ongoing reconstruction, and major international-partner engagement (WHO, World Bank, USAID, UNICEF, ICRC) for both rebuilding and ongoing humanitarian needs."
              - "Active 2026: Iraq launched Dhamani digital health insurance platform and services — flagship digital-and-financing reform of the al-Sudani term; Ministry made positive progress in tackling drugs and antisocial behaviour (IINA news); conducted inspection visits to hospitals (2026 social media)."
              - "Owns federal Ministry of Health policy, coordination with KRG Ministry of Health, Iraqi Drug Regulatory Authority, Iraqi CDC, governorate Health Directorates, federal teaching hospitals, post-conflict reconstruction of Nineveh and Anbar health facilities, oncology and TB programmes, and WHO EMRO and Arab League health diplomacy."
              - "Hook: Dhamani digital health insurance rollout, oncology and TB programmes, post-conflict reconstruction, Iraqi Drug Authority reform, mental health (Al-Hasnawi's clinical specialty), and federal-KRG coordination land."
          - Tone advice:
              - "Open with Dhamani digital health insurance, oncology, mental health and federal-KRG coordination — these are his sustained authored lines and his psychiatry / public-health professional frame."
              - "Do not assume federal-Iraq uniformity — KRG operates its own Ministry of Health independently, and Sunni-majority governorates (Anbar, Nineveh, Salah ad-Din) require post-conflict-recovery-specific framings distinct from southern and central Iraq."
```

## 11. Out-of-band notes

For roles unfilled or in transition.

## 12. Open questions

- Named Deputy Ministers under al-Hasnawi with currency verified.
- KRG Minister of Health and Deputy with currency verified.
- Director-General Iraqi Drug Regulatory Authority and Iraqi CDC with currency verified.
- Director-Generals of Health Directorates of Baghdad, Basra, Nineveh, Diyala, Anbar, Najaf, Karbala.
- Chair Council of Representatives Health Committee in the current 6th parliamentary cycle (or after the next election).
- President Iraqi Medical Association, Iraqi Pharmacists Syndicate with currency verified.
