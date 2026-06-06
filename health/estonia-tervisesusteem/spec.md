# spec.md — `leaders.yml`

Single source of truth for the structure, semantics, and update rules of `leaders.yml` for the Estonian tervisesüsteem (health system). The YAML must conform to this spec; if they disagree, the spec wins and the YAML is fixed.

## 1. Purpose

`leaders.yml` is an engagement register of named individuals in and around the Estonian health system. Each entry helps a reader inside Sotsiaalministeerium, Tervisekassa (the statutory health insurance fund), Terviseamet (Health Board), Ravimiamet (Medicines Agency), Tervise Arengu Instituut (TAI), or an adjacent body decide who to engage, how, and where.

The Estonian system combines a state Sotsiaalministeerium with statutory single-payer insurance through Tervisekassa (Estonian Health Insurance Fund). Estonia is internationally recognised for digital-health maturity — the X-tee infrastructure, e-prescription, e-health record (and TIS) are operational baselines. In 2025 the dual Tervise- ja tööminister + Sotsiaalkaitseminister roles were consolidated back into a single Sotsiaalminister.

## 2. Scope

**In scope:** Peaminister; Sotsiaalminister; Sotsiaalministeeriumi kantsler and asekantslerid for tervishoiu and rahva tervise; Tervisekassa juhatuse esimees; Terviseameti peadirektor; Ravimiameti peadirektor; Tervise Arengu Instituudi (TAI) direktor; Tervise ja Heaolu Infosüsteemide Keskus (TEHIK) direktor; tervishoiuasutuste juhid for the largest hospitals (Põhja-Eesti Regionaalhaigla, Tartu Ülikooli Kliinikum, Ida-Tallinna Keskhaigla, Lääne-Tallinna Keskhaigla); Riigikogu sotsiaalkomisjoni esimees; Eesti Arstide Liidu, Eesti Õdede Liidu and Eesti Perearstide Seltsi presidents.

**Out of scope:** operational staff below osakonnajuhataja; vendors; historical post-holders.

## 3. Structure

```
Eesti tervisesüsteem — sidusrühmad:
  - {Organisation}:
      - {Person}:
          - Title: ...
          - Stakeholder engagement notes: [...]
          - Tone advice: [...]
```

Indentation 2/6/10/14 spaces. Ordering: Valitsus → Sotsiaalministeerium → Tervisekassa → Terviseamet → Ravimiamet → TAI → TEHIK → major hospitals → Riigikogu sotsiaalkomisjon → professional bodies.

## 4. Field definitions

Standard family conventions. Party affiliation using canonical Estonian abbreviations: `RE` (Reformierakond), `EE200` (Eesti 200), `SDE` (Sotsiaaldemokraatlik Erakond), `Isamaa`, `EKRE`, `Keskerakond`, `Parempoolsed`, `EER` (Eestimaa Rohelised). Titles in Estonian with English glosses.

## 5. Provenance and dating

Anchor facts to year, month or exact date. The Estonian government has been in coalition flux since 2024; the Kallas → Michal premiership transition in mid-2024 and subsequent reshuffles produced the 2025 ministerial-portfolio consolidation that merged the Tervise- ja tööminister role into the unified Sotsiaalminister.

## 6. Update workflow

1. Identify the change. 2. Verify against valitsus.ee, sm.ee, tervisekassa.ee, terviseamet.ee, ravimiamet.ee, tai.ee, riigikogu.ee, ERR, Postimees, Eesti Päevaleht, Äripäev. 3. Apply minimum diff. 4. Confirm structure. 5. Re-validate cross-references.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Importing NHS framings unmodified — Estonia is statutory insurance with strong digital infrastructure operated by TEHIK and Tervisekassa, not a tax-funded service.
- Treating Estonia as small-scale digital — the X-tee-and-TIS architecture is widely studied and informs other countries' digital roadmaps; the pitch baseline is high.

## 9. Acronym glossary

- **Ravimiamet** — Estonian Medicines Agency.
- **Sotsiaalministeerium** — Ministry of Social Affairs (combined health, social welfare and labour from 2025).
- **TEHIK** — Tervise ja Heaolu Infosüsteemide Keskus (Centre for Health and Welfare Information Systems).
- **Terviseamet** — Estonian Health Board.
- **Tervisekassa** — Estonian Health Insurance Fund (statutory single payer).
- **TIS** — Tervise infosüsteem (the central Estonian electronic health record).
- **TAI** — Tervise Arengu Instituut (National Institute for Health Development).
- **X-tee** — X-Road, the inter-agency data exchange backbone underpinning Estonian e-government.

## 10. Worked example

```yaml
      - Karmen Joller (RE):
          - Title: Sotsiaalminister (Minister of Social Affairs) (alates 2025)
          - Stakeholder engagement notes:
              - "Sotsiaalminister alates 2025; vastutab konsolideeritud sotsiaalvaldkonna eest pärast 2025. aasta portfellide ühendamist (eelnev Tervise- ja tööminister Riina Sikkut SDE lahkus 11. märtsil 2025)."
              - "Reformierakonna profiil; arstiteadusliku tausta ja perearsti-praktikuna toodud erudeerituse tervishoiusektori juhatust."
              - "Hook: tervishoiu rahastamine ja Tervisekassa eelarve, perearstindus, digiterve (TIS, eRetsept, X-tee), psühhiaatria, ravimite kättesaadavus ja eakatehoolekanne maanduvad."
          - Tone advice:
              - "Ava perearstindus, Tervisekassa rahastus ja digi-tervis — need on poliitilisemad kui akuuthooldus ja Joller suudab need ka klinitsisitiline keele kõnelema."
              - "Ära paku tsentraliseeritud raamistikku NHS-i stiilis — Eesti süsteem on Bismarcki, Tervisekassa-keskne ja tehnoloogiaküps, ja staatilised framing tagastatakse."
```

## 11. Out-of-band notes

For roles unfilled or interim.

## 12. Open questions

- Confirm Karmen Joller's biographical detail, party affiliation and date of taking office as Sotsiaalminister.
- Named kantsler and asekantslerid for tervishoiu and rahva tervise inside Sotsiaalministeerium.
- Tervisekassa juhatuse esimees with currency verified.
- Terviseameti, Ravimiameti, TAI and TEHIK peadirektorid with currency verified.
- Riigikogu sotsiaalkomisjoni esimees and party spokespeople in the current Riigikogu term.
- Eesti Arstide Liidu, Eesti Õdede Liidu and Eesti Perearstide Seltsi presidents with currency verified.
- Largest hospital juhid (Põhja-Eesti Regionaalhaigla, Tartu Ülikooli Kliinikum, Ida-Tallinna Keskhaigla, Lääne-Tallinna Keskhaigla).
