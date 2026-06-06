# spec.md — `leaders.yml`

Single source of truth for the structure, semantics, and update rules of `leaders.yml` for the French health system (système de santé français). Treat this document as the canonical specification: the YAML must conform to it; if the YAML and this spec disagree, the spec wins and the YAML is fixed.

## 1. Purpose

`leaders.yml` is an engagement register of named individuals in and around the French système de santé. Each entry exists so that a reader (typically inside the Ministère de la Santé, an Agence régionale de santé, the Assurance Maladie, a CHU, or an adjacent national body) can decide:

1. **Who to engage** for a given digital/transformation/policy topic.
2. **How to engage them** — the angle that lands and the angle that fails.
3. **Where to engage them** — which public channels they actually use.

It is not a phone book, not a CRM, and not a comms list. Entries that do not directly serve engagement decision-making are out of scope.

The French système de santé is a unitary state model with strong central institutions. The Ministère de la Santé, through its Direction générale de la santé (DGS), Direction générale de l'offre de soins (DGOS) and Direction de la sécurité sociale (DSS), sets policy. The Assurance Maladie (CNAM) funds and reimburses. Independent national authorities (HAS for evaluation; ANSM for medicines and devices; Santé publique France for surveillance; Agence de la biomédecine for transplantation, assisted reproduction and genetics; ANSES for food and environmental safety) regulate, evaluate, and surveil. The eighteen Agences régionales de santé (ARS) deliver state policy in each region and coordinate hospitals and ambulatory care. The CHUs (Centres hospitaliers universitaires) form the academic-hospital tier; the AP-HP is the largest public-hospital system in Europe.

## 2. Scope

