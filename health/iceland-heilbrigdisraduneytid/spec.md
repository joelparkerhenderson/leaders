# spec.md — `leaders.yml`

Single source of truth for the Icelandic health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Icelandic Ministry of Health (Heilbrigðisráðuneytið), Iceland Health (Heilbrigðisstofnun) regional networks, Landspítali (the national university hospital), Directorate of Health (Embætti landlæknis), Icelandic Medicines Agency (Lyfjastofnun), and adjacent bodies.

Iceland operates universal tax-funded coverage with the Ministry of Health setting policy. Landspítali is the dominant national hospital; six Iceland Health (Heilbrigðisstofnun) regional units run primary care and small-area hospital networks; SAk Akureyri Hospital is the second-largest hospital. The Directorate of Health (chief medical officer function) and Lyfjastofnun are arm's-length bodies.

## 2. Scope

In scope: Forseti Íslands; Forsætisráðherra; Heilbrigðisráðherra (Minister of Health); Director of Health (Landlæknir); Director Lyfjastofnun (Icelandic Medicines Agency); CEO Landspítali; CEO Heilbrigðisstofnun (Regional networks: Vestfjarða, Norðurlands, Austurlands, Suðurlands, Suðurnesja, Vesturlands); CEO SAk Akureyri; Chair Alþingi Welfare Committee; President Icelandic Medical Association; President Icelandic Nurses' Association.

## 3. Structure

Standard 2/6/10/14. Ordering: Forsetaembætti → Heilbrigðisráðuneytið → Embætti landlæknis → Lyfjastofnun → Landspítali → SAk → Heilbrigðisstofnun regional → Alþingi Welfare Committee → professional associations.

## 4. Field definitions

Party affiliation using canonical Icelandic abbreviations: `Samfylkingin` (Social Democratic Alliance — Frostadóttir government), `Sjálfstæðisflokkurinn` (Independence Party), `Framsóknarflokkurinn` (Progressive Party), `Viðreisn` (Reform Party), `VG` (Left-Green Movement), `Píratar` (Pirates), `Flokkur fólksins` (People's Party), `Miðflokkurinn` (Centre Party). Titles in Icelandic with English glosses.

## 5. Provenance and dating

Alma Dagbjört Möller has served as Heilbrigðisráðherra (Minister of Health) since 21 December 2024 in the Kristrún Frostadóttir (Samfylkingin) government formed after the 2024 election. Doctor; previously Chief Epidemiologist; played a prominent role in Iceland's Covid-19 response. Born 24 June 1961.

## 6. Update workflow

Verify against government.is, althingi.is, landlaeknir.is, lyfjastofnun.is, landspitali.is, RÚV, Vísir, Morgunblaðið, Fréttablaðið, Iceland Review, The Grapevine.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating Iceland as a single-hospital system — Landspítali dominates but regional Heilbrigðisstofnun networks have meaningful operational roles in primary care.
- Importing NHS framings unmodified — Iceland is small-population universal Beveridgean with strong civil-society and academic-clinical integration.

## 9. Acronym glossary

- **Embætti landlæknis** — Directorate of Health (chief medical officer office).
- **Heilbrigðisráðuneytið** — Ministry of Health.
- **Heilbrigðisstofnun** — Iceland Health (regional health institution; six regional networks).
- **Landspítali** — National University Hospital of Iceland (Reykjavík).
- **Lyfjastofnun** — Icelandic Medicines Agency.
- **SAk** — Sjúkrahúsið á Akureyri (Akureyri Hospital).

## 10. Worked example

```yaml
      - Alma Dagbjört Möller (Samfylkingin):
          - Title: Heilbrigðisráðherra (Minister of Health) (since 21 December 2024)
          - Stakeholder engagement notes:
              - "Heilbrigðisráðherra since 21 December 2024 in the Kristrún Frostadóttir (Samfylkingin / Social Democratic Alliance) government formed after the 2024 Alþingi election; Samfylkingin MP; doctor; born 24 June 1961."
              - "Pre-political career as Chief Epidemiologist of Iceland (Sóttvarnalæknir) during the Covid-19 pandemic — high national-profile clinical-public-health role; brings clinical credibility and pandemic-response experience to the portfolio."
              - "Active 2026 public lines: proposed a new National Action Plan on Obesity (Grapevine February 2026); visited Heilbrigðisstofnun Norðurlands (HSN); announced 100 new nursing spaces at Urðarhvarf (March 2026); visited the Icelandic Radiation Safety Authority; oversaw Emergency Power Funding for Rural Healthcare."
              - "Owns Ministry of Health policy, Landspítali financing and reform, regional Heilbrigðisstofnun coordination, Lyfjastofnun medicines regulation, mental health and obesity policy, healthcare workforce (nurses, doctors), and Nordic health-cooperation."
              - "Hook: National Obesity Action Plan, mental health, nursing workforce, rural healthcare resilience, Landspítali development, Nordic cooperation aterrissent."
          - Tone advice:
              - "Open with obesity action plan, mental health, nursing workforce and rural healthcare — these are her authored 2026 public lines."
              - "Do not pitch as if Iceland were resource-poor — small population but high-income, with strong digital infrastructure and academic-clinical integration."
```

## 11. Out-of-band notes

For roles unfilled or in transition.

## 12. Open questions

- Named Permanent Secretary / Director of the Ministry of Health under Möller with currency verified.
- Director of Health (Landlæknir) with currency verified.
- Director Lyfjastofnun, CEO Landspítali, CEO SAk Akureyri with currency verified.
- CEOs of the six Heilbrigðisstofnun regional networks.
- Chair Alþingi Welfare Committee in the current Alþingi term.
- Presidents of the Icelandic Medical Association and Icelandic Nurses' Association with currency verified.
