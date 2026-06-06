# spec.md — `leaders.yml` (NHS England)

Single source of truth for the structure, semantics, and update rules of `leaders.yml`. Treat this document as the canonical specification: the YAML must conform to it; if the YAML and this spec disagree, the spec wins and the YAML is fixed.

## 1. Purpose

`leaders.yml` is an engagement register of named individuals in and around NHS England. Each entry exists so that a reader (typically inside NHS England, DHSC, an ICB, or an adjacent system body) can decide:

1. **Who to engage** for a given digital/transformation/policy topic.
2. **How to engage them** — the angle that lands and the angle that fails.
3. **Where to engage them** — which public channels they actually use.

It is not a phone book, not a CRM, and not a comms list. Entries that do not directly serve engagement decision-making are out of scope.

## 2. Scope

**In scope:**
- The Department of Health and Social Care (DHSC): Secretary of State, Ministers of State, Parliamentary Under-Secretaries, Shadow team, Permanent Secretary, Director General tier.
- NHS England (in transition into DHSC): Chair, CEO, COO, National Directors, CMO, CNO, regional directors.
- Arm's-length bodies: CQC, NICE, MHRA, UKHSA, NHS Resolution, Healthwatch England, HSSIB, NAO, PHSO, PSA.
- Professional regulators: GMC, NMC, GPhC, GDC.
- Integrated Care Boards (ICBs): Chairs and Chief Executives of the larger/strategically-significant systems (e.g. North East London, Greater Manchester, West Yorkshire, Birmingham/Black Country, Cheshire and Merseyside, NENC, Kent and Medway, Surrey and Sussex, Hampshire and IoW, Devon, Bristol/NS/SG).
- UK Parliament roles material to NHS scrutiny: House of Commons Health and Social Care Committee, Public Accounts Committee, relevant Lords spokespeople.
- Royal Colleges and professional bodies: RCGP, RCN, RCP, RCS England, RCPsych, RCM, RCPCH, BMA, BCS Faculty of Health and Care.
- Industry and patient-voice bodies: ABHI, ABPI, NHS Employers, Community Pharmacy England, National Voices.
- Think-tanks and external influencers shaping the DHSC agenda: The King's Fund, Nuffield Trust, Health Foundation, Tony Blair Institute, Lord Darzi / IGHI Imperial.
- For each organisation: only stakeholders senior enough that engagement with them shapes decisions across the organisation (typically CEO, Chair, National/Executive Directors, programme SROs, professional-college Presidents).

**Out of scope:**
- Operational staff below director / programme-SRO level.
- Suppliers, vendors, consultancies (their leaders may appear only when they hold a named role in an English NHS body, e.g. a NED or government adviser).
- Historical post-holders (unless explicitly flagged as predecessor for context).
- Welsh / Scottish / NI counterparts (unless they also hold an England-facing role).
- NHS Trusts and Foundation Trusts at provider level (engagement is via the ICB, NHS England region, or relevant Royal College).

## 3. Structure

The YAML is a single top-level mapping with one key.

