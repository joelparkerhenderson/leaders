# spec.md — `leaders.yml`

Single source of truth for the structure, semantics, and update rules of `leaders.yml` for the Spanish Sistema Nacional de Salud (SNS). Treat this document as the canonical specification: the YAML must conform to it; if the YAML and this spec disagree, the spec wins and the YAML is fixed.

## 1. Purpose

`leaders.yml` is an engagement register of named individuals in and around the SNS. Each entry exists so that a reader (typically inside the Ministerio de Sanidad, an Autonomous Community Consejería de Sanidad, an SNS regional service, an academic hospital, or an adjacent national body) can decide:

1. **Who to engage** for a given digital/transformation/policy topic.
2. **How to engage them** — the angle that lands and the angle that fails.
3. **Where to engage them** — which public channels they actually use.

It is not a phone book, not a CRM, and not a comms list. Entries that do not directly serve engagement decision-making are out of scope.

The SNS is statutorily a single national health system (Ley 14/1986 General de Sanidad; Ley 16/2003 de cohesión y calidad del SNS) operationally delivered by 17 Autonomous Communities (Comunidades Autónomas, CCAA) and the cities of Ceuta and Melilla. Central government, through the Ministerio de Sanidad, sets policy, the common service portfolio (cartera común de servicios), pricing and reimbursement of medicines, public-health emergency response, and the inter-territorial coordination via the Consejo Interterritorial del SNS (CISNS). The seventeen regional health services (Servicios de Salud) deliver care; INGESA delivers in Ceuta and Melilla. Central agencies (AEMPS, ISCIII, ONT, AECOSAN/AESAN where it touches food safety) regulate, evaluate, license, and coordinate national programmes.

## 2. Scope

**In scope:**
- Gobierno de España: Presidente del Gobierno, Vicepresidentes, Ministra de Sanidad, Secretaría de Estado de Sanidad, Subsecretaría, the Direcciones Generales of Sanidad (Salud Pública y Equidad en Salud, Cartera Común de Servicios del SNS y Farmacia, Ordenación Profesional, Salud Digital y Sistemas de Información).
- Central state health agencies and bodies: Agencia Española de Medicamentos y Productos Sanitarios (AEMPS); Instituto de Salud Carlos III (ISCIII); Organización Nacional de Trasplantes (ONT); Instituto Nacional de Gestión Sanitaria (INGESA); Agencia Española de Seguridad Alimentaria y Nutrición (AESAN) where the brief touches food and nutrition policy; Consejo Asesor de Sanidad and other ministerial advisory councils where leadership is publicly named.
- Consejo Interterritorial del Sistema Nacional de Salud (CISNS): the Ministra de Sanidad as President; the seventeen Consejeros/as de Sanidad of the Autonomous Communities; the Consejeros/as de Ceuta and Melilla.
- Autonomous Community health systems (Servicios de Salud): the Consejero/a de Sanidad and the Director/a Gerente of the regional health service for the seven largest by population (Andalucía SAS, Cataluña CatSalut, Comunidad de Madrid SERMAS, Comunitat Valenciana, Galicia SERGAS, Castilla y León SACYL, País Vasco Osakidetza). Smaller CCAA included where the Consejero/a holds national posture (e.g. through chairing CISNS technical commissions).
- Cortes Generales: Comisión de Sanidad del Congreso de los Diputados (Presidente, Vicepresidentes, party spokespeople) and the Comisión de Sanidad del Senado.
- Statutory and oversight bodies: Defensor del Pueblo where directly relevant to health; Tribunal de Cuentas where directly relevant; Agencia Española de Protección de Datos (AEPD) on health-data matters.
- Related sector bodies of national significance: Consejo General de Colegios Oficiales de Médicos (OMC), Consejo General de Colegios Oficiales de Enfermería de España, Consejo General de Colegios Oficiales de Farmacéuticos, Consejo General de Colegios Oficiales de Odontólogos y Estomatólogos; Confederación Estatal de Sindicatos Médicos (CESM); Sindicato de Enfermería (SATSE); Federación de Asociaciones para la Defensa de la Sanidad Pública (FADSP).
- For each organisation: only stakeholders senior enough that engagement with them shapes decisions across the organisation (typically Minister, Secretary of State, Director General, Consejero/a, Gerente de Servicio de Salud, college president).

