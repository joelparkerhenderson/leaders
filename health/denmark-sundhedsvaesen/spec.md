# spec.md — `leaders.yml`

Single source of truth for the structure, semantics, and update rules of `leaders.yml` for the Danish sundhedsvæsen. Treat this document as the canonical specification: the YAML must conform to it; if the YAML and this spec disagree, the spec wins and the YAML is fixed.

## 1. Purpose

`leaders.yml` is an engagement register of named individuals in and around the Danish sundhedsvæsen. Each entry exists so that a reader (typically inside Indenrigs- og Sundhedsministeriet, a Sundhedsministeriet styrelse, a region, a hospital, or an adjacent national body) can decide:

1. **Who to engage** for a given digital/transformation/policy topic.
2. **How to engage them** — the angle that lands and the angle that fails.
3. **Where to engage them** — which public channels they actually use.

It is not a phone book, not a CRM, and not a comms list. Entries that do not directly serve engagement decision-making are out of scope.

The Danish sundhedsvæsen is tax-funded and operationally split: the five regions (Region Hovedstaden, Region Sjælland, Region Syddanmark, Region Midtjylland, Region Nordjylland) run hospitals and pay general practitioners under the regional Praksisplan; 98 kommuner run elder care, home care, rehabilitation and parts of mental health; the state, through Sundhedsministeriet, Sundhedsstyrelsen, Lægemiddelstyrelsen, Statens Serum Institut (SSI) and Styrelsen for Patientsikkerhed, sets the framework, oversees quality and supervises licensing. The 2024 Sundhedsreform tightened the state's steering role over the regions' service planning. Danske Regioner is the political-employer organisation for the regions; KL is the equivalent for the kommuner.

## 2. Scope

**In scope:**
- Regering: Statsminister; Sundhedsminister (and Kirkeminister in the current Frederiksen III configuration); Indenrigsminister or Økonomi- og Indenrigsminister where relevant to health.
- Sundhedsministeriet and Indenrigs- og Sundhedsministeriet: Departementschef, Direktør for Sundhedsdepartementet, afdelingschefer.
- Statslige styrelser: Sundhedsstyrelsen (Direktør, Vicedirektør); Lægemiddelstyrelsen (Direktør); Statens Serum Institut (Direktør); Styrelsen for Patientsikkerhed (Direktør); Sundhedsdatastyrelsen / Digitaliseringsstyrelsen where the brief touches health; Datatilsynet on health-data matters.
- Regioner: Regionsrådsformand and Koncerndirektør (administrerende direktør) of each of the five regions; Sundhedsdirektør of each region.
- Danske Regioner: Bestyrelsesformand and Direktør.
- KL (Kommunernes Landsforening): Bestyrelsesformand and Direktør where the brief touches sundhedsområdet.
- Hospital tier of national significance: Rigshospitalet (København); Aarhus Universitetshospital; Odense Universitetshospital; Aalborg Universitetshospital; Sjællands Universitetshospital — administrerende direktør and lægefaglig direktør where the role is national-policy facing.
- Folketinget: Sundhedsudvalget formand and næstformand; party spokespeople (ordførere) on sundhed where they hold a national posture.
- Statutory and oversight bodies: Rigsrevisionen where directly relevant; Folketingets Ombudsmand where directly relevant; Det Etiske Råd; Patientombuddet; Klagenævnet for Lægemiddelreklame.
- Related sector bodies of national significance: Lægeforeningen (Danish Medical Association); Yngre Læger; Praktiserende Lægers Organisation (PLO); Dansk Sygeplejeråd (DSR); FOA (welfare and care union); Danmarks Apotekerforening; Dansk Selskab for Almen Medicin (DSAM); Lægevidenskabelige Selskaber (LVS).
- For each organisation: only stakeholders senior enough that engagement with them shapes decisions across the organisation.

**Out of scope:**
- Operational staff below kontorchef level inside ministry and styrelser, and below afdelingsledelse level inside regions and hospitals.
- Suppliers, vendors, consultancies.
- Historical post-holders.
- Other Nordic counterparts unless they hold a Denmark-facing role.

## 3. Structure

The YAML is a single top-level mapping with one key.

```
Danske sundhedsvæsen interessenter:
  - {Organisation}:
      - {Person}:
          - Title: ...
          - {optional contact fields}
          - Stakeholder engagement notes: [...]
          - Tone advice: [...]
```

### Indentation rules

Same as the wider register family — 2/6/10/14 spaces; no tabs; one newline between sibling entries.

### Ordering

