# spec.md — `leaders.yml`

Single source of truth for the structure, semantics, and update rules of `leaders.yml` for the German Gesundheitswesen. Treat this document as the canonical specification: the YAML must conform to it; if the YAML and this spec disagree, the spec wins and the YAML is fixed.

## 1. Purpose

`leaders.yml` is an engagement register of named individuals in and around the German Gesundheitswesen. Each entry exists so that a reader (typically inside the Bundesministerium für Gesundheit (BMG), a federal institute, a Land health ministry, a statutory body of joint self-administration (gemeinsame Selbstverwaltung), or an academic-medical body) can decide:

1. **Who to engage** for a given digital/transformation/policy topic.
2. **How to engage them** — the angle that lands and the angle that fails.
3. **Where to engage them** — which public channels they actually use.

It is not a phone book, not a CRM, and not a comms list. Entries that do not directly serve engagement decision-making are out of scope.

The German Gesundheitswesen is structurally a Bismarckian social-insurance model embedded in a federal state. The Bundesministerium für Gesundheit (BMG) sets policy and the statutory framework (SGB V — Gesetzliche Krankenversicherung; SGB XI — Pflegeversicherung). The sixteen Länder retain hospital-planning, public-health and supervision powers. Federal institutes (RKI, BfArM, PEI, BZgA / BIPAM, BIfG) execute statutory tasks under BMG supervision. The gemeinsame Selbstverwaltung — the joint self-administration of statutory health insurance (GKV) and providers — operates through the Gemeinsamer Bundesausschuss (G-BA), the GKV-Spitzenverband, the Kassenärztliche Bundesvereinigung (KBV), the Kassenzahnärztliche Bundesvereinigung (KZBV), and the Deutsche Krankenhausgesellschaft (DKG); it makes the bulk of operational decisions on benefits, prices and quality. This makes the German health system unusually decentralised at the decision-making layer even where it appears centralised at the legislative layer.

## 2. Scope

**In scope:**
- Bundesregierung: Bundeskanzler, Bundesgesundheitsminister/in, Parlamentarische Staatssekretäre and Beamtete Staatssekretäre at BMG, Leiter/in der Abteilung Gesundheitsversorgung, Pflegeversicherung, Prävention and Digitalisierung at BMG.
- Federal institutes (Bundesinstitute) under BMG supervision: Robert Koch-Institut (RKI; public health and infectious diseases); Paul-Ehrlich-Institut (PEI; vaccines, biologics, blood and tissue products); Bundesinstitut für Arzneimittel und Medizinprodukte (BfArM; medicines and devices regulator); Bundeszentrale für gesundheitliche Aufklärung (BZgA) / Bundesinstitut für Öffentliche Gesundheit (BIPAM); Bundesinstitut für Risikobewertung (BfR) where the brief touches food and consumer-product safety; Deutsches Institut für Medizinische Dokumentation und Information (DIMDI) and successor digital institute BIfG (Bundesinstitut für Gesundheitsdatennutzung) where the brief is health data.
- Gemeinsame Selbstverwaltung: Gemeinsamer Bundesausschuss (G-BA — Vorsitzender, unparteiische Mitglieder); GKV-Spitzenverband (Vorstandsvorsitzende/r, Vorstandsmitglieder); Kassenärztliche Bundesvereinigung (KBV — Vorstandsvorsitzende/r and Vorstandsmitglieder); Kassenzahnärztliche Bundesvereinigung (KZBV); Deutsche Krankenhausgesellschaft (DKG — Präsident/in, Vorstandsvorsitzende/r); Medizinischer Dienst Bund (MD Bund).
- Sixteen Länder health ministries: Gesundheitsminister/in or Gesundheitssenator/in of each Bundesland, particularly the larger Länder (Bayern, Baden-Württemberg, Nordrhein-Westfalen, Niedersachsen, Hessen, Berlin, Hamburg, Sachsen).
- Federal academic and professional bodies: Bundesärztekammer (BÄK — Präsident/in); Deutscher Pflegerat; Bundesvereinigung Deutscher Apothekerverbände (ABDA); Bundeszahnärztekammer (BZÄK); Verband der Universitätsklinika Deutschlands (VUD).
- Bundestag committee leadership for health: Vorsitz, stellvertretender Vorsitz, Obleute (party spokespeople) of the Bundestag Gesundheitsausschuss; Vorsitz of the Bundestag Ausschuss für Familie, Senioren, Frauen und Jugend where the brief touches care of the elderly.
- Statutory and oversight bodies: Bundesrechnungshof where directly relevant to health; Bundesbeauftragte für den Datenschutz und die Informationsfreiheit (BfDI) on health-data matters; Patientenbeauftragte/r der Bundesregierung; Drogen- und Suchtbeauftragte/r der Bundesregierung.
- For each organisation: only stakeholders senior enough that engagement with them shapes decisions across the organisation (typically Minister, Staatssekretär, Präsident, Vorstandsvorsitzende/r, Vorsitz).

