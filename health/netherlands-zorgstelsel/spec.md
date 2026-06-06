# spec.md — `leaders.yml`

Single source of truth for the structure, semantics, and update rules of `leaders.yml` for the Dutch zorgstelsel (healthcare system). Treat this document as the canonical specification: the YAML must conform to it; if the YAML and this spec disagree, the spec wins and the YAML is fixed.

## 1. Purpose

`leaders.yml` is an engagement register of named individuals in and around the Dutch zorgstelsel. Each entry exists so that a reader (typically inside the Ministerie van Volksgezondheid, Welzijn en Sport (VWS), a zelfstandig bestuursorgaan (ZBO), a zorgverzekeraar, an academic medical centre (UMC), or an adjacent national body) can decide:

1. **Who to engage** for a given digital/transformation/policy topic.
2. **How to engage them** — the angle that lands and the angle that fails.
3. **Where to engage them** — which public channels they actually use.

It is not a phone book, not a CRM, and not a comms list. Entries that do not directly serve engagement decision-making are out of scope.

The Dutch zorgstelsel is a regulated-market model. Since the 2006 reform (Zorgverzekeringswet, Zvw) curative care has been delivered by competing private providers and purchased by competing private health insurers operating under statutory acceptance and risk-equalisation obligations. Long-term care is funded under the Wet langdurige zorg (Wlz) via Zorgkantoren; community and social care under the Wet maatschappelijke ondersteuning (Wmo) by 342 municipalities; youth care under the Jeugdwet by municipalities. VWS sets the statutory framework. Independent regulators and arm's-length bodies (NZa, Zorginstituut Nederland, IGJ, ACM) regulate tariffs, the basic-insurance benefits package, quality, and competition. The RIVM provides public-health surveillance and evidence; the CBG regulates medicines. The result is a uniquely intermediated system: most operational decisions are made by zorgverzekeraars and providers under arm's-length regulator oversight, not by the Ministry.

## 2. Scope

**In scope:**
- Kabinet: Minister-President; Minister van Volksgezondheid, Welzijn en Sport (VWS); Minister voor Medische Zorg or equivalent split portfolio when filled; Staatssecretaris(en) van VWS (typically Langdurige Zorg en Sport, Jeugd en Preventie); Directeur-Generaal Volksgezondheid, Directeur-Generaal Curatieve Zorg, Directeur-Generaal Langdurige Zorg, Secretaris-Generaal VWS.
- Independent regulators and arm's-length bodies: Nederlandse Zorgautoriteit (NZa); Zorginstituut Nederland (ZIN); Inspectie Gezondheidszorg en Jeugd (IGJ); College ter Beoordeling van Geneesmiddelen (CBG); Rijksinstituut voor Volksgezondheid en Milieu (RIVM); Autoriteit Consument & Markt (ACM) where the brief is health-sector competition; Autoriteit Persoonsgegevens (AP) on health-data matters.
- Public-health and digital infrastructure bodies: Nictiz; Nederlandse Federatie van Universitair Medische Centra (NFU) where the role is national-policy facing; Stichting MedMij; Health-RI.
- Sector representative organisations: Zorgverzekeraars Nederland (ZN); Nederlandse Vereniging van Ziekenhuizen (NVZ); Nederlandse Federatie van Universitair Medische Centra (NFU); ActiZ (long-term care); Vereniging Gehandicaptenzorg Nederland (VGN); GGZ Nederland / de Nederlandse ggz; InEen (primary-care collaboratives); Landelijke Huisartsen Vereniging (LHV); Koninklijke Nederlandse Maatschappij tot bevordering der Geneeskunst (KNMG); Federatie Medisch Specialisten (FMS); Verpleegkundigen & Verzorgenden Nederland (V&VN); Koninklijke Nederlandse Maatschappij ter bevordering der Pharmacie (KNMP); Patiëntenfederatie Nederland.
- Tweede Kamer and Eerste Kamer committee leadership for VWS: voorzitter and ondervoorzitters of the vaste commissie voor Volksgezondheid, Welzijn en Sport; party spokespeople (woordvoerders zorg) where they hold a national posture.
- Statutory and oversight bodies of relevance to health: Algemene Rekenkamer where directly relevant; Nationale ombudsman where directly relevant; Sociaal-Economische Raad (SER) on health workforce and labour-market matters.
- For each organisation: only stakeholders senior enough that engagement with them shapes decisions across the organisation (typically Minister, Staatssecretaris, Directeur-Generaal, Voorzitter Raad van Bestuur, Inspecteur-Generaal).

