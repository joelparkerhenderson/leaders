# spec.md — `leaders.yml`

Single source of truth for the Surinamese health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around Suriname's Ministerie van Volksgezondheid, BOG (Bureau voor Openbare Gezondheidszorg), state hospitals, and adjacent bodies.

Suriname operates a mixed system: state social health insurance via SZF (Staatsziekenfonds) covers public-sector workers and dependents; the private sector and other funds cover other segments; the Ministry runs hinterland medical services through the Medische Zending. The 2019 Basiszorgwet aimed at universal health insurance.

## 2. Scope

In scope: President; Minister van Volksgezondheid; Permanente Vertegenwoordiger / Directeur; Directeur BOG; SZF Directeur; Medische Zending Directeur; Directeurs of Academisch Ziekenhuis Paramaribo, 's Lands Hospitaal, St Vincentius Ziekenhuis; National Assembly Health Committee Chair; President Vereniging van Medici in Suriname (VMS).

## 3. Structure

Standard 2/6/10/14 indentation. Ordering: Regering → Ministerie → BOG → SZF → Medische Zending → ziekenhuizen → DNA Health Committee → VMS.

## 4. Field definitions

Party affiliation using canonical Surinamese abbreviations: `VHP` (Vooruitstrevende Hervormings-Partij), `NDP` (Nationale Democratische Partij), `ABOP` (Algemene Bevrijdings- en Ontwikkelings Partij), `PL` (Pertjajah Luhur), `NPS` (Nationale Partij Suriname). Titles in Dutch (or Sranan where used officially) with English glosses.

## 5. Provenance and dating

Anchor facts to year, month or exact date. The Santokhi (VHP) government has been in office since 2020 and won re-election in 2025. Minister van Volksgezondheid identity to be verified — Amar Ramadhin (VHP) was Health Minister from 2020 in the first Santokhi term; the current Minister of Health in the second Santokhi term requires verification.

## 6. Update workflow

Verify against gov.sr, dna.sr, Suriname Herald, Starnieuws, De Ware Tijd, Times of Suriname.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating Suriname as small without specifics — the hinterland (Medische Zending) operates a distinctive model in Maroon and Indigenous areas.
- Importing NHS framings unmodified — Suriname has a multi-payer mixed model with the public Staatsziekenfonds as a core component.

## 9. Acronym glossary

- **BOG** — Bureau voor Openbare Gezondheidszorg.
- **DNA** — De Nationale Assemblée.
- **Medische Zending** — interior-region medical-mission service run by churches under Ministry contract.
- **SZF** — Staatsziekenfonds.

## 10. Worked example

```yaml
      - Notes on Minister van Volksgezondheid:
          - Status: Currentidentity of the Minister van Volksgezondheid in the second Santokhi government (sworn in after the 2025 election) to be verified. Amar Ramadhin (VHP), who served 2020-2025, may have been retained, replaced, or succeeded — official Suriname government communications should be consulted.
          - Implication: Engagement should be routed through the Permanent Secretary (Permanente Vertegenwoordiger) or Director of the Ministerie van Volksgezondheid until a substantive Minister is publicly confirmed and added to this register.
```

## 11. Out-of-band notes

The above Notes block is used because the substantive identity of the current Minister of Health is not yet verifiable in this register.

## 12. Open questions

- Confirm identity, party affiliation and swearing-in date of the current Minister van Volksgezondheid in the second Santokhi government.
- Director BOG, SZF Directeur, Medische Zending Directeur with currency verified.
- Directeur Academisch Ziekenhuis Paramaribo, 's Lands Hospitaal, St Vincentius Ziekenhuis.
- DNA Health Committee Chair in the current legislative term.
- President Vereniging van Medici in Suriname (VMS).
