# spec.md — `leaders.yml`

Single source of truth for the structure, semantics, and update rules of `leaders.yml` for Swedish health and medical care (hälso- och sjukvård). Treat this document as the canonical specification: the YAML must conform to it; if the YAML and this spec disagree, the spec wins and the YAML is fixed.

## 1. Purpose

`leaders.yml` is an engagement register of named individuals in and around Swedish health and medical care. Each entry exists so that a reader (typically inside the Ministry of Health and Social Affairs (Socialdepartementet), a state agency, a region (regioner), a university hospital, or an adjacent national body) can decide:

1. **Who to engage** for a given digital/transformation/policy topic.
2. **How to engage them** — the angle that lands and the angle that fails.
3. **Where to engage them** — which public channels they actually use.

It is not a phone book, not a CRM, and not a comms list. Entries that do not directly serve engagement decision-making are out of scope.

Sweden's health system has no single national service. The state, via the Ministry of Health and Social Affairs, sets the statutory framework (Hälso- och sjukvårdslagen 2017:30) and policy. Twenty-one regions (regioner) deliver healthcare; 290 municipalities (kommuner) deliver social care for older people and people with disabilities. A federation of state agencies under the Ministry — Socialstyrelsen, Folkhälsomyndigheten, Läkemedelsverket, IVO, TLV, E-hälsomyndigheten, SBU, Forte, MSB, and others — regulate, evaluate, license, and reimburse. SKR (Sveriges Kommuner och Regioner) is the employer and member organisation for the regions and municipalities and is the principal counterparty for the state on collective negotiations and joint reform programmes such as God och nära vård.

## 2. Scope