```
NHS England stakeholders:
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

- Organisations are grouped by tier: DHSC first (ministerial team in seniority order, then Shadow team, then Permanent Secretary and DG tier), then external influencers on the DHSC agenda (Lord Darzi / IGHI, Tony Blair Institute), then arm's-length bodies (CQC, NICE, MHRA, UKHSA, NHS Resolution, Healthwatch England, NHS Confederation, NAO, HSSIB, PHSO, PSA), then professional regulators (GMC, NMC, GPhC, GDC), then think-tanks (Health Foundation, King's Fund, Nuffield Trust), then NHS England (national directors, then regional directors), then ICBs (by population / strategic weight), then Royal Colleges, then BMA and BCS, then industry bodies (ABHI, ABPI), then NHS Employers, Community Pharmacy England, National Voices.
- Within an organisation, people are ordered: Secretary of State / CEO → Chair → Permanent Secretary / Chief Operating Officer → National / Executive Directors → CMO → CNO → Director of Digital / CDIO → Director of Finance → NEDs / independent members.
- Programme leads and SROs follow their accountable director.

## 4. Field definitions

### 4.1 Organisation name

The key under which a person sits. Use the official name as the organisation publishes it. Acronyms in parentheses where helpful (e.g. `Department of Health and Social Care (DHSC)`, `National Institute for Health and Care Excellence (NICE)`).

### 4.2 Person name

Include honorifics that the person actually uses publicly: `Dr`, `Professor`, `Sir`, `Dame`, `The Rt Hon`, `MP`, `Baroness`, `Lord`, post-nominals (`OBE`, `CBE`, `MBE`, `KCB`, `DBE`, `FRCP`, `FRCS`, `FRCGP`, `FRCN`, `FFCI`). Do not invent honorifics. Match what appears on the organisation's official board page or gov.uk biography.

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
- `NHS / gov.uk email:` — only for people whose `@nhs.net`, `@dhsc.gov.uk`, or equivalent address is published or who have explicitly authorised its inclusion.

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
- When a fact changes (e.g. a Permanent Secretary leaves, a Minister is reshuffled), update the affected fields in the same commit; do not leave stale notes alongside a new title.

## 6. Update workflow

1. **Identify the change** — a new appointment, departure, reshuffle, contract, statement.
2. **Verify against a public source** — official org page, gov.uk announcement, named press article, named board paper, Hansard, select-committee transcript.
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

- **ABHI** — Association of British HealthTech Industries.
- **ABPI** — Association of the British Pharmaceutical Industry.
- **ALB** — Arm's-length body (of DHSC).
- **BCS** — British Computer Society (host of the BCS Faculty of Health and Care).
- **BMA** — British Medical Association.
- **CCIO** — Chief Clinical Information Officer.
- **CDIO / CIO** — Chief Digital and Information Officer / Chief Information Officer.
- **CMO / CNO** — Chief Medical Officer / Chief Nursing Officer (for England).
- **CNIO** — Chief Nursing Information Officer.
- **CPE** — Community Pharmacy England.
- **CQC** — Care Quality Commission.
- **DG** — Director General (DHSC senior civil service tier).
- **DHSC** — Department of Health and Social Care.
- **DSIT** — Department for Science, Innovation and Technology.
- **EPR** — Electronic Patient Record.
- **GDC** — General Dental Council.
- **GMC** — General Medical Council.
- **GPhC** — General Pharmaceutical Council.
- **HSSIB** — Health Services Safety Investigations Body.
- **ICB** — Integrated Care Board.
- **ICS** — Integrated Care System.
- **IGHI** — Institute of Global Health Innovation (Imperial College London; Lord Darzi).
- **MHRA** — Medicines and Healthcare products Regulatory Agency.
- **NAO** — National Audit Office.
- **NED** — Non-Executive Director.
- **NENC** — North East and North Cumbria (ICB).
- **NHS App** — DHSC / NHS England consumer-facing app (contract due for re-procurement June 2026).
- **NHS Confed** — NHS Confederation (merging with NHS Providers as "The NHS Alliance", April 2026).
- **NICE** — National Institute for Health and Care Excellence.
- **NMC** — Nursing and Midwifery Council.
- **PAC** — House of Commons Public Accounts Committee.
- **PHSO** — Parliamentary and Health Service Ombudsman.
- **PSA** — Professional Standards Authority for Health and Social Care.
- **RCGP** — Royal College of General Practitioners.
- **RCM** — Royal College of Midwives.
- **RCN** — Royal College of Nursing.
- **RCP** — Royal College of Physicians.
- **RCPCH** — Royal College of Paediatrics and Child Health.
- **RCPsych** — Royal College of Psychiatrists.
- **RCS England** — Royal College of Surgeons of England.
- **SCS** — Senior Civil Service.
- **SIRO** — Senior Information Risk Owner.
- **SRO** — Senior Responsible Owner.
- **TBI** — Tony Blair Institute for Global Change.
- **UKHSA** — UK Health Security Agency.
- **10-Year Health Plan** — DHSC strategy setting NHS direction over the decade from publication.

## 10. Worked example

This is the canonical shape of one person. Any new entry should match it field-for-field (omitting optional contact fields where not verifiable).

```yaml
      - Samantha Jones:
          - Title: Permanent Secretary, Department of Health and Social Care (from April 2025)
          - LinkedIn: https://www.linkedin.com/in/samantha-jones-cbe-ba5b4413
          - Stakeholder engagement notes:
              - "Confirmed Permanent Secretary April 2025 after Sir Chris Wormald moved to Cabinet Secretary December 2024; rare Perm Sec with hands-on NHS operational delivery experience — former hospital CEO and led NHS England's New Models of Care (Vanguard) programme."
              - "CEO of Operose Health 2019-2021 (Centene-owned primary-care provider) — controversial in the GP world; acknowledge but do not dwell on the private-equity association."
              - "Expert adviser on NHS Transformation and Social Care to PM Boris Johnson from 2021; interim Permanent Secretary and COO of 10 Downing Street — fluent in centre-of-government operating rhythm."
              - "Owns implementation of the 10-Year Health Plan and the NHS England merger into DHSC; will judge propositions on delivery credibility and measurable productivity gain."
          - Tone advice:
              - "Lead with delivery track record and operational evidence — she has done the job at hospital, system, and centre-of-government level and will probe for the same in others."
              - "Avoid framing pitches as transformation theory or vision-led change — she has lived through enough national programmes to discount anything without a credible delivery spine."
```

## 11. Out-of-band notes

Some organisation blocks in the YAML contain a non-person entry such as:

```yaml
      - Notes on House of Commons Health and Social Care Committee:
          - Status: ...
          - Implication: ...
```

These are permitted only where they explain why a role is *not* listed (e.g. unfilled at the time of writing, or in flux due to the NHS England merger into DHSC) and should be removed once a named person can be added. They do not need `Tone advice`.

## 12. Open questions

These are known gaps to track and resolve:

- The substantive NHS England CEO line through the DHSC merger transition (currently led by Sir Jim Mackey on transition mandate).
- The full set of ICB Chair and CEO appointments after the April 2026 cluster mergers reducing the ICB count.
- Confirmed Chair and CEO of "The NHS Alliance" (post-merger NHS Confederation / NHS Providers) once vesting day passes April 2026.
- The named DHSC owner of the NHS App re-contracting decision once the current contract expires June 2026.
- The full named membership of the AI for Health Innovation board / Lord Darzi follow-on commission beyond the publicly named chair.
- The successor as DG / SCS lead for digital, data and technology inside DHSC following NHS England absorption.
- The Seventh Parliament Health and Social Care Committee membership stabilisation once chair and member elections complete.

Each open question should be closed by editing this spec and the YAML in the same commit when resolved.
