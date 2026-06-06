# spec.md — `leaders.yml`

Single source of truth for the structure, semantics, and update rules of `leaders.yml` for the Canadian health portfolio. The YAML must conform to this spec; if they disagree, the spec wins and the YAML is fixed.

## 1. Purpose

`leaders.yml` is an engagement register of named individuals in and around the Canadian health system. Each entry helps a reader inside Health Canada / Santé Canada, the Public Health Agency of Canada (PHAC) / Agence de la santé publique du Canada (ASPC), Canadian Institutes of Health Research (CIHR), Canadian Drug Agency (CDA-AMC, formerly CADTH), or a provincial/territorial ministry of health decide who to engage, how, and where.

Canada has a constitutionally devolved health system: the Canada Health Act provides the federal framework and federal funding contribution; the 13 provinces and territories own delivery, billing, professional regulation and hospital ownership. Health Canada administers the federal portfolio; PHAC handles public-health surveillance and emergency response; CIHR funds biomedical research; the Canadian Drug Agency (created 2024 from CADTH's expanded mandate) handles HTA, common drug review, formulary advice and prescription-drug data. Provincial-territorial Ministers of Health meet via the FPT (Federal-Provincial-Territorial) Health Conference.

## 2. Scope

**In scope:** Prime Minister; federal Minister of Health; Minister of Mental Health and Addictions where filled separately; Deputy Minister of Health; Chief Public Health Officer of Canada (PHAC); President of PHAC; President of CIHR; CEO Canadian Drug Agency (CDA-AMC); Chief Medical Officer of Health (and equivalents) for each province and territory; provincial/territorial Ministers of Health; Presidents of Canadian Medical Association (CMA), Canadian Nurses Association (CNA), Canadian Pharmacists Association (CPhA), College of Family Physicians of Canada, Royal College of Physicians and Surgeons of Canada; chairs of the House of Commons Standing Committee on Health (HESA) and Senate Standing Committee on Social Affairs, Science and Technology (SOCI) where health is the focus.

**Out of scope:** operational staff below assistant deputy minister inside federal departments and below assistant deputy/division head inside provincial ministries; vendors; historical post-holders.

## 3. Structure

```
Canadian health portfolio stakeholders / Acteurs du portefeuille santé canadien:
  - {Organisation}:
      - {Person}:
          - Title: ...
          - Stakeholder engagement notes: [...]
          - Tone advice: [...]
```

Indentation 2/6/10/14 spaces. Ordering: federal Cabinet → Health Canada → PHAC → CIHR → Canadian Drug Agency → provinces and territories (in population order: Ontario, Quebec, BC, Alberta, Manitoba, Saskatchewan, Nova Scotia, NB, NL, PEI, Nunavut, NWT, Yukon) → House and Senate health committees → professional bodies (CMA, CNA, CPhA, CFPC, RCPSC).

## 4. Field definitions

Standard family conventions. Party affiliation using canonical Canadian abbreviations: federal `LPC` (Liberal Party of Canada), `CPC` (Conservative Party of Canada), `NDP` (New Democratic Party), `BQ` (Bloc Québécois), `Green`; provincial labels (ON `PC` / `OLP` / `ONDP` / `Green`; QC `CAQ` / `QS` / `PQ` / `PLQ`; AB `UCP` / `NDP`; BC `BC NDP` / `BC United` / `BC Conservative`; etc.). Titles in English (and French where the body uses both).

## 5. Provenance and dating

Anchor facts to year, month or exact date. Mark Carney (LPC) won the 2025 federal election and was sworn in as Prime Minister; the Carney 28-member Cabinet includes Marjorie Michel as Minister of Health (the post-Carney era replaces the Trudeau government's Mark Holland as Health Minister). Treat any federal Cabinet entry pre-dating the Carney swearing-in as warranting re-verification.

## 6. Update workflow

1. Identify the change. 2. Verify against canada.ca, healthcanada.gc.ca, ourcommons.ca, sencanada.ca, provincial government websites, Globe and Mail, National Post, CBC, CTV, Radio-Canada, Le Devoir, La Presse, Healthy Debate, CMAJ. 3. Apply minimum diff. 4. Confirm structure. 5. Re-validate cross-references.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating the system as federally directed — provinces own delivery, billing and professional regulation; federal levers are funding contribution and standard-setting.
- Importing NHS or US framings unmodified — Canada is provincially-administered universal coverage with federal coordination, distinct from both.

## 9. Acronym glossary

- **CDA-AMC** — Canadian Drug Agency / Agence des médicaments du Canada (formerly CADTH).
- **CIHI** — Canadian Institute for Health Information.
- **CIHR** — Canadian Institutes of Health Research.
- **CMA** — Canadian Medical Association.
- **CMOH** — Chief Medical Officer of Health (provincial / territorial).
- **CNA** — Canadian Nurses Association.
- **CPhA** — Canadian Pharmacists Association.
- **FPT** — Federal-Provincial-Territorial (Health Ministers' Conference).
- **HESA** — House of Commons Standing Committee on Health.
- **NIHB** — Non-Insured Health Benefits (federal programme for First Nations and Inuit).
- **PHAC** — Public Health Agency of Canada / Agence de la santé publique du Canada (ASPC).
- **RCPSC** — Royal College of Physicians and Surgeons of Canada.
- **SOCI** — Senate Standing Committee on Social Affairs, Science and Technology.

## 10. Worked example

```yaml
      - Marjorie Michel (LPC):
          - Title: Minister of Health / Ministre de la Santé (in the Carney 28-member Cabinet, 2025)
          - Stakeholder engagement notes:
              - "Federal Minister of Health in the Mark Carney (LPC) 28-member Cabinet sworn in 2025; LPC; born in Haiti; elected federal MP for Papineau, Quebec in 2025 (the seat previously held by Justin Trudeau)."
              - "Reaffirmed in 2026 the federal commitment to drug safety, pharmaceutical-pricing reform and a new federal approach on drugs framed as 'save lives, reduce cost and build the economy'; delivered remarks at C.D. Howe Institute in May 2026 on Health and Economic Prosperity."
              - "Owns the federal share of the Canada Health Transfer and FPT relationships, the Canadian Drug Agency, the post-Trudeau pharmacare and dental-care implementation envelopes, and the federal role in non-insured health benefits for First Nations and Inuit (NIHB), plus regulatory oversight of medicines and devices."
              - "Hook: pharmacare implementation, dental care, drug pricing, FPT health funding, Indigenous health, federal regulation of medicines and devices, health-and-economic-prosperity framing land; province-bypassing framings do not."
          - Tone advice:
              - "Lead with pharmacare and dental-care implementation, drug pricing reform, FPT funding, Indigenous health, and health-economic-prosperity framing — these are the federal priorities of the Carney mandate."
              - "Do not pitch as if federal health were the operational buyer — Michel will route operational questions to provincial Ministers and the federal levers are framework and funding, not service delivery."
```

## 11. Out-of-band notes

For roles unfilled or interim.

## 12. Open questions

- Named Deputy Minister of Health and Associate Deputy Ministers under Michel with currency verified.
- Chief Public Health Officer of Canada and President of PHAC with currency verified.
- President of CIHR and CEO of CDA-AMC with currency verified.
- Provincial and territorial Ministers of Health for all 13 jurisdictions — particularly large jurisdictions (Ontario, Quebec, BC, Alberta).
- Chief Medical Officers of Health for all 13 jurisdictions with currency verified.
- Chair HESA and Chair SOCI (Senate) in the current Parliament after the 2025 election.
- Presidents of CMA, CNA, CPhA, CFPC and RCPSC with currency verified.
