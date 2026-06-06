# spec.md — `leaders.yml`

Single source of truth for the structure, semantics, and update rules of `leaders.yml` for the Luxembourg système de santé. The YAML must conform to this spec; if they disagree, the spec wins and the YAML is fixed.

## 1. Purpose

`leaders.yml` is an engagement register of named individuals in and around the Luxembourg health system. Each entry helps a reader inside the Ministère de la Santé et de la Sécurité sociale (M3S), the Caisse nationale de santé (CNS), the Direction de la Santé, the Laboratoire national de santé (LNS), the Inspection générale de la sécurité sociale (IGSS), a hôpital, or an adjacent body decide who to engage, how, and where.

The Luxembourg system is Bismarckian, financed by mandatory social insurance through the CNS, with the M3S setting policy. Care is delivered by four general hospital centres (CHL, CHEM, CHdN, HRS Robert Schuman) and specialist providers, contracted by the CNS. The Direction de la Santé is the medical-policy directorate of the Ministry; LNS provides public-health laboratory services.

## 2. Scope

**In scope:** Premier ministre; Ministre de la Santé et de la Sécurité sociale; Secrétaire d'État à la Santé where filled; Directeur de la Santé; Président du Comité directeur and Directeur de la CNS; Directeur du LNS; Directeur de l'IGSS; Présidents and Directeurs généraux of the four hospital centres (CHL, CHEM, CHdN, HRS); Président de la Commission Santé et sécurité sociale de la Chambre des députés; Président du Collège médical; Président de l'Association des médecins et médecins-dentistes (AMMD); Président de l'Association nationale des infirmiers et infirmières du Luxembourg; Président du Syndicat des pharmaciens.

**Out of scope:** operational staff below directeur level; vendors; historical post-holders.

## 3. Structure

```
Système de santé luxembourgeois — parties prenantes:
  - {Organisation}:
      - {Person}:
          - Title: ...
          - Stakeholder engagement notes: [...]
          - Tone advice: [...]
```

Indentation 2/6/10/14 spaces. Ordering: Gouvernement → M3S → Direction de la Santé → CNS → IGSS → LNS → four CH → Chambre des députés Commission Santé → professional bodies.

## 4. Field definitions

Standard family conventions. Party affiliation using canonical Luxembourg abbreviations: `CSV` (Chrëschtlech Sozial Vollekspartei), `DP` (Demokratesch Partei), `LSAP` (Lëtzebuerger Sozialistesch Aarbechterpartei), `déi gréng`, `ADR`, `déi Lénk`, `Piraten`, `Fokus`. Titles in French (or Luxembourgish where used officially) with English glosses.

## 5. Provenance and dating

Anchor facts to year, month or exact date. The Frieden government (CSV-DP coalition) was sworn in 17 November 2023. Martine Deprez (CSV) is Ministre de la Santé et de la Sécurité sociale since 17 November 2023. Treat any Ministère entry pre-dating 17 November 2023 as warranting re-verification.

## 6. Update workflow

1. Identify the change. 2. Verify against gouvernement.lu, m3s.gouvernement.lu, sante.public.lu, cns.lu, lns.lu, igss.gouvernement.lu, chd.lu, Wort, Tageblatt, Luxemburger Wort, Paperjam, Le Quotidien. 3. Apply minimum diff. 4. Confirm structure. 5. Re-validate cross-references.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating Luxembourg as a small system without specifics — its cross-border workforce (~50% of healthcare workers commute from France, Belgium, Germany) is a distinct engagement geometry.
- Importing NHS framings unmodified — Luxembourg is Bismarckian single-payer, with CNS as the universal commissioner.

## 9. Acronym glossary

- **AMMD** — Association des médecins et médecins-dentistes.
- **CHdN** — Centre Hospitalier du Nord (Ettelbruck).
- **CHEM** — Centre Hospitalier Émile Mayrisch (Esch-sur-Alzette).
- **CHL** — Centre Hospitalier de Luxembourg (Luxembourg city).
- **CNS** — Caisse nationale de santé.
- **HRS** — Hôpitaux Robert Schuman (Luxembourg city / Kirchberg).
- **IGSS** — Inspection générale de la sécurité sociale.
- **LNS** — Laboratoire national de santé.
- **M3S** — Ministère de la Santé et de la Sécurité sociale.

## 10. Worked example

```yaml
      - Martine Deprez (CSV):
          - Title: Ministre de la Santé et de la Sécurité sociale (Minister of Health and Social Security) (depuis le 17 novembre 2023)
          - Stakeholder engagement notes:
              - "Ministre de la Santé et de la Sécurité sociale dans le gouvernement Frieden (coalition CSV-DP) depuis le 17 novembre 2023; CSV; profil technique avec accent santé et sécurité sociale combinées dans un seul portefeuille."
              - "A représenté le Luxembourg à la 79e Assemblée mondiale de la santé à Genève en mai 2026, à la Conférence sur la santé mentale et l'inclusivité à Nicosie en janvier 2026, et au Conseil EPSCO en mars 2026."
              - "Pression budgétaire majeure: l'assurance maladie-maternité prévoit un déficit de 126,5 millions d'euros en 2026 — la stabilisation financière de la CNS est un dossier dominant."
              - "Owns la politique hospitalière, les conventions CNS, la santé mentale, la santé numérique, le PRR Luxembourg pour la santé, et la coordination transfrontalière (France, Belgique, Allemagne) sur la mobilité des patients et professionnels."
              - "Hook: déficit CNS, hôpitaux, santé mentale, professionnels de la santé transfrontaliers, e-santé (DSP, eSanté), et l'Initiative des petits États (Riga juin 2026) aterrissent."
          - Tone advice:
              - "Ouvrir avec déficit CNS, hôpitaux, santé mentale et coopération transfrontalière — ce sont ses dossiers de mandat dominants."
              - "Ne pas pitcher comme si CNS et M3S étaient une seule entité — la CNS est l'assureur statutaire avec son comité directeur propre; les framings centralistes seront ramenés à la structure bismarckienne."
```

## 11. Out-of-band notes

For roles unfilled or interim.

## 12. Open questions

- Named Directeur de la Santé and Directeurs des départements de la Direction de la Santé with currency verified.
- Président du Comité directeur and Directeur de la CNS with currency verified.
- Directeur du LNS and de l'IGSS with currency verified.
- Présidents and Directeurs généraux of CHL, CHEM, CHdN and HRS with currency verified.
- Président de la Commission Santé et sécurité sociale de la Chambre des députés in the current législature.
- Président du Collège médical, AMMD, Association nationale des infirmiers et infirmières du Luxembourg, and Syndicat des pharmaciens with currency verified.
