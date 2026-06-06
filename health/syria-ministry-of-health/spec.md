# spec.md — `leaders.yml`

Single source of truth for the Syrian health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Syrian Ministry of Health (MoH) under the post-Assad transitional government formed after the 8 December 2024 fall of Bashar al-Assad's regime, and the adjacent bodies.

Syria's health system was devastated by 13+ years of civil war (2011-2024). The new transitional government in Damascus is led by Ahmed al-Sharaa (formerly Abu Mohammed al-Jolani, leader of Hayat Tahrir al-Sham — HTS) and is reconstituting state institutions including the MoH. Sanctions architecture is in transition: the US, UK and EU have lifted or eased some sanctions in early 2025 to enable humanitarian and reconstruction activity.

## 2. Scope

In scope: Transitional President; Prime Minister; Minister of Health; Director-General Damascus University Hospital; Damascus governorate health-administration coordination; northern and northeast Syria administration health-administration coordination (under the Autonomous Administration of North and East Syria — AANES — Kurdish-led).

Out of scope: hospital-level managers; provincial health office heads.

## 3. Structure

Standard 2/6/10/14 indentation. Top-level key: `Syrian health stakeholders:`. Ordering: Transitional Government → MoH → AANES note → UN-coordination.

## 4. Field definitions

Party affiliation in the post-Assad context is unsettled; current ministers are technocrats or HTS-aligned. Use `Transitional Government` for current Damascus officials. Titles in English.

## 5. Provenance and dating

Anchor to year, month or date. Musab Nazzal al-Ali was named Minister of Health in the transitional cabinet under interim Prime Minister Mohammed al-Bashir / Mohammad Ghazi al-Jalali transition; the cabinet has been subsequently reorganised under the al-Sharaa presidency and Prime Minister architecture; verify currency against SANA (Syrian Arab News Agency, under new editorial direction) and the Ministry of Information.

## 6. Update workflow

Verify against sana.sy (under new editorial direction), Al-Watan, Enab Baladi, Syria Direct, Levant 24, North Press Agency (AANES), WHO Syria country office briefings.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Assuming pre-2024 architecture — the Assad-era MoH organisational structures, leadership and donor architecture have been substantially recomposed since December 2024; framings that assume continuity from the pre-fall era are inaccurate.
- Ignoring the AANES — northeast Syria operates under the Autonomous Administration of North and East Syria with its own health-administration structures distinct from Damascus; framings that assume Damascus monopoly are inaccurate.
- Ignoring the sanctions transition — sanctions are being adjusted in 2025; specific licensing and compliance requirements remain.

## 9. Acronym glossary

- **AANES** — Autonomous Administration of North and East Syria.
- **HTS** — Hayat Tahrir al-Sham (the political formation behind the transitional government).
- **MoH** — Ministry of Health.
- **SARC** — Syrian Arab Red Crescent.

## 10. Worked example

```yaml
      - Musab Nazzal al-Ali:
          - Title: Minister of Health (transitional government)
          - Stakeholder engagement notes:
              - "Minister of Health in the Syrian transitional cabinet under interim PM following the 8 December 2024 fall of Assad; verify currency against SANA."
              - "Owns reconstituting MoH policy and budget, Damascus University Hospital, Al-Mouwasat University Hospital, the hospital network across the fourteen governorates (under variable degrees of central control), pharmaceutical supply restoration, donor coordination (WHO, UNICEF, WFP, MSF, ICRC, SARC, UNHCR, IOM), and post-sanctions transition cooperation with reactivating bilateral partners."
              - "Hook: health-system reconstruction, refugee and IDP return health planning, mpox and cholera outbreak response, mental health and trauma services, conflict-injury rehabilitation, pharmaceutical sector reactivation, and humanitarian-development nexus framing land."
          - Tone advice:
              - "Open with reconstruction, refugee return, outbreak response, mental health, rehabilitation and pharmaceutical reactivation — operational priorities of the transition."
              - "Do not assume pre-2024 architecture, do not ignore the AANES, do not ignore the sanctions transition."
```

## 11. Out-of-band notes

For roles unfilled or under reorganisation.

## 12. Open questions

- Substantive identity of current Minister of Health and Prime Minister with currency verified.
- Director-General Damascus University Hospital.
- AANES Health Authority interlocutor.
