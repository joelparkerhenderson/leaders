# spec.md — `leaders.yml`

Single source of truth for the structure, semantics, and update rules of `leaders.yml` for Croatian health care (zdravstvo). The YAML must conform to this spec; if they disagree, the spec wins and the YAML is fixed.

## 1. Purpose

`leaders.yml` is an engagement register of named individuals in and around the Croatian zdravstvo. Each entry helps a reader inside the Ministarstvo zdravstva, HZZO (Hrvatski zavod za zdravstveno osiguranje), HZJZ (Hrvatski zavod za javno zdravstvo), HALMED, a county-level zavod, or a hospital decide who to engage, how, and where.

The Croatian system is statutory social-insurance financed through HZZO, with the Ministry of Health setting policy. Specialist care is delivered by national, county and city hospitals; primary care sits at the županijski (county) level under the Domovi zdravlja and through contracts with HZZO. HZJZ runs national public health. HALMED regulates medicines and devices.

## 2. Scope

**In scope:** Predsjednik Vlade; Ministar/Ministrica zdravstva; državni tajnici za zdravstvo; ravnatelj HZZO; ravnatelj HZJZ; ravnatelj HALMED; ravnatelj Agencije za kvalitetu i akreditaciju u zdravstvu i socijalnoj skrbi (AAZ); directors of the largest hospitals (KBC Zagreb / Rebro, KB Dubrava, KB Sveti Duh, KBC Sestre milosrdnice, KBC Split, KBC Rijeka, KBC Osijek); Predsjednik Saborski odbor za zdravstvo i socijalnu politiku; Predsjednik Hrvatskog liječničkog zbora (HLZ); Predsjednik Hrvatske liječničke komore (HLK); Predsjednik Hrvatske komore medicinskih sestara; Predsjednik Hrvatske ljekarničke komore.

**Out of scope:** operational staff below voditelj sektora; vendors; historical post-holders.

## 3. Structure

```
Hrvatski sustav zdravstva — dionici:
  - {Organisation}:
      - {Person}:
          - Title: ...
          - Stakeholder engagement notes: [...]
          - Tone advice: [...]
```

Indentation 2/6/10/14 spaces. Ordering: Vlada → Ministarstvo zdravstva → HZZO → HZJZ → HALMED → AAZ → major hospitals → Hrvatski sabor Odbor za zdravstvo → professional bodies.

## 4. Field definitions

Standard family conventions. Party affiliation in parentheses using canonical Croatian abbreviations: `HDZ`, `SDP`, `Most`, `Možemo!`, `Domovinski pokret (DP)`, `Centar`, `IDS`, `HSS`. Titles in Croatian with English glosses where useful.

## 5. Provenance and dating

Anchor facts to year, month or exact date. The Plenković III government (HDZ-DP-HSLS-NPS / National Minorities) has been in office since 17 May 2024 following the April 2024 election. Treat any Vlada entry pre-dating 17 May 2024 as warranting re-verification.

The European Public Prosecutor's Office (EPPO) opened an investigation in 2024 into a Minister of Health and seven others over medical robotics procurement; subsequent reshuffles to the Health portfolio should be checked against EPPO and DORH (Croatian state prosecutor) updates.

## 6. Update workflow

1. Identify the change. 2. Verify against vlada.gov.hr, zdravstvo.gov.hr, hzzo.hr, hzjz.hr, halmed.hr, sabor.hr, Jutarnji list, Večernji list, Novi list, Index.hr, Telegram.hr, N1 Hrvatska. 3. Apply minimum diff. 4. Confirm structure. 5. Re-validate cross-references.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating the system as fully Zagreb-centric — county hospitals carry significant operational weight in Croatia's regional geography.
- Importing NHS framings unmodified — Croatia is statutory insurance with HZZO as single payer, not a Beveridgean service.

## 9. Acronym glossary

- **AAZ** — Agencija za kvalitetu i akreditaciju u zdravstvu i socijalnoj skrbi.
- **DORH** — Državno odvjetništvo Republike Hrvatske (state prosecutor's office).
- **HALMED** — Agencija za lijekove i medicinske proizvode (Croatian medicines agency).
- **HLK** — Hrvatska liječnička komora.
- **HLZ** — Hrvatski liječnički zbor.
- **HZJZ** — Hrvatski zavod za javno zdravstvo.
- **HZZO** — Hrvatski zavod za zdravstveno osiguranje (single statutory health insurer).
- **KBC** — Klinički bolnički centar (university hospital).

## 10. Worked example

```yaml
      - Irena Hrstić (HDZ):
          - Title: Ministrica zdravstva (Minister of Health) (u Vladi Andreja Plenkovića III)
          - Stakeholder engagement notes:
              - "Ministrica zdravstva u trećoj Vladi Andreja Plenkovića (HDZ-DP-HSLS-NPS, od 17. svibnja 2024); preuzima portfelj u razdoblju nakon ostavki vezanih uz istragu EPPO-a o nabavi medicinske robotike koju je ured otvorio 2024."
              - "Profil tehnokratsko-stručan u resoru s povijesnim političkim turbulencijama; rad na stabilizaciji sustava nakon nedavnih političkih kriza u Ministarstvu."
              - "Hook: bolnička mreža i konsolidacija, EU sredstva (NPOO Zdravstvo), nedostatak liječničkog kadra, dugotrajne liste čekanja, suradnja s HZZO-om na novim modelima ugovaranja."
          - Tone advice:
              - "Otvori s reformom bolničke mreže, EU sredstvima, listama čekanja i kadrovima — to su prioriteti aktualnog mandata."
              - "Ne pristupaj ministarstvu izvan konteksta EPPO istrage iz 2024 — pitanja nabave i integriteta su politički osjetljiva; framings koji ignoriraju to su rizični."
```

## 11. Out-of-band notes

For roles unfilled or interim.

## 12. Open questions

- Verify the exact date of Irena Hrstić's appointment as Minister of Health and any subsequent reshuffle following the EPPO procurement investigation.
- Named državni tajnici (state secretaries) under the current Minister.
- Ravnatelj HZZO, HZJZ, HALMED, AAZ with currency verified.
- Predsjednik Saborski odbor za zdravstvo i socijalnu politiku in the current Sabor.
- Predsjednik HLK, HLZ, Hrvatske komore medicinskih sestara, and Hrvatske ljekarničke komore with currency verified.
- Ravnatelji of the largest KBC and KB hospitals (KBC Zagreb, KB Dubrava, KBC Split, KBC Rijeka, KBC Osijek) with currency verified.