**Out of scope:**
- Operational staff below Subdirección General / Gerencia de Área de Salud level.
- Suppliers, vendors, consultancies (their leaders may appear only when they hold a named role in a Spanish public body, e.g. as a Consejo Asesor member).
- Historical post-holders (unless explicitly flagged as predecessor for context).
- Other EU counterparts (unless they also hold a Spain-facing role).

## 3. Structure

The YAML is a single top-level mapping with one key.

```
Sistema Nacional de Salud stakeholders:
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

- Organisations are grouped by tier: Gobierno (Ministerio de Sanidad, Secretaría de Estado, Direcciones Generales) → central state agencies (AEMPS, ISCIII, ONT, INGESA, AESAN) → Consejo Interterritorial del SNS → Cortes Generales (Comisión de Sanidad Congreso, Senado) → Autonomous Community health systems alphabetised by official name (Andalucía, Aragón, Asturias, Illes Balears, Canarias, Cantabria, Castilla-La Mancha, Castilla y León, Cataluña, Comunitat Valenciana, Extremadura, Galicia, La Rioja, Madrid, Murcia, Navarra, País Vasco) followed by Ceuta and Melilla → professional colleges and unions → oversight bodies.
- Within an organisation, people are ordered: Minister / Director General / Consejero/a → Secretary of State / Deputy / Vice-Consejero/a → Medical Director / Chief Medical Officer → Nursing Director → Other Directors → Director of Digital → Director of Finance → Board members where named.
- Programme leads and SROs follow their accountable director.

## 4. Field definitions

### 4.1 Organisation name

The key under which a person sits. Use the official name as the organisation publishes it. Acronyms in parentheses where helpful. Provide the Spanish name first, and the English in parentheses where the body is widely known by both (e.g. `Agencia Española de Medicamentos y Productos Sanitarios (AEMPS)`, `Organización Nacional de Trasplantes (ONT)`). For Autonomous Community health services, use the official name of the Servicio de Salud (e.g. `Servicio Andaluz de Salud (SAS)`, `Servei Català de la Salut (CatSalut)`, `Servicio Madrileño de Salud (SERMAS)`, `Osakidetza — Servicio Vasco de Salud`).

### 4.2 Person name

Include honorifics and academic titles that the person actually uses publicly: `Dr`, `Dra`, `Profesor/a`. Party affiliation in parentheses for elected officials, using the canonical Spanish abbreviations (`PSOE`, `PP`, `Sumar`, `Vox`, `ERC`, `Junts`, `PNV`, `EH Bildu`, `BNG`, `Más Madrid`, `Compromís`, `CC`). Match what appears on the organisation's official biography page or the BOE (Boletín Oficial del Estado) appointment notice.

### 4.3 `Title:` (required, one)

Current job title, verified to within the last six months. Use the Spanish title and add an English gloss in parentheses where the Spanish title is not self-evident to an English reader (e.g. `Ministra de Sanidad (Minister of Health)`). Include effective dates or status flags inline where helpful:
- `En funciones` (acting) if not substantive.
- `(desde {fecha})` if newly in post.
- `(verificar vigencia)` if there is a known reason to re-check.

### 4.4 Contact fields (optional, zero or more, in this order)

Each appears at most once per person.

- `LinkedIn:` — full canonical URL. Skip if not verifiable.
- `X:` — full URL (`https://x.com/{handle}`). Skip if not verifiable, even if a handle was found.
- `Bluesky:` — full URL (`https://bsky.app/profile/{handle}`). Particularly relevant for Spanish public-sector figures, where Bluesky adoption is high in the health-policy commentariat.
- `Mastodon:` — full URL (`https://{instance}/@{handle}`).
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

Anti-pattern: generic CV bullets ("líder con amplia trayectoria"). If the bullet would apply to any senior SNS leader, it should not be in the register.

### 4.6 `Tone advice:` (required, exactly two strings)

Two bullets, each a YAML scalar wrapped in double quotes, ending in a full stop.

- **Bullet 1 — what to lead with.** The framing, vocabulary, or precedent that will land. May reference specific programmes, reports, or quotes from the engagement notes above (e.g. cartera común de servicios, Estrategia de Salud Digital del SNS, Plan Nacional de Salud Mental, modelo ONT).
- **Bullet 2 — what to avoid.** A failure mode specific to this person — not generic. Should be derivable from their engagement notes (career, public statements, current pressures).

Tone advice is a derived field: it must be consistent with the engagement notes for the same person. If you change the notes materially, re-check the tone advice.

### 4.7 Other fields

