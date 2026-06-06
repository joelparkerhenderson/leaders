# spec.md

Single source of truth for the structure, semantics, and update rules.

Treat this document as the canonical specification: the YAML must conform to it;
if the YAML and this spec disagree, the spec wins and the YAML is fixed.

## 1. Purpose

These \*.yml files are engagement registers of named individuals who are leaders in a sector, area, cause, purpose.

Each entry exists so that a reader can decide:

1. **Who to engage** for a given topic.
2. **How to engage them** — the angle that lands and the angle that fails.
3. **Where to engage them** — which public channels they actually use.

It is not a phone book, not a CRM, and not a comms list.

Entries that do not directly serve engagement decision-making are out of scope.

## 2. Scope

**In scope:**

- Statutory bodies, commissioners, auditors.
- Government roles that are relevant to the purpose.
- Senedd Cymru roles material to NHS Wales scrutiny.
- Related sector bodies, community bodies, think-tanks, professional organizations.
- For each organisation: only stakeholders senior enough that engagement with them shapes decisions across the organisation (typically CEO, Chair, Directors, programme SROs, professional-college Chairs).

**Out of scope:**

- Operational staff below director / programme-SRO level.
- Suppliers, vendors, consultancies (their leaders may appear only when they hold a named role).
- Historical post-holders (unless explicitly flagged as predecessor for context).

## 3. Structure

The YAML is a single top-level mapping with one key.

```
Leaders:
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

- Organisations are grouped by importance for engagement, such as priority, breadth, involvement.
- Within an organisation, people are ordered: CEO → Chair → Director → members.
- Programme leads, product leads, project leads, etc. all follow their accountable director.

## 4. Field definitions

### 4.1 Organisation name

The key under which a person sits. Use the official name as the organisation publishes it. Acronyms in parentheses where helpful.

### 4.2 Person name

Include honorifics that the person actually uses publicly: `Dr`, `Professor`, post-nominals (`OBE`, `CBE`, `MBE`, `MS`, `FCPara`, `RN`, `FCIPD`, `MBE FRSPH`).

Do not invent honorifics. Match what appears on the organisation's official board page.

### 4.3 `Title:` (required, one)

Current job title, verified to within the last six months. Include effective dates or status flags inline where helpful:

- `Interim` or `Acting` if not substantive.
- `(from {date})` if newly in post.
- `(verify currency)` if there is a known reason to re-check.

### 4.4 Contact fields (optional, zero or more, in this order)

Each appears at most once per person.

- `Email:` — only for people whose email address is published or who have explicitly authorised its inclusion.
- `Website:` — full URL of personal/professional site (not the org page).
- `LinkedIn:` — full canonical URL. Skip if not verifiable.
- `Instagram:` — full URL (`https://instagram.com/{handle}`). Skip if not verifiable, even if a handle was found.
- `X:` — full URL (`https://x.com/{handle}`). Skip if not verifiable, even if a handle was found.
- `Bluesky:` — full URL (`https://bsky.app/profile/{handle}`).
- `GitHub:` — full URL (`https://github.com/{handle}`). Skip if not verifiable, even if a handle was found.
- `GitLab:` — full URL (`https://gitlab.com/{handle}`). Skip if not verifiable, even if a handle was found.
- `Codeberg:` — full URL (`https://codeberg.org/{handle}`). Skip if not verifiable, even if a handle was found.

**Verification rule:**

- A contact field is only added if a public source attributable to the named person confirms it.
- Bare URLs without bio/role match are excluded.
- Better to omit than to guess.

### 4.5 `Stakeholder engagement notes:` (required, list of strings)

Three to seven short bullets. Each bullet is a YAML scalar wrapped in double quotes, ending in a full stop. Each bullet should answer at least one of:

- **What is their career background?** — specialisms, prior roles, qualifications, distinctive experience.
- **What do they own?** — programmes, contracts, statutory functions, public commitments.
- **What have they said publicly?** — direct quotes or paraphrased positions with date context.
- **What is the hook?** — the angle a supplier or strategist would lead with.

Anti-pattern:

- Generic CV bullets ("experienced leader with strong track record").
- If the bullet would apply to any senior leader, it should not be in the register.

### 4.6 `Tone advice:` (required, exactly two strings)

Two bullets, each a YAML scalar wrapped in double quotes, ending in a full stop.

- **Bullet 1 — what to lead with.** The framing, vocabulary, or precedent that will land. May reference specific programmes, reports, or quotes from the engagement notes above.
- **Bullet 2 — what to avoid.** A failure mode specific to this person — not generic. Should be derivable from their engagement notes (career, public statements, current pressures).

Tone advice is a derived field: it must be consistent with the engagement notes
for the same person. If you change the notes materially, re-check the tone
advice.

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

Acronyms used inside the YAML that readers may not know.

## 10. Worked example

This is the canonical shape of one person. Any new entry should match it field-for-field (omitting optional contact fields where not verifiable).

```yaml
- Alice Adams:
    - Title: Chief Executive Officer
    - Email: alice.adams@example.com
    - LinkedIn: https://linkedin.com/in/alice-adams
    - X: https://x.com/alice-adams
    - Stakeholder engagement notes:
        - "CEO since Example Org launched April 2021; 30+ years in sector. BA in Art, Harvard University."
        - "Named CEO of the Year 2021; finalist Leaders 100 'Digital Leader of the Year' 2024."
        - "Questioned at government committed on 14 May 2025 over work in progress — she is under intense political scrutiny."
    - Tone advice:
        - "Interoperability and standards lands — 'stop compromising on integration, move to a streamlined, standard approach' is her line. Lead with de-risking and delivery credibility."
        - "Political scrutiny on delivery means vision pitches land worse than recovery / de-risking ones."
```

## 11. Out-of-band notes

Some organisation blocks in the YAML contain a non-person entry such as:

```yaml
- Notes on Ge Covernment Committee:
    - Status: ...
    - Implication: ...
```

These are permitted only where they explain why a role is _not_ listed (e.g.
unfilled at the time of writing) and should be removed once a named person can
be added. They do not need `Tone advice`.

## 12. Open questions

List any known gaps to track and resolve.

Each open question should be closed by editing this spec and the YAML in the same commit when resolved.