**Out of scope:**
- Operational staff below Abteilungsleitung (department head) level inside BMG and federal institutes, and below board level inside the Selbstverwaltung bodies.
- Suppliers, vendors, consultancies (their leaders may appear only when they hold a named role in a German public body, e.g. a Verwaltungsrat seat in a GKV body).
- Historical post-holders (unless explicitly flagged as predecessor for context).
- Other EU counterparts (unless they also hold a Germany-facing role).

## 3. Structure

The YAML is a single top-level mapping with one key.

```
Gesundheitswesen Deutschland stakeholders:
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

- Organisations are grouped by tier: Bundeskanzleramt and BMG (Minister, Staatssekretäre, Abteilungen) → federal institutes (RKI, PEI, BfArM, BZgA/BIPAM, BfR, BIfG) → gemeinsame Selbstverwaltung (G-BA, GKV-Spitzenverband, KBV, KZBV, DKG, MD Bund) → Bundestag Gesundheitsausschuss → Länder health ministries alphabetised (Baden-Württemberg, Bayern, Berlin, Brandenburg, Bremen, Hamburg, Hessen, Mecklenburg-Vorpommern, Niedersachsen, Nordrhein-Westfalen, Rheinland-Pfalz, Saarland, Sachsen, Sachsen-Anhalt, Schleswig-Holstein, Thüringen) → professional bodies (BÄK, Pflegerat, ABDA, BZÄK, VUD) → oversight bodies.
- Within an organisation, people are ordered: Minister / Präsident / Vorstandsvorsitzende/r → Staatssekretär/in / Stellvertretende/r Vorsitzende/r / Vorstandsmitglieder → Medical Director / Ärztliche/r Direktor/in → Other Directors / Geschäftsführer/in → Director of Digital → Director of Finance → Aufsichtsrat or Verwaltungsrat members where named.
- Programme leads and SROs follow their accountable director.

## 4. Field definitions

### 4.1 Organisation name

The key under which a person sits. Use the official name as the organisation publishes it. Acronyms in parentheses where helpful. Provide the German name first and the English in parentheses where the body is widely known by both (e.g. `Gemeinsamer Bundesausschuss (G-BA, Federal Joint Committee)`, `Robert Koch-Institut (RKI)`, `Bundesinstitut für Arzneimittel und Medizinprodukte (BfArM)`).

### 4.2 Person name

Include academic titles that the person actually uses publicly: `Dr.`, `Prof. Dr.`, `Prof. Dr. med.`, `Prof. Dr. rer. nat.`, `Dr. med.`, `Dr. rer. pol.`. Doctoral and habilitation titles are commonly used in German public life and are part of the canonical name in formal contexts. Party affiliation in parentheses for elected officials, using the canonical German abbreviations (`CDU`, `CSU`, `SPD`, `Bündnis 90/Die Grünen`, `FDP`, `Die Linke`, `AfD`, `BSW`, `Freie Wähler`). Match what appears on the organisation's official biography or the Bundesanzeiger.

### 4.3 `Title:` (required, one)

Current job title, verified to within the last six months. Use the German title and add an English gloss in parentheses where the German title is not self-evident to an English reader (e.g. `Bundesministerin für Gesundheit (Federal Minister of Health)`, `Unparteiischer Vorsitzender (Impartial Chairman)`). Include effective dates or status flags inline where helpful:
- `kommissarisch` (acting / interim) if not substantive.
- `(seit {Datum})` if newly in post.
- `(Aktualität prüfen)` if there is a known reason to re-check.

### 4.4 Contact fields (optional, zero or more, in this order)

Each appears at most once per person.

- `LinkedIn:` — full canonical URL. Skip if not verifiable.
- `X:` — full URL (`https://x.com/{handle}`). Skip if not verifiable, even if a handle was found.
- `Bluesky:` — full URL (`https://bsky.app/profile/{handle}`).
- `Mastodon:` — full URL (`https://{instance}/@{handle}`). German federal-public-administration Mastodon adoption is notable; many BMG / RKI / BfArM communications appear on bund.social.
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

