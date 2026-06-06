# spec.md — `leaders.yml`

Single source of truth for the structure, semantics, and update rules of `leaders.yml` for Bulgarian health care (здравеопазване). The YAML must conform to this spec; if they disagree, the spec wins and the YAML is fixed.

## 1. Purpose

`leaders.yml` is an engagement register of named individuals in and around the Bulgarian health system. Each entry helps a reader inside the Министерство на здравеопазването (Ministry of Health), the Национална здравноосигурителна каса (NHIF), the Изпълнителна агенция по лекарствата (BDA), a hospital, or an adjacent body decide who to engage, how to engage them, and where.

The Bulgarian system combines a state Ministry of Health with single-payer statutory insurance through the NHIF (Национална здравноосигурителна каса). Hospitals are predominantly state, regional and municipal joint-stock companies. The Изпълнителна агенция по лекарствата (BDA) regulates medicines; the Регионална здравна инспекция (RZI) network supervises public health regionally. Bulgaria has experienced unusually high political instability since 2021 — seven elections in four years — producing frequent ministerial turnover and recurring caretaker governments appointed by the President under Article 99 of the Constitution.

## 2. Scope

**In scope:** Минист˅р-председател; Министър на здравеопазването; deputy ministers (заместник-министри); chief secretariat (главен секретар); Изпълнителен директор на NHIF; Изпълнителен директор of the Изпълнителна агенция по лекарствата (BDA) and the Изпълнителна агенция "Медицински надзор"; Директор на Националния център по обществено здраве и анализи (NCPHA); director of major university hospitals (Александровска, Пирогов, Свети Иван Рилски, Майчин дом, Лозенец, ИСУЛ); Председател на Народно събрание Комисия по здравеопазването; Председател на Българския лекарски съюз; Председател на Българския фармацевтичен съюз; Председател на Българската асоциация на професионалистите по здравни грижи.

**Out of scope:** operational staff below dirzhaven ekspert level; vendors; historical post-holders.

## 3. Structure

```
Заинтересовани страни в българското здравеопазване:
  - {Organisation}:
      - {Person}:
          - Title: ...
          - Stakeholder engagement notes: [...]
          - Tone advice: [...]
```

Indentation 2/6/10/14 spaces. Ordering: Правителство → Министерство на здравеопазването → NHIF → agencies (BDA, "Medicinski nadzor", NCPHA) → major hospitals → Народно събрание Комисия по здравеопазването → professional bodies.

## 4. Field definitions

Same family conventions. Party affiliation in parentheses using canonical Bulgarian abbreviations: `ГЕРБ-СДС`, `ПП-ДБ`, `ВЪзраждане`, `ДПС`, `БСП`, `Има такъв народ` (ITN), `Величие`, `МЕЧ`. Caretaker government members are typically non-partisan (technocratic) and should be noted as `(служебен / caretaker)`.

Names in Cyrillic with Romanised transliteration on first occurrence is acceptable; English-gloss titles where Bulgarian title is not self-evident.

## 5. Provenance and dating

Anchor facts to year, month or exact date. The Желязков coalition government (formed 16 January 2025) resigned 11 December 2025; the caretaker government of Андрей Гюров (Andrey Gyurov), appointed by President Rumen Radev, took office 19 February 2026 with Михаил Околийски (Mihail Okoliyski) as Minister of Health. Treat any Ministry entry pre-dating 19 February 2026 as stale; treat the caretaker tier as time-bounded — once the next elected government forms, the Health Minister will change.

## 6. Update workflow

1. Identify the change. 2. Verify against gov.bg, mh.government.bg, president.bg, parliament.bg, NHIF.bg, BDA.bg, Sofia Globe, Novinite, BTA, Capital, Mediapool, Dnevnik. 3. Apply minimum diff. 4. Confirm structure. 5. Re-validate cross-references.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating the Ministry as a continuous decision-making body — frequent caretaker rotations mean engagement is often time-bounded to a specific government.
- Importing NHS framings unmodified — Bulgaria has single-payer statutory insurance financed through wage-based contributions, with strong informal payments still documented as a persistent challenge.

## 9. Acronym glossary

- **БЛС** — Български лекарски съюз (Bulgarian Medical Association).
- **БФС** — Български фармацевтичен съюз.
- **BDA** — Изпълнителна агенция по лекарствата (Bulgarian Drug Agency).
- **NCPHA** — Национален център по обществено здраве и анализи.
- **NHIF / НЗОК** — Национална здравноосигурителна каса (National Health Insurance Fund).
- **RZI** — Регионална здравна инспекция (regional health inspectorate).

## 10. Worked example

```yaml
      - Михаил Околийски (Mihail Okoliyski) (служебен / caretaker):
          - Title: Министър на здравеопазването (Minister of Health) (от 19 февруари 2026, служебно правителство Андрей Гюров)
          - Stakeholder engagement notes:
              - "Министър на здравеопазването в служебното правителство на Андрей Гюров (назначено от Президента Румен Радев на 19 февруари 2026) след оставката на правителството на Желязков на 11 декември 2025."
              - "Поема ресорта в продължителен политически период на нестабилност: седем избори за четири години, повтарящи се служебни правителства, и продължаващи реформи в болничната мрежа и в системата на спешната медицинска помощ."
              - "Hook: реформа на болничната мрежа, спешна медицинска помощ, лекарствена политика, кадри и заплати в здравеопазването; пропазарни питчове без отчитане на политическата нестабилност не кацат."
          - Tone advice:
              - "Започвай с реформа на болничната мрежа, кадри в здравеопазването, лекарствена политика и Европейски фондове за здравеопазване — това са приоритетите на служебния етап."
              - "Не пишите дългосрочни мандатни ангажименти — служебното правителство е времево ограничено и стратегическите ангажименти ще бъдат отложени до следваща постоянна власт."
```

## 11. Out-of-band notes

For roles unfilled or interim.

## 12. Open questions

- Substantive Minister of Health after the next parliamentary election ends the Andrey Gyurov caretaker period.
- Named deputy ministers and chief secretary inside the Ministry of Health under the caretaker tier.
- Изпълнителен директор на NHIF following the December 2025 government resignation.
- Изпълнителен директор of the Изпълнителна агенция по лекарствата (BDA) and the Изпълнителна агенция "Медицински надзор" with currency verified.
- Председател на Народно събрание Комисия по здравеопазването in the current 51st National Assembly.
- Председател на Българския лекарски съюз, на Българския фармацевтичен съюз, and on the Българската асоциация на професионалистите по здравни грижи.
- Directors of the largest university hospitals (Александровска, Пирогов, Свети Иван Рилски, Майчин дом, Лозенец, ИСУЛ) with currency verified.
