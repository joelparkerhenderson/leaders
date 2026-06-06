# spec.md — `leaders.yml`

Single source of truth for the UAE health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the UAE federal Ministry of Health and Prevention (MoHAP), the Department of Health – Abu Dhabi (DoH), the Dubai Health Authority (DHA), Sharjah Health Authority and other Emirate-level bodies, and adjacent entities.

The UAE health system is federal-and-emirate-distributed: MoHAP at federal level (formerly Ministry of Health); Department of Health – Abu Dhabi (DoH) and Abu Dhabi Public Health Centre (ADPHC), with SEHA as the public provider and Abu Dhabi Health Services Co.; Dubai Health Authority (DHA) and the new Dubai Health network unifying Dubai's academic medical centres; Sharjah Health Authority. Mandatory health insurance is established in Abu Dhabi and Dubai; the UAE Cabinet decided in 2023 to extend mandatory insurance nationally by 2025-2026.

## 2. Scope

In scope: President; Vice President / Prime Minister of UAE (Ruler of Dubai); Minister of Health and Prevention; Undersecretary MoHAP; Chair Department of Health – Abu Dhabi; CEO SEHA; Director-General Dubai Health Authority; Director-General Dubai Health; Director Sharjah Health Authority; CEO Emirates Drug Establishment (EDE); Federal National Council Health Committee chair; Emirates Medical Association.

## 3. Structure

Standard 2/6/10/14. Ordering: Federal Government → MoHAP → Department of Health Abu Dhabi → DHA / Dubai Health → SEHA → Sharjah Health Authority → Federal National Council → Emirates Medical Association.

## 4. Field definitions

UAE does not have political parties; titles use 'H.E.' or 'His Highness' (HH) where official. Names with Arabic transliteration.

## 5. Provenance and dating

H.E. Ahmed Ali Al Sayegh became Minister of Health and Prevention on 1 September 2025, as announced by HH Sheikh Mohammed bin Rashid Al Maktoum; succeeded AbdulRahman Al Owais who served as Minister of Health for more than 12 years (now Minister of State for Federal National Council Affairs). Previously Al Sayegh served as Minister of State at the Ministry of Foreign Affairs since September 2018, heading the economic and commercial affairs portfolio.

## 6. Update workflow

Verify against mohap.gov.ae, u.ae, gulftoday.ae, doh.gov.ae, dha.gov.ae, gulfnews.com, Khaleej Times, The National (UAE), Emirates News Agency (WAM).

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating MoHAP as the whole system — DoH Abu Dhabi and DHA / Dubai Health operate largely autonomously within their Emirates.
- Importing US framings unmodified — UAE is mandatory-insurance-funded with public, private, and PPP delivery and explicit federal-emirate division.

## 9. Acronym glossary

- **ADPHC** — Abu Dhabi Public Health Centre.
- **DHA** — Dubai Health Authority.
- **Dubai Health** — Dubai's unified academic and provider network (formed from DHCC / Mohammed bin Rashid University of Medicine merger).
- **DoH** — Department of Health, Abu Dhabi.
- **EDE** — Emirates Drug Establishment (new federal medicines body).
- **FNC** — Federal National Council.
- **MoHAP** — Ministry of Health and Prevention.
- **SEHA** — Abu Dhabi Health Services Company (public provider).

## 10. Worked example

```yaml
      - H.E. Ahmed Ali Al Sayegh:
          - Title: Minister of Health and Prevention (since 1 September 2025)
          - Stakeholder engagement notes:
              - "Minister of Health and Prevention since 1 September 2025; appointed by HH Sheikh Mohammed bin Rashid Al Maktoum in a limited Cabinet reshuffle (Khaleej Times; Arab Weekly); succeeded AbdulRahman Al Owais after Owais's 12-plus-year tenure, with Owais transitioning to Minister of State for Federal National Council Affairs."
              - "Previously Minister of State at the Ministry of Foreign Affairs since September 2018, where he led the economic and commercial-affairs portfolio and strengthened UAE ties with Asian nations and Commonwealth of Independent States — a diplomatic-economic background unusual for the health portfolio."
              - "MoHAP affirmed continuity of the UAE healthcare system following the transition (Emirates 24|7, March 2026); Al Sayegh has met international counterparts including Malta's Minister of Health Jo Etienne Abela at MedTech World Dubai 2026."
              - "Owns federal MoHAP policy, coordination with Department of Health Abu Dhabi and Dubai Health Authority / Dubai Health, the national mandatory-health-insurance rollout, the Emirates Drug Establishment (new federal medicines body), and UAE health diplomacy in BRICS+, GCC, OIC, and WHO EMRO."
              - "Hook: national mandatory insurance rollout, MedTech / med-tech hub framing, Emirates Drug Establishment, AI in healthcare (Abu Dhabi G42 ecosystem), HealthTech investment and FDI, Hajj-Umrah health logistics with Saudi Arabia, and BRICS+ / OECD health cooperation land."
          - Tone advice:
              - "Open with national mandatory-insurance rollout, MedTech hub, Emirates Drug Establishment, AI in healthcare, and BRICS+ / OECD cooperation — these align with Al Sayegh's economic-diplomatic background and the UAE's transformation framing."
              - "Do not pitch MoHAP as the operational owner of healthcare in Abu Dhabi and Dubai — DoH Abu Dhabi (under SEHA delivery) and DHA / Dubai Health own the largest emirate-level networks autonomously."
```

## 11. Out-of-band notes

For roles unfilled or in transition.

## 12. Open questions

- Named Undersecretary MoHAP under Al Sayegh with currency verified.
- Chair Department of Health Abu Dhabi and CEO SEHA with currency verified.
- Director-General Dubai Health Authority and Director-General Dubai Health with currency verified.
- Director Sharjah Health Authority with currency verified.
- CEO Emirates Drug Establishment with currency verified.
- Chair Federal National Council Health Committee in the current FNC term.
- President Emirates Medical Association with currency verified.
