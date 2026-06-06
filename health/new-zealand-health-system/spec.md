# spec.md — `leaders.yml`

Single source of truth for the structure, semantics, and update rules of `leaders.yml` for the Aotearoa New Zealand health system. The YAML must conform to this spec; if they disagree, the spec wins and the YAML is fixed.

## 1. Purpose

`leaders.yml` is an engagement register of named individuals in and around the Aotearoa New Zealand health system. Each entry helps a reader inside the Ministry of Health (Manatū Hauora), Health New Zealand — Te Whatu Ora, the Māori Health Authority's successor arrangements after the 2024 disestablishment of Te Aka Whai Ora, Pharmac (Pharmaceutical Management Agency), Medsafe, a district / region of Te Whatu Ora, or an adjacent body decide who to engage, how, and where.

The 2022 Pae Ora reforms created Health New Zealand — Te Whatu Ora as a single national delivery entity replacing the 20 former DHBs, and a parallel Māori Health Authority — Te Aka Whai Ora. The Luxon-led coalition government (National, ACT, NZ First) disestablished Te Aka Whai Ora in 2024 and folded its functions into Te Whatu Ora and Manatū Hauora; Hauora Māori Advisory Committees and Iwi-Māori Partnership Boards remain. Pharmac is the central buyer of pharmaceuticals. Medsafe regulates medicines and devices.

## 2. Scope

**In scope:** Prime Minister; Minister of Health; Associate Ministers (Mental Health; Pacific Peoples Health where filled; Pharmac portfolio); Director-General of Health and Chief Executive of Manatū Hauora; CEO Health New Zealand — Te Whatu Ora and Te Whatu Ora Board Chair; CE Pharmac and Pharmac Board Chair; Director Medsafe; Chief Medical Officer; Chief Nursing Officer; Chair Hauora Māori Advisory Committee; Chair Health Select Committee of Parliament; President NZMA, NZNO and PSNZ; Chair RNZCGP.

**Out of scope:** operational staff below Deputy Director-General federally and below Group Director inside Te Whatu Ora; vendors; historical post-holders.

## 3. Structure

```
Aotearoa New Zealand health stakeholders:
  - {Organisation}:
      - {Person}:
          - Title: ...
          - Stakeholder engagement notes: [...]
          - Tone advice: [...]
```

Indentation 2/6/10/14 spaces. Ordering: Cabinet → Manatū Hauora → Health NZ — Te Whatu Ora → Pharmac → Medsafe → Hauora Māori arrangements → Parliament Health Select Committee → professional bodies (NZMA, NZNO, RNZCGP, PSNZ).

## 4. Field definitions

Standard family conventions. Party affiliation using canonical NZ abbreviations: `National`, `Labour`, `Greens`, `ACT`, `NZ First`, `Te Pāti Māori`. Titles in English with te reo Māori names where used officially.

## 5. Provenance and dating

Anchor facts to year, month or exact date. The Luxon coalition (National-ACT-NZ First) has been in office since November 2023. Simeon Brown (National) was appointed Minister of Health in January 2025 in a reshuffle that moved Shane Reti out of the portfolio.

## 6. Update workflow

1. Identify the change. 2. Verify against beehive.govt.nz, health.govt.nz, tewhatuora.govt.nz, pharmac.govt.nz, medsafe.govt.nz, parliament.nz, RNZ, NZ Herald, Stuff, 1News, Newshub, NewsGP NZ. 3. Apply minimum diff. 4. Confirm structure. 5. Re-validate cross-references.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating Health NZ — Te Whatu Ora as a Ministry sub-unit — it is a Crown entity with its own board and operational authority.
- Importing NHS framings without adapting for te Tiriti o Waitangi obligations and Hauora Māori partnership arrangements.

## 9. Acronym glossary

- **DHB** — District Health Board (the 20 pre-2022 entities, now subsumed into Te Whatu Ora).
- **Hauora Māori** — Māori health.
- **HQSC** — Health Quality and Safety Commission.
- **IMPB** — Iwi-Māori Partnership Boards (statutory bodies under Pae Ora).
- **Manatū Hauora** — Ministry of Health.
- **Pae Ora** — the 2022 Pae Ora (Healthy Futures) Act.
- **Pharmac** — Pharmaceutical Management Agency.
- **PHO** — Primary Health Organisation.
- **RNZCGP** — Royal New Zealand College of General Practitioners.
- **Te Aka Whai Ora** — former Māori Health Authority (disestablished 2024).
- **Te Tiriti o Waitangi** — Treaty of Waitangi.
- **Te Whatu Ora** — Health New Zealand (the operational delivery Crown entity).

## 10. Worked example

```yaml
      - Hon Simeon Brown (National):
          - Title: Minister of Health (from January 2025)
          - Stakeholder engagement notes:
              - "Minister of Health from January 2025 in the Luxon (National-ACT-NZ First) coalition; National; took over the portfolio from Hon Shane Reti in a Cabinet reshuffle; previously held the Transport, Auckland and Local Government portfolios."
              - "Mandate framed around accessibility, waiting times, frontline service strengthening and delivery against the Government Health Targets — explicit ministerial vocabulary used in 2026 Budget releases."
              - "Announced February 2026: AI scribes introduced in emergency departments nationally — first major minister-led digital-health policy of the term; April 2026 announced new Health NZ Board Chair and Board members."
              - "Owns the 2026 Budget Health envelope (described publicly as 'record health funding'), Health NZ accountability, the post-disestablishment Hauora Māori arrangements, Pharmac, Medsafe, and the national priority on workforce and infrastructure."
              - "Hook: waiting times, workforce, AI in clinical settings, hospital infrastructure investment, Health NZ accountability and Government Health Targets land; the post-Pae Ora institutional rearrangement is a sensitive zone — pitches must respect the Hauora Māori Advisory Committee and IMPB roles."
          - Tone advice:
              - "Lead with waiting times, workforce, frontline service strengthening, hospital infrastructure and digital health (AI scribes, electronic medication management) — these are Brown's authored target-frame priorities."
              - "Do not pitch as if Hauora Māori has been removed from the system — Te Aka Whai Ora was disestablished but Hauora Māori Advisory Committees and IMPBs remain; treaty-blind framings will be marked down."
```

## 11. Out-of-band notes

For roles unfilled or interim.

## 12. Open questions

- Named Associate Ministers (Mental Health, Pharmac and others) under Brown with currency verified.
- Director-General of Health and Chief Executive of Manatū Hauora with currency verified.
- CEO Health New Zealand — Te Whatu Ora and the new Te Whatu Ora Board Chair and members announced in April 2026.
- CE Pharmac, Chair Pharmac Board, Director Medsafe with currency verified.
- Chair Hauora Māori Advisory Committee and key IMPB chairs with currency verified.
- Chair Health Select Committee of Parliament in the current 54th Parliament.
- Presidents of NZMA, NZNO, PSNZ and Chair RNZCGP with currency verified.
