# spec.md — `leaders.yml`

Single source of truth for the Namibian health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Namibian Ministry of Health and Social Services (MoHSS), the Namibia Medicines Regulatory Council (NMRC), and adjacent bodies.

Namibia operates a two-tier system: a public network of intermediate, district and primary hospitals plus clinics under MoHSS serving the majority; and a private network (Welwitschia, Mediclinic, Lady Pohamba) serving formal-sector employees through PSEMAS and private medical aid funds. The country is under the SWAPO government of President Netumbo Nandi-Ndaitwah (since 21 March 2025 — first woman President of Namibia).

## 2. Scope

In scope: President; Vice President; Minister of Health and Social Services; Deputy Minister; Executive Director (Permanent Secretary); Registrar NMRC; Chief Health Programmes Officer; Parliamentary Standing Committee on Human Resources, Social and Community Development; Medical Association of Namibia (MAN).

Out of scope: regional health directorate heads; hospital superintendents.

## 3. Structure

Standard 2/6/10/14 indentation. Top-level key: `Namibian health stakeholders:`. Ordering: Presidency → MoHSS → NMRC → Parliament → professional associations.

## 4. Field definitions

Party affiliation: `SWAPO` (South West Africa People's Organisation, ruling since independence in 1990), `IPC` (Independent Patriots for Change, principal opposition), `PDM` (Popular Democratic Movement), `LPM` (Landless People's Movement), `AR` (Affirmative Repositioning). Independent for non-aligned. Titles in English.

## 5. Provenance and dating

Anchor to year, month or date. Dr. Esperance Luvindao was sworn in as Minister of Health and Social Services on 22 March 2025 by President Netumbo Nandi-Ndaitwah; at 34 years old she is the youngest health minister in Namibian history and among the youngest globally; born in the Democratic Republic of the Congo; Namibian by naturalisation; medical doctor.

## 6. Update workflow

Verify against mhss.gov.na, op.gov.na, parliament.na, The Namibian, New Era, Namibian Sun, Windhoek Observer.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating Namibia as part of South Africa's NHI orbit — Namibia operates an independent health system with its own architecture, and is not part of the South African NHI; framings that assume SA-NHI alignment are inaccurate.
- Conflating PSEMAS (the Public Service Employee Medical Aid Scheme) with the MoHSS public system — PSEMAS purchases private care for civil servants and is administered separately; framings that bundle them confuse the structure.
- Ignoring the 2025 presidential transition — Namibia transitioned to its first woman President (Nandi-Ndaitwah) in March 2025 following President Hage Geingob's death in office; the cabinet, including health, is materially recomposed.

## 9. Acronym glossary

- **IPC** — Independent Patriots for Change.
- **MAN** — Medical Association of Namibia.
- **MoHSS** — Ministry of Health and Social Services.
- **NMRC** — Namibia Medicines Regulatory Council.
- **PSEMAS** — Public Service Employee Medical Aid Scheme.
- **SWAPO** — South West Africa People's Organisation.

## 10. Worked example

```yaml
      - Dr. Esperance Luvindao (SWAPO):
          - Title: Minister of Health and Social Services (since 22 March 2025)
          - Stakeholder engagement notes:
              - "Sworn in as Minister of Health and Social Services on 22 March 2025 by President Netumbo Nandi-Ndaitwah, the first woman President of Namibia; at 34 years old, the youngest health minister in Namibian history and among the youngest in Africa; medical doctor; born in the Democratic Republic of the Congo, Namibian by naturalisation; SWAPO-aligned."
              - "Owns MoHSS policy and budget, the intermediate hospital network (Windhoek Central, Katutura, Oshakati, Rundu, Onandjokwe), the district hospitals and primary-care clinic network across the fourteen regions, NMRC oversight, the HIV/AIDS programme (Namibia is a sustained PEPFAR partner with very high coverage), and SADC health diplomacy."
              - "Hook: HIV continuity and sustainability, maternal and child health, NCDs, mental health, rural-service delivery (Namibia's geography poses access challenges), HR retention, and the Nandi-Ndaitwah presidential modernisation agenda land."
          - Tone advice:
              - "Open with HIV continuity, maternal and child health, NCDs, mental health, rural delivery and the presidential modernisation agenda — these are Luvindao's first-term priorities and the SWAPO-Nandi-Ndaitwah direction of travel."
              - "Do not assume South African NHI alignment or PSEMAS-MoHSS unity — Namibia is institutionally distinct from South Africa; PSEMAS is administratively separate from MoHSS service provision; framings that bundle them will be corrected."
```

## 11. Out-of-band notes

For roles unfilled or interim.

## 12. Open questions

- Named Deputy Minister and Executive Director (Permanent Secretary) with currency verified.
- Registrar NMRC with currency verified.
- Parliamentary Standing Committee Chair with currency verified.
