# spec.md — `leaders.yml`

Single source of truth for the structure, semantics, and update rules of `leaders.yml` for the Greenland (Kalaallit Nunaat) health system. The YAML must conform to this spec; if they disagree, the spec wins and the YAML is fixed.

## 1. Purpose

`leaders.yml` is an engagement register of named individuals in and around the Greenland health system. Each entry helps a reader inside Naalakkersuisut (Government of Greenland), the Ministry of Health (Peqqissutsimut Naalakkersuisoqarfik), the national health service (Peqqissutsimut Sulinerit / Sundhedsvæsenet) operating out of Queen Ingrid Hospital (Dronning Ingrids Hospital, DIH) in Nuuk, or an adjacent body decide who to engage, how, and where.

The Greenland health system is tax-funded universal under devolved competence inherited at self-government in 2009. The Naalakkersuisoq for Health steers; the Sundhedsvæsenet runs hospitals, regional clinics (sundhedscentre) and primary care across five health regions (Sermersooq, Avannaata, Kujalleq, Qeqqata, Qeqertalik). Patients in need of specialist care are referred to Denmark under bilateral arrangements; some patients to Iceland. Telemedicine is a defining operational pillar because of geography. Greenland's relationship with the United States — heightened under the second Trump administration's 2025-2026 statements on US interest in Greenland — has health-policy implications, particularly around foreign health-research access.

## 2. Scope

**In scope:** Naalakkersuisut Siulittaasuat (Prime Minister); Naalakkersuisoq for Health (and where filled, for Persons with Disabilities); Departementschef in the Ministry of Health; CEO and Medical Director of Peqqissutsimut Sulinerit / Sundhedsvæsenet; Chief Doctor of Dronning Ingrids Hospital; Director of Inatsisartut Health Committee; representatives of professional bodies (Lægeforeningen for Læger i Grønland; Greenlandic Nurses' Association); Danish Ministerial counterparts where the bilateral patient-care, IT and education arrangements are material; Department of Health and Prevention liaison roles to WHO.

**Out of scope:** operational staff below afdelingsledelse / department-head level; vendors; historical post-holders.

## 3. Structure

```
Kalaallit Nunaani peqqissutsimut tunngaviusut / Greenland health stakeholders:
  - {Organisation}:
      - {Person}:
          - Title: ...
          - Stakeholder engagement notes: [...]
          - Tone advice: [...]
```

Indentation 2/6/10/14 spaces. Ordering: Naalakkersuisut → Ministry of Health → Sundhedsvæsenet (CEO, Medical Director) → Dronning Ingrids Hospital → regional health regions → Inatsisartut Health Committee → professional bodies → Danish-bilateral liaisons.

## 4. Field definitions

Standard family conventions. Party affiliation using canonical Greenlandic abbreviations: `IA` (Inuit Ataqatigiit), `S` (Siumut), `D` (Demokraatit), `N` (Naleraq), `A` (Atassut), `S+` (Siumut affiliates). Titles in Greenlandic (where used officially) and Danish, with English glosses.

## 5. Provenance and dating

Anchor facts to year, month or exact date. The Nielsen cabinet (Jens-Frederik Nielsen, Demokraatit) was formed in 2025. As of 2026, Anna Wangenheim is Minister of Health and Persons with Disabilities. The Trump-administration interest in Greenland from January 2025 has produced explicit Naalakkersuisut public statements rejecting US interest in using Greenlandic citizens as research subjects, including by the Minister of Health (May 2026).

## 6. Update workflow

1. Identify the change. 2. Verify against naalakkersuisut.gl, peqqik.gl, Sermitsiaq, KNR (Kalaallit Nunaata Radioa), Reuters, AP, BBC Arctic coverage. 3. Apply minimum diff. 4. Confirm structure. 5. Re-validate cross-references.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating the system as small without specifics — Greenland's geography (16 settlements with no road network) shapes service delivery uniquely.
- Importing US framings unmodified — Greenland is in the Realm of Denmark and follows a Scandinavian universalist tradition; framings imported from the US healthcare market will not land.

## 9. Acronym glossary

- **DIH** — Dronning Ingrids Hospital (Queen Ingrid Hospital, Nuuk).
- **Inatsisartut** — Parliament of Greenland.
- **KNR** — Kalaallit Nunaata Radioa (Greenland Broadcasting Corporation).
- **Naalakkersuisoq** — Member of the Greenland government (cabinet minister).
- **Naalakkersuisut** — Government of Greenland.
- **Peqqissutsimut Naalakkersuisoqarfik** — Ministry of Health (Greenlandic).
- **Peqqissutsimut Sulinerit / Sundhedsvæsenet** — the national health service.
- **Realm of Denmark** — the constitutional framework that includes Denmark, the Faroe Islands and Greenland.

## 10. Worked example

```yaml
      - Anna Wangenheim:
          - Title: Naalakkersuisoq for Health and Persons with Disabilities (Minister of Health and Persons with Disabilities) (in the Nielsen cabinet)
          - Stakeholder engagement notes:
              - "Naalakkersuisoq for Health and Persons with Disabilities in the Jens-Frederik Nielsen (Demokraatit) cabinet formed 2025; portfolio combines health and disability into a single ministerial brief, reflecting small-population system architecture."
              - "Public statement May 2026: Greenlanders are not 'guinea pigs' for US research interests — explicit rejection of suggestions that US-administration-aligned research could use Greenlandic citizens; positioned health policy as a sovereignty question in the Trump-administration context."
              - "Owns operational steering of Sundhedsvæsenet (Peqqissutsimut Sulinerit), the bilateral patient-care arrangements with Denmark (referrals to Rigshospitalet and other Danish CHU equivalents), and telemedicine programmes to remote settlements."
              - "Hook: telemedicine, mental health and suicide prevention (a recurring policy priority), substance abuse, maternal and child health, Inuit cultural-adapted care models, bilateral DK-GL arrangements, and sovereignty-in-research land."
          - Tone advice:
              - "Lead with telemedicine, mental health and suicide prevention, Inuit cultural-adapted care, and bilateral DK-GL arrangements — these are the operational and political priorities of the small-population health system."
              - "Do not pitch as if Greenland were a US-market segment — Wangenheim has made the sovereignty-in-research point explicitly; US-style framings will be politically charged in the current Trump-administration period."
```

## 11. Out-of-band notes

For roles unfilled or interim. Useful for the bilateral Denmark-Greenland health-cooperation liaison roles where the named individual on the Danish side rotates with Danish cabinet changes.

## 12. Open questions

- Named Departementschef in the Ministry of Health under Wangenheim with currency verified.
- CEO and Medical Director of Sundhedsvæsenet / Peqqissutsimut Sulinerit with currency verified.
- Chief Doctor (Lægefaglig direktør) of Dronning Ingrids Hospital with currency verified.
- Heads of the five regional health regions (Sermersooq, Avannaata, Kujalleq, Qeqqata, Qeqertalik).
- Inatsisartut Health Committee chair and members in the current valgperiode.
- Greenland members of the Rigsfællesskab health-coordination bodies and the WHO Europe Greenland focal point.
