# spec.md — `leaders.yml`

Single source of truth for the structure, semantics, and update rules of `leaders.yml` for the Romanian sistemul de sănătate. The YAML must conform to this spec; if they disagree, the spec wins and the YAML is fixed.

## 1. Purpose

`leaders.yml` is an engagement register of named individuals in and around the Romanian health system. Each entry helps a reader inside Ministerul Sănătății, Casa Națională de Asigurări de Sănătate (CNAS), Agenția Națională a Medicamentului și a Dispozitivelor Medicale (ANMDMR), Institutul Național de Sănătate Publică (INSP), or an adjacent body decide who to engage, how, and where.

The Romanian system is Bismarckian single-payer through CNAS, with the Ministry setting policy. CNAS contracts hospitals and primary-care providers. ANMDMR regulates medicines and devices. INSP is the public-health institute. Hospitals are split between national, county (consilii județene) and municipal ownership. Political instability since the cancelled November 2024 presidential election produced the Bolojan government in mid-2025 and a coalition rupture leading to a partial caretaker arrangement in mid-2026.

## 2. Scope

**In scope:** Prim-ministrul; Ministrul Sănătății; secretari de stat; secretar general; Președinte CNAS; Președinte ANMDMR; Director General INSP; Director General Direcția Generală Asistență Medicală; Manageri ai marilor spitale (Spitalul Clinic Județean de Urgență București, Institutul Clinic Fundeni, Spitalul Universitar de Urgență București, Spitalul Universitar de Urgență Elias, SCJU Cluj, SCJU Iași, SCJU Timișoara); Președintele Comisiei pentru Sănătate a Camerei Deputaților; Președintele Comisiei pentru Sănătate Publică a Senatului; Președinte Colegiul Medicilor din România (CMR); Președinte Ordinul Asistenților Medicali Generaliști, Moașelor și Asistenților Medicali (OAMGMAMR); Președinte Colegiul Farmaciștilor din România.

**Out of scope:** operational staff below director de departament; vendors; historical post-holders.

## 3. Structure

```
Sistemul de sănătate românesc — părți interesate:
  - {Organisation}:
      - {Person}:
          - Title: ...
          - Stakeholder engagement notes: [...]
          - Tone advice: [...]
```

Indentation 2/6/10/14 spaces. Ordering: Guvern → Ministerul Sănătății → CNAS → ANMDMR → INSP → spitalele mari → Parlament (Camera și Senat) → Colegii.

## 4. Field definitions

Standard family conventions. Party affiliation using canonical Romanian abbreviations: `PSD`, `PNL`, `USR`, `AUR`, `UDMR` (Uniunea Democrată Maghiară din România), `Forța Dreptei`, `REPER`, `SOS România`. Titles in Romanian with English glosses.

## 5. Provenance and dating

Anchor facts to year, month or exact date. The Bolojan government formed in mid-2025 (PSD-PNL-USR-UDMR national-unity-style coalition) following the political crisis triggered by the cancelled November 2024 presidential election. Alexandru Rogobete (PSD) was Minister of Health for around 10 months before resigning in May 2026; Cseke Attila (UDMR), already Minister of Development, took over as interim Minister of Health following Rogobete's resignation. Treat any Minister of Health entry pre-dating the Bolojan government as warranting re-verification and treat the current arrangement as time-bounded pending coalition reconfiguration.

## 6. Update workflow

1. Identify the change. 2. Verify against gov.ro, ms.ro, cnas.ro, anm.ro, insp.gov.ro, cdep.ro, senat.ro, Digi24, G4Media, HotNews, Mediafax, Agerpres, Adevărul, Ziarul Financiar. 3. Apply minimum diff. 4. Confirm structure. 5. Re-validate cross-references.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating the Ministry as politically stable — the 2024-2026 cycle has produced multiple coalition shifts and ministerial transitions; engagement is time-bounded.
- Importing NHS framings unmodified — Romania is Bismarckian single-payer with strong informal payments documented as a persistent challenge.

## 9. Acronym glossary

- **ANMDMR** — Agenția Națională a Medicamentului și a Dispozitivelor Medicale din România.
- **CMR** — Colegiul Medicilor din România.
- **CNAS** — Casa Națională de Asigurări de Sănătate (statutory single payer).
- **INSP** — Institutul Național de Sănătate Publică.
- **OAMGMAMR** — Ordinul Asistenților Medicali Generaliști, Moașelor și Asistenților Medicali din România.
- **PNRR** — Planul Național de Redresare și Reziliență (national recovery plan; significant health investment envelope).
- **SCJU** — Spitalul Clinic Județean de Urgență (county emergency clinical hospital).

## 10. Worked example

```yaml
      - Cseke Attila (UDMR):
          - Title: Ministru al Sănătății (interimar) (Minister of Health, interim) (din mai 2026, în paralel cu funcția de Ministru al Dezvoltării)
          - Stakeholder engagement notes:
              - "Ministru al Sănătății în regim interimar din mai 2026 în guvernul Ilie Bolojan, după demisia ministrului Alexandru Rogobete (PSD) după 10 luni de mandat; păstrează în paralel funcția de Ministru al Dezvoltării — situație provizorie până la reconfigurarea coaliției."
              - "UDMR (Uniunea Democrată Maghiară din România); jurist de profesie; carieră politică lungă, cu multiple roluri ministeriale, inclusiv Dezvoltare (din 2025) — semnatar al actelor de continuitate pentru investițiile PNRR în sănătate."
              - "Owns continuarea investițiilor PNRR în sănătate (semnarea actelor adiționale, prelungirea termenelor de proiect până în august 2026), supravegherea CNAS, ANMDMR și INSP, și gestionarea fără politică de fond a unui resort în tranziție."
              - "Hook: PNRR Sănătate (spitale noi, dotări), continuitate administrativă, finanțarea CNAS, salarii personal medical, fonduri europene; pitch-uri strategice pe termen lung vor fi amânate până la un ministru titular."
          - Tone advice:
              - "Deschideți cu PNRR Sănătate, continuitate administrativă și finanțare CNAS — sunt prioritățile interimatului și terenul în care Cseke Attila este pregătit să decidă."
              - "Nu propuneți reforme structurale de mandat — interimatul este timp-limitat și reformele structurale vor fi amânate pentru următorul ministru titular și ciclul coaliției."
```

## 11. Out-of-band notes

For roles unfilled or interim.

## 12. Open questions

- Substantive Ministru al Sănătății after the interim arrangement ends.
- Named secretari de stat in Ministerul Sănătății during the interim period and after.
- Președinte CNAS, Președinte ANMDMR, Director General INSP with currency verified.
- Manageri ai marilor spitale clinice (Fundeni, SUUB, Elias, SCJU Cluj, SCJU Iași, SCJU Timișoara) with currency verified.
- Președinții Comisiilor pentru Sănătate ale Camerei Deputaților și Senatului în legislatura actuală.
- Președinte CMR, OAMGMAMR, Colegiul Farmaciștilor din România with currency verified.
