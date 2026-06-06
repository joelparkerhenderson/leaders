# spec.md — `leaders.yml`

Single source of truth for the structure, semantics, and update rules of `leaders.yml` for Finnish social and health care (sosiaali- ja terveydenhuolto). Treat this document as the canonical specification: the YAML must conform to it; if the YAML and this spec disagree, the spec wins and the YAML is fixed.

## 1. Purpose

`leaders.yml` is an engagement register of named individuals in and around Finnish sosiaali- ja terveydenhuolto. Each entry exists so that a reader (typically inside the Sosiaali- ja terveysministeriö (STM), a state agency, a hyvinvointialue (wellbeing services county), a university hospital, or an adjacent national body) can decide:

1. **Who to engage** for a given digital/transformation/policy topic.
2. **How to engage them** — the angle that lands and the angle that fails.
3. **Where to engage them** — which public channels they actually use.

It is not a phone book, not a CRM, and not a comms list. Entries that do not directly serve engagement decision-making are out of scope.

The Finnish system underwent a structural reform on 1 January 2023 (sote-uudistus): responsibility for social and health services and rescue services was transferred from 309 municipalities and joint authorities to 21 newly created hyvinvointialueet (wellbeing services counties) plus the City of Helsinki and the HUS-yhtymä (Helsinki and Uusimaa Hospital District). The state (STM) sets the framework, funds the hyvinvointialueet directly from the state budget, and steers them through the THL knowledge function and the Valvira / aluehallintovirastot oversight. Kela administers national insurance, the Sairausvakuutus (sickness insurance), and the digital Kanta services. The five university hospital regions (yliopistollinen sairaala) provide the demanding-care backbone.

## 2. Scope