Currently none. Do not add new field types without updating this spec first.

## 5. Provenance and dating

- All facts are anchored to a year (preferably a month or exact date) where helpful. "Toma de posesión {mes año}" beats "recientemente nombrado".
- Convert relative dates to absolute when writing the YAML ("el año pasado" → `2025`).
- When a fact changes (e.g. a Consejero/a leaves after an autonomic election), update the affected fields in the same commit; do not leave stale notes alongside a new title.
- Spanish autonomic political cycles produce frequent Consejero/a turnover; treat any CCAA entry as warranting re-verification after a regional election.

## 6. Update workflow

1. **Identify the change** — a new appointment, departure, statement, or BOE publication.
2. **Verify against a public source** — official Ministry / agency page, BOE notice, autonomic gazette (DOGC, BOJA, BOCM, DOG, etc.), named press article in El País, El Mundo, Redacción Médica, Diario Médico, Gaceta Médica.
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
- **Speculation.** "Probablemente receptivo a la IA." If you cannot point to a public source for the disposition, omit it.
- **Vendor-flattering language.** Tone advice exists to make engagement realistic, not optimistic.
- **Stale role titles.** A person's role in this register must be their current substantive (or named acting) role, not their most famous previous one.
- **Duplicate entries.** A person belongs to one organisation. If they hold roles in two, choose the one most relevant for engagement and note the second in prose.
- **Mixing facts and aspirations.** Hooks describe what would land *given the person's stated priorities*, not what the writer wishes the person cared about.
- **Treating the SNS as a single operational customer.** Care delivery sits with seventeen Servicios de Salud, each with its own procurement, IT architecture, professional collective agreements, and political accountability. The CISNS coordinates; it does not deliver. Pitches that assume a single national delivery counterparty will fail.
- **Importing NHS framings unmodified.** The SNS is universal and tax-funded but autonomic in delivery; the cartera común de servicios, autonomic financing through the LOFCA system, and the ONT national programme model are distinctive Spanish constructs that do not map cleanly to NHS England.

## 9. Acronym and term glossary (selective)

Terms and acronyms used inside the YAML that readers may not know:

- **AEMPS** — Agencia Española de Medicamentos y Productos Sanitarios; Spanish Medicines and Medical Devices Agency.
- **AEPD** — Agencia Española de Protección de Datos; Spanish data protection authority.
- **AESAN** — Agencia Española de Seguridad Alimentaria y Nutrición.
- **BOE** — Boletín Oficial del Estado; the Spanish state gazette.
- **Cartera común de servicios del SNS** — common portfolio of services of the National Health System, set centrally.
- **CatSalut** — Servei Català de la Salut; the Catalan regional health service.
- **CCAA** — Comunidades Autónomas; the seventeen Spanish Autonomous Communities.
- **CESM** — Confederación Estatal de Sindicatos Médicos; the principal physicians' union.
- **CISNS** — Consejo Interterritorial del Sistema Nacional de Salud; the inter-territorial coordination council chaired by the Ministra de Sanidad.
- **Consejero/a de Sanidad** — the senior politician responsible for health in an Autonomous Community government.
- **Conselleria de Salut / Conselleria de Sanitat Universal** — Catalan / Valencian forms of the regional health portfolio.
- **DG** — Dirección General (Directorate General) inside a ministry or government.
- **DGT** — Dirección General de Tráfico (not health, but the model for the ONT registry model and donor consent).
- **ENS** — Estrategia Nacional de Salud / Esquema Nacional de Seguridad (context-dependent — disambiguate in prose).
- **FADSP** — Federación de Asociaciones para la Defensa de la Sanidad Pública.
- **HMA** — Heads of Medicines Agencies (the EU network whose Management Group is currently chaired by the Director of AEMPS).
- **INGESA** — Instituto Nacional de Gestión Sanitaria; runs SNS delivery in Ceuta and Melilla.
- **ISCIII** — Instituto de Salud Carlos III; the public-health research and biomedical research funding institute.
- **LOFCA** — Ley Orgánica de Financiación de las Comunidades Autónomas; the autonomic financing law that underpins regional health budgets.
- **ONT** — Organización Nacional de Trasplantes; the world-renowned Spanish transplant coordination body, structurally embedded in the Ministerio de Sanidad.
- **OMC** — Consejo General de Colegios Oficiales de Médicos (Organización Médica Colegial); the umbrella body of provincial medical colleges.
- **Osakidetza** — Servicio Vasco de Salud; the Basque regional health service.
- **PSOE / PP / Sumar / Vox / ERC / Junts / PNV / EH Bildu / BNG / Más Madrid / Compromís / CC** — Spanish political parties relevant to health policy at state and autonomic level.
- **SAS** — Servicio Andaluz de Salud; the Andalusian regional health service.
- **SACYL** — Sanidad de Castilla y León.
- **SATSE** — Sindicato de Enfermería; the principal nursing union.
- **SERGAS** — Servizo Galego de Saúde; the Galician regional health service.
- **SERMAS** — Servicio Madrileño de Salud; the Madrid regional health service.
- **SNS** — Sistema Nacional de Salud; the National Health System.

