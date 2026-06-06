# spec.md — `leaders.yml`

Single source of truth for the Moldovan health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Moldovan Ministerul Sănătății (Ministry of Health), Compania Naţională de Asigurări în Medicină (CNAM), Agenția Medicamentului și Dispozitivelor Medicale (AMDM), Agenția Națională pentru Sănătate Publică (ANSP), and adjacent bodies.

The Moldovan system has compulsory health insurance through CNAM; the Ministry sets policy; AMDM regulates medicines; ANSP runs public health. The Maia Sandu government has pursued reform aligned with EU accession; signed WHO agreement for 2026-2027 health-system modernisation.

## 2. Scope

In scope: President; PM; Minister of Health; Secretary of State; Director CNAM; Director AMDM; Director ANSP; Heads of major hospitals (Institutul Mamei și Copilului, Spitalul Clinic Republican Toma Ciorbă, Spitalul Clinic Municipal Bălți); Parliament Health, Social Protection and Family Committee Chair; Moldovan Medical Association.

## 3. Structure

Standard. Ordering: PM → Ministry → CNAM → AMDM → ANSP → major hospitals → Parliament Committee → Moldovan Medical Association.

## 4. Field definitions

Party affiliation: `PAS` (Partidul Acțiune și Solidaritate — Sandu), `BCS` (Bloc Comunist-Socialist), `PMA` (Partidul nostru), `MAN` (Mișcarea Alternativă Națională), `Șor`. Titles in Romanian / English.

## 5. Provenance and dating

Emil Ceban has served as Ministrul Sănătății in the post-2025-cabinet-reshuffle PAS government; signed WHO Europe Cooperation Agreement for 2026-2027 with WHO Regional Director Hans Kluge; active 2026 on hospital reform, hantavirus surveillance reassurance, and Spitalul Florești searches comments.

## 6. Update workflow

Verify against gov.md, parlament.md, ms.gov.md, cnam.md, amed.md, ansp.md, Realitatea.md, Telegraph.md, Moldpres, Newsmaker.md, Ziarul de Gardă.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating Ministry as buyer — CNAM is the statutory insurer.
- Importing US framings — Moldova is small-country mandatory insurance with significant EU-funded reform.

## 9. Acronym glossary

- **AMDM** — Agenția Medicamentului și Dispozitivelor Medicale.
- **ANSP** — Agenția Națională pentru Sănătate Publică.
- **CNAM** — Compania Naţională de Asigurări în Medicină.

## 10. Worked example

```yaml
      - Emil Ceban (PAS):
          - Title: Ministrul Sănătății (Minister of Health) (in the PAS government, since 2025 cabinet reshuffle)
          - Stakeholder engagement notes:
              - "Ministrul Sănătății in the PAS (Partidul Acțiune și Solidaritate — Maia Sandu) government following the 2025 cabinet reshuffle (the gov.md/en/team/minister-health-0 page confirms his role); pre-political background includes leadership of Universitatea de Stat de Medicină și Farmacie 'Nicolae Testemițanu' as Rector."
              - "Active 2026: signed Cooperation Agreement with WHO for 2026-2027 modernisation of the healthcare system with WHO Regional Director for Europe Hans Henri P. Kluge (DoctorulZilei); reassured public after hantavirus outbreak (Realitatea.md: 'nu este niciun risc pentru Republica Moldova'); statement that Spitalul Clinic de Boli Infecțioase 'Toma Ciorbă' nu se închide și nu vor fi concedieri (Moldpres); commented on Spitalul Raional Florești searches; presented 2026 priorities (Realitatea: 'între reforme și deficit de personal')."
              - "Met UN Resident Coordinator and WHO Head of Office (UN Moldova X post 2026)."
              - "Owns Ministry policy, CNAM coordination, AMDM medicines regulation, ANSP public health, hospital network modernisation, doctor-shortage / workforce-retention programmes, EU accession health-acquis alignment, and Moldova's WHO Europe and Eastern Partnership health cooperation."
              - "Hook: WHO-Moldova 2026-2027 cooperation, EU accession health-acquis alignment, hospital reform (Bălți construction), workforce retention, mental health, hantavirus and infectious-disease surveillance, refugee-health (Ukrainian war IDPs in Moldova) land."
          - Tone advice:
              - "Open with WHO cooperation, EU acquis alignment, Bălți hospital construction and workforce retention — these are his sustained 2025-2026 priorities."
              - "Do not pitch with Russia-aligned framings — the PAS government is explicitly EU-accession-oriented; Russia-aligned framings will be politically misaligned with Moldovan executive direction."
```

## 11. Out-of-band notes

For roles unfilled or in transition.

## 12. Open questions

- Named Secretaries of State under Ceban with currency verified.
- Director CNAM, Director AMDM, Director ANSP with currency verified.
- Heads of Institutul Mamei și Copilului, Spitalul Clinic Republican Toma Ciorbă, Spitalul Clinic Municipal Bălți with currency verified.
- Parliament Health, Social Protection and Family Committee Chair with currency verified.
- President Moldovan Medical Association with currency verified.
