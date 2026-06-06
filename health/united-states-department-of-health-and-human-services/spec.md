# spec.md — `leaders.yml`

Single source of truth for the structure, semantics, and update rules of `leaders.yml` for the United States Department of Health and Human Services (HHS) and the surrounding federal health leadership tier. Treat this document as the canonical specification: the YAML must conform to it; if the YAML and this spec disagree, the spec wins and the YAML is fixed.

## 1. Purpose

`leaders.yml` is an engagement register of named individuals in and around US federal health leadership. Each entry exists so that a reader (typically inside HHS, a federal advisory committee, a state health department, an academic medical centre, or an adjacent national body) can decide:

1. **Who to engage** for a given digital/transformation/policy topic.
2. **How to engage them** — the angle that lands and the angle that fails.
3. **Where to engage them** — which public channels they actually use.

It is not a phone book, not a CRM, and not a comms list. Entries that do not directly serve engagement decision-making are out of scope.

The US federal health system has no single national NHS-equivalent. Instead, federal health leadership is distributed across HHS and its operating divisions (CMS, FDA, CDC, NIH, HRSA, IHS, SAMHSA, ACF, ACL, ASPR, ASTP/ONC), the Department of Veterans Affairs (which runs the largest integrated US health system through the Veterans Health Administration), the Department of Defense (Defense Health Agency), and the surgeons general of the uniformed services. Congressional health-committee leadership is also in scope because of the authorising and appropriations role. State-level health leadership is out of scope for this register; a parallel state-level register may be added later.

## 2. Scope

**In scope:**
- HHS Office of the Secretary: Secretary, Deputy Secretary, Chief of Staff, General Counsel, Assistant Secretary for Health, Surgeon General, ASPR, ASTP/ONC (National Coordinator for Health IT), Assistant Secretary for Planning and Evaluation (ASPE), Assistant Secretary for Public Affairs.
- HHS operating divisions: Centers for Medicare & Medicaid Services (CMS), Food and Drug Administration (FDA), Centers for Disease Control and Prevention (CDC), National Institutes of Health (NIH), Health Resources and Services Administration (HRSA), Indian Health Service (IHS), Substance Abuse and Mental Health Services Administration (SAMHSA), Agency for Healthcare Research and Quality (AHRQ), Administration for Children and Families (ACF), Administration for Community Living (ACL).
- Department of Veterans Affairs health leadership: Secretary, Deputy Secretary, Under Secretary for Health (VHA), Deputy Under Secretary for Health, Chief Medical Officer, EHRM-IO (Electronic Health Record Modernization Integration Office) leadership.
- Department of Defense Health Affairs: Assistant Secretary of Defense for Health Affairs, Defense Health Agency (DHA) Director.
- Surgeons General of the uniformed services: US Public Health Service Surgeon General; Army, Navy, Air Force Surgeons General where they hold public posture on military-veteran health.
- White House: Domestic Policy Council Health Lead; National Security Council Global Health Director where post is filled.
- US Congress: Senate Health, Education, Labor and Pensions (HELP) Committee Chair and Ranking Member; Senate Finance Committee Chair and Ranking Member (Medicare/Medicaid); House Energy and Commerce Health Subcommittee Chair and Ranking Member; House Ways and Means Health Subcommittee Chair and Ranking Member; Senate and House Veterans Affairs Committee Chairs.
- Federal advisory committees of national significance: US Preventive Services Task Force (USPSTF), Advisory Committee on Immunization Practices (ACIP), Medicare Payment Advisory Commission (MedPAC), Medicaid and CHIP Payment and Access Commission (MACPAC) — when leadership is publicly named and material.
- For each organisation: only stakeholders senior enough that engagement with them shapes decisions across the organisation (typically Secretary-equivalent, Administrator/Director of an operating division, Commissioner, Deputy, named programme SROs).

**Out of scope:**
- Operational staff below Deputy Administrator / Bureau Director level inside operating divisions.
- State health commissioners and state Medicaid directors (covered by a future state-level register).
- Suppliers, vendors, consultancies (their leaders may appear only when they hold a named federal advisory or commissioner role).
- Historical post-holders (unless explicitly flagged as predecessor for context).
- UK / Irish / other foreign counterparts (unless they also hold a US-facing federal role).

