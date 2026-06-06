# spec.md — `leaders.yml`

Single source of truth for the structure, semantics, and update rules of `leaders.yml` for Health and Social Care (HSC) in Northern Ireland. Treat this document as the canonical specification: the YAML must conform to it; if the YAML and this spec disagree, the spec wins and the YAML is fixed.

## 1. Purpose

`leaders.yml` is an engagement register of named individuals in and around HSC in Northern Ireland. Each entry exists so that a reader (typically inside the Department of Health, an HSC Trust, the Strategic Planning and Performance Group, or an adjacent regional body) can decide:

1. **Who to engage** for a given digital/transformation/policy topic.
2. **How to engage them** — the angle that lands and the angle that fails.
3. **Where to engage them** — which public channels they actually use.

It is not a phone book, not a CRM, and not a comms list. Entries that do not directly serve engagement decision-making are out of scope.

Northern Ireland is the only part of the United Kingdom in which health and social care are statutorily integrated. The HSC system therefore has no direct NHS analogue: directors of social work, social-care commissioning, and integrated service planning sit inside the same register as acute, primary-care, and digital leadership.

## 2. Scope

**In scope:**
- HSC statutory bodies: the five integrated Health and Social Care Trusts (Belfast, Northern, South Eastern, Southern, Western) and the Northern Ireland Ambulance Service Trust (NIAS).
- HSC regional bodies: Public Health Agency (PHA), Business Services Organisation (BSO), Northern Ireland Blood Transfusion Service (NIBTS), Northern Ireland Medical and Dental Training Agency (NIMDTA), Northern Ireland Practice and Education Council for Nursing and Midwifery (NIPEC), Patient and Client Council (PCC), Regulation and Quality Improvement Authority (RQIA).
- Department of Health (DoH): the Minister of Health, the Permanent Secretary, the Strategic Planning and Performance Group (SPPG) Chief Officer, the Chief Professional Officers (CMO, CNO, CDO, CPhO, CAHPO, CSW, CSO), and the digital leadership (Chief Digital Information Officer).
- Northern Ireland Executive Office where directly material to health (First Minister, deputy First Minister) and the Northern Ireland Civil Service Head where they intervene in HSC governance.
- Northern Ireland Assembly roles material to HSC scrutiny — Committee for Health Chairperson, Deputy Chairperson and members; opposition health spokespeople.
- Statutory commissioners and audit bodies: Northern Ireland Audit Office, Northern Ireland Public Services Ombudsman (NIPSO), Commissioner for Older People for Northern Ireland (COPNI), Children's Commissioner (NICCY), Mental Health Commissioner (where established).
- Related Northern Ireland sector bodies in mental health, community health, dental health, nutritional health, primary-care professional bodies, and digital delivery (encompass programme leadership).
- For each organisation: only stakeholders senior enough that engagement with them shapes decisions across the organisation (typically CEO, Chair, Directors, programme SROs, professional-college Chairs).

**Out of scope:**
- Operational staff below director / programme-SRO level.
- Suppliers, vendors, consultancies (their leaders may appear only when they hold a named role in a Northern Ireland body, e.g. a Non-Executive Director).
- Historical post-holders (unless explicitly flagged as predecessor for context).
- English / Scottish / Welsh counterparts (unless they also hold a Northern Ireland-facing role).

## 3. Structure

The YAML is a single top-level mapping with one key.