**Out of scope:**
- Operational staff below afdelingshoofd / directielid level inside VWS, regulators and ZBOs, and below Raad van Bestuur level inside provider organisations.
- Suppliers, vendors, consultancies (their leaders may appear only when they hold a named role in a Dutch public body, e.g. a Raad van Toezicht seat in a ZBO).
- Historical post-holders (unless explicitly flagged as predecessor for context).
- Other EU counterparts (unless they also hold a Netherlands-facing role).

## 3. Structure

The YAML is a single top-level mapping with one key.

```
Nederlands zorgstelsel stakeholders:
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

- Organisations are grouped by tier: Kabinet (Minister-President, Ministerie van VWS) → independent regulators and ZBOs (NZa, Zorginstituut Nederland, IGJ, CBG, RIVM, ACM) → public-health and digital infrastructure (Nictiz, Health-RI, MedMij) → sector representative organisations in the order ZN → NVZ → NFU → ActiZ → VGN → de Nederlandse ggz → InEen → LHV → KNMG → FMS → V&VN → KNMP → Patiëntenfederatie → Tweede Kamer commissie VWS → Eerste Kamer commissie VWS → oversight bodies.
- Within an organisation, people are ordered: Minister / Voorzitter Raad van Bestuur / Inspecteur-Generaal → Staatssecretaris / Vicevoorzitter / lid Raad van Bestuur → Medisch Directeur → Verpleegkundig Directeur → Andere directors → Director of Digital → Director of Finance → Raad van Toezicht members where named.
- Programme leads and SROs follow their accountable director.

## 4. Field definitions

### 4.1 Organisation name

The key under which a person sits. Use the official name as the organisation publishes it. Acronyms in parentheses where helpful. Provide the Dutch name first and the English in parentheses where the body is widely known by both (e.g. `Nederlandse Zorgautoriteit (NZa, Dutch Healthcare Authority)`, `Zorginstituut Nederland (ZIN, National Health Care Institute)`, `Rijksinstituut voor Volksgezondheid en Milieu (RIVM, National Institute for Public Health and the Environment)`).

### 4.2 Person name

Include academic titles that the person actually uses publicly: `dr.`, `drs.`, `mr.`, `prof. dr.`, `prof. dr. ir.` — the title sequence is part of canonical Dutch professional naming. Party affiliation in parentheses for elected officials and political appointees, using the canonical Dutch abbreviations (`VVD`, `D66`, `CDA`, `PvdA`, `GroenLinks`, `GL-PvdA`, `PVV`, `NSC`, `BBB`, `SP`, `ChristenUnie`, `SGP`, `Volt`, `JA21`, `FvD`, `DENK`). Match what appears on Rijksoverheid.nl or the organisation's official biography.

### 4.3 `Title:` (required, one)

Current job title, verified to within the last six months. Use the Dutch title and add an English gloss in parentheses where the Dutch title is not self-evident to an English reader (e.g. `Minister van Volksgezondheid, Welzijn en Sport (Minister of Health, Welfare and Sport)`, `Inspecteur-Generaal (Inspector-General)`). Include effective dates or status flags inline where helpful:
- `waarnemend` (acting) if not substantive.
- `(per {datum})` if newly in post.
- `(actualiteit controleren)` if there is a known reason to re-check.

### 4.4 Contact fields (optional, zero or more, in this order)

Each appears at most once per person.

- `LinkedIn:` — full canonical URL. Skip if not verifiable. LinkedIn penetration is exceptionally high in Dutch public-sector senior leadership; expect LinkedIn to be the most reliable contact field.
- `X:` — full URL (`https://x.com/{handle}`). Skip if not verifiable, even if a handle was found.
- `Bluesky:` — full URL (`https://bsky.app/profile/{handle}`).
- `Mastodon:` — full URL (`https://{instance}/@{handle}`). Mastodon adoption among Dutch public-health figures is meaningful (`mastodon.social`, `bsky.social`, `social.overheid.nl`).
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