## 3. Structure

The YAML is a single top-level mapping with one key.

```
US federal health stakeholders:
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

- Organisations are grouped by tier: White House → Cabinet (HHS Office of the Secretary, Department of Veterans Affairs, Department of Defense Health Affairs) → HHS operating divisions in order of budget weight (CMS, FDA, CDC, NIH, HRSA, IHS, SAMHSA, AHRQ, ACF, ACL, ASTP/ONC, ASPR) → Veterans Health Administration → Defense Health Agency → US Public Health Service uniformed services → Congress (Senate HELP, Senate Finance, Senate Veterans Affairs, House Energy and Commerce, House Ways and Means, House Veterans Affairs) → federal advisory committees (USPSTF, ACIP, MedPAC, MACPAC).
- Within an organisation, people are ordered: Secretary / Administrator / Director → Deputy → Chief of Staff → Chief Medical Officer → Other named senior officials → advisory-committee leadership.
- Programme leads and SROs follow their accountable director.

## 4. Field definitions

### 4.1 Organisation name

The key under which a person sits. Use the official name as the organisation publishes it. Acronyms in parentheses where helpful (e.g. `Centers for Medicare & Medicaid Services (CMS)`, `Veterans Health Administration (VHA)`).

### 4.2 Person name

Include honorifics and post-nominals that the person actually uses publicly: `Dr`, `MD`, `PhD`, `MPH`, `MBA`, `JD`, `RN`, `DVM`, `MG` (Major General), `LTG`, `RDML`, `VADM`, `Sen.`, `Rep.`. Do not invent honorifics. Match what appears on the organisation's official biography page or the HHS / VA website.

### 4.3 `Title:` (required, one)

Current job title, verified to within the last six months. Include effective dates or status flags inline where helpful:
- `Acting` if not Senate-confirmed or otherwise substantive.
- `Nominee` if announced but not yet confirmed.
- `(from {date})` if newly in post.
- `(verify currency)` if there is a known reason to re-check — relevant under the second Trump administration given the unusually high turnover and acting-appointment density in 2025-2026.

### 4.4 Contact fields (optional, zero or more, in this order)

Each appears at most once per person.

- `LinkedIn:` — full canonical URL. Skip if not verifiable.
- `X:` — full URL (`https://x.com/{handle}`). Skip if not verifiable, even if a handle was found.
- `Bluesky:` — full URL (`https://bsky.app/profile/{handle}`).
- `Website:` — full URL of personal/professional site (not the org page).
- `GitHub:` — full URL.
- `Email:` — only for people whose professional email address is published or who have explicitly authorised its inclusion (rare for federal officials; congressional staff and press contacts go through office channels, not personal email).

**Verification rule:** a contact field is only added if a public source attributable to the named person confirms it. Bare URLs without bio/role match are excluded. Better to omit than to guess.

### 4.5 `Stakeholder engagement notes:` (required, list of strings)

Three to seven short bullets. Each bullet is a YAML scalar wrapped in double quotes, ending in a full stop. Each bullet should answer at least one of:

- **What is their career background?** — specialisms, prior roles, qualifications, distinctive experience.
- **What do they own?** — programmes, contracts, statutory functions, public commitments.
- **What have they said publicly?** — direct quotes or paraphrased positions with date context.
- **What is the hook?** — the angle a supplier or strategist would lead with.

Anti-pattern: generic CV bullets ("experienced leader with strong track record"). If the bullet would apply to any senior federal official, it should not be in the register.

### 4.6 `Tone advice:` (required, exactly two strings)

Two bullets, each a YAML scalar wrapped in double quotes, ending in a full stop.

- **Bullet 1 — what to lead with.** The framing, vocabulary, or precedent that will land. May reference specific programmes, reports, or quotes from the engagement notes above.
- **Bullet 2 — what to avoid.** A failure mode specific to this person — not generic. Should be derivable from their engagement notes (career, public statements, current pressures).

Tone advice is a derived field: it must be consistent with the engagement notes for the same person. If you change the notes materially, re-check the tone advice.

### 4.7 Other fields