## 10. Worked example

This is the canonical shape of one person. Any new entry should match it field-for-field (omitting optional contact fields where not verifiable).

```yaml
      - Mónica García Gómez (Sumar / Más Madrid):
          - Title: Ministra de Sanidad (Minister of Health) (desde 21 de noviembre de 2023)
          - X: https://x.com/Monica_Garcia_G
          - Stakeholder engagement notes:
              - "Anestesióloga del Hospital 12 de Octubre desde 2004; Licenciada en Medicina y Cirugía por la Universidad Complutense; Máster en Gestión Clínica por la Escuela Nacional de Sanidad."
              - "Toma de posesión como Ministra de Sanidad el 21 de noviembre de 2023 en el tercer gobierno Sánchez tras la entrada de Sumar en la coalición, en representación de Más Madrid."
              - "Anunció en diciembre de 2025 una norma a principios de 2026 para limitar la colaboración público-privada en Sanidad — la línea más definitoria del mandato."
              - "Lideró la posición española en la 79ª Asamblea Mundial de la Salud en Ginebra (mayo 2026) impulsando una alianza Europa-América sobre atención primaria; el 40 aniversario de la Ley General de Sanidad (abril 2026) marcó el aniversario simbólico de su mandato."
              - "Hook: atención primaria, salud pública, regulación de la colaboración público-privada, salud mental y sostenibilidad financiera del SNS aterrizan; propuestas que olvidan el marco autonómico o priorizan el sector privado no aterrizan."
          - Tone advice:
              - "Liderar con atención primaria, salud pública y refuerzo de lo público — son las líneas de su mandato y de Más Madrid / Sumar en sanidad."
              - "No proponer marcos centrados en el sector privado o que tensen con las CCAA del PP — son su línea política explícita y la propuesta será rechazada de raíz."
```

## 11. Out-of-band notes

Some organisation blocks in the YAML contain a non-person entry such as:

```yaml
      - Notes on Consejo Interterritorial del SNS:
          - Status: ...
          - Implication: ...
```

These are permitted only where they explain why a role is *not* listed (e.g. CCAA Consejeros/as in transition after a regional election; INGESA gerencia not yet substantive) and should be removed once a named person can be added. They do not need `Tone advice`.

## 12. Open questions

These are known gaps to track and resolve:

- Named Consejeros/as de Sanidad and Directores/as Gerentes of the seventeen Servicios de Salud — to be added per CCAA, with priority for Andalucía (SAS), Cataluña (CatSalut), Madrid (SERMAS), Comunitat Valenciana, Galicia (SERGAS), Castilla y León (SACYL), País Vasco (Osakidetza).
- The Directores/as Generales inside the Ministerio de Sanidad — Salud Pública y Equidad en Salud, Cartera Común de Servicios del SNS y Farmacia, Ordenación Profesional, Salud Digital y Sistemas de Información.
- Substantive INGESA leadership and the named Gerencia de Ceuta and Melilla.
- The president of the Comisión de Sanidad del Senado and the spokespeople of the major parties on that commission.
- Presidente of the Organización Médica Colegial (OMC) and the Consejo General de Enfermería with currency verified.
- Presidente de la AESAN and the leadership of the Centro Nacional de Epidemiología (within ISCIII).
- Named leadership of the Sociedad Española de Medicina de Familia y Comunitaria (semFYC), Sociedad Española de Salud Pública y Administración Sanitaria (SESPAS), and other learned societies of national health-policy weight.
- The composition and chairs of the principal CISNS technical commissions (Salud Pública, Farmacia, Salud Digital, Recursos Humanos) where leadership is publicly named.

Each open question should be closed by editing this spec and the YAML in the same commit when resolved.
