# spec.md — `leaders.yml`

Single source of truth for the structure, semantics, and update rules of `leaders.yml` for the Lithuanian sveikatos sistema. The YAML must conform to this spec; if they disagree, the spec wins and the YAML is fixed.

## 1. Purpose

`leaders.yml` is an engagement register of named individuals in and around the Lithuanian health system. Each entry helps a reader inside Sveikatos apsaugos ministerija (SAM), Valstybinė ligonių kasa (VLK, statutory health-insurance fund), Valstybinė vaistų kontrolės tarnyba (VVKT, medicines agency), Higienos institutas, an LSMU teaching hospital, or an adjacent body decide who to engage, how, and where.

The Lithuanian system is Bismarckian social-insurance through VLK financed by Privalomojo sveikatos draudimo (PSD) contributions. SAM sets policy; VLK commissions care. Major hospitals include Vilniaus universiteto ligoninė Santaros klinikos and Lietuvos sveikatos mokslų universiteto ligoninė Kauno klinikos.

## 2. Scope

**In scope:** Ministras pirmininkas; Sveikatos apsaugos ministras; viceministrai; SAM kanceliarijos vadovas; VLK direktorius; VVKT direktorius; Higienos instituto direktorius; Nacionalinio visuomenės sveikatos centro direktorius; Vilniaus universiteto ligoninės Santaros klinikų generalinis direktorius; LSMU Kauno klinikų generalinis direktorius; Seimo Sveikatos reikalų komiteto pirmininkas; Lietuvos gydytojų sąjungos pirmininkas; Lietuvos slaugos specialistų organizacijos pirmininkas; Lietuvos farmacijos sąjungos prezidentas.

**Out of scope:** operational staff below skyriaus vedėjo; vendors; historical post-holders.

## 3. Structure

```
Lietuvos sveikatos sistema — suinteresuotosios šalys:
  - {Organisation}:
      - {Person}:
          - Title: ...
          - Stakeholder engagement notes: [...]
          - Tone advice: [...]
```

Indentation 2/6/10/14 spaces. Ordering: Vyriausybė → SAM → VLK → VVKT → Higienos institutas → NVSC → major hospitals → Seimo Sveikatos reikalų komitetas → professional bodies.

## 4. Field definitions

Standard family conventions. Party affiliation using canonical Lithuanian abbreviations: `LSDP` (Lietuvos socialdemokratų partija), `TS-LKD` (Tėvynės sąjunga–Lietuvos krikščionys demokratai), `DSVL` (Demokratų sąjunga 'Vardan Lietuvos'), `LVŽS` (Lietuvos valstiečių ir žaliųjų sąjunga), `LRLS` (Lietuvos Respublikos liberalų sąjūdis), `LP` (Laisvės partija), `LLRA-KŠS`, `NA` (Nacionalinis susivienijimas). Titles in Lithuanian with English glosses.

## 5. Provenance and dating

Anchor facts to year, month or exact date. After the October 2024 Seimas election and subsequent coalition formation, Marija Jakubauskienė took office as Sveikatos apsaugos ministrė on 12 December 2024. Treat any SAM entry pre-dating 12 December 2024 as warranting re-verification.

## 6. Update workflow

1. Identify the change. 2. Verify against lrv.lt, sam.lrv.lt, vlk.lt, vvkt.lt, hi.lt, nvsc.lrv.lt, lrs.lt, LRT, BNS, 15min.lt, Lietuvos rytas, Verslo žinios, Medicinos žinios. 3. Apply minimum diff. 4. Confirm structure. 5. Re-validate cross-references.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Importing NHS framings unmodified — Lithuania is Bismarckian single-payer through VLK, not Beveridgean.
- Ignoring the LSMU-VU duopoly — the two academic-clinical centres (Vilnius Santaros and Kaunas Klinikos) dominate tertiary care and are key engagement counterparties.

## 9. Acronym glossary

- **LSMU** — Lietuvos sveikatos mokslų universitetas (Lithuanian University of Health Sciences, Kaunas).
- **NVSC** — Nacionalinis visuomenės sveikatos centras (National Public Health Centre).
- **PSD** — Privalomasis sveikatos draudimas (compulsory health insurance).
- **SAM** — Sveikatos apsaugos ministerija (Ministry of Health).
- **Santaros klinikos** — Vilniaus universiteto ligoninė Santaros klinikos.
- **VLK** — Valstybinė ligonių kasa (statutory health-insurance fund).
- **VVKT** — Valstybinė vaistų kontrolės tarnyba (medicines agency).

## 10. Worked example

```yaml
      - Marija Jakubauskienė:
          - Title: Sveikatos apsaugos ministrė (Minister of Health) (nuo 2024 m. gruodžio 12 d.)
          - Stakeholder engagement notes:
              - "Sveikatos apsaugos ministrė nuo 2024 m. gruodžio 12 d., prisaikdinta Seime; akademinė karjera — biomedicinos mokslų daktarė, asocijuota profesorė ir Vilniaus universiteto Medicinos fakulteto Sveikatos mokslų instituto direktorė."
              - "Pareigas užima trumpu po Seimo rinkimų (2024 m. spalis) suformuotos koalicinės vyriausybės laikotarpiu; politinė laikrodžio rodyklė trumpa, ir prioritetai turi būti vykdomi greitai."
              - "Owns VLK biudžeto derybas, paslaugų krepšelio peržiūrą, VVKT ir Higienos instituto priežiūrą, EU lėšų (RRF) panaudojimą sveikatos sektoriuje, ir Baltijos politinį dialogą sveikatos srityje (gegužės 2026 d. 20-asis Baltijos politinis dialogas Vilniuje)."
              - "Hook: VLK paslaugų krepšelis, slaugos ir gydytojų trūkumas, regioninių ligoninių konsolidacija, e. sveikata ir Baltijos bendradarbiavimas (Latvija, Estija) nuleidžia; pitch, kuris ignoruoja VLK kaip pirkėją, nenuleidžia."
          - Tone advice:
              - "Pradėk nuo VLK krepšelio, gydytojų trūkumo, regioninių ligoninių, e. sveikatos ir Baltijos bendradarbiavimo — tai politinės linijos su trumpu kadencijos laikrodžiu."
              - "Nesiūlyk centralizuotos ministerijos kaip pirkėjo — Lietuva veikia per VLK kaip vienintelį PSD pirkėją; framingai, ignoruojantys VLK, bus pataisyti."
```

## 11. Out-of-band notes

For roles unfilled or interim.

## 12. Open questions

- Confirm Marija Jakubauskienė's koalicijos pozicija ir partinė priklausomybė.
- Named viceministrai and kanceliarijos vadovas under Jakubauskienė with currency verified.
- VLK, VVKT, Higienos instituto, NVSC direktoriai with currency verified.
- Seimo Sveikatos reikalų komiteto pirmininkas in the post-October-2024 Seimas.
- Vilniaus universiteto ligoninės Santaros klinikų ir LSMU Kauno klinikų generaliniai direktoriai with currency verified.
- Lietuvos gydytojų sąjungos, Lietuvos slaugos specialistų organizacijos, ir Lietuvos farmacijos sąjungos vadovai with currency verified.