Currently none. Do not add new field types without updating this spec first.

## 5. Provenance and dating

- All facts are anchored to a year (preferably a month or exact date) where helpful. "Sworn in {month year}" beats "newly in post".
- Convert relative dates to absolute when writing the YAML ("last year" → `2025`).
- When a fact changes (e.g. a CDC Director is removed and a new acting director is named), update the affected fields in the same commit; do not leave stale notes alongside a new title.
- The second Trump administration has produced an unusually high rate of resignations, terminations, and acting-status appointments in HHS leadership during 2025-2026. Treat any HHS Office of the Secretary, CDC, FDA, or Surgeon General entry as warranting re-verification when more than 90 days old.

## 6. Update workflow

1. **Identify the change** — a new nomination, confirmation, resignation, termination, or public statement.
2. **Verify against a public source** — official HHS / VA / Congressional press release, named press article in a national outlet, Federal Register notice, Congressional Record.
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
- **Stale role titles.** A person's role in this register must be their current substantive (or named acting) role, not their most famous previous one. Particularly important for media-prominent figures whose pre-government careers — TV doctors, podcast hosts, academic celebrities — can dominate public memory of them.
- **Duplicate entries.** A person belongs to one organisation. If they hold roles in two, choose the one most relevant for engagement and note the second in prose.
- **Mixing facts and aspirations.** Hooks describe what would land *given the person's stated priorities*, not what the writer wishes the person cared about.
- **Treating HHS as monolithic.** HHS operating divisions have very different cultures, statutory missions, and political postures; CMS is not FDA is not CDC is not NIH. Flatten at your peril.
- **Importing NHS framings unmodified.** The US system is mixed public-private with statutory programmes (Medicare, Medicaid, Veterans, IHS, Tricare) rather than a single national service. Concepts like "the NHS" do not have a single US analog.

## 9. Acronym glossary (selective)

Acronyms used inside the YAML that readers may not know:

- **ACA** — Affordable Care Act.
- **ACF** — Administration for Children and Families (HHS operating division).
- **ACIP** — Advisory Committee on Immunization Practices (CDC vaccine recommendations).
- **ACL** — Administration for Community Living (HHS operating division).
- **AHRQ** — Agency for Healthcare Research and Quality.
- **ASH** — Assistant Secretary for Health (HHS).
- **ASPE** — Assistant Secretary for Planning and Evaluation (HHS).
- **ASPR** — Administration for Strategic Preparedness and Response.
- **ASTP/ONC** — Assistant Secretary for Technology Policy / Office of the National Coordinator for Health Information Technology.
- **CDC** — Centers for Disease Control and Prevention.
- **CHIP** — Children's Health Insurance Program.
- **CMS** — Centers for Medicare & Medicaid Services.
- **CTO / CAIO / CDO** — Chief Technology Officer / Chief Artificial Intelligence Officer / Chief Data Officer (HHS roles, re-scoped 2026).
- **DHA** — Defense Health Agency.
- **DPC** — Domestic Policy Council (White House).
- **EHRM-IO** — Electronic Health Record Modernization Integration Office (VA).
- **FDA** — Food and Drug Administration.
- **FHIR** — Fast Healthcare Interoperability Resources (HL7 standard).
- **FY** — Fiscal Year.
- **HELP** — Senate Committee on Health, Education, Labor and Pensions.
- **HHS** — Department of Health and Human Services.
- **HTI-2 / HTI-5** — Health Data, Technology, and Interoperability rulemakings (ASTP/ONC).
- **IHS** — Indian Health Service.
- **MACPAC** — Medicaid and CHIP Payment and Access Commission.
- **MAHA** — "Make America Healthy Again", the policy slogan of the Secretary Kennedy era HHS.
- **MedPAC** — Medicare Payment Advisory Commission.
- **NIH** — National Institutes of Health.
- **OASH** — Office of the Assistant Secretary for Health.
- **OGC** — Office of the General Counsel.
- **OIG** — Office of the Inspector General.
- **OMB** — Office of Management and Budget (Executive Office of the President).
- **SAMHSA** — Substance Abuse and Mental Health Services Administration.
- **STAT** — STAT News (commonly cited trade outlet for federal health policy).
- **TrumpRx** — government-sponsored prescription drug platform launched under CMS in the second Trump administration.
- **USPHS** — US Public Health Service Commissioned Corps.
- **USPSTF** — US Preventive Services Task Force.
- **VA** — Department of Veterans Affairs.
- **VHA** — Veterans Health Administration.

