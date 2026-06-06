# spec.md

Single source of truth for the structure, semantics, and update rules. Treat this document as the canonical specification: the YAML must conform to it; if the YAML and this spec disagree, the spec wins and the YAML is fixed.

## 1. Purpose

`leaders.yml` is an engagement register of named individuals in and around United Kingdom (UK) National Health Service (NHS) Wales.

Each entry exists so that a reader (typically inside a UK NHS Wales body) can decide:

1. **Who to engage** for a given digital/transformation/policy topic.
2. **How to engage them** — the angle that lands and the angle that fails.
3. **Where to engage them** — which public channels they actually use.

It is not a phone book, not a CRM, and not a comms list. Entries that do not directly serve engagement decision-making are out of scope.

## 2. Scope

**In scope:**

- NHS Wales statutory bodies: the seven UHBs and three Trusts.
- National NHS Wales bodies: DHCW, HEIW, NHS Wales Performance and Improvement (NWPI), NWSSP.
- Welsh Government health-and-social-care tier: ministers, senior civil servants, chief professional officers.
- Senedd Cymru roles material to NHS Wales scrutiny.
- Statutory commissioners and audit bodies (Audit Wales, PSOW, Future Generations Commissioner, Older People's Commissioner).
- Related Welsh sector bodies in mental health, community health, dental health, nutritional health, primary-care professional bodies, and digital delivery (CDPS).
- For each organisation: only stakeholders senior enough that engagement with them shapes decisions across the organisation (typically CEO, Chair, Directors, programme SROs, professional-college Chairs).

**Out of scope:**

- Operational staff below director / programme-SRO level.
- Suppliers, vendors, consultancies (their leaders may appear only when they hold a named role in a Welsh body, e.g. a NED).
- Historical post-holders (unless explicitly flagged as predecessor for context).
- English / Scottish / NI counterparts (unless they also hold a Wales-facing role).

## 3. Structure

The YAML is a single top-level mapping with one key.

```
NHS Wales stakeholders:
  - {Organisation}:
      - {Person}:
          - Title: ...
          - {optional contact fields}
          - Stakeholder engagement notes:
              - "..."
              - "..."
          - Tone advice:
              - "..."
              - "..."
```

### Indentation rules (strict)

- 2 spaces for the organisation-list dash.
- 6 spaces for the person-list dash (4 spaces deeper than the org dash).
- 10 spaces for the field-list dash inside a person (4 spaces deeper than the person dash).
- 14 spaces for sub-bullets inside `Stakeholder engagement notes` and `Tone advice`.
- No tabs anywhere.
- One newline between sibling entries; no blank lines inside a person block.

### Ordering

- Organisations are grouped by tier: UHBs first (alphabetical), then Trusts (WAST, Velindre, PHW), then national bodies (DHCW, HEIW, NWPI), then Welsh Government, then NWSSP/CDPS, then Senedd, then commissioners, then related-sector bodies (mental → community → dental → nutritional).
- Within an organisation, people are ordered: CEO → Chair → Medical Director → Nursing Director → Other Directors → Director of Digital/CDIO → Director of Finance → NEDs/independent members.
- Programme leads and SROs follow their accountable director.

## 4. Field definitions

### 4.1 Organisation name

The key under which a person sits. Use the official name as the organisation publishes it. Acronyms in parentheses where helpful (e.g. `Digital Health and Care Wales (DHCW)`).

### 4.2 Person name

Include honorifics that the person actually uses publicly: `Dr`, `Professor`, post-nominals (`OBE`, `CBE`, `MBE`, `MS`, `FCPara`, `RN`, `FCIPD`, `MBE FRSPH`). Do not invent honorifics. Match what appears on the organisation's official board page.

### 4.3 `Title:` (required, one)

Current job title, verified to within the last six months. Include effective dates or status flags inline where helpful:

- `Interim` or `Acting` if not substantive.
- `(from {date})` if newly in post.
- `(verify currency)` if there is a known reason to re-check.

### 4.4 Contact fields (optional, zero or more, in this order)

Each appears at most once per person.

- `LinkedIn:` — full canonical URL. Skip if not verifiable.
- `X:` — full URL (`https://x.com/{handle}`). Skip if not verifiable, even if a handle was found.
- `Bluesky:` — full URL (`https://bsky.app/profile/{handle}`).
- `Website:` — full URL of personal/professional site (not the org page).
- `GitHub:` — full URL.
- `Email:` — only for people whose professional email address is published or who have explicitly authorised its inclusion.

**Verification rule:** a contact field is only added if a public source attributable to the named person confirms it. Bare URLs without bio/role match are excluded. Better to omit than to guess.

### 4.5 `Stakeholder engagement notes:` (required, list of strings)

Three to seven short bullets. Each bullet is a YAML scalar wrapped in double quotes, ending in a full stop. Each bullet should answer at least one of:

- **What is their career background?** — specialisms, prior roles, qualifications, distinctive experience.
- **What do they own?** — programmes, contracts, statutory functions, public commitments.
- **What have they said publicly?** — direct quotes or paraphrased positions with date context.
- **What is the hook?** — the angle a supplier or strategist would lead with.

Anti-pattern: generic CV bullets ("experienced leader with strong track record"). If the bullet would apply to any senior NHS leader, it should not be in the register.

### 4.6 `Tone advice:` (required, exactly two strings)

Two bullets, each a YAML scalar wrapped in double quotes, ending in a full stop.

- **Bullet 1 — what to lead with.** The framing, vocabulary, or precedent that will land. May reference specific programmes, reports, or quotes from the engagement notes above.
- **Bullet 2 — what to avoid.** A failure mode specific to this person — not generic. Should be derivable from their engagement notes (career, public statements, current pressures).

Tone advice is a derived field: it must be consistent with the engagement notes for the same person. If you change the notes materially, re-check the tone advice.

### 4.7 Other fields

Currently none. Do not add new field types without updating this spec first.

## 5. Provenance and dating

- All facts are anchored to a year (preferably a month or exact date) where helpful. "Took up post {month year}" beats "newly in post".
- Convert relative dates to absolute when writing the YAML ("last year" → `2025`).
- When a fact changes (e.g. a CEO leaves), update the affected fields in the same commit; do not leave stale notes alongside a new title.

## 6. Update workflow

1. **Identify the change** — a new appointment, departure, contract, statement.
2. **Verify against a public source** — official org page, gov.wales announcement, named press article, named board paper, Senedd record.
3. **Apply minimum diff** — change only the fields the new fact touches. Re-check `Tone advice` if engagement notes changed.
4. **Confirm structure** — indentation, ordering, no `?` placeholders left behind.
5. **Re-validate cross-references** — if person A moved orgs, update both old-org and new-org blocks.

## 7. Invariants

These must always hold:

- Every person has exactly one `Title:` and exactly one `Stakeholder engagement notes:` block and exactly one `Tone advice:` block.
- `Tone advice:` has exactly two bullets.
- No `"?"` placeholders remain in any published version.
- Every quoted string is on one line (no folded scalars).
- Every URL is HTTPS.
- Every person sits under exactly one organisation (cross-referencing is done in prose inside notes, not by duplicating entries).
- No two organisations share a name; no two people inside an organisation share a name.

## 8. Anti-patterns

- **Padding.** Long blocks of vanilla CV facts. A short, sharp entry is more useful than a long one.
- **Speculation.** "Likely to be receptive to AI." If you cannot point to a public source for the disposition, omit it.
- **Vendor-flattering language.** Tone advice exists to make engagement realistic, not optimistic.
- **Stale role titles.** A person's role in this register must be their current substantive (or named interim) role, not their most famous previous one.
- **Duplicate entries.** A person belongs to one organisation. If they hold roles in two, choose the one most relevant for engagement and note the second in prose.
- **Mixing facts and aspirations.** Hooks describe what would land _given the person's stated priorities_, not what the writer wishes the person cared about.

## 9. Acronym glossary (selective)

Acronyms used inside the YAML that readers may not know:

- **ABUHB** — Aneurin Bevan University Health Board.
- **BCUHB** — Betsi Cadwaladr University Health Board.
- **CAV** — Cardiff and Vale University Health Board.
- **CTM / CTMUHB** — Cwm Taf Morgannwg University Health Board.
- **CDPS** — Centre for Digital Public Services (Welsh Government delivery arm).
- **CDIO / CIO** — Chief Digital and Information Officer / Chief Information Officer.
- **CCIO** — Chief Clinical Information Officer.
- **CNIO** — Chief Nursing Information Officer.
- **CPhIO** — Chief Pharmacy Information Officer.
- **CAHPIO** — Chief Allied Health Professions Information Officer.
- **CMO / CNO / CPhO / CAHPA** — Chief Medical / Nursing / Pharmaceutical Officer; Chief Allied Health Professions Adviser (Wales).
- **DHCW** — Digital Health and Care Wales.
- **DMTP** — Digital Medicines Transformation Portfolio.
- **DSPP** — Digital Services for Patients and the Public (DHCW programme).
- **EASC** — Emergency Ambulance Services Committee.
- **EPMA** — Electronic Prescribing and Medicines Administration.
- **EPS** — Electronic Prescription Service.
- **HEIW** — Health Education and Improvement Wales.
- **HIW** — Healthcare Inspectorate Wales.
- **HSSG** — Health and Social Services Group (Welsh Government).
- **IMTP** — Integrated Medium Term Plan.
- **MAG** — Ministerial Advisory Group on Performance and Productivity.
- **NDR** — National Data Resource.
- **NWE / NWPI** — NHS Wales Executive / NHS Wales Performance and Improvement (renamed 1 June 2025).
- **NWSSP** — NHS Wales Shared Services Partnership.
- **OAC** — Obesity Alliance Cymru.
- **PHW** — Public Health Wales NHS Trust.
- **PSOW** — Public Services Ombudsman for Wales.
- **RCM / RCN / RCGP / RCPsych** — Royal Colleges of Midwives / Nursing / GPs / Psychiatrists.
- **RPS** — Royal Pharmaceutical Society.
- **RTT** — Referral to Treatment (waiting time standard).
- **SCP** — Single Cancer Pathway.
- **SCS** — Senior Civil Service.
- **SIRO** — Senior Information Risk Owner.
- **SRO** — Senior Responsible Owner.
- **TCS** — Transforming Cancer Services (Velindre programme).
- **TEC Cymru** — Technology Enabled Care Wales.
- **UHB** — University Health Board.
- **VBHC** — Value-Based Healthcare.
- **WAST** — Welsh Ambulance Services NHS Trust.
- **WCCIS** — Welsh Community Care Information System.
- **WGDPC** — Welsh General Dental Practice Committee.
- **WGOS** — Welsh General Ophthalmic Services.
- **WNCR** — Welsh Nursing Care Record.
- **WOHIU** — Welsh Oral Health Information Unit.

## 10. Worked example

This is the canonical shape of one person. Any new entry should match it field-for-field (omitting optional contact fields where not verifiable).

```yaml
- Helen Thomas:
    - Title: Chief Executive Officer
    - LinkedIn: https://uk.linkedin.com/in/helen-thomas-058b72113
    - X: https://x.com/helenthomas100
    - Stakeholder engagement notes:
        - "CEO since DHCW launched as a Special Health Authority April 2021; 30+ years in NHS, started in finance, moved into health informatics in 2000. MSc Health Informatics, Swansea."
        - "Named Digital NHS CEO of the Year 2021; finalist Digital Leaders 100 'Digital Leader of the Year' 2024."
        - "Questioned at Senedd Health and Social Care Committee on 14 May 2025 over digital eye-care delays; DHCW placed at escalation level 3 in March 2025 — she is under intense political scrutiny on delivery."
    - Tone advice:
        - "Interoperability and standards lands — 'stop compromising on integration, move to a streamlined, standard approach' is her line. Lead with de-risking and delivery credibility."
        - "DHCW at escalation level 3 since March 2025 — political scrutiny on delivery means vision pitches land worse than recovery / de-risking ones."
```

## 11. Out-of-band notes

Some organisation blocks in the YAML contain a non-person entry such as:

```yaml
- Notes on Senedd Health and Social Care Committee:
    - Status: ...
    - Implication: ...
```

These are permitted only where they explain why a role is _not_ listed (e.g. unfilled at the time of writing) and should be removed once a named person can be added. They do not need `Tone advice`.

## 12. Open questions

These are known gaps to track and resolve:

- The Director of Finance interim/substantive status at Swansea Bay UHB (Darren Griffiths vs Claire Osmundsen-Little).
- The current PHW Chair after Jan Williams OBE moved to chair Swansea Bay UHB (June 2024).
- The DHCW Chair after Simon Jones's term ended 30 September 2025 (Ruth Glazzard deputised).
- The successor to Dr Rowena Christmas MBE as RCGP Cymru Wales Chair (announced March 2026; named successor to verify).
- The Seventh Senedd Health and Social Care Committee Chair (committees not yet formed as of June 2026).
- The substantive HEIW Medical Director after Prof Push Mangat moved to the GMC in July 2025 (Dr Tom Lawson acting).
- Named members of the AI Commission for Health and Social Care in Wales beyond Mike Emery (Chair), Iain Bell, Helen Thomas, Nick Elliott.

Each open question should be closed by editing this spec and the YAML in the same commit when resolved.