Anti-pattern: generic CV bullets ("erfahrene Führungspersönlichkeit"). If the bullet would apply to any senior German federal health figure, it should not be in the register.

### 4.6 `Tone advice:` (required, exactly two strings)

Two bullets, each a YAML scalar wrapped in double quotes, ending in a full stop.

- **Bullet 1 — what to lead with.** The framing, vocabulary, or precedent that will land. May reference specific programmes, reports, or quotes from the engagement notes above (e.g. Krankenhausreform / KHVVG, Digital-Gesetz, Gesundheitsdatennutzungsgesetz, ePA für alle, AMNOG, GKV-Finanzstabilisierungsgesetz).
- **Bullet 2 — what to avoid.** A failure mode specific to this person — not generic. Should be derivable from their engagement notes (career, public statements, current pressures).

Tone advice is a derived field: it must be consistent with the engagement notes for the same person. If you change the notes materially, re-check the tone advice.

### 4.7 Other fields

Currently none. Do not add new field types without updating this spec first.

## 5. Provenance and dating

- All facts are anchored to a year (preferably a month or exact date) where helpful. "Amtsantritt {Monat Jahr}" beats "kürzlich ernannt".
- Convert relative dates to absolute when writing the YAML ("letztes Jahr" → `2025`).
- When a fact changes (e.g. a Präsident leaves), update the affected fields in the same commit; do not leave stale notes alongside a new title.
- The Merz government formed 6 May 2025 after the February 2025 Bundestag election and replaced the Scholz cabinet — treat any Ministry or BMG-supervised institute entry pre-dating that as warranting re-verification, and treat any Länder entry as warranting re-verification after each Landtag election.

## 6. Update workflow

1. **Identify the change** — a new appointment, departure, statement, or Bundesanzeiger publication.
2. **Verify against a public source** — official BMG / institute / Selbstverwaltungsbody page, Bundesanzeiger / Bundesgesetzblatt, named press article in Deutsches Ärzteblatt, Ärzte Zeitung, Pharmazeutische Zeitung, Handelsblatt, FAZ.
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
- **Speculation.** "Vermutlich aufgeschlossen für KI." If you cannot point to a public source for the disposition, omit it.
- **Vendor-flattering language.** Tone advice exists to make engagement realistic, not optimistic.
- **Stale role titles.** A person's role in this register must be their current substantive (or named acting) role, not their most famous previous one.
- **Duplicate entries.** A person belongs to one organisation. If they hold roles in two, choose the one most relevant for engagement and note the second in prose.
- **Mixing facts and aspirations.** Hooks describe what would land *given the person's stated priorities*, not what the writer wishes the person cared about.
- **Treating the Gesundheitswesen as state-led.** The bulk of operational health-system decisions are made by the gemeinsame Selbstverwaltung (G-BA, GKV-Spitzenverband, KBV, KZBV, DKG) inside the statutory framework set by BMG. Pitches that assume BMG is the operational counterparty for GKV-side decisions will fail.
- **Importing NHS or US framings unmodified.** The German system is plural insurer (110+ GKV funds, plus PKV), Selbstverwaltungs-led, and federal in hospital planning. Concepts like 'a single NHS' or 'one CMS' do not have a German analog.

## 9. Acronym and term glossary (selective)

Terms and acronyms used inside the YAML that readers may not know:

