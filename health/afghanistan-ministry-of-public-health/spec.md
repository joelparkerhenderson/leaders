# spec.md — `leaders.yml`

Single source of truth for the Afghan health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Afghan Ministry of Public Health (MoPH) of the de facto Islamic Emirate of Afghanistan (Taliban-controlled administration, since 15 August 2021) and adjacent bodies.

Afghanistan's health system is heavily donor-supported, with the Sehatmandi project (World Bank-financed via WHO/UNICEF) as the central service-delivery mechanism. The Islamic Emirate is not internationally recognised but is the de facto administration; engagement with the MoPH proceeds via humanitarian-exception frameworks.

## 2. Scope

In scope: Supreme Leader (Mullah Hibatullah Akhundzada — political head); Prime Minister (Mullah Hasan Akhund); Acting Minister of Public Health; Deputy Minister(s); Director-General of Tertiary Hospitals; provincial public-health director coordination.

Out of scope: NGO programme leads under MoPH MoUs; foreign donor staff.

## 3. Structure

Standard 2/6/10/14 indentation. Top-level key: `Afghan health stakeholders:`. Ordering: Supreme Leader → Prime Minister → MoPH → provincial coordination.

## 4. Field definitions

Affiliation: Taliban / Islamic Emirate (no party system). Titles in English; use `Acting` for all ministerial titles since the IEA has been operating under acting-minister conventions; honorific `Mawlavi` or `Dr.` as applicable.

## 5. Provenance and dating

Anchor to year, month or date. Mawlavi Noor Jalal Jalali has served as Acting Minister of Public Health; verify currency against IEA spokesperson Zabihullah Mujahid, MoPH-Afghanistan communications, WHO Afghanistan and the UN Country Team reporting.

## 6. Update workflow

Verify against moph.gov.af (intermittent), Bakhtar News Agency, TOLOnews, Khaama Press, Pajhwok, Afghanistan Analysts Network, UNAMA briefings, WHO Afghanistan.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Assuming international recognition — no UN Member State has recognised the IEA government; framings that assume normalised diplomatic engagement are inaccurate.
- Ignoring the women-and-girls access constraints — IEA policy restricts women's participation in education and many professional roles; this directly impacts midwifery, female community health workers, and women's access to care; framings that ignore this dimension miss a central operational challenge.
- Sanctioning ambiguity — humanitarian engagement is permitted under specific licences (OFAC General License, UN sanctions exceptions); routine commercial framings risk sanctions-compliance issues.

## 9. Acronym glossary

- **IEA** — Islamic Emirate of Afghanistan (Taliban de facto administration).
- **MoPH** — Ministry of Public Health.
- **Sehatmandi** — World Bank-financed essential package of health services project.
- **UNAMA** — United Nations Assistance Mission in Afghanistan.

## 10. Worked example

```yaml
      - Mawlavi Noor Jalal Jalali:
          - Title: Acting Minister of Public Health
          - Stakeholder engagement notes:
              - "Acting Minister of Public Health in the Islamic Emirate of Afghanistan (de facto administration since 15 August 2021); verify currency against Bakhtar News Agency, TOLOnews and WHO Afghanistan."
              - "Owns MoPH policy and the de facto coordination of tertiary hospitals (Wazir Akbar Khan, Jamhuriat, Indira Gandhi Children's), provincial-public-health directorates across the 34 provinces, and engagement with the Sehatmandi-successor project (financed via World Bank with WHO and UNICEF as service-delivery proxies under the post-2021 humanitarian-exception architecture)."
              - "Hook: Sehatmandi-successor continuity, maternal-and-child mortality reduction (Afghanistan has very high MMR), polio (Afghanistan is one of two remaining wild poliovirus countries), measles outbreaks, malnutrition, mpox and cholera preparedness, and humanitarian-exception engagement land."
          - Tone advice:
              - "Open with Sehatmandi continuity, polio, MCH, malnutrition and humanitarian-exception coordination — operational priorities."
              - "Do not assume normalised diplomatic engagement and do not ignore the women-and-girls access constraints — central to feasibility of any framing."
```

## 11. Out-of-band notes

For roles held in acting capacity under the IEA.

## 12. Open questions

- Deputy Ministers and Director-General of Tertiary Hospitals with currency verified.
- Provincial public-health director coordination.
