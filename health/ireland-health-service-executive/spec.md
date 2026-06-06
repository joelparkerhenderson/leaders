# spec.md — `leaders.yml` (Ireland HSE)

Single source of truth for the structure, semantics, and update rules of `leaders.yml`. Treat this document as the canonical specification: the YAML must conform to it; if the YAML and this spec disagree, the spec wins and the YAML is fixed.

## 1. Purpose

`leaders.yml` is an engagement register of named individuals in and around the Health Service Executive (HSE) and the wider Irish health system. Each entry exists so that a reader (typically inside the HSE, the Department of Health, a Regional Health Area, or an adjacent statutory body) can decide:

1. **Who to engage** for a given digital/transformation/policy topic.
2. **How to engage them** — the angle that lands and the angle that fails.
3. **Where to engage them** — which public channels they actually use.

It is not a phone book, not a CRM, and not a comms list. Entries that do not directly serve engagement decision-making are out of scope.

## 2. Scope

**In scope:**
- The Department of Health (DoH): Minister for Health, Ministers of State, opposition spokespeople, Secretary General, Assistant Secretaries.
- The HSE national tier: Chair, CEO, COO, National Directors, Chief Clinical Officer, Chief Operations Officer, Chief Strategy Officer, Chief Information Officer / Chief Technology and Transformation Officer.
- The six Regional Executive Officers (REOs) of the new HSE Regional Health Areas (RHAs): HSE Dublin and South East, HSE Dublin and Midlands, HSE Dublin and North East, HSE Mid West, HSE South West, HSE West and North West.
- HSE Digital / Office of the CIO leadership: CIO, Chief Technology and Transformation Officer, programme SROs for shared care records, e-prescribing, e-referrals, and the HSE App.
- Statutory and regulatory bodies: HIQA, HPRA, Mental Health Commission, Health Research Board, Food Safety Authority of Ireland, Health and Safety Authority.
- Professional regulators: Medical Council, NMBI (Nursing and Midwifery Board of Ireland), PSI (Pharmaceutical Society of Ireland), Dental Council, CORU.
- Oireachtas roles material to HSE scrutiny: Joint Committee on Health, Committee of Public Accounts, Comptroller and Auditor General, Ombudsman, Ombudsman for Children.
- Royal Colleges and professional bodies: RCSI, RCPI, ICGP, College of Psychiatrists of Ireland, Faculty of Public Health Medicine, IMO, IHCA, INMO, IPU.
- Industry and patient-voice bodies: IPHA, Medtech Ireland (Ibec), IPPOSI, IPA (Irish Patients Association).
- Think-tanks and academic influencers shaping the DoH / Sláintecare agenda: ESRI Health Research Programme, Trinity Centre for Health Sciences, RCSI Graduate School of Healthcare Management.
- For each organisation: only stakeholders senior enough that engagement with them shapes decisions across the organisation (typically CEO, Chair, National/Executive Directors, REOs, programme SROs, professional-college Presidents).

**Out of scope:**
- Operational staff below National Director / REO / programme-SRO level.
- Suppliers, vendors, consultancies (their leaders may appear only when they hold a named role in an Irish statutory body, e.g. an NED of the HSE board or a member of a HIQA advisory group).
- Historical post-holders (unless explicitly flagged as predecessor for context).
- Northern Ireland / UK counterparts (unless they also hold an Ireland-facing role, e.g. a cross-border body officer).
- Section 38/39 voluntary hospital and disability-services CEOs at provider level (engagement is via the RHA, HSE National Director, or the relevant Royal College).

## 3. Structure

The YAML is a single top-level mapping with one key.