Anti-pattern: generic CV bullets ("ervaren bestuurder met groot netwerk"). If the bullet would apply to any senior Dutch ZBO bestuurder, it should not be in the register.

### 4.6 `Tone advice:` (required, exactly two strings)

Two bullets, each a YAML scalar wrapped in double quotes, ending in a full stop.

- **Bullet 1 — what to lead with.** The framing, vocabulary, or precedent that will land. May reference specific programmes, reports, or quotes from the engagement notes above (e.g. Integraal Zorgakkoord (IZA), Wet op zorgcoördinatie, Zorginstituut-pakketbeoordeling, NZa-tariefbeschikking, ePD/eOverdracht, passende zorg).
- **Bullet 2 — what to avoid.** A failure mode specific to this person — not generic. Should be derivable from their engagement notes (career, public statements, current pressures).

Tone advice is a derived field: it must be consistent with the engagement notes for the same person. If you change the notes materially, re-check the tone advice.

### 4.7 Other fields

Currently none. Do not add new field types without updating this spec first.

## 5. Provenance and dating

- All facts are anchored to a year (preferably a month or exact date) where helpful. "Aangetreden per {datum}" beats "onlangs benoemd".
- Convert relative dates to absolute when writing the YAML ("vorig jaar" → `2025`).
- When a fact changes (e.g. a Voorzitter Raad van Bestuur leaves), update the affected fields in the same commit; do not leave stale notes alongside a new title.
- Cabinet instability since the Schoof cabinet collapse (June 2025), the October 2025 election, and the formation of the Jetten cabinet (sworn in 23 February 2026) has produced exceptionally rapid VWS Minister turnover. Treat any Ministerie van VWS entry pre-dating 23 February 2026 as warranting re-verification.

## 6. Update workflow

1. **Identify the change** — a new appointment, departure, statement, or Staatscourant publication.
2. **Verify against a public source** — official Rijksoverheid.nl / regulator / ZBO page, Staatscourant / Staatsblad, named press article in NRC, de Volkskrant, Trouw, Skipr, Zorgvisie, Medisch Contact, NRC Handelsblad.
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
- **Speculation.** "Vermoedelijk welwillend tegenover AI." If you cannot point to a public source for the disposition, omit it.
- **Vendor-flattering language.** Tone advice exists to make engagement realistic, not optimistic.
- **Stale role titles.** A person's role in this register must be their current substantive (or named acting) role, not their most famous previous one.
- **Duplicate entries.** A person belongs to one organisation. If they hold roles in two, choose the one most relevant for engagement and note the second in prose.
- **Mixing facts and aspirations.** Hooks describe what would land *given the person's stated priorities*, not what the writer wishes the person cared about.
- **Treating the zorgstelsel as state-delivered.** Care is delivered by private and not-for-profit providers and purchased by competing zorgverzekeraars; the Ministry sets the framework and the regulators (NZa, Zorginstituut, IGJ) referee. Pitches that assume VWS is the operational buyer will be redirected.
- **Importing NHS or US framings unmodified.** The Netherlands has neither a single national service (UK) nor a fragmented public-private patchwork (US); it is a regulated insurance market with arm's-length expert regulators that do not have direct UK or US analogues.

## 9. Acronym and term glossary (selective)

Terms and acronyms used inside the YAML that readers may not know:

