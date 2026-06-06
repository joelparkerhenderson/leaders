# spec.md — `leaders.yml`

Single source of truth for the Mauritian health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Mauritius Ministry of Health and Wellness, the Pharmacy Board, Central Health Laboratory, five Regional Hospitals (Dr A G Jeetoo, Sir Seewoosagur Ramgoolam, Victoria, J Nehru, Flacq), and adjacent bodies.

The Mauritian system is tax-funded universal free at point of use through MoH facilities; substantial private sector and overseas referrals supplement. India-Mauritius bilateral health cooperation is structural.

## 2. Scope

In scope: President; PM; Minister of Health and Wellness; Permanent Secretary; CMO; Director Health Services; Director Pharmacy; CEOs of the five Regional Hospitals; Parliament Public Accounts Committee Chair where relevant to health; Medical Council of Mauritius.

## 3. Structure

Standard. Ordering: PM → Ministry → CMO → 5 Regional Hospitals → Pharmacy Board → Parliament Committee → Medical Council.

## 4. Field definitions

Party affiliation: `Labour Party` (Ramgoolam), `MSM` (Mouvement Socialiste Militant — Jugnauth), `MMM` (Mouvement Militant Mauricien), `PMSD`. Titles in English with French / Kreol.

## 5. Provenance and dating

Hon. Anil Kumar Bachoo GOSK has served as Minister of Health and Wellness since November 2024 in the Navin Ramgoolam (Labour Party-led Alliance du Changement) government following the November 2024 general election; born 6 September 1953; previously Vice-Prime Minister 2011-2014.

## 6. Update workflow

Verify against health.govmu.org, pmo.govmu.org, govmu.org, L'Express, Le Mauricien, Le Défi Plus, Lalit, Inside News.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Importing US framings — Mauritius is tax-funded universal Beveridgean.
- Ignoring overseas referral system — significant Mauritian patients travel to India for complex care.

## 9. Acronym glossary

- **GOSK** — Grand Officer of the Order of the Star and Key of the Indian Ocean.

## 10. Worked example

```yaml
      - Hon. Anil Kumar Bachoo, GOSK (Labour Party):
          - Title: Minister of Health and Wellness (since November 2024)
          - Stakeholder engagement notes:
              - "Minister of Health and Wellness since November 2024 in the Navin Ramgoolam Labour Party-led Alliance du Changement government following the November 2024 general election; Labour Party; born 6 September 1953; previously Vice-Prime Minister under Ramgoolam 2011-2014; long-time Labour Party figure."
              - "Active 2026: site visits at three hospitals across Mauritius (govmu.org); met Indian specialists on Reconstructive Surgery and Orthodontics (allAfrica August 2025); welcomed Urban Dodo launch with India High Commission; bilateral meetings with Indian Acting High Commissioner; CAJ News Africa April 2026 'Mauritius denounces attacks against doctors'."
              - "Owns Ministry policy, the 5 Regional Hospitals network, primary care through Area Health Centres and Community Health Centres, Pharmacy Board, Central Health Laboratory, overseas-referral system (significant flow to India), and Mauritius's WHO Africa, SADC, Indian Ocean Commission and Commonwealth health diplomacy."
              - "Hook: hospital modernisation, India-Mauritius cooperation, NCDs (Mauritius has one of the world's highest diabetes prevalences), mental health, Urban Dodo healthy-living initiative, SADC cooperation, and Indian Ocean Commission cooperation."
          - Tone advice:
              - "Open with hospital modernisation, NCDs, India-Mauritius cooperation and Indian Ocean cooperation — these are his authored 2025-2026 lines."
              - "Do not assume small-system framings — Mauritius's NCD burden, ageing population and economic position require sophisticated health-policy framings."
```

## 11. Out-of-band notes

For roles unfilled or in transition.

## 12. Open questions

- Named Permanent Secretary, CMO, Director Health Services with currency verified.
- CEOs of Dr A G Jeetoo, Sir Seewoosagur Ramgoolam, Victoria, J Nehru, Flacq Regional Hospitals.
- President Medical Council of Mauritius with currency verified.
