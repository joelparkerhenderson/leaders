# spec.md — `leaders.yml`

Single source of truth for the structure, semantics, and update rules of `leaders.yml` for NHS Scotland. Treat this document as the canonical specification: the YAML must conform to it; if the YAML and this spec disagree, the spec wins and the YAML is fixed.

## 1. Purpose

`leaders.yml` is an engagement register of named individuals in and around NHS Scotland. Each entry exists so that a reader (typically inside the Scottish Government Health and Social Care Directorates, a territorial NHS Board, or an adjacent national body) can decide:

1. **Who to engage** for a given digital/transformation/policy topic.
2. **How to engage them** — the angle that lands and the angle that fails.
3. **Where to engage them** — which public channels they actually use.

It is not a phone book, not a CRM, and not a comms list. Entries that do not directly serve engagement decision-making are out of scope.

## 2. Scope

**In scope:**
- NHS Scotland statutory bodies: the fourteen territorial NHS Boards and the special NHS Boards (NES, NSS, PHS, HIS, NHS 24, SAS, State Hospitals Board, NHS Golden Jubilee).
- Scottish Government Health and Social Care Directorates: the DG Health and Social Care / Chief Executive of NHS Scotland, directorate Directors, and the Chief Professional Officers (CMO, CNO, CPhO, CSO, CDO, CAHPO).
- Scottish Cabinet and Ministerial tier covering health and social care, drugs and alcohol, mental wellbeing, social care, and public health.
- Scottish Parliament (Holyrood) roles material to NHS Scotland scrutiny — the Health, Social Care and Sport Committee, opposition spokespeople, and the Presiding Officer where directly relevant.
- Statutory commissioners and audit bodies: Audit Scotland, SPSO, Mental Welfare Commission for Scotland, Care Inspectorate, Scottish Social Services Council.
- Related Scottish sector bodies in mental health, community health, dental health, nutritional health, primary-care professional bodies, and digital delivery (Digital Health and Care Innovation Centre, TEC Scotland).
- For each organisation: only stakeholders senior enough that engagement with them shapes decisions across the organisation (typically CEO, Chair, Directors, programme SROs, professional-college Chairs).

**Out of scope:**
- Operational staff below director / programme-SRO level.
- Suppliers, vendors, consultancies (their leaders may appear only when they hold a named role in a Scottish body, e.g. a Non-Executive Board Member).
- Historical post-holders (unless explicitly flagged as predecessor for context).
- English / Welsh / NI counterparts (unless they also hold a Scotland-facing role).

## 3. Structure

The YAML is a single top-level mapping with one key.

