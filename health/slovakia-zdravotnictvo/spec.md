# spec.md — `leaders.yml`

Single source of truth for the structure, semantics, and update rules of `leaders.yml` for Slovak zdravotníctvo. The YAML must conform to this spec; if they disagree, the spec wins and the YAML is fixed.

## 1. Purpose

`leaders.yml` is an engagement register of named individuals in and around the Slovak health system. Each entry helps a reader inside Ministerstvo zdravotníctva SR (MZ SR), Všeobecná zdravotná poisťovňa (VšZP), Úrad pre dohľad nad zdravotnou starostlivosťou (ÚDZS), Štátny ústav pre kontrolu liečiv (ŠÚKL), Úrad verejného zdravotníctva (ÚVZ), or an adjacent body decide who to engage, how, and where.

The Slovak system is Bismarckian with three statutory funds (VšZP plus Dôvera and Union). MZ SR sets policy and contracts university hospitals; the regional ownership of smaller hospitals sits with VÚC (samosprávne kraje). ŠÚKL regulates medicines and devices; ÚVZ runs public health.

## 2. Scope

**In scope:** Predseda vlády; Minister zdravotníctva; štátni tajomníci; generálny tajomník MZ; predseda predstavenstva VšZP and generálni riaditelia Dôvery and Union; predseda ÚDZS; riaditeľ ŠÚKL; hlavný hygienik SR (ÚVZ); riaditelia veľkých univerzitných nemocníc (UNB Bratislava, UNM Martin, FN Trenčín, FNsP Žilina, UNLP Košice, FN Trnava, FN Nitra); predseda Výboru NR SR pre zdravotníctvo; prezident Slovenskej lekárskej komory (SLK); prezident Slovenskej komory sestier a pôrodných asistentiek (SKSaPA); prezident Slovenskej lekárnickej komory.

**Out of scope:** operational staff below riaditeľa odboru; vendors; historical post-holders.

## 3. Structure

```
Slovenské zdravotníctvo — zainteresované strany:
  - {Organisation}:
      - {Person}:
          - Title: ...
          - Stakeholder engagement notes: [...]
          - Tone advice: [...]
```

Indentation 2/6/10/14 spaces. Ordering: Vláda → MZ SR → zdravotné poisťovne (VšZP, Dôvera, Union) → ÚDZS → ŠÚKL → ÚVZ → univerzitné a fakultné nemocnice → NR SR Výbor pre zdravotníctvo → komory.

## 4. Field definitions

Standard family conventions. Party affiliation using canonical Slovak abbreviations: `Smer-SD`, `Hlas-SD`, `SNS`, `PS` (Progresívne Slovensko), `KDH`, `SaS`, `Sme rodina`, `Republika`. Titles in Slovak with English glosses.

## 5. Provenance and dating

Anchor facts to year, month or exact date. The fourth Fico government (Smer-SD, Hlas-SD, SNS) was sworn in 25 October 2023. Kamil Šaško (Hlas-SD) became Minister of Health on 10 October 2024.

## 6. Update workflow

1. Identify the change. 2. Verify against vlada.gov.sk, health.gov.sk, vszp.sk, udzs-sk.sk, sukl.sk, uvzsr.sk, nrsr.sk, Pravda, SME, Denník N, Trend, Zdravotnícke noviny. 3. Apply minimum diff. 4. Confirm structure. 5. Re-validate cross-references.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating Slovakia as a single-fund system — three statutory funds compete for members within a uniform benefits framework, and VšZP is dominant but not exclusive.
- Importing NHS framings unmodified — Slovakia is Bismarckian multi-payer with VÚC-level regional hospital ownership.

## 9. Acronym glossary

- **MZ SR** — Ministerstvo zdravotníctva Slovenskej republiky.
- **SKSaPA** — Slovenská komora sestier a pôrodných asistentiek.
- **SLK** — Slovenská lekárska komora.
- **ŠÚKL** — Štátny ústav pre kontrolu liečiv (medicines and devices regulator).
- **ÚDZS** — Úrad pre dohľad nad zdravotnou starostlivosťou (supervisory authority over health care).
- **ÚVZ SR** — Úrad verejného zdravotníctva Slovenskej republiky.
- **UNB / UNM / UNLP** — Univerzitná nemocnica Bratislava / Martin / L. Pasteura Košice.
- **VšZP** — Všeobecná zdravotná poisťovňa.
- **VÚC** — Vyšší územný celok (samosprávny kraj; eight of them; many regional hospitals are VÚC-owned).

## 10. Worked example

```yaml
      - Kamil Šaško (Hlas-SD):
          - Title: Minister zdravotníctva (Minister of Health) (od 10. októbra 2024)
          - Stakeholder engagement notes:
              - "Minister zdravotníctva v štvrtej vláde Roberta Fica (Smer-SD, Hlas-SD, SNS) od 10. októbra 2024; Hlas-SD; nahradil Zuzanu Dolinkovú (Hlas-SD), ktorá rezignovala."
              - "Narodený 5. novembra 1985 v Poprade; ekonomista; štúdium Applied Science and Management na University of Sussex v Anglicku, neskôr investičné bankovníctvo v Londýne — netradičný profil pre slovenského ministra zdravotníctva (zvyčajne lekár alebo zdravotnícky manažér)."
              - "Owns kontrakty medzi MZ SR a tromi zdravotnými poisťovňami (VšZP, Dôvera, Union), dohodu o cenách bodov, lieková politika, sieť nemocníc, kategorizácia liekov, e-zdravotníctvo (eRecept, ezdravie) a komunikáciu s komorami."
              - "Predstavil v máji 2026 'sedem kľúčových zmien' v liekovej politike — reforma kategorizácie liekov, dostupnosť moderných terapií pre deti a vážne chorých pacientov; lieková reforma je centrálnym dokumentom jeho mandátu."
              - "Hook: lieková reforma a dostupnosť, sieť nemocníc, dohoda s poisťovňami, e-zdravotníctvo a digitalizácia, EÚ fondy (Plán obnovy) landujú; pitchy ignorujúce tri-poisťovňový systém nelandujú."
          - Tone advice:
              - "Otvor liekovou reformou, sieťou nemocníc a digitalizáciou — sú to verejne komunikované priority a Šaškove profesionálne (ekonomické) silné stránky."
              - "Nepitchuj cez VšZP ako jediného plátcu — Slovensko má tri poisťovne v konkurenčnom prostredí, a framingy s jediným plátcom budú opravené."
```

## 11. Out-of-band notes

For roles unfilled or interim.

## 12. Open questions

- Named štátni tajomníci pod Šaškom with currency verified.
- Predseda predstavenstva VšZP, generálni riaditelia Dôvery a Union with currency verified.
- Predseda ÚDZS, riaditeľ ŠÚKL, hlavný hygienik SR with currency verified.
- Predseda Výboru NR SR pre zdravotníctvo in the current parlamentné obdobie.
- Riaditelia veľkých univerzitných a fakultných nemocníc (UNB Bratislava, UNM Martin, UNLP Košice, FN Trenčín, FNsP Žilina, FN Trnava, FN Nitra) with currency verified.
- Prezident SLK, SKSaPA, Slovenskej lekárnickej komory with currency verified.