```
HSC Northern Ireland stakeholders:
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

- Organisations are grouped by tier: Northern Ireland Executive Office and Assembly (First Minister, deputy First Minister, Committee for Health) → Department of Health (Minister, Permanent Secretary, Chief Professional Officers, Strategic Planning and Performance Group) → regional HSC bodies (PHA, BSO, NIBTS, NIMDTA, NIPEC, PCC, RQIA) → HSC Trusts in alphabetical order (Belfast, Northern, South Eastern, Southern, Western) → NIAS → audit and commissioners (NI Audit Office, NIPSO, COPNI, NICCY) → Royal Colleges and professional bodies (BMA NI, RCN NI, RCGP NI, RCM NI, RPS NI, RCSEd NI, BDA NI) → think tanks and policy bodies → third-sector charities.
- Within an organisation, people are ordered: CEO → Chair → Medical Director → Nursing Director → Director of Social Work → Other Directors → Director of Digital/CDIO → Director of Finance → Non-Executive Directors.
- Programme leads and SROs follow their accountable director.

## 4. Field definitions

### 4.1 Organisation name

The key under which a person sits. Use the official name as the organisation publishes it. Acronyms in parentheses where helpful (e.g. `Belfast Health and Social Care Trust (BHSCT)`, `Strategic Planning and Performance Group (SPPG)`).

### 4.2 Person name

Include honorifics that the person actually uses publicly: `Dr`, `Professor`, `Sir`, `Dame`, post-nominals (`OBE`, `CBE`, `MBE`, `MLA`, `QPM`, `FRCP`, `FRCN`, `FFPH`, `FRCSI`). Do not invent honorifics. Match what appears on the organisation's official board page or the Department of Health website.

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
- `HSC email:` — only for people whose `@hscni.net` or board-specific HSC address is published or who have explicitly authorised its inclusion.

**Verification rule:** a contact field is only added if a public source attributable to the named person confirms it. Bare URLs without bio/role match are excluded. Better to omit than to guess.

### 4.5 `Stakeholder engagement notes:` (required, list of strings)

Three to seven short bullets. Each bullet is a YAML scalar wrapped in double quotes, ending in a full stop. Each bullet should answer at least one of:

- **What is their career background?** — specialisms, prior roles, qualifications, distinctive experience.
- **What do they own?** — programmes, contracts, statutory functions, public commitments.
- **What have they said publicly?** — direct quotes or paraphrased positions with date context.
- **What is the hook?** — the angle a supplier or strategist would lead with.

Anti-pattern: generic CV bullets ("experienced leader with strong track record"). If the bullet would apply to any senior HSC leader, it should not be in the register.

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
- When a fact changes (e.g. a Trust CEO leaves), update the affected fields in the same commit; do not leave stale notes alongside a new title.

## 6. Update workflow

1. **Identify the change** — a new appointment, departure, contract, statement.
2. **Verify against a public source** — official Trust page, Department of Health press release, named press article, Assembly Official Report, Northern Ireland Executive announcement.
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
- **Treating HSC as NHS.** Northern Ireland integrates health and social care statutorily — social work and social-care leadership are first-class, not adjuncts. Do not parachute NHS England framings.

## 9. Acronym glossary (selective)

Acronyms used inside the YAML that readers may not know:

- **BDA NI** — British Dental Association Northern Ireland.
- **BHSCT** — Belfast Health and Social Care Trust.
- **BMA NI** — British Medical Association Northern Ireland.
- **BSO** — Business Services Organisation (HSC shared-services body).
- **CAHPO** — Chief Allied Health Professions Officer (Northern Ireland).
- **CDIO / CIO** — Chief Digital and Information Officer / Chief Information Officer.
- **CCIO** — Chief Clinical Information Officer.
- **CDO** — Chief Dental Officer (Northern Ireland).
- **CMO / CNO / CPhO / CSO / CSW** — Chief Medical / Nursing / Pharmaceutical / Scientific Officer; Chief Social Worker (Northern Ireland).
- **COPNI** — Commissioner for Older People for Northern Ireland.
- **DoH** — Department of Health (Northern Ireland).
- **encompass** — the regional electronic patient record programme being rolled out across all five HSC Trusts.
- **FM / dFM** — First Minister / deputy First Minister.
- **HSC** — Health and Social Care (the integrated NI system; the equivalent of NHS in the other UK jurisdictions).
- **HSCB** — Health and Social Care Board (dissolved 31 March 2022; SPPG took over its commissioning and performance functions inside the DoH).
- **INT** — Integrated Neighbourhood Team (the local model under the Care Closer to Home plan, 17 INTs each serving ~115,000 people).
- **MAHI** — Muckamore Abbey Hospital Inquiry.
- **MLA** — Member of the Legislative Assembly (Northern Ireland Assembly).
- **NHSCT** — Northern Health and Social Care Trust.
- **NIAS** — Northern Ireland Ambulance Service Trust.
- **NIAO** — Northern Ireland Audit Office.
- **NIBTS** — Northern Ireland Blood Transfusion Service.
- **NICCY** — Northern Ireland Commissioner for Children and Young People.
- **NICS** — Northern Ireland Civil Service.
- **NIMDTA** — Northern Ireland Medical and Dental Training Agency.
- **NIPEC** — Northern Ireland Practice and Education Council for Nursing and Midwifery.
- **NIPSO** — Northern Ireland Public Services Ombudsman.
- **PCC** — Patient and Client Council.
- **PHA** — Public Health Agency (Northern Ireland).
- **RCGP NI** — Royal College of General Practitioners Northern Ireland.
- **RCM NI / RCN NI / RCPsych NI** — Royal Colleges of Midwives / Nursing / Psychiatrists (Northern Ireland branches).
- **RCSEd / RCSI** — Royal College of Surgeons of Edinburgh / Royal College of Surgeons in Ireland (both operate across the island).
- **RQIA** — Regulation and Quality Improvement Authority.
- **SEHSCT** — South Eastern Health and Social Care Trust.
- **SHSCT** — Southern Health and Social Care Trust.
- **SIRO** — Senior Information Risk Owner.
- **SPPG** — Strategic Planning and Performance Group (the DoH directorate that absorbed HSCB commissioning and performance functions in April 2022).
- **SRO** — Senior Responsible Owner.
- **WHSCT** — Western Health and Social Care Trust.

## 10. Worked example

This is the canonical shape of one person. Any new entry should match it field-for-field (omitting optional contact fields where not verifiable).

```yaml
      - Mike Nesbitt MLA:
          - Title: Minister of Health (from 28 May 2024)
          - X: https://x.com/mikenesbittni
          - Stakeholder engagement notes:
              - "Ulster Unionist Party MLA for Strangford since 2011; appointed Minister of Health 28 May 2024 in the restored Northern Ireland Executive; previously UUP Leader 2012-2017 and again 30 August 2024 - 31 January 2026."
              - "Pre-politics career as a UTV journalist and newsreader; Victims' Commissioner for Northern Ireland 2008-2010; brings a public-communications and victims-and-survivors lens to the brief."
              - "Has announced he will stand down as an MLA at the next Assembly election — the Care Closer to Home plan and the 2026-27 Budget are the legacy bets; he does not have a long horizon."
              - "Unveiled the 'Care Closer to Home' plan in March 2026 — 17 Integrated Neighbourhood Teams (INTs) each serving ~115,000 people — against an £800m DoH deficit warning for the year."
              - "Hook: digital propositions that demonstrably accelerate INT delivery, reduce acute deficit pressure, or measurably shift activity from hospital to community will land; vision-only pitches will not."
          - Tone advice:
              - "Lead with INT delivery, deficit recovery, and concrete shift-left evidence — Nesbitt is a communicator who needs lines he can take publicly within days, not multi-year transformation theory."
              - "Do not pitch slow-burn transformation or strategic-reform vehicles — he is a minister on a shortening clock with an £800m deficit and a standing-down date; he will mark down anything that lacks an in-mandate delivery window."