**In scope:**
- Government and Ministry of Health and Social Affairs (Socialdepartementet): the Minister for Social Affairs and Public Health (Socialminister / minister för folkhälsa), the Minister for Health Care (Sjukvårdsminister), the Minister for Social Services (Socialtjänstminister) where the brief is filled separately, the State Secretaries (statssekreterare), and the Director-General for Legal Affairs in the social ministry.
- State agencies (myndigheter) under the Ministry of Health and Social Affairs: Socialstyrelsen (National Board of Health and Welfare), Folkhälsomyndigheten (Public Health Agency), Läkemedelsverket (Medical Products Agency), Inspektionen för vård och omsorg (IVO), Tandvårds- och läkemedelsförmånsverket (TLV), E-hälsomyndigheten (eHealth Agency), Statens beredning för medicinsk och social utvärdering (SBU), Forte, Vetenskapsrådet (medical research), Försäkringskassan (Social Insurance Agency where the brief touches health benefits), Myndigheten för vård- och omsorgsanalys (Vård- och omsorgsanalys), Statens institutionsstyrelse (SiS) where the brief touches forensic-care services.
- SKR (Sveriges Kommuner och Regioner): the Chair (ordförande), Vice Chairs, and President (verkställande direktör / VD).
- The 21 regional health systems (Sweden's regioner): the political chair of the regional health board (hälso- och sjukvårdsstyrelsen) and the regional director of health and medical care (hälso- och sjukvårdsdirektör) for the largest regions (Stockholm, Västra Götaland, Skåne, Östergötland, Uppsala, Värmland) where national roles attach.
- University hospital leadership where the role has national scope (e.g. Karolinska Universitetssjukhuset, Sahlgrenska Universitetssjukhuset, Skånes universitetssjukhus, Akademiska sjukhuset Uppsala).
- Riksdag committees material to health policy scrutiny: Socialutskottet (Social Affairs Committee) Chair and Deputy Chair; party spokespeople for social affairs and health where they hold a national posture.
- Statutory commissioners and oversight bodies: Riksrevisionen (National Audit Office) where directly relevant to health; Justitieombudsmannen (Parliamentary Ombudsman) where directly relevant; Datainspektionen / Integritetsskyddsmyndigheten (IMY) on health-data matters.
- Related sector bodies of national significance: Sveriges läkarförbund (Swedish Medical Association), Vårdförbundet (the nursing and midwifery union), Svensk sjuksköterskeförening, Svenska Läkaresällskapet (Swedish Society of Medicine), Tandläkarförbundet, Sveriges Farmaceuter, and the Karolinska Institutet leadership where the role is health-policy facing.
- For each organisation: only stakeholders senior enough that engagement with them shapes decisions across the organisation (typically Minister, statssekreterare, generaldirektör (DG), regional sjukvårdsdirektör, hospital director, professional-society chair).

**Out of scope:**
- Operational staff below department head (avdelningschef) / programme owner level inside agencies and regions.
- Suppliers, vendors, consultancies (their leaders may appear only when they hold a named role in a Swedish public body, e.g. as a Board member).
- Historical post-holders (unless explicitly flagged as predecessor for context).
- Other Nordic counterparts (Denmark, Norway, Finland, Iceland) unless they also hold a Sweden-facing role.

## 3. Structure

The YAML is a single top-level mapping with one key.

```
Swedish health and medical care stakeholders:
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

- Organisations are grouped by tier: Government and Ministry of Health and Social Affairs → State agencies in order of policy weight (Socialstyrelsen, Folkhälsomyndigheten, Läkemedelsverket, IVO, TLV, E-hälsomyndigheten, SBU, Forte, Vård- och omsorgsanalys) → SKR → Riksdag Socialutskottet → 21 regional health systems alphabetised (Blekinge, Dalarna, Gotland, Gävleborg, Halland, Jämtland Härjedalen, Jönköping, Kalmar, Kronoberg, Norrbotten, Skåne, Stockholm, Sörmland, Uppsala, Värmland, Västerbotten, Västernorrland, Västmanland, Västra Götaland, Örebro, Östergötland) → university hospitals → professional associations → oversight bodies.
- Within an organisation, people are ordered: Minister / generaldirektör (DG) / hälso- och sjukvårdsdirektör → Deputy / vice-DG / vice ordförande → Medical Director / Chief Medical Officer → Nursing Director → Other Directors → Director of Digital / CDIO → Director of Finance → Board members where named.
- Programme leads and SROs follow their accountable director.

## 4. Field definitions

### 4.1 Organisation name

The key under which a person sits. Use the official name as the organisation publishes it. Acronyms in parentheses where helpful. Provide the Swedish name first and the English in parentheses where the body is widely known by both (e.g. `Socialstyrelsen (National Board of Health and Welfare)`, `Folkhälsomyndigheten (Public Health Agency of Sweden)`, `Sveriges Kommuner och Regioner (SKR)`).

### 4.2 Person name

Include honorifics and academic titles that the person actually uses publicly: `Dr`, `Professor`, `Docent` (associate professor), `Med Dr` (Doctor of Medicine). Post-nominals are rare in Swedish public-life convention; party affiliation in parentheses for elected officials (e.g. `(M)` Moderaterna, `(S)` Socialdemokraterna, `(KD)` Kristdemokraterna, `(SD)` Sverigedemokraterna, `(L)` Liberalerna, `(C)` Centerpartiet, `(MP)` Miljöpartiet, `(V)` Vänsterpartiet) is the strong norm. Match what appears on the organisation's official biography page or regeringen.se.

### 4.3 `Title:` (required, one)

Current job title, verified to within the last six months. Use the Swedish title and add an English gloss in parentheses where the Swedish title is not self-evident to an English reader (e.g. `Sjukvårdsminister (Minister for Health Care)`). Include effective dates or status flags inline where helpful:
- `Tillförordnad` (acting) if not substantive.
- `(från {datum})` if newly in post.
- `(verifiera aktualitet)` if there is a known reason to re-check.

### 4.4 Contact fields (optional, zero or more, in this order)

Each appears at most once per person.

- `LinkedIn:` — full canonical URL. Skip if not verifiable.
- `X:` — full URL (`https://x.com/{handle}`). Skip if not verifiable, even if a handle was found.
- `Bluesky:` — full URL (`https://bsky.app/profile/{handle}`).
- `Mastodon:` — full URL (`https://{instance}/@{handle}`). Particularly relevant for Swedish public-sector figures who maintain Mastodon presence.
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

Anti-pattern: generic CV bullets ("erfaren ledare med stark leveransförmåga"). If the bullet would apply to any Swedish generaldirektör, it should not be in the register.

### 4.6 `Tone advice:` (required, exactly two strings)

Two bullets, each a YAML scalar wrapped in double quotes, ending in a full stop.

- **Bullet 1 — what to lead with.** The framing, vocabulary, or precedent that will land. May reference specific programmes, reports, or quotes from the engagement notes above (e.g. God och nära vård, Vision e-hälsa 2025, nationell kunskapsstyrning, kömiljarden).
- **Bullet 2 — what to avoid.** A failure mode specific to this person — not generic. Should be derivable from their engagement notes (career, public statements, current pressures).

Tone advice is a derived field: it must be consistent with the engagement notes for the same person. If you change the notes materially, re-check the tone advice.

### 4.7 Other fields

Currently none. Do not add new field types without updating this spec first.

## 5. Provenance and dating

- All facts are anchored to a year (preferably a month or exact date) where helpful. "Tillträdde {månad år}" beats "nytillträdd".
- Convert relative dates to absolute when writing the YAML ("förra året" → `2025`).
- When a fact changes (e.g. a generaldirektör leaves), update the affected fields in the same commit; do not leave stale notes alongside a new title.
- Swedish agency leadership has been unusually mobile in 2024-2026 (Eriksson Läkemedelsverket → Socialstyrelsen; Wigzell Socialstyrelsen → Folkhälsomyndigheten; Tegmark Wisell Folkhälsomyndigheten → global health ambassador). Treat any agency DG entry as warranting re-verification when more than 90 days old.

## 6. Update workflow

1. **Identify the change** — a new appointment, departure, statement.
2. **Verify against a public source** — official agency page, regeringen.se announcement, named press article, SKR press release, regional press release.
3. **Apply minimum diff** — change only the fields the new fact touches. Re-check `Tone advice` if engagement notes changed.
4. **Confirm structure** — indentation, ordering, no `?` placeholders left behind.
5. **Re-validate cross-references** — if person A moved bodies, update both old-body and new-body blocks.

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
- **Speculation.** "Sannolikt mottaglig för AI." If you cannot point to a public source for the disposition, omit it.
- **Vendor-flattering language.** Tone advice exists to make engagement realistic, not optimistic.
- **Stale role titles.** A person's role in this register must be their current substantive (or named acting) role, not their most famous previous one. Particularly important in Sweden where agency DGs often move between agencies.
- **Duplicate entries.** A person belongs to one organisation. If they hold roles in two, choose the one most relevant for engagement and note the second in prose.
- **Mixing facts and aspirations.** Hooks describe what would land *given the person's stated priorities*, not what the writer wishes the person cared about.
- **Treating Sweden as a single national service.** Healthcare delivery sits with 21 regions and social care with 290 municipalities. National policy is set in the Ministry; implementation is negotiated through SKR and the regions. Pitches that assume a single national customer will fail.
- **Importing NHS framings unmodified.** Swedish self-governance, regional accountability, and the agency-federation model do not map cleanly to NHS England structures.

## 9. Acronym and term glossary (selective)

Terms and acronyms used inside the YAML that readers may not know:

- **Generaldirektör (GD)** — Director General, the chief executive of a Swedish state agency.
- **Statssekreterare** — State Secretary, the political deputy to a minister.
- **Sakkunnig** — political adviser inside a ministry.
- **Socialdepartementet** — Ministry of Health and Social Affairs.
- **Sjukvårdsminister** — Minister for Health Care.
- **Socialminister** — Minister for Social Affairs (and, in the current Kristersson cabinet, Public Health).
- **Region / Regionerna** — the 21 directly elected regional authorities responsible for healthcare delivery.
- **Hälso- och sjukvårdslagen (HSL)** — Health and Medical Care Act 2017:30, the statutory base for healthcare.
- **Hälso- och sjukvårdsstyrelsen** — regional health and medical care board (political).
- **Hälso- och sjukvårdsdirektör** — regional director of health and medical care (administrative).
- **Sjukhusdirektör** — hospital director.
- **God och nära vård** — "Good and Close Care", the long-running national reform shifting activity from hospital to primary and community care.
- **Vision e-hälsa 2025** — national digital health strategy.
- **Nationell högspecialiserad vård (NHV)** — national highly-specialised care designations.
- **Kunskapsstyrning** — national knowledge-management system (SKR-led, regions-owned).
- **Kömiljarden** — "Queue billion", the targeted state grant to reduce healthcare waiting times.
- **Socialstyrelsen** — National Board of Health and Welfare; sets norms, registers professionals, runs national registries, issues knowledge guidance.
- **Folkhälsomyndigheten** — Public Health Agency.
- **Läkemedelsverket** — Medical Products Agency (the Swedish medicines and devices regulator).
- **Inspektionen för vård och omsorg (IVO)** — Health and Social Care Inspectorate.
- **TLV** — Tandvårds- och läkemedelsförmånsverket; Dental and Pharmaceutical Benefits Agency (national HTA / reimbursement decisions).
- **E-hälsomyndigheten** — eHealth Agency (national e-prescription, pharmacy data, health-data infrastructure).
- **SBU** — Statens beredning för medicinsk och social utvärdering; Swedish Agency for Health Technology Assessment.
- **Forte** — Forskningsrådet för hälsa, arbetsliv och välfärd; Research Council for Health, Working Life and Welfare.
- **Vård- och omsorgsanalys** — Myndigheten för vård- och omsorgsanalys; the agency that audits and evaluates care services.
- **SKR** — Sveriges Kommuner och Regioner; Swedish Association of Local Authorities and Regions.
- **Socialutskottet** — the Riksdag Committee on Social Affairs (the parliamentary committee scrutinising health).
- **Riksrevisionen** — National Audit Office.
- **JO** — Justitieombudsmannen, Parliamentary Ombudsman.
- **IMY** — Integritetsskyddsmyndigheten, Swedish Authority for Privacy Protection.
- **KI** — Karolinska Institutet (the medical university).
- **Karolinska / NKS** — Karolinska Universitetssjukhuset (Karolinska University Hospital, Solna and Huddinge).
- **Sahlgrenska** — Sahlgrenska Universitetssjukhuset, Gothenburg.
- **SUS** — Skånes universitetssjukhus, Malmö and Lund.
- **NPÖ / Nationell patientöversikt** — National Patient Summary (cross-region clinical record sharing).
- **Vårdval** — patient choice of provider; introduced in primary care from 2010 onwards.

## 10. Worked example

This is the canonical shape of one person. Any new entry should match it field-for-field (omitting optional contact fields where not verifiable).

```yaml
      - Jakob Forssmed (KD):
          - Title: Socialminister (Minister for Social Affairs and Public Health) (från oktober 2022)
          - X: https://x.com/jakobforssmed
          - Stakeholder engagement notes:
              - "Kristdemokraterna (KD); appointed Socialminister in the Kristersson cabinet 18 October 2022; member of the Riksdag since 2014; first deputy chair of the Christian Democrats since 2015."
              - "Brief covers social services, public health, dental policy, pharmaceuticals, alcohol and tobacco policy — the Sjukvårdsminister (currently Elisabet Lann, KD) is the separate care-delivery brief in the same ministry."
              - "Long-running public posture on loneliness, mental health, and youth screen-time policy — early author of the 2024-2026 KD positioning that produced the Care Closer to Home and screen-time policy frames."
              - "Active counterpart for SKR, Socialstyrelsen, Folkhälsomyndigheten, Läkemedelsverket, TLV, E-hälsomyndigheten and IVO on Ministry-level reform decisions; the senior Minister on the social side of the brief."
              - "Hook: mental-health, youth and addictive-substance policy, pharmaceutical access (TLV) and public-health-prevention propositions land; pure acute-throughput pitches are not his brief and will be redirected."
          - Tone advice:
              - "Lead with mental health, youth wellbeing, screen-time, public-health prevention, and pharmaceutical access — these are his authored Ministry priorities since 2022."
              - "Do not pitch acute hospital productivity or kömiljarden mechanics direct to him — that is the Sjukvårdsminister's brief, and he will route the conversation accordingly."
```

## 11. Out-of-band notes

Some organisation blocks in the YAML contain a non-person entry such as:

```yaml
      - Notes on Läkemedelsverket:
          - Status: ...
          - Implication: ...
```

These are permitted only where they explain why a role is *not* listed (e.g. unfilled at the time of writing because of an acting appointment chain or governance restructuring) and should be removed once a named person can be added. They do not need `Tone advice`. Used here for agencies currently under acting / interim leadership or restructure (Läkemedelsverket post-Eriksson, IVO board-led transition from 15 June 2026).

## 12. Open questions

These are known gaps to track and resolve:

- The substantive generaldirektör for Läkemedelsverket after Björn Eriksson moved to Socialstyrelsen 15 August 2024 (Joakim Brandenberg acting; substantive recruitment continuing into 2026).
- The substantive generaldirektör for E-hälsomyndigheten after Gunilla Nordlöf's term extension ends 31 July 2026 (substantive recruitment underway since January 2026).
- The named generaldirektör and the named ordförande of the new IVO board after the governance shift to board-led leadership from 15 June 2026.
- The current verkställande direktör (VD) of SKR and the post-2026 SKR Chair after the regional-political ordförande cycle following the September 2026 Riksdag election.
- The 2026-2030 regional sjukvårdsdirektörer for the largest regions (Stockholm, Västra Götaland, Skåne) after the post-2026 election regional administrative reshuffles.
- The named ordförande of Socialutskottet for the new Riksdag term following the September 2026 election.
- The current Chair (ordförande) of Sveriges läkarförbund, Vårdförbundet, Svenska Läkaresällskapet, and Tandläkarförbundet, with currency verified to within six months.
- Named sakkunniga (political advisers) and ministry directors-general inside Socialdepartementet across the health, social-services, and pharmaceutical files.

Each open question should be closed by editing this spec and the YAML in the same commit when resolved.