**In scope:**
- Gouvernement: Président de la République, Premier ministre, Ministre de la Santé and Ministres délégués in the health-and-care family, Cabinet du Ministre (Directeur de cabinet, Conseiller santé du Président de la République, Conseiller santé du Premier ministre).
- Ministère de la Santé administrations centrales: Directeur général de la santé (DGS), Directeur général de l'offre de soins (DGOS), Directeur de la sécurité sociale (DSS), Directeur général de la cohésion sociale (DGCS), Délégué ministériel au numérique en santé.
- Independent national authorities and operators: Haute Autorité de Santé (HAS); Agence nationale de sécurité du médicament et des produits de santé (ANSM); Santé publique France; Agence de la biomédecine (ABM); Agence nationale de sécurité sanitaire de l'alimentation, de l'environnement et du travail (ANSES); Institut national du cancer (INCa); Agence du numérique en santé (ANS); Institut national de la santé et de la recherche médicale (INSERM) where the role is health-policy facing.
- Assurance Maladie: Caisse nationale de l'Assurance Maladie (CNAM) Directeur général and Directeur médical; Caisse centrale de la Mutualité sociale agricole (CCMSA) where the brief is health.
- Agences régionales de santé (ARS): the eighteen Directeurs/trices généraux/ales of ARS, particularly the larger regions (Île-de-France, Auvergne-Rhône-Alpes, Hauts-de-France, Nouvelle-Aquitaine, Occitanie, Grand Est, Provence-Alpes-Côte d'Azur, Pays de la Loire, Bretagne, Normandie).
- Hospital tier of national significance: AP-HP Directeur général and Président de la Commission médicale d'établissement; Hospices civils de Lyon Directeur général; AP-HM Marseille; CHU de Toulouse, CHU de Bordeaux, CHU de Nantes; Conférence nationale des Directeurs généraux de CHU; Conférence des Présidents de CME de CHU.
- Parlement: Commission des Affaires sociales de l'Assemblée nationale (Président, Rapporteur de la branche maladie du PLFSS); Commission des Affaires sociales du Sénat (Président, Rapporteure générale, Rapporteure de la branche maladie); MECSS where relevant.
- Statutory and oversight bodies: Cour des comptes (Présidente, Présidente de la 6e chambre when relevant to health); Défenseur des droits where directly relevant; Commission nationale de l'informatique et des libertés (CNIL) on health-data matters.
- Related sector bodies of national significance: Conseil national de l'Ordre des médecins (CNOM); Conseil national de l'Ordre des pharmaciens (CNOP); Conseil national de l'Ordre des infirmiers (ONI); Conseil national de l'Ordre des chirurgiens-dentistes; Académie nationale de médecine; Confédération des syndicats médicaux français (CSMF); MG France; Avenir Spé–Le Bloc; SML; Fédération hospitalière de France (FHF); Fédération de l'hospitalisation privée (FHP); Fédération des établissements hospitaliers et d'aide à la personne privés non lucratifs (FEHAP).
- For each organisation: only stakeholders senior enough that engagement with them shapes decisions across the organisation (typically Ministre, Directeur général, Directeur, Président, Directeur du cabinet).

**Out of scope:**
- Operational staff below sous-direction / chefferie de bureau level inside the administrations centrales, and below directorate level inside ARS and CHUs.
- Suppliers, vendors, consultancies (their leaders may appear only when they hold a named role in a French public body, e.g. a Conseil d'administration seat).
- Historical post-holders (unless explicitly flagged as predecessor for context).
- Other EU counterparts (unless they also hold a France-facing role).

## 3. Structure

The YAML is a single top-level mapping with one key.

```
Système de santé français stakeholders:
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

- Organisations are grouped by tier: Élysée and Matignon → Ministère de la Santé (Ministre, cabinet, DGS, DGOS, DSS, Délégation au numérique en santé) → national authorities (HAS, ANSM, Santé publique France, ABM, ANSES, INCa, ANS) → Assurance Maladie (CNAM, CCMSA) → ARS in the order Île-de-France first, then alphabetical (Auvergne-Rhône-Alpes, Bourgogne-Franche-Comté, Bretagne, Centre-Val de Loire, Corse, Grand Est, Guadeloupe, Guyane, Hauts-de-France, La Réunion, Martinique, Mayotte, Normandie, Nouvelle-Aquitaine, Occitanie, Pays de la Loire, Provence-Alpes-Côte d'Azur) → hospital tier (AP-HP first, then CHU conferences, then individual CHUs) → Parlement → ordres et fédérations → oversight bodies.
- Within an organisation, people are ordered: Ministre / Directeur général → Directeur du cabinet / Directeur adjoint → Directeur médical → Directeur des soins → Other Directeurs → Directeur du numérique → Directeur financier → Conseil d'administration members where named.
- Programme leads and SROs follow their accountable director.

## 4. Field definitions

### 4.1 Organisation name

The key under which a person sits. Use the official name as the organisation publishes it. Acronyms in parentheses where helpful. Provide the French name first and the English in parentheses where the body is widely known by both (e.g. `Haute Autorité de Santé (HAS)`, `Caisse nationale de l'Assurance Maladie (CNAM)`, `Agence nationale de sécurité du médicament et des produits de santé (ANSM)`).

### 4.2 Person name

Include honorifics and academic titles that the person actually uses publicly: `Dr`, `Pr`, `Pre`. Post-nominal honours such as the Légion d'honneur (Chevalier, Officier, Commandeur) are not normally written in inline names but may be referenced in notes. Party affiliation in parentheses for elected officials, using the canonical abbreviations (`Renaissance / RE`, `LR`, `PS`, `LFI`, `RN`, `Horizons`, `MoDem`, `EELV / Les Écologistes`, `PCF`, `UDI`, `LIOT`). Match what appears on the organisation's official biography or the Journal officiel notice.

### 4.3 `Title:` (required, one)

Current job title, verified to within the last six months. Use the French title and add an English gloss in parentheses where the French title is not self-evident to an English reader (e.g. `Ministre de la Santé (Minister of Health)`). Include effective dates or status flags inline where helpful:
- `par intérim` (acting / interim) if not substantive.
- `(depuis le {date})` if newly in post.
- `(vérifier l'actualité)` if there is a known reason to re-check.

### 4.4 Contact fields (optional, zero or more, in this order)

Each appears at most once per person.

- `LinkedIn:` — full canonical URL. Skip if not verifiable.
- `X:` — full URL (`https://x.com/{handle}`). Skip if not verifiable, even if a handle was found.
- `Bluesky:` — full URL (`https://bsky.app/profile/{handle}`). Particularly relevant for French public-sector and academic figures who maintain Bluesky presence.
- `Mastodon:` — full URL (`https://{instance}/@{handle}`). Public-administration Mastodon adoption in France is meaningful (`mastodon.social`, `mamot.fr`).
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

Anti-pattern: generic CV bullets ("haut fonctionnaire de très grande qualité"). If the bullet would apply to any senior French civil servant, it should not be in the register.

### 4.6 `Tone advice:` (required, exactly two strings)

Two bullets, each a YAML scalar wrapped in double quotes, ending in a full stop.

- **Bullet 1 — what to lead with.** The framing, vocabulary, or precedent that will land. May reference specific programmes, reports, or quotes from the engagement notes above (e.g. Ma santé 2022, Ségur de la santé, PLFSS, CSIS, France 2030 santé, Mon espace santé).
- **Bullet 2 — what to avoid.** A failure mode specific to this person — not generic. Should be derivable from their engagement notes (career, public statements, current pressures).

Tone advice is a derived field: it must be consistent with the engagement notes for the same person. If you change the notes materially, re-check the tone advice.

### 4.7 Other fields

Currently none. Do not add new field types without updating this spec first.

## 5. Provenance and dating

- All facts are anchored to a year (preferably a month or exact date) where helpful. "Nommée le {date}" beats "récemment nommée".
- Convert relative dates to absolute when writing the YAML ("l'an dernier" → `2025`).
- When a fact changes (e.g. a Directeur général leaves), update the affected fields in the same commit; do not leave stale notes alongside a new title.
- Government instability since the June 2024 dissolution (Attal → Barnier → Bayrou → Lecornu I → Lecornu II) has produced extremely rapid Ministre and cabinet turnover. Treat any Ministère entry as warranting re-verification when more than 60 days old.

## 6. Update workflow

1. **Identify the change** — a new appointment (décret de nomination), departure, statement.
2. **Verify against a public source** — Journal officiel (Légifrance), info.gouv.fr, official agency page, Hospimedia, Quotidien du Médecin, Le Monde, Mediapart, APMnews.
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
- **Speculation.** "Probablement réceptif à l'IA." If you cannot point to a public source for the disposition, omit it.
- **Vendor-flattering language.** Tone advice exists to make engagement realistic, not optimistic.
- **Stale role titles.** A person's role in this register must be their current substantive (or named interim) role, not their most famous previous one.
- **Duplicate entries.** A person belongs to one organisation. If they hold roles in two, choose the one most relevant for engagement and note the second in prose.
- **Mixing facts and aspirations.** Hooks describe what would land *given the person's stated priorities*, not what the writer wishes the person cared about.
- **Treating the système de santé as fully centralised.** Care delivery is operationally distributed across eighteen ARS, public hospitals, private not-for-profit hospitals (FEHAP), private for-profit hospitals (FHP), CPAMs and the liberal medical professions. Pitches that assume a single national operational customer will fail.
- **Importing NHS or US framings unmodified.** France has Bismarckian financing (Assurance Maladie) with a strong state directorate; HAS evaluates differently from NICE; ANSM operates inside the EMA / HMA network; the ARS are state operators, not autonomous regional buyers like the NHS England ICBs.

## 9. Acronym and term glossary (selective)

Terms and acronyms used inside the YAML that readers may not know:

- **ABM** — Agence de la biomédecine (transplantation, assisted reproduction, embryonic research, genetics).
- **ANS** — Agence du numérique en santé.
- **ANSES** — Agence nationale de sécurité sanitaire de l'alimentation, de l'environnement et du travail.
- **ANSM** — Agence nationale de sécurité du médicament et des produits de santé.
- **AP-HP** — Assistance publique – Hôpitaux de Paris (39 hospitals, ~100,000 staff, the largest CHU in Europe).
- **AP-HM** — Assistance publique – Hôpitaux de Marseille.
- **ARS** — Agence régionale de santé (regional state operator for the system; 18 in total including overseas).
- **CHU** — Centre hospitalier universitaire (academic hospital).
- **CME** — Commission médicale d'établissement (hospital medical commission).
- **CNAM** — Caisse nationale de l'Assurance Maladie.
- **CNOM** — Conseil national de l'Ordre des médecins.
- **COG** — Convention d'objectifs et de gestion (the multi-year state-Assurance Maladie performance contract).
- **CPAM** — Caisse primaire d'Assurance Maladie (the departmental statutory insurance fund).
- **CSIS** — Conseil stratégique des industries de santé (industrial strategy council).
- **CSMF** — Confédération des syndicats médicaux français.
- **DGS** — Direction générale de la santé (Ministry directorate; public health and crises).
- **DGOS** — Direction générale de l'offre de soins (Ministry directorate; hospital and ambulatory care organisation).
- **DSS** — Direction de la sécurité sociale (Ministry directorate; social insurance, including health).
- **EHESP** — École des hautes études en santé publique (Rennes; the public health school training senior managers).
- **ENA / INSP** — École nationale d'administration (replaced by Institut national du service public in 2022).
- **FEHAP** — Fédération des établissements hospitaliers et d'aide à la personne privés non lucratifs.
- **FHF** — Fédération hospitalière de France (public-hospital federation).
- **FHP** — Fédération de l'hospitalisation privée (private for-profit hospital federation).
- **HAS** — Haute Autorité de Santé (the independent national authority for evaluation, accreditation and guidelines).
- **INCa** — Institut national du cancer.
- **INSERM** — Institut national de la santé et de la recherche médicale.
- **JO** — Journal officiel (official gazette).
- **LFSS / PLFSS** — Loi / Projet de loi de financement de la sécurité sociale (annual social-security funding law, the principal vehicle for health-system funding decisions).
- **Mon espace santé** — the national personal health record.
- **Ma santé 2022 / Ségur de la santé** — the two principal Macron-era reform frames.
- **MECSS** — Mission d'évaluation et de contrôle des lois de financement de la sécurité sociale.
- **MG France** — Médecins généralistes France (general-practitioner union).
- **ONDAM** — Objectif national de dépenses d'assurance maladie (the annual health-spending objective set by Parliament).
- **PMI** — Protection maternelle et infantile.
- **SAS** — Service d'accès aux soins (the post-Covid unscheduled-care access service).
- **Ségur du numérique en santé** — the multi-billion-euro post-Covid digital-health investment programme.
- **Santé publique France** — Agence nationale de santé publique.

## 10. Worked example

This is the canonical shape of one person. Any new entry should match it field-for-field (omitting optional contact fields where not verifiable).

```yaml
      - Stéphanie Rist (Renaissance):
          - Title: Ministre de la Santé, des Familles, de l'Autonomie et des Personnes handicapées (Minister of Health, Families, Autonomy and Disability) (depuis le 26 février 2026)
          - Stakeholder engagement notes:
              - "Nommée Ministre de la Santé, des Familles, de l'Autonomie et des Personnes handicapées par décret du 26 février 2026 dans le gouvernement Lecornu II; auparavant Députée du Loiret depuis 2017 et figure parlementaire majeure de Renaissance sur les sujets de santé."
              - "Rhumatologue de profession au CHU d'Orléans avant l'élection; auteure de la 'loi Rist' (2023) ouvrant l'accès direct à certaines professions paramédicales et l'expérimentation des infirmiers en pratique avancée — l'identité parlementaire est l'accès aux soins et la délégation de tâches."
              - "Camille Galliard-Minier (Renaissance) est Ministre déléguée chargée de l'Autonomie et des Personnes handicapées auprès d'elle depuis le 26 février 2026; le périmètre du ministère intègre famille, autonomie et handicap, redonnant cohérence parcours de vie."
              - "Hook: accès aux soins, délégation de tâches, professions paramédicales, autonomie, PLFSS 2027 et financement hospitalier post-Ségur aterrissent; pitches purement vendeurs de plateformes sans ancrage parlementaire risquent d'être renvoyés au cabinet."
          - Tone advice:
              - "Liderar avec accès aux soins, délégation de tâches et professions paramédicales — ce sont ses lignes d'auteure parlementaire et le pont entre médecine clinique et politique publique."
              - "Ne pas pitcher sur la centralisation du système — Rist est venue à la politique par la pratique hospitalière régionale et le langage technocratique parisien sera rebondi vers l'ancrage territorial."
```

## 11. Out-of-band notes

Some organisation blocks in the YAML contain a non-person entry such as:

```yaml
      - Notes on Santé publique France:
          - Status: ...
          - Implication: ...
```

These are permitted only where they explain why a role is *not* listed (e.g. a Directeur général par intérim with announced departure) and should be removed once a named person can be added. They do not need `Tone advice`.

## 12. Open questions

These are known gaps to track and resolve:

- The substantive Directeur/trice général/e of Santé publique France after Caroline Semaille's interim term ends 30 June 2026 (she did not request renewal).
- The named Directeur du cabinet of Stéphanie Rist following her appointment 26 February 2026, and named Conseillers in the cabinet on hôpitaux, ambulatoire, numérique en santé, autonomie.
- Named DGS, DGOS, DSS and Délégué ministériel au numérique en santé with currency verified to within six months — the Bayrou-to-Lecornu transitions have produced rotation at the directorial level.
- Named Directeurs/trices générales of the eighteen ARS, in particular Île-de-France, Auvergne-Rhône-Alpes, Hauts-de-France and Grand Est (the last led by Christelle Ratignier-Carbonneil from 15 June 2025).
- Named Directeur général de l'AP-HP and Présidente de la CME de l'AP-HP, plus the Conférence nationale des Directeurs généraux de CHU.
- Présidents and rapporteurs of the Commission des Affaires sociales of both chambers and the rapporteur de la branche maladie of the PLFSS — these change with each cabinet shift and parliamentary cycle.
- Named Présidents of the Conseils nationaux des Ordres (médecins, pharmaciens, infirmiers, chirurgiens-dentistes) with currency verified.
- Named Présidents of the principal hospital federations (FHF, FHP, FEHAP) with currency verified.

Each open question should be closed by editing this spec and the YAML in the same commit when resolved.