```

## 11. Out-of-band notes

Some organisation blocks in the YAML contain a non-person entry such as:

```yaml
      - Notes on Mental Health Commissioner for Northern Ireland:
          - Status: ...
          - Implication: ...
```

These are permitted only where they explain why a role is *not* listed (e.g. unfilled at the time of writing, or the body has not yet been established in statute) and should be removed once a named person can be added. They do not need `Tone advice`.

## 12. Open questions

These are known gaps to track and resolve:

- The substantive Permanent Secretary of the Department of Health after Mike Farrar's fixed-term interim appointment from April 2025 (12 months, with potential for extension; permanent post to be filled through open recruitment).
- The substantive Chief Executive of the Northern Health and Social Care Trust after Suzanne Pullins's interim appointment from 1 October 2025.
- The substantive Chief Executive of the Northern Ireland Ambulance Service after Maxine Paterson's interim appointment from April 2025.
- The substantive Chief Medical Officer succession plan after Professor Sir Michael McBride's continuous tenure since September 2006.
- The composition of the Northern Ireland Executive's Mental Health Champion and Commissioner posts, where status varies between mandates.
- The current Chair of the BMA Northern Ireland Council and the RCGP Northern Ireland Chair following recent term endings.
- Named members of the Phase Three Bengoa-derived transformation governance, where Department of Health structures continue to evolve under the Care Closer to Home plan announced March 2026.
- Named Director of Digital / CDIO for each HSC Trust where the post is vacant, interim, or held alongside another portfolio at the time of writing.

Each open question should be closed by editing this spec and the YAML in the same commit when resolved.
