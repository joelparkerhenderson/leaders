# spec.md — `leaders.yml`

Single source of truth for the structure, semantics, and update rules of `leaders.yml` for the Latvian veselības aprūpes sistēma. The YAML must conform to this spec; if they disagree, the spec wins and the YAML is fixed.

## 1. Purpose

`leaders.yml` is an engagement register of named individuals in and around the Latvian health system. Each entry helps a reader inside Veselības ministrija, Nacionālais veselības dienests (NVD, single payer), Zāļu valsts aģentūra (ZVA, medicines agency), Slimību profilakses un kontroles centrs (SPKC, public health), Veselības inspekcija, or an adjacent body decide who to engage, how, and where.

The Latvian system is tax-funded (with limited compulsory health insurance contributions phased in then largely reversed). NVD acts as the single payer commissioning hospital and primary-care services. Major hospitals include Paula Stradiņa klīniskā universitātes slimnīca, Rīgas Austrumu klīniskā universitātes slimnīca, and the children's hospital Bērnu klīniskā universitātes slimnīca.

## 2. Scope

**In scope:** Ministru prezidents; Veselības ministrs; Veselības ministrijas valsts sekretārs; NVD direktors; ZVA direktors; SPKC direktors; Veselības inspekcijas vadītājs; lielāko slimnīcu vadītāji; Saeimas Sociālo un darba lietu komisijas priekšsēdētājs; Latvijas Ārstu biedrības (LĀB) prezidents; Latvijas Māsu asociācijas prezidents; Latvijas Farmaceitu biedrības prezidents.

**Out of scope:** operational staff below departamenta direktora; vendors; historical post-holders.

## 3. Structure

```
Latvijas veselības aprūpes sistēma — ieinteresētās puses:
  - {Organisation}:
      - {Person}:
          - Title: ...
          - Stakeholder engagement notes: [...]
          - Tone advice: [...]
```

Indentation 2/6/10/14 spaces. Ordering: Valdība → Veselības ministrija → NVD → ZVA → SPKC → Veselības inspekcija → major hospitals → Saeima Sociālo un darba lietu komisija → professional bodies.

## 4. Field definitions

Standard family conventions. Party affiliation using canonical Latvian abbreviations: `JV` (Jaunā Vienotība), `ZZS` (Zaļo un Zemnieku Savienība), `AS!` (Apvienotais saraksts), `LA` (Latvija pirmajā vietā), `NA` (Nacionālā apvienība), `Stabilitātei!`, `Progresīvie`, `Latvijas Reģionu Apvienība`. Titles in Latvian with English glosses.

## 5. Provenance and dating

Anchor facts to year, month or exact date. The new Latvian Cabinet of Ministers was confirmed by the Saeima on 28 May 2026; Hosams Abu Meri (JV) remains Veselības ministrs in the new configuration. Treat any Veselības ministrija entry pre-dating 28 May 2026 as warranting re-verification.

## 6. Update workflow

1. Identify the change. 2. Verify against mk.gov.lv, vm.gov.lv, vmnvd.gov.lv, zva.gov.lv, spkc.gov.lv, vi.gov.lv, saeima.lv, LSM.lv, Diena, Latvijas Avīze, Delfi, IR. 3. Apply minimum diff. 4. Confirm structure. 5. Re-validate cross-references.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating Latvia as a small system without specifics — the NVD single-payer model and hospital concentration in Riga produce distinct engagement geometry.
- Importing NHS framings unmodified — Latvia is tax-funded but with a centralised single-payer purchasing function.

## 9. Acronym glossary

- **LĀB** — Latvijas Ārstu biedrība (Latvian Medical Association).
- **NVD** — Nacionālais veselības dienests (National Health Service of Latvia; the single payer / commissioner).
- **SPKC** — Slimību profilakses un kontroles centrs (Centre for Disease Prevention and Control).
- **ZVA** — Zāļu valsts aģentūra (State Agency of Medicines).

## 10. Worked example

```yaml
      - Hosams Abu Meri (JV):
          - Title: Veselības ministrs (Minister for Health) (kopš 28. maija 2026; turpina amatu jaunajā Ministru kabinetā)
          - Stakeholder engagement notes:
              - "Veselības ministrs jaunajā Ministru kabinetā, ko Saeima apstiprināja 2026. gada 28. maijā; Jaunās Vienotības (JV) partijas pārstāvis; saglabā amatu pēc valdības rotācijas, kas notika 2026. gada pavasarī."
              - "Sektorā ar pastāvīgu uzmanību no plašsaziņas līdzekļu un Saeimas puses — ārstu un māsu trūkums, garas rindas, NVD finansējuma stabilitāte, slimnīcu konsolidācija."
              - "Owns NVD līgumus ar ārstniecības iestādēm, valsts apmaksāto pakalpojumu grozu, ZVA un SPKC uzraudzību, kā arī EU fondu un Atveseļošanas un noturības mehānisma (AF) īstenošanu veselības nozarē."
              - "Hook: rindu samazināšana, slimnīcu konsolidācija, primārā aprūpe, medicīnas darbinieku atalgojums, ES fondi un digitālā veselība (e-veselība) nolaižas; pitch, kas ignorē NVD lomu kā vienīgo pircēju, neielaižas."
          - Tone advice:
              - "Sāc ar rindu samazināšanu, slimnīcu konsolidāciju, NVD finansējumu un medicīnas darbinieku trūkumu — tās ir politiski jutīgākās līnijas un Saeimas pārbaudes priekšmeti."
              - "Nepiedāvājiet centralizētas valdības iepirkuma modeļus — Latvijas modelī NVD darbojas kā vienīgais komisionārs; pārkārtojot to ārpus NVD, sarunas tiek pārvirzītas atpakaļ uz NVD."
```

## 11. Out-of-band notes

For roles unfilled or interim.

## 12. Open questions

- Confirm Hosams Abu Meri's biographical detail, full term dates and koalīcijas portfeļa pozīciju jaunajā 2026 Ministru kabinetā.
- Named Veselības ministrijas valsts sekretārs and parlamentārie sekretāri with currency verified.
- NVD, ZVA, SPKC, Veselības inspekcijas direktori with currency verified.
- Saeimas Sociālo un darba lietu komisijas priekšsēdētājs in the current Saeima.
- Largest slimnīcu vadītāji (Paula Stradiņa klīniskā universitātes slimnīca, Rīgas Austrumu klīniskā universitātes slimnīca, Bērnu klīniskā universitātes slimnīca).
- Latvijas Ārstu biedrības, Latvijas Māsu asociācijas, Latvijas Farmaceitu biedrības prezidenti with currency verified.