- **ABDA** — Bundesvereinigung Deutscher Apothekerverbände (federal pharmacists' association).
- **AMNOG** — Arzneimittelmarktneuordnungsgesetz (the early-benefit-assessment law that structures G-BA evaluation of new medicines).
- **BÄK** — Bundesärztekammer (federal medical chamber).
- **BfArM** — Bundesinstitut für Arzneimittel und Medizinprodukte (Federal Institute for Drugs and Medical Devices; the medicines and devices regulator).
- **BfDI** — Bundesbeauftragte/r für den Datenschutz und die Informationsfreiheit (federal data-protection commissioner).
- **BIfG** — Bundesinstitut für Gesundheitsdatennutzung (federal health-data-use institute).
- **BIPAM** — Bundesinstitut für Öffentliche Gesundheit (successor body to BZgA on public health).
- **BMG** — Bundesministerium für Gesundheit (Federal Ministry of Health).
- **BZgA** — Bundeszentrale für gesundheitliche Aufklärung (federal centre for health education).
- **CDU / CSU / SPD / Bündnis 90/Die Grünen / FDP / Die Linke / AfD / BSW / Freie Wähler** — German political parties relevant to health policy at federal and Länder level.
- **DiGA** — Digitale Gesundheitsanwendungen (the prescription-reimbursed digital health applications register at BfArM).
- **DKG** — Deutsche Krankenhausgesellschaft (German Hospital Federation).
- **DRG** — Diagnosis-Related Groups (the hospital-payment classification, German version: G-DRG).
- **ePA** — elektronische Patientenakte (electronic patient record, in 'ePA für alle' opt-out rollout from 2025).
- **G-BA** — Gemeinsamer Bundesausschuss (Federal Joint Committee; defines the benefits catalogue of the GKV and the quality framework).
- **gematik** — gematik GmbH; the national agency for the telematics infrastructure of the German health system.
- **GKV** — Gesetzliche Krankenversicherung (statutory health insurance, covering ~88% of the population through 95+ funds).
- **GKV-Spitzenverband** — the federal association of the GKV funds (central counterparty in joint self-administration).
- **GKV-FinStG** — GKV-Finanzstabilisierungsgesetz (the GKV financial stabilisation law).
- **IQTIG** — Institut für Qualitätssicherung und Transparenz im Gesundheitswesen (commissioned by G-BA for quality measurement).
- **IQWiG** — Institut für Qualität und Wirtschaftlichkeit im Gesundheitswesen (commissioned by G-BA for evidence assessment).
- **Kassenärztliche Bundesvereinigung (KBV)** — the federal body of the seventeen Land-level Kassenärztliche Vereinigungen of statutory-insurance physicians.
- **KHVVG** — Krankenhausversorgungsverbesserungsgesetz (the hospital reform law).
- **KZBV** — Kassenzahnärztliche Bundesvereinigung (the federal body of statutory-insurance dentists).
- **Land / Länder** — the sixteen German states, each with substantial autonomy in hospital planning, public health, and supervision.
- **MD Bund / MD** — Medizinischer Dienst (Bund) (the federal medical-review service of the GKV; spun off from the Medizinischer Dienst der Krankenversicherung in 2021).
- **PEI** — Paul-Ehrlich-Institut (the federal institute for vaccines and biomedicines).
- **PKV** — Private Krankenversicherung (private health insurance, covering ~11% of the population).
- **RKI** — Robert Koch-Institut (the federal public-health and infectious-diseases institute).
- **SGB V** — Fünftes Buch Sozialgesetzbuch (the statute that governs statutory health insurance).
- **SGB XI** — Elftes Buch Sozialgesetzbuch (the statute that governs long-term care insurance).
- **Unparteiische** — the impartial members of the G-BA, including the Vorsitzende/r.
- **VUD** — Verband der Universitätsklinika Deutschlands (federal university-hospitals' association).

## 10. Worked example

This is the canonical shape of one person. Any new entry should match it field-for-field (omitting optional contact fields where not verifiable).

```yaml
      - Nina Warken (CDU):
          - Title: Bundesministerin für Gesundheit (Federal Minister of Health) (seit 6. Mai 2025)
          - Stakeholder engagement notes:
              - "Bundesministerin für Gesundheit seit dem 6. Mai 2025 im Kabinett Merz; Volljuristin (Juristin / lawyer); zuvor parlamentarische Geschäftsführerin der Unionsfraktion seit 2021 und Generalsekretärin der CDU Baden-Württemberg seit 2023."
              - "Mit 45 Jahren und ohne klinische oder kassenärztliche Vorerfahrung das jüngste Mitglied im Merz-Kabinett auf einem Ressort, das traditionell ärztlich besetzt war (Lauterbach, Spahn) — politisch-juristischer Zugang statt sektorale Vorprägung."
              - "Im April 2026 angekündigt: zwölf Milliarden Euro Einsparungen über alle Leistungsbereiche des Gesundheitssystems hinweg im Jahr 2026 und rund zwanzig Milliarden Euro Einsparungen mit zusätzlichen Instrumenten für 2027 — die Krankenkassenreform und die GKV-Finanzstabilisierung sind die definierenden Mandatslinien."
              - "Krankenhausreform (KHVVG), GKV-Finanzstabilisierung, Pflegereform und die Einführung einer verbindlichen Primärversorgung sind die vier zentralen Gesetzgebungsstränge des Mandats; Pressestatement nach Beschluss der Krankenkassenreform mit Bundeskanzler Merz markiert die politische Linie."
              - "Hook: Krankenhausreform-Umsetzung, GKV-Konsolidierung, verbindliche Primärversorgung, Pflegereform und Digital-Gesetz-Folgegesetze landen; Pitches, die fiskalische Konsolidierung ignorieren, landen nicht."
          - Tone advice:
              - "Mit Krankenhausreform, GKV-Konsolidierung, Primärversorgung und Pflegereform einsteigen — das sind die definierenden Linien des Merz-Kabinetts auf dem Ressort."
              - "Nicht klinisch-fachlich pitchen, als wäre Warken eine SPD-geprägte ärztliche Ministerin — die Ressortlogik ist juristisch-fiskalisch und CDU-konsolidierend; Lauterbach-Stil-Framings werden zurückgewiesen."
```

## 11. Out-of-band notes

Some organisation blocks in the YAML contain a non-person entry such as:

```yaml
      - Notes on Gemeinsamer Bundesausschuss (G-BA):
          - Status: ...
          - Implication: ...
```

These are permitted only where they explain why a role is *not* listed (e.g. a Vorsitz with an announced early departure but no confirmed successor; an institute under restructuring) and should be removed once a named person can be added. They do not need `Tone advice`.

## 12. Open questions

These are known gaps to track and resolve:

- The substantive Unparteiische/r Vorsitzende/r des G-BA succession plan after Prof. Josef Hecken signalled in February 2026 a likely early departure for personal-family reasons (third term originally to run until 2030).
- Named Beamtete and Parlamentarische Staatssekretäre at BMG under Minister Warken with currency verified, and named Abteilungsleitungen for Gesundheitsversorgung, Pflegeversicherung, Prävention, Digitalisierung.
- The substantive Präsident/in of the Paul-Ehrlich-Institut (PEI) and of the BIPAM (Bundesinstitut für Öffentliche Gesundheit) with currency verified — both institutes have been in transition.
- Named Vorstand of GKV-Spitzenverband beyond Oliver Blatt as Vorstandsvorsitzender (seit 1. Juli 2025), and named Vorstandsmitglieder of KBV beyond Andreas Gassen, and named Präsident/in and Vorstand of DKG.
- Vorsitz, stellvertretender Vorsitz and Obleute of the Bundestag Gesundheitsausschuss in the 21. Wahlperiode following the February 2025 Bundestag election and Merz government formation.
- Named Gesundheitsminister/innen of the sixteen Länder with currency verified — significant turnover in 2024-2026 across Länder elections.
- Named Präsident/in of the Bundesärztekammer (BÄK), Präsident/in of the Bundeszahnärztekammer (BZÄK), and Präsident/in of ABDA with currency verified.
- Named Patientenbeauftragte/r and Drogen- und Suchtbeauftragte/r of the Bundesregierung under the Merz government.

Each open question should be closed by editing this spec and the YAML in the same commit when resolved.
