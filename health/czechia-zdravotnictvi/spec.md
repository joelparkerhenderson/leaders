# spec.md — `leaders.yml`

Single source of truth for the structure, semantics, and update rules of `leaders.yml` for Czech health care (zdravotnictví). The YAML must conform to this spec; if they disagree, the spec wins and the YAML is fixed.

## 1. Purpose

`leaders.yml` is an engagement register of named individuals in and around Czech zdravotnictví. Each entry helps a reader inside Ministerstvo zdravotnictví ČR (MZČR), Všeobecná zdravotní pojišťovna (VZP) or another statutory fund, Státní ústav pro kontrolu léčiv (SÚKL), Státní zdravotní ústav (SZÚ), a hospital, or an adjacent body decide who to engage, how, and where.

The Czech system is Bismarckian statutory insurance financed through several health funds — VZP (the largest) plus six employee-and-sector funds — under a single benefits framework set by MZČR. Hospitals are predominantly state, regional and university joint-stock or contributory organisations. SÚKL regulates medicines and devices; SZÚ provides national public health; ÚZIS handles health information and statistics.

## 2. Scope

**In scope:** Předseda vlády; Ministr/Ministryně zdravotnictví; náměstci ministra (deputy ministers); ředitel VZP and the directors of the six other statutory funds; ředitel SÚKL; ředitel SZÚ; ředitel ÚZIS; ředitelé fakultních nemocnic (FN Motol, FN v Motole, VFN, FN Bulovka, FN Královské Vinohrady, FN Olomouc, FN Plzeň, FN Hradec Králové, FN Brno, FN Ostrava); předseda Sněmovní výbor pro zdravotnictví; prezident České lékařské komory (ČLK); prezident České stomatologické komory; prezident České lékárnické komory; předseda České asociace sester.

**Out of scope:** operational staff below ředitel odboru; vendors; historical post-holders.

## 3. Structure

```
České zdravotnictví — zúčastněné strany:
  - {Organisation}:
      - {Person}:
          - Title: ...
          - Stakeholder engagement notes: [...]
          - Tone advice: [...]
```

Indentation 2/6/10/14 spaces. Ordering: Vláda → Ministerstvo zdravotnictví → VZP a další zdravotní pojišťovny → SÚKL → SZÚ → ÚZIS → fakultní nemocnice → Poslanecká sněmovna výbor pro zdravotnictví → profesní komory.

## 4. Field definitions

Standard family conventions. Party affiliation in parentheses using canonical Czech abbreviations: `ANO`, `ODS`, `STAN`, `Piráti`, `KDU-ČSL`, `TOP 09`, `SPD`, `SOCDEM`, `Stačilo!`, `Přísaha`, `Motoristé sobě`. Titles in Czech with English glosses where useful.

## 5. Provenance and dating

Anchor facts to year, month or exact date. The Babiš government (ANO-SPD-Motoristé sobě coalition) was sworn in after the October 2025 election with Adam Vojtěch (ANO) returning as Ministr zdravotnictví — the post he held under the first Babiš government 2017-2020. Treat any Vláda entry pre-dating the Babiš government's confirmation in late 2025 / early 2026 as warranting re-verification; this is a discontinuity from the Fiala / Petr Pavel-era Vlastimil Válek (TOP 09) period.

## 6. Update workflow

1. Identify the change. 2. Verify against vlada.gov.cz, mzd.gov.cz, vzp.cz, sukl.cz, szu.cz, uzis.cz, psp.cz, Hospodářské noviny, Lidové noviny, Mladá fronta DNES, Zdravotnický deník, Medical Tribune CZ. 3. Apply minimum diff. 4. Confirm structure. 5. Re-validate cross-references.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating VZP as the only statutory insurer — six other funds operate and compete for members within a uniform benefits framework.
- Importing NHS framings unmodified — Czechia is Bismarckian multi-payer with regional ownership of hospitals; the comparators are Germany and Austria, not the UK.

## 9. Acronym glossary

- **ČLK** — Česká lékařská komora.
- **FN** — Fakultní nemocnice (university hospital).
- **MZČR** — Ministerstvo zdravotnictví České republiky.
- **SÚKL** — Státní ústav pro kontrolu léčiv (State Institute for Drug Control).
- **SZÚ** — Státní zdravotní ústav (National Institute of Public Health).
- **ÚZIS** — Ústav zdravotnických informací a statistiky.
- **VFN** — Všeobecná fakultní nemocnice v Praze (General University Hospital, Prague).
- **VZP** — Všeobecná zdravotní pojišťovna (the largest of seven statutory health funds; ~6 million enrollees of ~11 million population).

## 10. Worked example

```yaml
      - Adam Vojtěch (ANO):
          - Title: Ministr zdravotnictví (Minister of Health) (vlády Andreje Babiše, druhá Babišova vláda)
          - Stakeholder engagement notes:
              - "Ministr zdravotnictví ve druhé Babišově vládě (ANO-SPD-Motoristé sobě) po volbách do Poslanecké sněmovny v říjnu 2025; vrací se na pozici, kterou už zastával 2017-2020 v první Babišově vládě; ANO."
              - "Vystřídal Vlastimila Válka (TOP 09), který resort vedl čtyři roky ve Fialově vládě 2021-2025; přebírá poreformní agendu Válka včetně novely zákona o zdravotních službách a změn v lékové politice."
              - "Owns smlouvy mezi MZČR a VZP, dohodovací řízení o úhradách, lékovou politiku ve spolupráci se SÚKL, síť fakultních nemocnic, a vyjednávání s ČLK o platech a podmínkách lékařů."
              - "Hook: úhradová politika, dohodovací řízení, lékové reformy, fakultní nemocnice, digitalizace zdravotnictví, čerpání EU fondů na obnovu landují; pitche, které ignorují vícepojišťovnický systém, nelandují."
          - Tone advice:
              - "Otevři s úhradami, lékovou politikou a fakultními nemocnicemi — to jsou klasické MZČR páky a Vojtěchova oblast z prvního období."
              - "Necarguj s vícepojišťovnickým systémem — VZP je jen jedna ze sedmi pojišťoven, a pitche, které předpokládají jediného plátce, budou opraveny."
```

## 11. Out-of-band notes

For roles unfilled or interim.

## 12. Open questions

- Confirm Adam Vojtěch's substantive appointment date as Ministr zdravotnictví in the second Babiš government and the names of his náměstci.
- Ředitel VZP and ředitelé of the six other statutory funds with currency verified.
- Ředitel SÚKL, SZÚ and ÚZIS with currency verified.
- Předseda Poslanecké sněmovny výbor pro zdravotnictví in the current voličské období.
- Prezident České lékařské komory, České stomatologické komory, České lékárnické komory and předseda České asociace sester with currency verified.
- Ředitelé largest fakultní nemocnice (FN Motol, VFN, FN Bulovka, FN Královské Vinohrady, FN Olomouc, FN Plzeň, FN Hradec Králové, FN Brno, FN Ostrava) with currency verified.
