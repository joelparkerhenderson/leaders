# spec.md — `leaders.yml`

Single source of truth for the Samoan health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Samoa Ministry of Health (MoH) and adjacent bodies.

Samoa (Independent State of Samoa, formerly Western Samoa) is a parliamentary republic; the Fiamē Naomi Mataʻafa (FAST — Faʻatuatua i le Atua Samoa ua Tasi) government was in office from 2021; the political landscape has been turbulent in 2025 with parliamentary instability and possible early elections. Member of PIF, ACP, Commonwealth and PSIDS.

## 2. Scope

In scope: O le Ao o le Malo (Head of State); Prime Minister; Minister of Health; Director-General Tupua Tamasese Meaole Hospital; Legislative Assembly Committee.

Out of scope: district health officers.

## 3. Structure

Standard 2/6/10/14 indentation. Top-level key: `Samoan health stakeholders:`.

## 4. Field definitions

Party affiliation: `FAST` (Faʻatuatua i le Atua Samoa ua Tasi), `HRPP` (Human Rights Protection Party). Titles in English; Samoan chiefly titles (matai) may precede personal names.

## 5. Provenance and dating

Anchor to year, month or date. Verify the current Minister of Health against the Samoa Government and Samoa Observer; the cabinet has been recomposed during 2025 political reshuffles.

## 6. Update workflow

Verify against samoagovt.ws, parliament.gov.ws, Samoa Observer, Samoa News, RNZ Pacific.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Conflating Samoa with American Samoa — distinct sovereign vs US unincorporated territory.
- Ignoring the 2019 measles outbreak legacy — measles immunisation gaps remain a sustained policy frame.

## 9. Acronym glossary

- **FAST** — Faʻatuatua i le Atua Samoa ua Tasi.
- **HRPP** — Human Rights Protection Party.

## 10. Worked example

```yaml
      - Notes on Minister of Health of Samoa:
          - Status: Verify against samoagovt.ws.
          - Implication: Engagement requires recognition of post-2019-measles-outbreak immunisation rebuild, NCDs and climate-and-health.
          - Hook: NCDs, measles, MCH, climate-and-health, mental health.
          - Tone: Open with NCDs, immunisation, climate-and-health and PIF cooperation; distinguish from American Samoa.
```

## 11. Out-of-band notes

For roles unfilled or interim during 2025 political reshuffles.

## 12. Open questions

- Substantive identity of Minister of Health with currency verified.