- **ACM** — Autoriteit Consument & Markt (the competition and consumer authority; has health-sector merger and competition powers).
- **ActiZ** — branchevereniging voor zorgorganisaties (the federation of long-term care providers).
- **AP** — Autoriteit Persoonsgegevens (Dutch data protection authority).
- **CBG** — College ter Beoordeling van Geneesmiddelen (Medicines Evaluation Board).
- **CIb** — Centrum Infectieziektebestrijding (Centre for Infectious Disease Control, inside RIVM).
- **DBC / DOT** — Diagnose-Behandeling-Combinatie / DBCs Op weg naar Transparantie (the Dutch hospital-product-payment system).
- **ePD / eOverdracht** — elektronisch patiëntendossier / elektronische overdracht (electronic patient record / electronic handover standards).
- **Federatie Medisch Specialisten (FMS)** — federation of medical-specialist scientific societies.
- **GGD** — Gemeentelijke Gezondheidsdienst (municipal public-health service; 25 regional GGDs nationally).
- **GGZ** — Geestelijke Gezondheidszorg (mental healthcare); de Nederlandse ggz is the branche association.
- **GVS** — Geneesmiddelenvergoedingssysteem (the outpatient pharmaceutical reimbursement system).
- **Health-RI** — national initiative for health-data research infrastructure.
- **IGJ** — Inspectie Gezondheidszorg en Jeugd (Health and Youth Care Inspectorate).
- **IZA** — Integraal Zorgakkoord (the multi-year sector pact 2022-2026 between VWS, ZN, providers and patients on reform priorities; the IZA replaces the Hoofdlijnenakkoorden of the 2010s).
- **Jeugdwet** — Youth Act (devolved youth-care to municipalities from 2015).
- **KNMG** — Koninklijke Nederlandse Maatschappij tot bevordering der Geneeskunst (Royal Dutch Medical Association).
- **KNMP** — Koninklijke Nederlandse Maatschappij ter bevordering der Pharmacie (Royal Dutch Pharmacists' Association).
- **LHV** — Landelijke Huisartsen Vereniging (National General Practitioners' Association).
- **MedMij** — the national framework for personal-health-record exchange.
- **NFU** — Nederlandse Federatie van Universitair Medische Centra (federation of UMCs).
- **Nictiz** — Nationaal ICT Instituut in de Zorg (the national digital-health competence centre).
- **NVZ** — Nederlandse Vereniging van Ziekenhuizen (Dutch hospital federation, excluding UMCs).
- **NZa** — Nederlandse Zorgautoriteit (Dutch Healthcare Authority, regulates tariffs, market conduct, and care access).
- **Passende zorg** — 'appropriate care', the umbrella reform framing used jointly by Zorginstituut and the IZA.
- **Patiëntenfederatie Nederland** — federation of patient organisations.
- **Rijksoverheid.nl** — central Dutch government portal (the canonical source for ministerial CVs).
- **RIVM** — Rijksinstituut voor Volksgezondheid en Milieu (National Institute for Public Health and the Environment).
- **UMC** — Universitair Medisch Centrum (academic medical centre; seven in the Netherlands plus the Princess Máxima Center).
- **V&VN** — Verpleegkundigen & Verzorgenden Nederland (Dutch nurses' and care workers' professional body).
- **VWS** — Volksgezondheid, Welzijn en Sport; the Ministry.
- **Wlz** — Wet langdurige zorg (Long-Term Care Act).
- **Wmo** — Wet maatschappelijke ondersteuning (Social Support Act; municipalities are the buyers).
- **ZBO** — Zelfstandig bestuursorgaan (independent administrative body; the legal form of NZa, Zorginstituut, CBG, and most regulators).
- **ZIN** — Zorginstituut Nederland (National Health Care Institute; defines the basic-insurance benefits package and HTA).
- **ZN** — Zorgverzekeraars Nederland (the association of health insurers).
- **Zorgkantoor** — regional purchasing office for Wlz care (one per Wlz region, operated by a designated insurer).
- **Zvw** — Zorgverzekeringswet (Health Insurance Act 2006, the statutory base of the current market model).

## 10. Worked example

This is the canonical shape of one person. Any new entry should match it field-for-field (omitting optional contact fields where not verifiable).

```yaml
      - Sophie Hermans (VVD):
          - Title: Minister van Volksgezondheid, Welzijn en Sport (Minister of Health, Welfare and Sport) (per 23 februari 2026)
          - Stakeholder engagement notes:
              - "Minister van VWS in het kabinet-Jetten, beëdigd 23 februari 2026; VVD; in het demissionaire kabinet-Schoof Minister van Klimaat en Groene Groei en viceminister-president; meer dan zeven jaar Tweede Kamerlid voor de VVD met portefeuille langdurige zorg en preventie."
              - "Treedt aan in een crisismandaat: IZA-uitvoering blijft achter op afspraken, GGZ-wachtlijsten en personeelstekorten in V&V dominant, en VWS-begroting onder druk vanwege landelijke financiële consolidatie na de val van het kabinet-Schoof in juni 2025."
              - "Mirjam Sterk (CDA) treedt aan VWS-zijde naast haar op (minister of staatssecretaris met aanpalend portefeuille — actualiteit verifiëren); de combinatie VVD-Hermans + CDA-Sterk is de definitieve VWS-bezetting van het kabinet-Jetten."
              - "Hook: IZA-uitvoering, GGZ-toegang, personeel V&V, passende zorg en preventie landen; vendor pitches die de zorgverzekeraars en de NZa als routering negeren landen niet."
          - Tone advice:
              - "Open met IZA-uitvoering, passende zorg en arbeidsmarkt — dit zijn de centrale frames van het kabinet-Jetten op VWS en sluiten aan op Hermans' Kamerverleden over langdurige zorg en preventie."
              - "Niet pitchen alsof VWS direct kan inkopen — Hermans zal door verwijzen naar ZN, NZa en Zorginstituut; centralistische framings worden expliciet teruggewezen."
```

## 11. Out-of-band notes

Some organisation blocks in the YAML contain a non-person entry such as:

```yaml
      - Notes on Ministerie van VWS:
          - Status: ...
          - Implication: ...
```

These are permitted only where they explain why a role is *not* listed (e.g. a Staatssecretaris portefeuille not yet announced; a Directeur-Generaal in transitie) and should be removed once a named person can be added. They do not need `Tone advice`.

## 12. Open questions

These are known gaps to track and resolve:

- The substantive portefeuille and exact title of Mirjam Sterk (CDA) at VWS in the Jetten cabinet (Minister voor Medische Zorg, Staatssecretaris Langdurige Zorg en Sport, or other).
- Named Directeur-Generaal Volksgezondheid, Directeur-Generaal Curatieve Zorg, Directeur-Generaal Langdurige Zorg, Secretaris-Generaal VWS under the Jetten cabinet with currency verified to within six months.
- Named Voorzitter Raad van Bestuur of Zorgverzekeraars Nederland (ZN) and of the four large zorgverzekeraars (Achmea Zilveren Kruis, CZ, Menzis, VGZ) with currency verified.
- Named Voorzitter Raad van Bestuur of NVZ, NFU, ActiZ, VGN, de Nederlandse ggz, InEen, and the Patiëntenfederatie Nederland with currency verified.
- Named Voorzitter of the LHV, KNMG, KNMP, FMS and V&VN with currency verified.
- Voorzitter and ondervoorzitters of the Tweede Kamer vaste commissie voor Volksgezondheid, Welzijn en Sport in the post-October-2025 Kamer, and the woordvoerders zorg of the major coalition and opposition parties.
- Named Directeur Centrum Infectieziektebestrijding (CIb) inside RIVM under the new Directeur-Generaal Isabel Arends after Menno de Jong's term, and named directors of the Centrum Gezondheidsbescherming and Centrum Volksgezondheid en Zorg.
- Named Voorzitter Raad van Bestuur of Nictiz, MedMij and Health-RI with currency verified.

Each open question should be closed by editing this spec and the YAML in the same commit when resolved.
