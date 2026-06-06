# spec.md — `leaders.yml`

Single source of truth for the structure, semantics, and update rules of `leaders.yml` for the Maltese health system. The YAML must conform to this spec; if they disagree, the spec wins and the YAML is fixed.

## 1. Purpose

`leaders.yml` is an engagement register of named individuals in and around the Maltese health system. Each entry helps a reader inside the Ministry for Health and Active Ageing, Mater Dei Hospital, the Medicines Authority, the Health Care Standards Directorate, or an adjacent body decide who to engage, how, and where.

The Maltese system is tax-funded universal Beveridgean — Mater Dei Hospital is the main acute facility; Gozo General Hospital serves the Gozo region; primary care is delivered through health centres. The Medicines Authority regulates medicines and devices. The Health Care Standards Directorate handles supervision and licensing. The Ministry's portfolio combines Health and Active Ageing in a single mandate.

## 2. Scope

**In scope:** Prime Minister; Minister for Health and Active Ageing; Parliamentary Secretary; Permanent Secretary; CEO of Mater Dei Hospital; CEO of Gozo General Hospital; Chairperson and CEO of the Medicines Authority; Superintendent of Public Health and Chief Medical Officer; Director General Strategy and Sustainability; Chairperson of the Parliamentary Standing Committee on Health; President of the Medical Association of Malta (MAM); President of the Malta Union of Midwives and Nurses (MUMN); President of the Pharmacy Association.

**Out of scope:** operational staff below directorate level; vendors; historical post-holders.

## 3. Structure

```
Maltese health system stakeholders:
  - {Organisation}:
      - {Person}:
          - Title: ...
          - Stakeholder engagement notes: [...]
          - Tone advice: [...]
```

Indentation 2/6/10/14 spaces. Ordering: Government → Ministry for Health and Active Ageing → Mater Dei Hospital → Gozo General Hospital → Medicines Authority → Public Health → Parliament Health Committee → professional bodies.

## 4. Field definitions

Standard family conventions. Party affiliation using canonical Maltese abbreviations: `PL` (Partit Laburista), `PN` (Partit Nazzjonalista), `ADPD` (Alternattiva Demokratika-Partit Demokratiku), `Imperium Europa`, `Volt Malta`. Titles in English with Maltese where commonly used.

## 5. Provenance and dating

Anchor facts to year, month or exact date. Jo Etienne Abela has been Minister for Health and Active Ageing since January 2024 in the second Robert Abela government (PL).

## 6. Update workflow

1. Identify the change. 2. Verify against gov.mt, deputyprimeminister.gov.mt, parlament.mt, materdeihospital.org.mt, medicinesauthority.gov.mt, Times of Malta, Malta Independent, MaltaToday, Lovin Malta, TVMnews. 3. Apply minimum diff. 4. Confirm structure. 5. Re-validate cross-references.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating Malta as a single-hospital system — Gozo's island geography and the cross-border medical hub aspirations make it a multi-node environment.
- Importing NHS England framings unmodified — Malta is universal and tax-funded but at small scale with strong international referrals.

## 9. Acronym glossary

- **MAM** — Medical Association of Malta.
- **MUMN** — Malta Union of Midwives and Nurses.
- **PEP / PrEP** — Post-exposure / pre-exposure prophylaxis (HIV).

## 10. Worked example

```yaml
      - Jo Etienne Abela (PL):
          - Title: Minister for Health and Active Ageing (from January 2024)
          - Stakeholder engagement notes:
              - "Minister for Health and Active Ageing in the second Robert Abela Labour government since January 2024; PL; born 29 November 1975 in Gozo; surgeon by background, with consultancy training in Glasgow specialising in oesophageal and pancreatic surgery."
              - "Studied medicine and surgery at the University of Malta (1993-1999) and worked at St Luke's Hospital and later Mater Dei; brings clinical surgical credibility into a portfolio that has historically been led by non-clinicians."
              - "Announced rare disease commitments and strengthened cross-border healthcare February 2026; made PEP and PrEP free of charge January 2026 — public-health-progressive line on infectious disease and HIV prevention."
              - "Active international profile: addressed MedTech World Dubai 2026 Conference; met UAE Minister for Health and Prevention — positions Malta as a Mediterranean medical-innovation hub."
              - "Hook: rare diseases, cross-border healthcare, medical innovation hub, active ageing, PEP/PrEP and infectious disease prevention, Mater Dei modernisation and Gozo service planning land; vendor-only pitches without clinical content do not."
          - Tone advice:
              - "Lead with rare diseases, cross-border, active ageing, surgical innovation and the Med-Tech hub framing — these are his clinical-surgical and Mediterranean-strategic priorities."
              - "Do not pitch as if the portfolio were 'Health' only — 'and Active Ageing' is a co-headline; framings that ignore ageing and the older-population services miss the brief."
```

## 11. Out-of-band notes

For roles unfilled or interim.

## 12. Open questions

- Named Parliamentary Secretary and Permanent Secretary in the Ministry for Health and Active Ageing with currency verified.
- CEO Mater Dei Hospital and CEO Gozo General Hospital with currency verified.
- Chairperson and CEO of the Medicines Authority with currency verified.
- Superintendent of Public Health and Chief Medical Officer with currency verified.
- Chairperson Parliamentary Standing Committee on Health in the current legislature.
- President of the Medical Association of Malta (MAM), Malta Union of Midwives and Nurses (MUMN), and Pharmacy Association with currency verified.