Organisations grouped by tier: Regering → Sundhedsministeriet (Indenrigs- og Sundhedsministeriet under Frederiksen II; Sundhedsministeriet under Frederiksen III) → styrelser (Sundhedsstyrelsen, Lægemiddelstyrelsen, SSI, Styrelsen for Patientsikkerhed, Sundhedsdatastyrelsen) → Danske Regioner → 5 regioner (Hovedstaden, Sjælland, Syddanmark, Midtjylland, Nordjylland) → KL where relevant to sundhedsområdet → universitetshospitaler → Folketinget Sundhedsudvalget → professional bodies → oversight bodies.

Within an organisation: Minister / Direktør / Regionsrådsformand → vice / koncerndirektør → lægefaglig direktør / sundhedsdirektør → other directors → digitaliseringsdirektør → økonomidirektør.

## 4. Field definitions

### 4.1 Organisation name

Use the official Danish name with English in parentheses where the body is widely known by both (e.g. `Sundhedsstyrelsen (Danish Health Authority)`, `Statens Serum Institut (SSI)`).

### 4.2 Person name

Academic titles `Dr.`, `Prof.`, `dr.med.` where the person uses them publicly. Party affiliation in parentheses using canonical Danish abbreviations: `S` Socialdemokratiet, `V` Venstre, `M` Moderaterne, `K` Det Konservative Folkeparti, `RV` Radikale Venstre, `SF` Socialistisk Folkeparti, `EL` Enhedslisten, `DD` Danmarksdemokraterne, `LA` Liberal Alliance, `DF` Dansk Folkeparti, `NB` Nye Borgerlige, `ALT` Alternativet.

### 4.3 `Title:` (required, one)

Use the Danish title with English gloss where not self-evident. Status flags:
- `kst.` (konstitueret, acting) if not substantive.
- `(per {dato})` if newly in post.
- `(verificer)` if there is a known reason to re-check.

### 4.4 Contact fields (optional, zero or more)

`LinkedIn:`, `X:`, `Bluesky:`, `Mastodon:`, `Website:`, `GitHub:`, `Email:` — each at most once, only with public attribution. LinkedIn adoption is very high among Danish senior public-sector leaders and is usually the most reliable.

### 4.5 `Stakeholder engagement notes:` (3-7 bullets)

Career background, ownership, public statements, hook. Anti-pattern: generic CV.

### 4.6 `Tone advice:` (exactly 2 bullets)

What to lead with; what to avoid. Danish-language reform frames such as Sundhedsreformen 2024, Nære Sundhedsvæsen, Robusthedsplan, Akutaftale, Strategi for Personlig Medicin should be used where they fit.

### 4.7 Other fields

None.

## 5. Provenance and dating

- Anchor facts to year, month or exact date.
- The Mette Frederiksen III government formed 3 June 2026 (S, SF, M, RV) and Ida Auken (S) became Sundheds- og Kirkeminister on the same date. Treat any Ministerie entry pre-dating 3 June 2026 as warranting re-verification; the Frederiksen II/III transition shifted the brief from Indenrigs- og Sundhedsministeriet (Løhde) to Sundhedsministeriet (Auken) and Økonomi- og Indenrigsministeriet (Pia Olsen Dyhr).

## 6. Update workflow

1. Identify the change.
2. Verify against stm.dk, sum.dk, ism.dk, sst.dk, ssi.dk, lmst.dk, regioner.dk, kl.dk, Folketinget.dk, Politiken, Berlingske, Altinget, Dagens Medicin, Ugeskrift for Læger.
3. Apply minimum diff; re-check Tone advice.
4. Confirm structure.
5. Re-validate cross-references.

## 7. Invariants

Standard register invariants apply — one Title, one engagement notes block, one Tone advice block (exactly two bullets); no `?` placeholders; one-line quoted strings; HTTPS URLs; one organisation per person; unique names within an organisation.

## 8. Anti-patterns

- Padding; speculation; vendor-flattering language; stale role titles; duplicate entries; mixing facts and aspirations.
- Treating regionerne as administrative subunits — they are directly elected with own budgets, own collective agreements, and own digital infrastructure decisions (Sundhedsplatformen vs MidtEPJ vs NordEPJ).
- Importing NHS framings unmodified — Denmark has tax-funded universal coverage like the NHS but a regional self-governance model with directly elected Regionsråd that is structurally closer to Sweden than to NHS England.

## 9. Acronym and term glossary (selective)

