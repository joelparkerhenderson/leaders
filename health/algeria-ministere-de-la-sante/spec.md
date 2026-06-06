# spec.md — `leaders.yml`

Single source of truth for the Algerian health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Algerian Ministère de la Santé, CNAS (Caisse Nationale des Assurances Sociales), Saidal (state pharmaceutical company), and adjacent bodies.

The Algerian system is tax-and-payroll-funded universal, free at point of use for citizens, with CNAS administering social-security health benefits for formal-sector workers. The Ministry runs a network of CHU (Centres Hospitaliers Universitaires), EPH (Établissements Publics Hospitaliers), EPSP polyclinics, and 1,500+ primary care centres. Saidal is a state-owned biopharmaceutical major.

## 2. Scope

In scope: Président; Premier Ministre; Ministre de la Santé; Secrétaires d'État; Secrétaire Général; Directeurs Centraux; DG CNAS; PDG Saidal; Directeurs Régionaux de la Santé (48 wilayas); Directeurs CHU; Présidents Commissions Santé APN et Conseil de la Nation; Conseil National de l'Ordre des Médecins; SNAPO (pharmaciens).

## 3. Structure

Standard. Ordering: Présidence → Premier Ministère → Ministère de la Santé → CNAS → Saidal → DRS wilayas → CHU → APN / Conseil de la Nation → Ordres.

## 4. Field definitions

Party affiliation using canonical Algerian abbreviations: `FLN`, `RND`, `MSP`, `MPA`, `FM`, `MEN`, et al. Titles in French / Arabic with English glosses.

## 5. Provenance and dating

Mohamed Esseddik Aït Messaoudène serves as Ministre de la Santé following the Tebboune government reshuffle in 2025-2026; Abdelhak Saihi previously held the portfolio (now Minister of Labour, Employment and Social Security).

## 6. Update workflow

Verify against sante.gov.dz, premier-ministre.gov.dz, aps.dz, El Moudjahid, Liberté, El Watan, TSA Algérie, Algerie360.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating the Ministère as the only counterparty — CNAS handles formal-sector benefits and Saidal handles much pharmaceutical supply.
- Importing NHS framings unmodified — Algeria is universal tax-funded with significant pharmaceutical-localisation policy.

## 9. Acronym glossary

- **APN** — Assemblée Populaire Nationale.
- **CHU** — Centre Hospitalier Universitaire.
- **CNAS** — Caisse Nationale des Assurances Sociales des Travailleurs Salariés.
- **DRS** — Direction Régionale de la Santé (wilaya).
- **EPH** — Établissement Public Hospitalier.
- **EPSP** — Établissement Public de Santé de Proximité.
- **Saidal** — state biopharmaceutical company.
- **SNAPO** — Syndicat National Algérien des Pharmaciens d'Officine.

## 10. Worked example

```yaml
      - Mohamed Esseddik Aït Messaoudène:
          - Title: Ministre de la Santé (in the Tebboune government, following 2025-2026 reshuffle)
          - Stakeholder engagement notes:
              - "Ministre de la Santé in the President Abdelmadjid Tebboune government following a ministerial reshuffle; replaced Abdelhak Saihi who moved to the Travail / Labour, Employment and Social Security portfolio; assumed responsibilities with the public commitment to 'be up to the aspirations of the Algerian State' (El Moudjahid)."
              - "Owns Ministère policy and the network of CHU, EPH, EPSP, polyclinics; coordination with CNAS on insurance benefits and with Saidal on local pharmaceutical production; Algerian pharmaceutical-localisation policy; oncology national programmes; primary-care strengthening; African and Arab health-cooperation."
              - "Hook: pharmaceutical localisation via Saidal, oncology national programme, hospital infrastructure modernisation, primary-care strengthening, maternal-and-child health, NCDs, climate-and-health, and African and BRICS+ cooperation land."
          - Tone advice:
              - "Open with pharmaceutical localisation, hospital modernisation and African / BRICS+ cooperation — these are the Tebboune-era policy framings."
              - "Do not pitch with French-cultural-default framings — Algeria's policy lexicon is in French and Arabic but politically distinct from former colonial-tied positioning; framings that acknowledge Algerian sovereignty and the BRICS+ partnership context will resonate better."
```

## 11. Out-of-band notes

For roles unfilled or in transition.

## 12. Open questions

- Confirm Mohamed Esseddik Aït Messaoudène's date of appointment and political profile under Tebboune.
- Named Secrétaire Général and Directeurs Centraux du Ministère with currency verified.
- DG CNAS and PDG Saidal with currency verified.
- Directeurs des 48 Directions Régionales de la Santé and Directeurs CHU (Mustapha Pacha, Frantz Fanon, Beni Messous, Constantine, Oran, Annaba, Tizi Ouzou).
- Présidents des Commissions Santé APN et Conseil de la Nation.
- Président Conseil National de l'Ordre des Médecins, SNAPO, et autres ordres avec actualité vérifiée.
