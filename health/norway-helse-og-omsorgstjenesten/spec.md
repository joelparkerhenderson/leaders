# spec.md — `leaders.yml`

Single source of truth for the structure, semantics, and update rules of `leaders.yml` for the Norwegian helse- og omsorgstjenesten. Treat this document as the canonical specification: the YAML must conform to it; if the YAML and this spec disagree, the spec wins and the YAML is fixed.

## 1. Purpose

`leaders.yml` is an engagement register of named individuals in and around the Norwegian helse- og omsorgstjenesten. Each entry exists so that a reader (typically inside Helse- og omsorgsdepartementet (HOD), a national directorate or institute, a regional health authority, a municipal helse- og omsorgstjeneste, or an adjacent national body) can decide:

1. **Who to engage** for a given digital/transformation/policy topic.
2. **How to engage them** — the angle that lands and the angle that fails.
3. **Where to engage them** — which public channels they actually use.

It is not a phone book, not a CRM, and not a comms list. Entries that do not directly serve engagement decision-making are out of scope.

The Norwegian helse- og omsorgstjenesten is tax-funded and split between two governance tiers. Specialist (hospital) care is delivered by four state-owned regionale helseforetak (RHF) — Helse Sør-Øst, Helse Vest, Helse Midt-Norge, Helse Nord — each owning local helseforetak (HF) that run the hospitals. Primary, municipal-health and elderly-care are delivered by the 357 kommuner. HOD steers; Helsedirektoratet sets norms and runs national programmes; Folkehelseinstituttet (FHI) provides surveillance and evidence; the medicines agency DMP (previously Statens legemiddelverk) regulates medicines; Statens helsetilsyn supervises; Direktoratet for medisinske produkter handles devices; Direktoratet for e-helse and Norsk helsenett run national digital infrastructure. KS is the political-employer organisation of the kommuner.

## 2. Scope