## 10. Worked example

This is the canonical shape of one person. Any new entry should match it field-for-field (omitting optional contact fields where not verifiable).

```yaml
      - Robert F. Kennedy Jr.:
          - Title: Secretary of Health and Human Services (26th; sworn in 13 February 2025)
          - X: https://x.com/SecKennedy
          - Stakeholder engagement notes:
              - "Sworn in 13 February 2025 as the 26th Secretary of HHS by Associate Justice Neil Gorsuch; the Make America Healthy Again (MAHA) executive order was signed the same day, framing the administration's health agenda."
              - "Pre-government career as an environmental lawyer (Riverkeeper, Waterkeeper Alliance) and as founder of Children's Health Defense; long-running public posture sceptical of vaccines, fluoridation, and pharmaceutical-industry influence on regulators."
              - "Has restructured HHS leadership rapidly through 2025-2026: dismissed CDC Director Susan Monarez in August 2025 after 28 days in post; accepted FDA Commissioner Marty Makary's resignation in May 2026; removed the two top USPSTF leaders in May 2026."
              - "FY27 HHS budget request released 3 April 2026 — $111.1bn discretionary, a $15.8bn (12.5%) reduction from FY26 enacted; vehicle for the MAHA programme restructuring."
              - "Hook: propositions framed around chronic-disease prevention, food and environmental contributors to disease, and reduced pharmaceutical and vaccine industry capture land; conventional public-health, vaccine-promotion, or industry-defending pitches will not."
          - Tone advice:
              - "Lead with chronic disease, environmental health, food policy, and scepticism of regulatory capture — these are the MAHA frame and Kennedy's authored priorities since the 1990s."
              - "Do not pitch conventional vaccine policy, fluoride, or pharma-industry framings — these are the explicit targets of his agenda and he will mark down anything that reads as defending the pre-2025 status quo."
```

## 11. Out-of-band notes

Some organisation blocks in the YAML contain a non-person entry such as:

```yaml
      - Notes on Centers for Disease Control and Prevention:
          - Status: ...
          - Implication: ...
```

These are permitted only where they explain why a role is *not* listed (e.g. unfilled at the time of writing, in acting status across multiple sub-posts, or the body has been restructured) and should be removed once a named person can be added. They do not need `Tone advice`. Given 2025-2026 HHS turbulence, this device is used more here than in the UK / Irish registers.

## 12. Open questions

These are known gaps to track and resolve:

- The substantive Senate-confirmed CDC Director after Susan Monarez's August 2025 termination — vacancy and acting-director chain ongoing as of June 2026, with multiple acting roles inside the agency.
- The substantive Senate-confirmed FDA Commissioner after Marty Makary's May 2026 resignation — Kyle Diamantas is acting commissioner.
- The Senate confirmation status of Surgeon General nominee Nicole Saphier (announced 30 April 2026 after the withdrawal of Casey Means's nomination).
- The full named leadership of the post-restructure ASTP / ONC arrangement after HHS shifted the CTO, CAIO and CDO roles out of the dual-titled office in early 2026.
- The named leadership of MedPAC, MACPAC, USPSTF and ACIP following the May 2026 termination of USPSTF leadership and ongoing membership reviews.
- The named senior leadership of IHS, SAMHSA, AHRQ, ACF and ACL — second-tier HHS operating divisions where the 2025-2026 acting / substantive picture is unstable.
- The DHA (Defense Health Agency) Director and Assistant Secretary of Defense for Health Affairs — the DoD health tier needs verification against current DoD biographies.
- The named White House Domestic Policy Council Health Lead.
- The Ranking Members of Senate HELP, Senate Finance, House Energy and Commerce Health Subcommittee, and House Ways and Means Health Subcommittee — to add for balanced engagement coverage.

Each open question should be closed by editing this spec and the YAML in the same commit when resolved.