- **Datatilsynet** — Danish Data Protection Authority.
- **Danske Regioner** — political-employer organisation for the five regions.
- **DSR** — Dansk Sygeplejeråd (Danish Nurses' Organisation).
- **EPJ** — Elektronisk patientjournal (electronic patient record); used regionally (Sundhedsplatformen, MidtEPJ, NordEPJ, EPJ Syd).
- **FMK** — Det Fælles Medicinkort (the national shared medication card).
- **Folketinget Sundhedsudvalget** — Folketing standing committee on health.
- **FOA** — Fag og Arbejde (welfare-and-care union).
- **KL** — Kommunernes Landsforening (Local Government Denmark).
- **Lægeforeningen** — Danish Medical Association.
- **Lægemiddelstyrelsen** — Danish Medicines Agency.
- **MedCom** — national communication coordinator for health-IT (interoperability between sectors).
- **Nære Sundhedsvæsen** — long-running policy frame for shifting activity to municipalities and primary care.
- **PLO** — Praktiserende Lægers Organisation (general-practitioner trade union).
- **Regionsråd** — directly elected regional council (one per region).
- **Robusthedsplan** — the multi-billion-DKK plan to strengthen the health workforce and acute services (2022 onwards).
- **Statens Serum Institut (SSI)** — national infectious-disease and biomedical institute.
- **Sundhedsdatastyrelsen** — Danish Health Data Authority.
- **Sundhedsplatformen** — the Epic-based EPJ used by Region Hovedstaden and Region Sjælland.
- **Sundhedsreformen** — the 2024 structural health reform tightening state steering of the regions.
- **Sundhedsstyrelsen** — Danish Health Authority (sets norms, guidelines, capacity planning, vaccinations).
- **Styrelsen for Patientsikkerhed** — Danish Patient Safety Authority (supervision, licensing, complaints).
- **WHO Europe** — Søren Brostrøm, the previous Sundhedsstyrelsen Direktør, moved to a senior advisor role at WHO in 2023 — useful context for the system's external networks.

## 10. Worked example

```yaml
      - Ida Auken (S):
          - Title: Sundheds- og Kirkeminister (Minister of Health and Ecclesiastical Affairs) (per 3. juni 2026)
          - Stakeholder engagement notes:
              - "Sundheds- og kirkeminister i regeringen Mette Frederiksen III fra 3. juni 2026 (S, SF, M, RV — mindretalsregering); overtog sundhedsområdet fra Sophie Løhde (V) ved ministerial overdragelse i Indenrigs- og Sundhedsministeriet."
              - "Teolog og præst af uddannelse; medlem af Folketinget siden 2007; miljøminister i Helle Thorning-Schmidts regering 2011-2014 for SF; skiftede partitilhørsforhold fra SF over Radikale Venstre til Socialdemokratiet i 2021 — det fælles træk er en grøn-progressiv-pragmatisk linje."
              - "Tiltræder på ressort efter Sophie Løhde's tre-årige periode i Indenrigs- og Sundhedsministeriet (2022-2026) under Frederiksen II; Sundhedsreformen 2024 og Robusthedsplanen er den arvede ramme."
              - "Hook: Sundhedsreformens videre implementering, Nære Sundhedsvæsen, sundhedspersonalets vilkår, klimasundhed og grøn omstilling i sundhedsvæsenet lander; pitches der ignorerer det regionale selvstyre lander ikke."
          - Tone advice:
              - "Åbn med Sundhedsreformens implementering, Nære Sundhedsvæsen og sundhedspersonalets vilkår — disse er regeringens overordnede linjer på sundhedsområdet."
              - "Pitch ikke som om Sundhedsministeriet kan diktere regionale drift — Auken vil henvise til Danske Regioner og regionsrådsformændene; centralistiske framings afvises."
```

## 11. Out-of-band notes

Used where a role is unfilled or in interim transition. Do not need Tone advice.

## 12. Open questions

- Named Sundhedsdirektør or Departementschef of the new Sundhedsministeriet under Auken following the 3 June 2026 portfolio split between Sundhedsministeriet and Økonomi- og Indenrigsministeriet.
- Named Direktør of Lægemiddelstyrelsen, Statens Serum Institut, Styrelsen for Patientsikkerhed, and Sundhedsdatastyrelsen with currency verified.
- Named Regionsrådsformand and Koncerndirektør of each of the five regioner under the current valgperiode.
- Named Direktør of Danske Regioner and Bestyrelsesformand of Danske Regioner.
- Named Sundhedsudvalget formand and næstformand in the current Folketing valgperiode following the Frederiksen II/III transition.
- Named Formand of Lægeforeningen, PLO, Yngre Læger, DSR, FOA and Danmarks Apotekerforening with currency verified.
- Named administrerende direktør of Rigshospitalet, Aarhus Universitetshospital, Odense Universitetshospital, Aalborg Universitetshospital and Sjællands Universitetshospital with currency verified.