**In scope:**
- Regjering: Statsminister; Helse- og omsorgsminister; Eldre- og folkehelseminister or other split portfolio when filled.
- Helse- og omsorgsdepartementet (HOD): Departementsråd, ekspedisjonssjefer of the major avdelinger (Sykehus, Spesialisthelsetjeneste, Folkehelse, Kommunale tjenester, Omsorg, e-helse og digitalisering).
- National directorates and institutes: Helsedirektoratet (Helsedirektør, divisjonsdirektører); Folkehelseinstituttet (FHI, direktør); Direktoratet for medisinske produkter (DMP, direktør — successor body to Statens legemiddelverk from 2024); Statens helsetilsyn (direktør); Direktoratet for e-helse (direktør); Norsk helsenett SF (administrerende direktør); Helseplattformen AS leadership where the role is national-policy facing.
- Regionale helseforetak: Styreleder and Administrerende direktør of Helse Sør-Øst RHF, Helse Vest RHF, Helse Midt-Norge RHF, Helse Nord RHF.
- University hospital tier: Administrerende direktør of Oslo universitetssykehus HF (Norway's largest hospital), Helse Bergen HF (Haukeland), St. Olavs hospital HF (Trondheim), Universitetssykehuset Nord-Norge HF (Tromsø); Akershus universitetssykehus HF.
- KS (Kommunesektorens organisasjon): Styreleder and Administrerende direktør where the brief touches helse- og omsorg.
- Stortinget: Helse- og omsorgskomiteen leder and nestleder; party spokespeople (helsepolitiske talspersoner).
- Statutory and oversight bodies: Riksrevisjonen where directly relevant; Sivilombudsmannen where directly relevant; Datatilsynet on health-data matters; Pasient- og brukerombudet (national coordinator).
- Related sector bodies of national significance: Den norske legeforening (Norwegian Medical Association); Norsk Sykepleierforbund (NSF); Fagforbundet (welfare and care union); Apotekerforeningen; Norsk Farmaceutisk Selskap; Allmennlegeforeningen and Norsk forening for allmennmedisin (NFA).
- For each organisation: only stakeholders senior enough that engagement with them shapes decisions across the organisation.

**Out of scope:**
- Operational staff below ekspedisjonssjef level inside HOD, below divisjonsdirektør inside Helsedirektoratet, and below klinikkleder level inside hospitals.
- Suppliers, vendors, consultancies.
- Historical post-holders.
- Other Nordic counterparts unless they hold a Norway-facing role.

## 3. Structure

The YAML is a single top-level mapping with one key.

```
Norske helse- og omsorgstjeneste interessenter:
  - {Organisation}:
      - {Person}:
          - Title: ...
          - {optional contact fields}
          - Stakeholder engagement notes: [...]
          - Tone advice: [...]
```

### Indentation rules

Standard 2/6/10/14 spaces; no tabs; one newline between sibling entries.

### Ordering

Organisations grouped by tier: Regjering → HOD → national directorates and institutes (Helsedirektoratet, FHI, DMP, Statens helsetilsyn, Direktoratet for e-helse, Norsk helsenett) → 4 RHF (Helse Sør-Øst, Helse Vest, Helse Midt-Norge, Helse Nord) → university hospital HF (OUS, Helse Bergen, St. Olavs, UNN, Ahus) → KS where brief touches helse → Stortinget Helse- og omsorgskomiteen → professional bodies → oversight bodies.

Within an organisation: Minister / Direktør / Styreleder / Administrerende direktør → vice / nestleder → fagdirektør / medisinsk direktør → other direktører → digitaliseringsdirektør → økonomidirektør.

## 4. Field definitions

### 4.1 Organisation name

Use the official Norwegian name with English in parentheses where the body is widely known by both (e.g. `Helsedirektoratet (Norwegian Directorate of Health)`, `Folkehelseinstituttet (FHI, Norwegian Institute of Public Health)`, `Direktoratet for medisinske produkter (DMP, Norwegian Medical Products Agency)`).

### 4.2 Person name

Academic titles `Dr.`, `Prof.`, `dr.med.` where the person uses them publicly. Party affiliation in parentheses using canonical Norwegian abbreviations: `Ap` Arbeiderpartiet, `H` Høyre, `Sp` Senterpartiet, `FrP` Fremskrittspartiet, `SV` Sosialistisk Venstreparti, `V` Venstre, `KrF` Kristelig Folkeparti, `R` Rødt, `MDG` Miljøpartiet De Grønne, `INP` Industri- og næringspartiet.

### 4.3 `Title:` (required, one)

Norwegian title with English gloss where not self-evident. Status flags:
- `konstituert` (acting) if not substantive.
- `(fra {dato})` if newly in post.
- `(verifiser aktualitet)` if there is a known reason to re-check.

### 4.4 Contact fields (optional, zero or more)

`LinkedIn:`, `X:`, `Bluesky:`, `Mastodon:`, `Website:`, `GitHub:`, `Email:` — each at most once, only with public attribution.

### 4.5 `Stakeholder engagement notes:` (3-7 bullets)

Career background, ownership, public statements, hook. Anti-pattern: generic CV.

### 4.6 `Tone advice:` (exactly 2 bullets)

What to lead with; what to avoid. Norwegian-language reform frames such as Nasjonal helse- og samhandlingsplan, Helsefellesskap, Samhandlingsreformen, pakkeforløp, fastlegeordningen-krisen, sykehusplan should be used where they fit.

### 4.7 Other fields

None.

## 5. Provenance and dating

- Anchor facts to year, month or exact date.
- The Støre-regjeringen continues as an Ap minority government after the 8 September 2025 Stortingsvalg where the red-green bloc retained a majority (Ap up to 53 seats). A minor cabinet reshuffle 16 September 2025 affected labour-and-inclusion and local-government; helse- og omsorgsministeren Jan Christian Vestre (Ap) was retained. Treat any Regjering entry pre-dating 16 September 2025 as warranting re-verification on the broader portfolio.

## 6. Update workflow

1. Identify the change.
2. Verify against regjeringen.no, helsedirektoratet.no, fhi.no, dmp.no, helsetilsynet.no, e-helse.no, the four RHF sites, KS.no, stortinget.no, Aftenposten, Dagens Medisin, Dagens Næringsliv, Altinget.no.
3. Apply minimum diff; re-check Tone advice.
4. Confirm structure.
5. Re-validate cross-references.

## 7. Invariants

Standard register invariants apply.

## 8. Anti-patterns

- Padding; speculation; vendor-flattering language; stale role titles; duplicate entries; mixing facts and aspirations.
- Treating the four RHF as administrative subunits of HOD — they are state-owned helseforetak with own boards, own budgets and own digital-investment authority.
- Treating Norwegian municipal health as small-scale — Bergen, Trondheim, Stavanger and Oslo each carry primary-care, elderly-care and addiction-services budgets larger than many small national systems.
- Importing NHS framings unmodified — Norway has the RHF/HF model and a parallel kommunal-helse tier; concepts like NHS England ICBs or US CMS do not have a Norwegian analog.

## 9. Acronym and term glossary (selective)

- **Akson / Felles kommunal journal** — the planned shared municipal medical record (politically contested; status varies by year).
- **DIPS** — the dominant Norwegian hospital EPR vendor (DIPS Arena).
- **DMP** — Direktoratet for medisinske produkter; the medicines and devices agency, successor to Statens legemiddelverk from 2024.
- **Direktoratet for e-helse** — Norwegian Directorate for e-Health.
- **Fastlegeordningen** — the contract-based GP / family-doctor scheme; in continuing crisis since the early 2020s.
- **FHI** — Folkehelseinstituttet; Norwegian Institute of Public Health.
- **Helsedirektoratet** — Norwegian Directorate of Health.
- **Helsefellesskap** — formal collaboration platform between HF and kommuner introduced as part of Nasjonal helse- og samhandlingsplan.
- **Helseforetak (HF)** — health enterprise; runs hospitals at local level under an RHF parent.
- **Helse Sør-Øst RHF / Helse Vest RHF / Helse Midt-Norge RHF / Helse Nord RHF** — the four regional health authorities.
- **Helseplattformen** — the Epic-based EPR for Helse Midt-Norge RHF.
- **HOD** — Helse- og omsorgsdepartementet; Ministry of Health and Care Services.
- **KS** — Kommunesektorens organisasjon; Norwegian Association of Local and Regional Authorities.
- **NHN / Norsk helsenett SF** — Norwegian Health Network state enterprise; runs the national digital infrastructure.
- **NSF** — Norsk Sykepleierforbund (Norwegian Nurses' Organisation).
- **OUS** — Oslo universitetssykehus HF.
- **Pakkeforløp** — cancer (and now mental-health) care pathway model.
- **Pasient- og brukerombudet** — patient and user ombudsman, one per county plus national coordinator.
- **RHF** — regionalt helseforetak; regional health authority.
- **Samhandlingsreformen** — the 2012 collaboration reform shifting activity to municipalities.
- **Sivilombudsmannen / Sivilombudet** — Parliamentary Ombudsman.
- **St. Olavs hospital HF** — Trondheim university hospital.
- **Statens helsetilsyn** — Norwegian Board of Health Supervision.
- **UNN** — Universitetssykehuset Nord-Norge HF, Tromsø.

## 10. Worked example

```yaml
      - Jan Christian Vestre (Ap):
          - Title: Helse- og omsorgsminister (Minister of Health and Care Services) (fra 19. april 2024)
          - Stakeholder engagement notes:
              - "Helse- og omsorgsminister fra 19. april 2024 etter Ingvild Kjerkols avgang (forskningsetisk sak); beholdt portføljen i den mindre regjeringsomrokeringen 16. september 2025 etter den rødgrønne blokkens valgseier 8. september 2025."
              - "Født 1986 i Stavanger; tidligere næringsminister i samme regjering fra 2021; gründerprofil og stifter av møbelvirksomheten Vestre AS (slottsparkmøbler) — uvanlig entreprenørbakgrunn for en Ap-helseminister."
              - "Arvet en helsesektor i langvarig fastlegekrise, vedvarende sykehusøkonomisk press og en uavklart digital infrastruktur (Helseplattformen-utfordringer i Midt-Norge); Nasjonal helse- og samhandlingsplan er rammen for hans periode."
              - "Hook: fastlegeordningen, sykehusøkonomi, Helsefellesskap, samhandling kommune-HF, og industri-vekslende perspektiv på helsetjenestens innkjøpsmakt og verdiskaping lander; pitches som ignorerer fastlegekrisen lander ikke."
          - Tone advice:
              - "Åpn med fastlegeordningen, sykehusøkonomi, Helsefellesskap og industriell verdiskaping — disse er hans politiske kjernelinjer og hans gründerblikk."
              - "Pitch ikke som om helsesystemet er en sentralt styrt enhet — Vestre vil henvise til RHF-styrene og kommunene; sentralistiske framings avvises."
```

## 11. Out-of-band notes

Used where a role is unfilled or in interim transition. Do not need Tone advice.

## 12. Open questions

- Named ekspedisjonssjefer of HOD for Sykehus, Folkehelse, Kommunale tjenester, e-helse og digitalisering with currency verified.
- Named Direktør of DMP (Direktoratet for medisinske produkter), Statens helsetilsyn, Direktoratet for e-helse, and Administrerende direktør of Norsk helsenett SF with currency verified.
- Named Styreleder and Administrerende direktør of each of the four RHF (Helse Sør-Øst, Helse Vest, Helse Midt-Norge, Helse Nord) under the current oppnevningsperiode.
- Named Administrerende direktør of OUS, Helse Bergen HF, St. Olavs hospital HF, UNN HF, and Ahus HF with currency verified.
- Leder and nestleder of Stortinget Helse- og omsorgskomiteen in the 2025-2029 valgperiode.
- Named President of Den norske legeforening, Forbundsleder of Norsk Sykepleierforbund, and Leder of Allmennlegeforeningen with currency verified.
