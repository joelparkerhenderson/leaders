# spec.md — `leaders.yml`

Single source of truth for the Bosnia and Herzegovina health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Federal Ministry of Health of the Federation of Bosnia and Herzegovina (Federalno ministarstvo zdravstva FBiH), Republika Srpska Ministry of Health and Social Welfare, Brčko District health services, and adjacent bodies.

The BiH health system is highly fragmented under the Dayton constitutional structure: the state-level Council of Ministers has limited health competence; the Federation of BiH operates through 10 cantons each with their own Ministry of Health and Cantonal Health Insurance Fund; Republika Srpska operates a centralised entity-level system with the Health Insurance Fund of RS; Brčko District operates separately. Reform is politically constrained by ethnic-cantonal politics.

## 2. Scope

In scope: State-level Council of Ministers (limited health competence); Federation of BiH PM and Federal Minister of Health; Republika Srpska Minister of Health and Social Welfare; Brčko District Health Department head; Cantonal Ministers of Health (10 cantons: USK, Posavski, Tuzla, Zenica-Doboj, Bosansko-Podrinjski, Srednjobosanski, HNK, ZHK, Sarajevski, Kanton 10); Director Sarajevo Clinical Center (UKCS); Director University Clinical Centre Banja Luka; Director Health Insurance Funds of FBiH cantons and RS; major hospital directors; Parliamentary Assembly committees.

## 3. Structure

Standard. Ordering: State Council of Ministers → Federal Minister of Health FBiH → 10 cantonal Ministers → RS Minister → Brčko District → UKCS / UKC Banja Luka → Health Insurance Funds.

## 4. Field definitions

Party affiliation: `SDA` (Stranka Demokratske Akcije — Bosniak), `HDZ BiH` (Croat), `SNSD` (Savez Nezavisnih Socijaldemokrata — RS Bosnian Serb), `SDS` (Srpska Demokratska Stranka), `Naša Stranka`, `Trojka` coalition, etc. Titles in Bosnian / Croatian / Serbian / English.

## 5. Provenance and dating

Nediljko Rimac (HDZ BiH-aligned) serves as Federal Minister of Health of the Federation of Bosnia and Herzegovina; identified as Minister on the Federal Ministry of Health official website (last updated 25 March 2026 per official source).

## 6. Update workflow

Verify against fbihvlada.gov.ba, vladars.net, vijeceministara.gov.ba, parlament.ba, Sarajevo Times, Klix, N1, BNN.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating the federal level as the operational owner — the 10 cantons of FBiH and RS run delivery.
- Importing US framings — BiH is highly fragmented Bismarckian SHI with multiple Cantonal Health Insurance Funds.

## 9. Acronym glossary

- **BiH** — Bosnia and Herzegovina.
- **FBiH** — Federation of Bosnia and Herzegovina (one of two entities).
- **RS** — Republika Srpska (one of two entities).
- **UKCS** — Univerzitetski Klinički Centar Sarajevo.

## 10. Worked example

```yaml
      - Nediljko Rimac (HDZ BiH-aligned):
          - Title: Federal Minister of Health, Federation of Bosnia and Herzegovina (per fbihvlada.gov.ba, currency to 25 March 2026)
          - Stakeholder engagement notes:
              - "Federal Minister of Health of the Federation of BiH per the official Federal Ministry of Health website (fbihvlada.gov.ba, last updated 25 March 2026); HDZ BiH-aligned by the cantonal-ethnic distribution arrangements of the post-2022-election coalition; medical-administrative background."
              - "Owns the Federal-level Ministry of Health policy (FBiH-level only), coordination with the 10 Cantonal Ministries of Health and their Cantonal Health Insurance Funds, articulation with the Republika Srpska Minister of Health, the Brčko District, and the State-level Council of Ministers on EU-accession and trans-entity matters."
              - "Hook: EU accession health-acquis alignment (Chapter 28), pharmaceutical regulation harmonisation, hospital sector financing reform, oncology and cardiology centres at UKCS, Sinopharm and other Chinese investment in BiH health (Sarajevo Times coverage), and SEEHN regional cooperation."
          - Tone advice:
              - "Open with EU acquis alignment, UKCS centres of excellence, cantonal-coordination and pharmaceutical regulation harmonisation — these are the federal-level levers within FBiH-level competence."
              - "Do not pitch as if BiH were a single national customer — Dayton-era fragmentation across two entities, ten cantons, Brčko District and the State-level Council of Ministers is structural; framings must respect the constitutional asymmetry."
```

## 11. Out-of-band notes

For roles unfilled or in transition.

## 12. Open questions

- Named Deputies and Secretaries in the FBiH Federal Ministry of Health under Rimac.
- Republika Srpska Minister of Health and Social Welfare with currency verified.
- Cantonal Ministers of Health for the 10 cantons with currency verified.
- Director UKCS Sarajevo, Director UKC Banja Luka, Director University Hospital Mostar with currency verified.
- Directors of the Cantonal Health Insurance Funds and RS Health Insurance Fund.
- Parliamentary Assembly health-related committee chairs.