**In scope:**
- Valtioneuvosto: Pääministeri (Prime Minister); Sosiaali- ja terveysministeri (Minister of Social Affairs and Health); other STM portfolio ministers when split (perhe- ja peruspalveluministeri / minister of family affairs and basic services; sosiaaliturvaministeri / minister of social security).
- STM administration: Kansliapäällikkö (Permanent Secretary); osastopäälliköt of Hyvinvointi- ja palveluosasto, Sosiaaliturvaosasto, Turvallisuus- ja terveysosasto, Työ- ja tasa-arvo-osasto; Strateginen johtaja for sosiaali- ja terveysuudistus.
- State agencies under STM: Terveyden ja hyvinvoinnin laitos (THL); Lääkealan turvallisuus- ja kehittämiskeskus (Fimea); Sosiaali- ja terveysalan lupa- ja valvontavirasto (Valvira); Säteilyturvakeskus (STUK); Työterveyslaitos (TTL).
- Kela (Kansaneläkelaitos): Pääjohtaja, johtoryhmä, Kanta-palvelujen johtaja.
- Hyvinvointialueet: aluehallituksen puheenjohtaja and hyvinvointialuejohtaja of the 21 hyvinvointialueet plus the City of Helsinki sosiaali-, terveys- ja pelastustoimialan toimialajohtaja and the HUS-yhtymä johtaja.
- University hospitals (yliopistollinen sairaala): HUS, TYKS (Turku), TAYS (Tampere), KYS (Kuopio), OYS (Oulu) — johtaja and ylilääkäri where the role is national-policy facing.
- Eduskunta: Sosiaali- ja terveysvaliokunta puheenjohtaja and varapuheenjohtaja; party group health spokespeople (sote-vastaavat) where they hold a national posture.
- Statutory and oversight bodies of relevance to health: Valtiontalouden tarkastusvirasto (VTV) where directly relevant; Eduskunnan oikeusasiamies and Oikeuskansleri where directly relevant to health; Tietosuojavaltuutettu on health-data matters.
- Related sector bodies of national significance: Suomen Lääkäriliitto (Finnish Medical Association); Tehy (the large nursing union); SuPer (practical nurses' union); Suomen sairaanhoitajat; Apteekkariliitto; KT Kuntatyönantajat for the workforce-collective tier where it bears on the hyvinvointialueet; Hyvinvointialueyhtiö Hyvil (the wellbeing-services-counties joint company).
- For each organisation: only stakeholders senior enough that engagement with them shapes decisions across the organisation (typically Minister, kansliapäällikkö, pääjohtaja, hyvinvointialuejohtaja, university hospital director, professional-union chair).

**Out of scope:**
- Operational staff below osastopäällikkö level inside STM and state agencies, and below directorate level inside hyvinvointialueet and university hospitals.
- Suppliers, vendors, consultancies.
- Historical post-holders (unless explicitly flagged as predecessor for context).
- Other Nordic counterparts unless they also hold a Finland-facing role.

## 3. Structure

The YAML is a single top-level mapping with one key.

```
Suomen sosiaali- ja terveydenhuollon sidosryhmät:
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

- Organisations are grouped by tier: Valtioneuvosto and STM → state agencies (THL, Fimea, Valvira, STUK, TTL) → Kela → hyvinvointialueet in the order Uusimaa-area first (Helsinki, HUS, Itä-Uusimaa, Keski-Uusimaa, Länsi-Uusimaa, Vantaa-Kerava) then alphabetical → university hospitals → Eduskunta sosiaali- ja terveysvaliokunta → professional bodies → oversight bodies.
- Within an organisation, people are ordered: Minister / kansliapäällikkö / pääjohtaja / hyvinvointialuejohtaja → deputy / vice → ylilääkäri (chief medical officer) → johtava ylihoitaja (chief nursing officer) → other osastopäälliköt → digital director → finance director.

## 4. Field definitions

### 4.1 Organisation name

Use the official Finnish name with English in parentheses where the body is widely known by both (e.g. `Terveyden ja hyvinvoinnin laitos (THL, Finnish Institute for Health and Welfare)`, `Lääkealan turvallisuus- ja kehittämiskeskus (Fimea, Finnish Medicines Agency)`, `Hyvinvointialueet (wellbeing services counties)`).

### 4.2 Person name

Academic titles such as `Dr.`, `Prof.`, `LT` (lääketieteen tohtori, MD), `THM`, `FT` are used in formal contexts. Party affiliation in parentheses using canonical Finnish abbreviations (`Kok.` Kokoomus, `PS` Perussuomalaiset, `SDP`, `KD` Kristillisdemokraatit, `RKP/SFP` Ruotsalainen kansanpuolue, `Kesk.` Keskusta, `Vihr.` Vihreät, `Vas.` Vasemmistoliitto, `Liik.` Liike Nyt).

### 4.3 `Title:` (required, one)

Use the Finnish title with English gloss where not self-evident. Status flags:
- `Vt.` (virkaa toimittava, acting) if not substantive.
- `({pvm} alkaen)` if newly in post.
- `(tarkistettava)` if there is a known reason to re-check.

### 4.4 Contact fields (optional, zero or more, in this order)

Each appears at most once per person.

- `LinkedIn:` — full canonical URL.
- `X:` — full URL.
- `Bluesky:` — full URL.
- `Mastodon:` — full URL.
- `Website:` — full URL.
- `GitHub:` — full URL.
- `Email:` — only if published or authorised.

**Verification rule:** add only if a public source attributable to the named person confirms it. Better to omit than to guess.

### 4.5 `Stakeholder engagement notes:` (required, list of strings)

Three to seven short bullets answering at least one of: career background, ownership and statutory functions, public statements, hook. Anti-pattern: generic CV bullets. If the bullet would apply to any senior Finnish virkamies, it should not be in the register.

### 4.6 `Tone advice:` (required, exactly two strings)

Two bullets: what to lead with; what to avoid. Specific to the person, derivable from the engagement notes. Sote-frames such as sote-uudistus, hyvinvointialueet, Kanta-palvelut, terveyspalvelujen yhdenvertaisuus, sote-rahoitusmalli are the natural Finnish vocabulary.

### 4.7 Other fields

Currently none. Do not add new field types without updating this spec first.

## 5. Provenance and dating

- Anchor facts to year (preferably month or exact date). Convert relative dates to absolute.
- The Orpo government (formed June 2023; Kok-PS-RKP-KD coalition) has produced significant STM portfolio turnover in 2025-2026 (Kaisa Juuso → Wille Rydman February 2026). Treat any STM Minister entry pre-dating 20 February 2026 as warranting re-verification.

## 6. Update workflow

1. Identify the change.
2. Verify against valtioneuvosto.fi, stm.fi, agency pages, Yle, Helsingin Sanomat, Lääkärilehti, Mediuutiset, Suomen Lääkärilehti.
3. Apply minimum diff; re-check Tone advice if engagement notes changed.
4. Confirm structure; no `?` placeholders.
5. Re-validate cross-references.

## 7. Invariants

- Every person has exactly one Title, one engagement notes block, one Tone advice block.
- Tone advice has exactly two bullets.
- No `"?"` placeholders remain.
- Every quoted string is on one line.
- Every URL is HTTPS.
- Every person under exactly one organisation.

## 8. Anti-patterns

- Padding; speculation; vendor-flattering language; stale role titles; duplicate entries; mixing facts and aspirations.
- Treating the system as municipal — since 1 January 2023 the hyvinvointialueet are the operational owners of social and health services, and pitches that route via municipalities (apart from environmental health, culture, education) will be redirected.
- Importing NHS or US framings unmodified — Finland funds the hyvinvointialueet directly from the state budget without a payer-provider split inside the public system; Kela handles separate national-insurance benefits and Kanta digital services.

## 9. Acronym and term glossary (selective)

- **Aluehallintovirasto (AVI)** — regional state administrative agency; supervises social and health services regionally alongside Valvira.
- **Eduskunta** — Finnish Parliament.
- **Fimea** — Lääkealan turvallisuus- ja kehittämiskeskus; Finnish Medicines Agency.
- **Hyvinvointialue (HVA)** — wellbeing services county; 21 in Finland (plus the City of Helsinki acting in the same role and the HUS-yhtymä).
- **Hyvinvointialuejohtaja** — chief executive of a hyvinvointialue.
- **HUS** — Helsingin ja Uudenmaan sairaanhoitopiiri / HUS-yhtymä; the largest university hospital district.
- **Kanta-palvelut** — the national digital health information services (e-prescription, Patient Data Repository, My Kanta Pages), operated by Kela.
- **Kela** — Kansaneläkelaitos; Social Insurance Institution.
- **KYS** — Kuopion yliopistollinen sairaala.
- **OYS** — Oulun yliopistollinen sairaala.
- **Pääjohtaja** — Director-General.
- **Pelastustoimi** — rescue services (transferred to hyvinvointialueet 1 January 2023 alongside social and health).
- **Perustuslakivaliokunta** — Constitutional Law Committee of Eduskunta (frequently cited as the body that shaped the sote reform's constitutional design).
- **Sairausvakuutus** — sickness insurance (administered by Kela).
- **Sosiaali- ja terveysministeriö (STM)** — Ministry of Social Affairs and Health.
- **Sosiaali- ja terveysvaliokunta (StV)** — Eduskunta Social Affairs and Health Committee.
- **Sote** / **Sote-uudistus** — social and health / the 2023 social and health reform.
- **STUK** — Säteilyturvakeskus; Radiation and Nuclear Safety Authority.
- **TAYS** — Tampereen yliopistollinen sairaala.
- **THL** — Terveyden ja hyvinvoinnin laitos; Finnish Institute for Health and Welfare.
- **TTL** — Työterveyslaitos; Finnish Institute of Occupational Health.
- **TYKS** — Turun yliopistollinen sairaala.
- **Valvira** — Sosiaali- ja terveysalan lupa- ja valvontavirasto; National Supervisory Authority for Welfare and Health.

## 10. Worked example

```yaml
      - Wille Rydman (PS):
          - Title: Sosiaali- ja terveysministeri (Minister of Social Affairs and Health) (20.2.2026 alkaen)
          - Stakeholder engagement notes:
              - "Nimitetty sosiaali- ja terveysministeriksi Tasavallan presidentin päätöksellä 20.2.2026 Perussuomalaisten ehdokkaana Kaisa Juuson erottua sairauslomalle uupumuksen vuoksi; ministerin ehdokkuus vahvistettiin PS:n eduskuntaryhmän ja puoluehallituksen yksimielisellä päätöksellä."
              - "Aiemmin Orpon hallituksen elinkeinoministeri 2023-2025; valtiotieteiden maisteri; kansanedustajakausi ja PS-puolueprofiili pitkä ennen ministeriyttä — siirtyminen elinkeinoportfoliosta sote-portfolioon edellyttää huomattavaa uudelleenkohdennusta."
              - "Astuu virkaan kireässä poliittisessa tilanteessa: hyvinvointialueiden talousahdinko, sote-rahoitusmallin tarkistus ja yliopistollisten sairaaloiden ohjauksen kysymykset ovat avoimena; Orpon hallituksen sote-linjan jatkuvuus on poliittisesti herkkä."
              - "Hook: hyvinvointialueiden talous, sote-rahoitusmallin tarkistus, työvoimakysymykset, lääkkeiden saatavuus ja Kanta-palvelujen kehitys laskeutuvat; centralized vendor-pitches ohi hyvinvointialueiden eivät laskeudu."
          - Tone advice:
              - "Avaa keskustelu hyvinvointialueiden talouden, sote-rahoituksen ja työvoiman kautta — nämä ovat Orpon hallituksen sote-linjan etusijaiset linjat."
              - "Älä pitchaa kuin STM olisi operatiivinen tilaaja — sote-palvelut ovat hyvinvointialueiden vastuulla, ja keskittävä framing torjutaan."
```

## 11. Out-of-band notes

Used where a role is unfilled or in interim. Do not need Tone advice.

## 12. Open questions

- Named portfolio split between the three STM ministers under Orpo government as of mid-2026 (Sosiaali- ja terveysministeri Rydman; perhe- ja peruspalveluministeri; sosiaaliturvaministeri).
- Named kansliapäällikkö of STM and the osastopäälliköt of the major STM osastot with currency verified.
- Substantive pääjohtaja of Valvira and STUK and TTL with currency verified.
- Hyvinvointialuejohtaja of each of the 21 hyvinvointialueet and the HUS-yhtymä johtaja with currency verified.
- Sosiaali- ja terveysvaliokunta puheenjohtaja and varapuheenjohtaja in the current Eduskunta cycle.
- Pääjohtaja of Kela post-2025; Kanta-palvelujen johtaja.
- Puheenjohtaja of Suomen Lääkäriliitto, Tehy, SuPer with currency verified.