```
NHS Scotland stakeholders:
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

- Organisations are grouped by tier: Scottish Cabinet → Scottish Parliament → Scottish Government Health and Social Care Directorates → special NHS Boards (NSS, PHS, HIS, NES, NHS 24, SAS, State Hospitals Board, NHS Golden Jubilee, DHI) → cross-cutting national roles (CIO, CCIO) → audit and commissioners (Audit Scotland, Mental Welfare Commission, Care Inspectorate, SPSO, SSSC) → Royal Colleges and professional bodies → think tanks and policy bodies → third-sector charities → territorial NHS Boards (NHSGGC, Lothian, Lanarkshire, Grampian, Tayside, Fife, Ayrshire and Arran, Forth Valley, Highland, Borders, Dumfries and Galloway, Orkney, Shetland, Western Isles).
- Within an organisation, people are ordered: CEO → Chair → Medical Director → Nursing Director → Other Directors → Director of Digital/CIO → Director of Finance → Non-Executive Board Members.
- Programme leads and SROs follow their accountable director.

## 4. Field definitions

### 4.1 Organisation name

The key under which a person sits. Use the official name as the organisation publishes it. Acronyms in parentheses where helpful (e.g. `NHS Greater Glasgow and Clyde (NHSGGC)`, `NHS National Services Scotland (NSS)`).

### 4.2 Person name

Include honorifics that the person actually uses publicly: `Dr`, `Professor`, `Sir`, `Dame`, post-nominals (`OBE`, `CBE`, `MBE`, `MSP`, `QPM`, `FRCP`, `FRCN`, `FFPH`). Do not invent honorifics. Match what appears on the organisation's official board page or the Scottish Government website.

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
- `NHS Scotland email:` — only for people whose `@nhs.scot` or board-specific NHS address is published or who have explicitly authorised its inclusion.

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
- When a fact changes (e.g. a Board CEO leaves), update the affected fields in the same commit; do not leave stale notes alongside a new title.

## 6. Update workflow

1. **Identify the change** — a new appointment, departure, contract, statement.
2. **Verify against a public source** — official board page, gov.scot announcement, named press article, named board paper, Scottish Parliament Official Report.
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
- **Mixing facts and aspirations.** Hooks describe what would land *given the person's stated priorities*, not what the writer wishes the person cared about.

## 9. Acronym glossary (selective)

Acronyms used inside the YAML that readers may not know:

- **CIO / CDIO** — Chief Information Officer / Chief Digital and Information Officer.
- **CCIO** — Chief Clinical Information Officer.
- **CNIO** — Chief Nursing Information Officer.
- **CMO / CNO / CPhO / CDO / CSO / CAHPO** — Chief Medical / Nursing / Pharmaceutical / Dental / Scientific / Allied Health Professions Officer (Scotland).
- **DG HSC** — Director-General Health and Social Care (Scottish Government); doubles as Chief Executive of NHS Scotland.
- **DHI** — Digital Health and Care Innovation Centre.
- **HIS** — Healthcare Improvement Scotland.
- **HSCP** — Health and Social Care Partnership (the integrated joint-board delivery vehicle in each council area).
- **IJB** — Integration Joint Board.
- **MAT Standards** — Medication-Assisted Treatment Standards (drugs policy).
- **MWC** — Mental Welfare Commission for Scotland.
- **NCA** — National Care Service (the proposed reform; status varies).
- **NDP** — National Digital Platform.
- **NES** — NHS Education for Scotland.
- **NHSGGC** — NHS Greater Glasgow and Clyde.
- **NHSL** — NHS Lothian (also used for Lanarkshire — disambiguate in prose).
- **NSS** — NHS National Services Scotland.
- **PHS** — Public Health Scotland.
- **RCPE / RCPSG / RCSEd** — Royal College of Physicians of Edinburgh / Royal College of Physicians and Surgeons of Glasgow / Royal College of Surgeons of Edinburgh.
- **RCN / RCGP / RCM / RCPsych** — Royal Colleges of Nursing / GPs / Midwives / Psychiatrists (Scotland branches).
- **SAS** — Scottish Ambulance Service.
- **SCS** — Senior Civil Service.
- **SIGN** — Scottish Intercollegiate Guidelines Network (hosted within HIS).
- **SIRO** — Senior Information Risk Owner.
- **SPSO** — Scottish Public Services Ombudsman.
- **SRO** — Senior Responsible Owner.
- **SSSC** — Scottish Social Services Council.
- **TEC Scotland** — Technology Enabled Care Scotland.
- **TTG** — Treatment Time Guarantee (12-week inpatient/day-case waiting time standard).

## 10. Worked example

This is the canonical shape of one person. Any new entry should match it field-for-field (omitting optional contact fields where not verifiable).

```yaml
      - Caroline Lamb:
          - Title: Director-General Health and Social Care and Chief Executive of NHS Scotland (retiring end of August 2026)
          - LinkedIn: https://uk.linkedin.com/in/caroline-lamb-3a420744
          - Stakeholder engagement notes:
              - "DG Health and Social Care and Chief Executive of NHS Scotland since January 2021; announced retirement at end of August 2026 — recruitment for successor under way."
              - "Chartered Accountant by training; Chief Executive of NHS Education for Scotland 2015-2019; led the Scottish Government Digital Health and Care Directorate from December 2019 — fluent in National Digital Platform and EPR-strategy framing."
              - "Owned NHS Scotland's pandemic response, the operating framework, and the 2023-24 NHS Recovery Plan; faced sustained political criticism in 2024-2026 over board escalations and reports of limited frontline visits."
          - Tone advice:
              - "Lead with finance-credible, digital-coherent propositions tied to NHS Scotland Recovery and the National Digital Platform — her CA and digital-directorate pedigree means she values rigour."
              - "Do not pitch wholesale strategy in her final months — the credible ask is delivery continuity and successor onboarding, not new strategic bets."
```

## 11. Out-of-band notes

Some organisation blocks in the YAML contain a non-person entry such as:

```yaml
      - Notes on the Holyrood Health, Social Care and Sport Committee:
          - Status: ...
          - Implication: ...
```

These are permitted only where they explain why a role is *not* listed (e.g. unfilled at the time of writing, or committees not yet constituted after a Holyrood election) and should be removed once a named person can be added. They do not need `Tone advice`.

## 12. Open questions

These are known gaps to track and resolve:

- The successor to Caroline Lamb as DG Health and Social Care / Chief Executive of NHS Scotland (Lamb retiring end of August 2026).
- The substantive National Clinical Director after Professor Sir Jason Leitch's departure (the post-Leitch gap referenced in the Cabinet Secretary's brief).
- The membership and Convener of the Session 7 Holyrood Health, Social Care and Sport Committee (committees re-formed after the 7 May 2026 Holyrood election).
- The status of the National Care Service legislation following the May 2026 Scottish Government reshuffle.
- The substantive Chair of NHS Highland and any other territorial NHS Board chairships currently filled on an interim basis.
- The current Convener of the BMA Scottish Council and the RCGP Scotland Chair following recent term endings.
- Named Director of Digital for any territorial NHS Board where the post is vacant or held on an interim basis at the time of writing.

Each open question should be closed by editing this spec and the YAML in the same commit when resolved.
