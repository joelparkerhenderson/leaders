# spec.md — `leaders.yml`

Single source of truth for the Kenyan health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Kenyan Ministry of Health, the Social Health Authority (SHA, successor to NHIF), Pharmacy and Poisons Board, KEMSA, KEMRI, the 47 county Departments of Health, KMA, KNDI, and adjacent bodies.

The Kenyan system is devolved under the 2010 Constitution: 47 counties own delivery; national Ministry sets policy and coordinates with the Council of Governors. In 2023-2024 NHIF was replaced by SHA implementing the Social Health Insurance Fund (SHIF) and Primary Healthcare Fund (PHF) — the Universal Health Coverage architecture under President Ruto.

## 2. Scope

In scope: President; Cabinet Secretary for Health; Principal Secretary State Department for Public Health and Professional Standards; PS State Department for Medical Services; Director-General Health; CEO SHA; CEO KEMSA; Director KEMRI; CEO Pharmacy and Poisons Board; CEO Kenyatta National Hospital; CEO Moi Teaching and Referral Hospital; CEC-Health Members (County Executive Committee Members for Health) of Nairobi, Mombasa, Kiambu, Kisumu, Nakuru, Machakos, Uasin Gishu, Kakamega; Chair National Assembly Health Committee; Chair Senate Health Committee; Kenya Medical Association (KMA); Kenya Medical Practitioners and Dentists Council (KMPDC); Pharmaceutical Society of Kenya; National Nurses Association of Kenya.

## 3. Structure

Standard 2/6/10/14. Ordering: Presidency → Ministry of Health → SHA → KEMSA → KEMRI → KNH and MTRH → 47 counties → Parliament committees → professional bodies.

## 4. Field definitions

Party affiliation using canonical Kenyan abbreviations: `UDA` (United Democratic Alliance — Ruto), `ODM` (Orange Democratic Movement), `Jubilee`, `Wiper`, `Ford-Kenya`, `ANC` (Amani National Congress), `KANU`, `Maendeleo Chap Chap`. Titles in English.

## 5. Provenance and dating

Aden Duale (UDA) was appointed Cabinet Secretary for Health in 2024 following the dissolution of the Cabinet by President William Ruto and the subsequent reconstitution. Replaced Susan Nakhumicha Wafula. Duale is a long-time UDA politician, ex-Leader of Majority in the National Assembly. Active 2026 on health reforms, SHA / SHIF rollout, NHIF claims backlog.

## 6. Update workflow

Verify against health.go.ke, president.go.ke, sha.go.ke, kemsa.co.ke, kemri.go.ke, parliament.go.ke, Nation Media Group (Daily Nation), Standard Media, The Star Kenya, Capital FM Kenya, Citizen TV.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating Ministry of Health as the operational buyer — counties run delivery and have CEC-Health Members.
- Ignoring SHA — the post-NHIF transition reorganised health financing.

## 9. Acronym glossary

- **CEC-Health** — County Executive Committee Member for Health (county-cabinet-level).
- **KEMRI** — Kenya Medical Research Institute.
- **KEMSA** — Kenya Medical Supplies Authority.
- **KMA** — Kenya Medical Association.
- **KMPDC** — Kenya Medical Practitioners and Dentists Council.
- **KNH** — Kenyatta National Hospital.
- **MTRH** — Moi Teaching and Referral Hospital.
- **NHIF** — National Hospital Insurance Fund (replaced by SHA in 2023-24).
- **PHF** — Primary Healthcare Fund.
- **SHA** — Social Health Authority.
- **SHIF** — Social Health Insurance Fund.
- **UHC** — Universal Health Coverage.

## 10. Worked example

```yaml
      - Aden Duale (UDA):
          - Title: Cabinet Secretary for Health (since 2024 Cabinet reconstitution under President Ruto)
          - Stakeholder engagement notes:
              - "Cabinet Secretary for Health in the William Ruto (UDA) government; appointed in 2024 after the dissolution and reconstitution of the Cabinet; UDA; previously Leader of Majority in the National Assembly during Uhuru Kenyatta's second term; long-time North Eastern Kenya political figure; replaced Susan Nakhumicha Wafula in the Health portfolio."
              - "Briefed Senate (Ministry of Health website June 2026) on progress on health reforms, NHIF claims and service delivery; comments to Hiiraan Online (June 2026) on freedoms gained by Kenyan Somalis under Ruto — political-frame statements that combine community and national positioning."
              - "Owns the SHA / SHIF rollout (replacing NHIF since 2023-24), the Primary Healthcare Fund implementation, NHIF claims backlog resolution, KEMSA supply chain reform, KEMRI research portfolio, and national-county coordination on Universal Health Coverage via the Council of Governors."
              - "Kenya hosting the World Health Summit Regional Meeting 2026 — Duale is the political host of the convening; raised Ministry's case for enhanced funding for public-health priorities (Ministry of Health website 2026)."
              - "Hook: SHA / SHIF rollout, NHIF claims, KEMSA reform, county-national coordination, primary healthcare networks, climate-and-health, HIV / TB / malaria programmes, Universal Health Coverage land."
          - Tone advice:
              - "Open with SHA / SHIF rollout, NHIF claims resolution, county coordination and UHC framing — these are the live Ruto-era reform priorities and Duale's authored political lines."
              - "Do not pitch as if counties were administrative subunits — under the 2010 Constitution counties are constitutionally autonomous on health delivery and CEC-Health Members hold operational authority; framings that bypass counties via Council of Governors will be redirected."
```

## 11. Out-of-band notes

For roles unfilled or in transition.

## 12. Open questions

- Named PSs (Public Health and Professional Standards; Medical Services) under Duale with currency verified.
- Director-General Health, CEO SHA, CEO KEMSA, Director KEMRI, CEO Pharmacy and Poisons Board with currency verified.
- CEO KNH and CEO MTRH with currency verified.
- CEC-Health Members of Nairobi, Mombasa, Kiambu, Kisumu, Nakuru, Machakos, Uasin Gishu, Kakamega counties.
- Chair National Assembly Health Committee and Chair Senate Health Committee in the 13th Parliament.
- KMA, KMPDC, PSK, NNAK leadership with currency verified.
