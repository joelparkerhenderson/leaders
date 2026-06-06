# spec.md — `leaders.yml`

Single source of truth for the Somali health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Somali Federal Ministry of Health and Human Services (MoHHS), the Federal Member State (FMS) Ministries of Health (Puntland, Jubaland, South West, Galmudug, Hirshabeelle), and Somaliland Ministry of Health Development (de facto, not internationally recognised). The Somali system is highly federalised, security-affected, and heavily donor-co-funded.

## 2. Scope

In scope: President of the Federal Government of Somalia; Federal Minister of Health and Human Services; Federal State Ministers of Health (each FMS); Somaliland Minister of Health Development; Director-General Federal MoHHS; Federal Parliament Health Committee.

Out of scope: hospital directors; district health officers.

## 3. Structure

Standard 2/6/10/14 indentation. Top-level key: `Somali health stakeholders:`. Ordering: Federal Government → Federal Member States → Somaliland note → Federal Parliament.

## 4. Field definitions

Party affiliation: contemporary Somali politics is clan-and-coalition based (Union for Peace and Development under HSM, Forward Somalia, Wadajir). Titles in English. For Somaliland: `Kulmiye`, `Waddani`, `UCID`.

## 5. Provenance and dating

Anchor to year, month or date. Dr. Ali Haji Adam Abubakar has served as Federal Minister of Health and Human Services in the Hassan Sheikh Mohamud (HSM) administration; verify currency against the Office of the Prime Minister and the Federal MoHHS.

## 6. Update workflow

Verify against moh.gov.so, villasomalia.gov.so, opm.gov.so, somaliland.gov.so (Somaliland), Hiiraan Online, Garowe Online, Goobjoog, Radio Dalsan, Somali Public Agenda.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating Somalia as a unitary jurisdiction — the Federal Government and the Federal Member States operate distinct health administrations under the Provisional Constitution; Somaliland operates a separate de facto administration in the north.
- Ignoring the security context — large parts of South-Central Somalia have access constraints due to Al-Shabaab presence; framings that assume universal access are inaccurate.
- Excluding Somaliland — Somaliland is not internationally recognised but is a substantive health-system administration in the north with its own MoHD.

## 9. Acronym glossary

- **FMS** — Federal Member State.
- **FGS** — Federal Government of Somalia.
- **HSM** — Hassan Sheikh Mohamud (President).
- **MoHHS** — Ministry of Health and Human Services (Federal).
- **MoHD** — Ministry of Health Development (Somaliland).

## 10. Worked example

```yaml
      - Dr. Ali Haji Adam Abubakar:
          - Title: Federal Minister of Health and Human Services
          - Stakeholder engagement notes:
              - "Federal Minister of Health and Human Services in the Hassan Sheikh Mohamud administration; verify currency against villasomalia.gov.so."
              - "Owns FGS MoHHS policy and budget, Banadir Regional Hospital, Erdogan Hospital and other Mogadishu facilities, coordination with FMS Ministries of Health, donor coordination (WHO, UNICEF, Global Fund, Gavi, World Bank, EU, FCDO, Turkish bilateral), and the security-affected access architecture."
              - "Hook: PHC and Essential Package of Health Services rollout, polio surveillance and immunisation, mpox and outbreak preparedness, maternal-and-child mortality reduction, and federal-state coordination land."
          - Tone advice:
              - "Open with EPHS, polio, outbreak preparedness, maternal-and-child mortality and federal-state coordination — these are MoHHS priorities."
              - "Do not assume unitary jurisdiction or open access — federal-FMS distribution and security constraints are central."
```

## 11. Out-of-band notes

Somaliland MoHD operates independently in the north and should be treated as a separate de facto administration.

## 12. Open questions

- FMS Ministers of Health (Puntland, Jubaland, South West, Galmudug, Hirshabeelle) with currency verified.
- Somaliland Minister of Health Development with currency verified.
- Federal Parliament Health Committee Chair with currency verified.