```
Ireland HSE stakeholders:
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

- Organisations are grouped by tier: Department of Health first (ministerial team in seniority order, then opposition spokespeople, then Secretary General and Assistant Secretary tier), then HSE national tier (Chair, CEO, COO, National Directors, CCO, CIO/CTTO), then the six RHAs (REOs, in geographic order: Dublin and South East, Dublin and Midlands, Dublin and North East, Mid West, South West, West and North West), then statutory and regulatory bodies (HIQA, HPRA, Mental Health Commission, HRB, FSAI, HSA), then professional regulators (Medical Council, NMBI, PSI, Dental Council, CORU), then Oireachtas committees and constitutional officers (C&AG, Ombudsman), then Royal Colleges and professional representative bodies (RCSI, RCPI, ICGP, College of Psychiatrists, IMO, IHCA, INMO, IPU), then industry bodies (IPHA, Medtech Ireland), then patient-voice bodies (IPPOSI, IPA), then think-tanks and academic influencers.
- Within an organisation, people are ordered: Minister / CEO → Chair → Secretary General / Chief Operating Officer → National / Executive Directors → CMO / CCO → CNO → CIO / CTTO → Director of Finance → NEDs / independent board members.
- Programme leads and SROs follow their accountable director.

## 4. Field definitions

### 4.1 Organisation name

The key under which a person sits. Use the official name as the organisation publishes it. Acronyms in parentheses where helpful (e.g. `Department of Health (DoH)`, `Health Information and Quality Authority (HIQA)`, `Health Service Executive (HSE)`).

### 4.2 Person name

Include honorifics that the person actually uses publicly: `Dr`, `Professor`, `Mr`, `Ms`, post-nominals (`TD`, `MEP`, `Senator`, `SC`, `FRCSI`, `FRCPI`, `MRCGP`, `FFPHMI`). Do not invent honorifics. Match what appears on the organisation's official board page, the gov.ie biography, or the Oireachtas member page.

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
- `HSE / gov.ie email:` — only for people whose `@hse.ie`, `@health.gov.ie`, or equivalent address is published or who have explicitly authorised its inclusion.

**Verification rule:** a contact field is only added if a public source attributable to the named person confirms it. Bare URLs without bio/role match are excluded. Better to omit than to guess.

### 4.5 `Stakeholder engagement notes:` (required, list of strings)

Three to seven short bullets. Each bullet is a YAML scalar wrapped in double quotes, ending in a full stop. Each bullet should answer at least one of:

- **What is their career background?** — specialisms, prior roles, qualifications, distinctive experience.
- **What do they own?** — programmes, contracts, statutory functions, public commitments.
- **What have they said publicly?** — direct quotes or paraphrased positions with date context.
- **What is the hook?** — the angle a supplier or strategist would lead with.

Anti-pattern: generic CV bullets ("experienced leader with strong track record"). If the bullet would apply to any senior HSE leader, it should not be in the register.

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
- When a fact changes (e.g. a Secretary General leaves, a Minister is reshuffled, an REO moves region), update the affected fields in the same commit; do not leave stale notes alongside a new title.

## 6. Update workflow

1. **Identify the change** — a new appointment, departure, reshuffle, contract, statement.
2. **Verify against a public source** — official org page, gov.ie announcement, named press article, named board paper, Oireachtas record, C&AG report.
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

- **C&AG** — Comptroller and Auditor General.
- **CCO** — Chief Clinical Officer (HSE).
- **CDIO / CIO** — Chief Digital and Information Officer / Chief Information Officer (HSE).
- **CHN** — Community Healthcare Network.
- **CHO** — Community Healthcare Organisation (legacy structure being absorbed into RHAs).
- **CMO / CNO** — Chief Medical Officer / Chief Nursing Officer (Department of Health).
- **CORU** — Health and Social Care Professionals regulator (Ireland).
- **CTTO** — Chief Technology and Transformation Officer (HSE).
- **DoH** — Department of Health (Republic of Ireland).
- **DPER** — Department of Public Expenditure, NDP Delivery and Reform.
- **EHR** — Electronic Health Record (national programme in scoping).
- **FSAI** — Food Safety Authority of Ireland.
- **GMS** — General Medical Services scheme.
- **GPIT** — General Practice Information Technology group.
- **HBS** — Health Business Services (HSE shared services).
- **HIQA** — Health Information and Quality Authority.
- **HPRA** — Health Products Regulatory Authority.
- **HRB** — Health Research Board.
- **HSA** — Health and Safety Authority.
- **HSE** — Health Service Executive.
- **ICGP** — Irish College of General Practitioners.
- **IHCA** — Irish Hospital Consultants Association.
- **IMO** — Irish Medical Organisation.
- **INMO** — Irish Nurses and Midwives Organisation.
- **IPHA** — Irish Pharmaceutical Healthcare Association.
- **IPPOSI** — Irish Platform for Patient Organisations, Science and Industry.
- **IPU** — Irish Pharmacy Union.
- **MHC** — Mental Health Commission.
- **NAS** — National Ambulance Service.
- **NCCP** — National Cancer Control Programme.
- **NDTP** — National Doctors Training and Planning (HSE).
- **NIMIS** — National Integrated Medical Imaging System.
- **NMBI** — Nursing and Midwifery Board of Ireland.
- **NTPF** — National Treatment Purchase Fund.
- **OoCIO** — Office of the Chief Information Officer (HSE).
- **PHECC** — Pre-Hospital Emergency Care Council.
- **PSI** — Pharmaceutical Society of Ireland.
- **RCPI** — Royal College of Physicians of Ireland.
- **RCSI** — Royal College of Surgeons in Ireland.
- **REO** — Regional Executive Officer (HSE Regional Health Area lead).
- **RHA** — Regional Health Area (the six new HSE regions established 1 March 2024).
- **SRO** — Senior Responsible Owner.
- **Sláintecare** — the cross-party ten-year programme of health reform published 2017.
- **Vote 38 / Vote 39** — DoH and HSE Estimates votes in the annual budget cycle.

## 10. Worked example

This is the canonical shape of one person. Any new entry should match it field-for-field (omitting optional contact fields where not verifiable).

```yaml
      - Anne O'Connor:
          - Title: Chief Executive Officer, Health Service Executive (from 23 March 2026)
          - LinkedIn: https://www.linkedin.com/in/anne-o-connor-8a06718a
          - Stakeholder engagement notes:
              - "CEO of the HSE from 23 March 2026, appointed by the HSE Board after an open competitive process and succeeding Bernard Gloster, who retired in March 2026."
              - "Occupational therapist by background; first joined HSE National Director ranks as National Director for Mental Health in 2014, became first National Director for Community Operations in early 2018, and was HSE Chief Operations Officer from May 2018 through the COVID-19 response."
              - "Left HSE to become Managing Director, Vhi Health & Wellbeing — returns to HSE as CEO with private-sector commissioning and integrated-care experience the previous CEO did not have."
              - "On appointment said she would 'lead the organisation and the reform programme already underway by supporting our staff to deliver quality healthcare services' — explicit continuity with Gloster's RHA implementation and the 2026 National Service Plan (29 billion euro budget)."
              - "Owns delivery of the six Regional Health Areas operating model in its second full year, the national EHR business case, the HSE App, and the productivity commitments in Budget 2026."
          - Tone advice:
              - "Lead with operational delivery, RHA bed-down, and credible community-acute integration — match her COO/Community-Operations background and Vhi integrated-care lens."
              - "Avoid pitching her as a clean-slate reformer or contrasting her with Gloster — she has explicitly framed her tenure as continuity with the reform programme already in flight."
```

## 11. Out-of-band notes

Some organisation blocks in the YAML contain a non-person entry such as:

```yaml
      - Notes on Oireachtas Joint Committee on Health:
          - Status: ...
          - Implication: ...
```

These are permitted only where they explain why a role is *not* listed (e.g. unfilled at the time of writing, or in flux due to a general-election cycle or a committee re-formation) and should be removed once a named person can be added. They do not need `Tone advice`.

## 12. Open questions

These are known gaps to track and resolve:

- The substantive Chair of the HSE Board after the current term cycle.
- The full set of the six RHA Regional Executive Officer appointments and their substantive vs interim status.
- The named SRO for the national Electronic Health Record programme once the business case is approved by DPER.
- The named DoH owner of the HSE App / digital front-door procurement decision.
- The current Chair of the Oireachtas Joint Committee on Health following the most recent committee re-formation.
- The substantive Secretary General of the Department of Health where any interim appointment is in place.
- The successor as President / CEO of each Royal College and representative body where the term is mid-cycle.

Each open question should be closed by editing this spec and the YAML in the same commit when resolved.
