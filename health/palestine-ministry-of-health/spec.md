# spec.md — `leaders.yml`

Single source of truth for the Palestinian health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Palestinian Ministry of Health (MoH) of the Palestinian Authority (PA / State of Palestine) headquartered in Ramallah, with attention to the parallel de facto Hamas-administered MoH that historically operated in Gaza (substantially destroyed and reorganised under the 2025 framework), the East Jerusalem and West Bank service architecture, UNRWA's health services, and the post-conflict reconstruction architecture in Gaza.

## 2. Scope

In scope: President of the State of Palestine; Prime Minister; Minister of Health (PA); Director-General PA MoH; East Jerusalem hospital network coordination; Gaza MoH coordination under the post-conflict transitional framework; Palestinian Legislative Council (in abeyance) — Health Committee; UNRWA Health Programme.

Out of scope: hospital directors below the apex tier.

## 3. Structure

Standard 2/6/10/14 indentation. Top-level key: `Palestinian health stakeholders:`. Ordering: PA Government → PA MoH → Gaza note → East Jerusalem note → UNRWA.

## 4. Field definitions

Party affiliation: `Fatah` (in the PA government), `Hamas` (historically administering Gaza MoH), `PFLP`, `DFLP`, `Independent technocrat`. Titles in English with Arabic transliterations as appropriate.

## 5. Provenance and dating

Anchor to year, month or date. Dr. Maged Abu Ramadan has served as Minister of Health in the technocratic government of Prime Minister Mohammad Mustafa formed in March 2024 under President Mahmoud Abbas; verify currency against WAFA (Palestinian News and Information Agency) and the State of Palestine Council of Ministers.

## 6. Update workflow

Verify against moh.ps, palestinecabinet.gov.ps, plo.ps, WAFA (wafa.ps), Maan News, Al-Quds Al-Arabi, Al-Hayat Al-Jadida, WHO occupied Palestinian territory (oPt) office briefings.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Conflating PA MoH with Gaza MoH or with UNRWA Health Programme — three distinct architectures with distinct authority and operational coverage.
- Ignoring the Gaza post-conflict reconstruction context — the Gaza health system was substantially destroyed in the 2023-2025 war and is being reconstituted under the 2025 ceasefire and reconstruction framework; framings that assume pre-October-2023 architecture are inaccurate.
- Ignoring East Jerusalem hospital network — the six East Jerusalem hospitals (Augusta Victoria, Makassed, St. Joseph, Princess Basma, St. John Eye Hospital, Red Crescent Maternity) serve as the apex referral network for Palestinians and operate under specific administrative status.

## 9. Acronym glossary

- **MoH** — Ministry of Health.
- **PA** — Palestinian Authority.
- **PRCS** — Palestine Red Crescent Society.
- **PNGO** — Palestinian Non-Governmental Organizations Network.
- **UNRWA** — United Nations Relief and Works Agency for Palestine Refugees in the Near East.
- **WAFA** — Palestinian News and Information Agency.

## 10. Worked example

```yaml
      - Dr. Maged Abu Ramadan:
          - Title: Minister of Health, State of Palestine (since March 2024 in the Mustafa technocratic government)
          - Stakeholder engagement notes:
              - "Minister of Health in the technocratic government of PM Mohammad Mustafa formed in March 2024 under President Mahmoud Abbas; ophthalmologist; former Mayor of Gaza (1997-2005); verify currency against WAFA and palestinecabinet.gov.ps."
              - "Owns PA MoH policy and budget across the West Bank, coordination with the East Jerusalem hospital network, coordination role for Gaza post-conflict reconstruction within the PA-led architecture, UNRWA Health Programme coordination, donor coordination (WHO oPt, UNICEF, UNFPA, EU-PEGASE, World Bank, EU, AHLC, Arab Fund, OIC, Qatari and Saudi bilateral), and WHO Eastern Mediterranean Region (EMRO) diplomacy."
              - "Hook: Gaza reconstruction (the central operational priority), conflict-trauma services and prosthetics, mental health, cholera and mpox preparedness, severe acute malnutrition, NCDs, immunisation catch-up, East Jerusalem hospitals sustainability, UNRWA Health Programme coordination, and the post-2024 PA-Gaza unified-administration agenda land."
          - Tone advice:
              - "Open with Gaza reconstruction, trauma services and mental health, malnutrition, immunisation catch-up, East Jerusalem hospitals and UNRWA coordination — operational priorities."
              - "Do not conflate PA MoH, the historically Hamas-administered Gaza MoH and UNRWA, do not ignore the Gaza post-conflict context, and do not ignore East Jerusalem hospitals."
```

## 11. Out-of-band notes

The Gaza MoH was historically administered by Hamas and the substantive identity of any successor administration is in flux post the 2025 ceasefire and Cairo / Riyadh-mediated transitional architecture; engagement framings must remain open to evolving authority structures.

## 12. Open questions

- Director-General PA MoH with currency verified.
- Gaza MoH transitional leadership.
- East Jerusalem Hospitals Network coordination point.
