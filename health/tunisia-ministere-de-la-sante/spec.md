# spec.md — `leaders.yml`

Single source of truth for the Tunisian health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Tunisian Ministère de la Santé (وزارة الصحة), CNAM (Caisse Nationale d'Assurance Maladie), Pharmacie Centrale de Tunisie (PCT), DPM (Direction de la Pharmacie et du Médicament), CHU centres hospitaliers universitaires, and adjacent bodies.

The Tunisian system has a universal social health insurance through CNAM covering ~85% of the population with public facilities (CHUs, regional hospitals, dispensaires) and contracted private providers; out-of-pocket spending remains significant. Tunisia is a regional reference for medical training and pharmaceutical manufacturing.

## 2. Scope

In scope: Président; Chef du Gouvernement; Ministre de la Santé; Secrétaires d'État; Directeurs Centraux; PDG CNAM; PDG Pharmacie Centrale de Tunisie; Directeur de la Pharmacie et du Médicament; Directeur Centre National de Pharmacovigilance; Directeurs CHU (La Rabta, Charles Nicolle, Sahloul Sousse, Fattouma Bourguiba Monastir, Hédi Chaker Sfax); Présidents Commissions Santé ARP; Conseil National de l'Ordre des Médecins; SNAP (Syndicat National des Pharmaciens d'Officine); Conseil de l'Ordre des Infirmiers.

## 3. Structure

Standard. Ordering: Présidence → Chef du Gouvernement → Ministère de la Santé → CNAM → PCT → DPM → CHU → ARP → Ordres.

## 4. Field definitions

Party affiliation: post-2021 the Saïed-led government dissolved Parliament and operates with technocratic appointees; no dominant party. Titles in French / Arabic with English glosses.

## 5. Provenance and dating

Dr. Mustapha Ferjani has served as Ministre de la Santé since August 2024 appointment by President Kais Saïed; previously ministerial adviser to the President 2022-2024; founder and president of the Tunisian health simulation society; published scientific works.

## 6. Update workflow

Verify against santetunisie.rns.tn, pm.gov.tn, cnam.nat.tn, arp.tn, La Presse de Tunisie, Le Quotidien, Mosaïque FM, WebManagerCenter, Réalités Magazine, allAfrica, Tap.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating the Ministère as the only buyer — CNAM is the financing axis for many specialist and outpatient services.
- Importing NHS framings unmodified — Tunisia is universal social insurance with mixed delivery.

## 9. Acronym glossary

- **ARP** — Assemblée des Représentants du Peuple.
- **CNAM** — Caisse Nationale d'Assurance Maladie.
- **DPM** — Direction de la Pharmacie et du Médicament.
- **PCT** — Pharmacie Centrale de Tunisie.

## 10. Worked example

```yaml
      - Dr. Mustapha Ferjani:
          - Title: Ministre de la Santé (since August 2024, under President Kais Saïed)
          - Stakeholder engagement notes:
              - "Ministre de la Santé designated by President Kais Saïed in a ministerial reshuffle announced August 2024; previously ministerial adviser to the President 2022-2024; founder and president of the Tunisian health simulation society; published numerous scientific works; clinical-academic background unusual for Tunisian political appointments."
              - "Active 2026: announced 'chaque citoyen aura bientôt un dossier médical numérique unique' (La Presse 15 May 2026); multiplied bilateral meetings in Geneva at 79th World Health Assembly (La Presse 20 May 2026); plaidoyer for global health sovereignty and equitable care access (WebManagerCenter); defended One Health approach in Lyon (April 2026); plaidoyer for systemic medicine reform and reinforced health sovereignty (Réalités Magazine 8e Forum de l'Officine)."
              - "Owns Ministère policy, CNAM coordination, PCT pharmaceutical management, DPM regulation, CHU network governance, digital health record initiative, pharmaceutical localisation, oncology national programmes, and Tunisia's WHO EMRO and Arab League positioning."
              - "Hook: dossier médical numérique unique, pharmaceutical sovereignty, One Health, CHU modernisation, oncology programmes, and WHO multilateral diplomacy land."
          - Tone advice:
              - "Open with digital health record, pharmaceutical sovereignty, One Health and WHO diplomacy — these are his sustained authored 2026 lines."
              - "Do not pitch politically partisan framings — the Saïed government operates technocratic-administrative; framings should respect the technocratic-clinical-academic frame Ferjani embodies."
```

## 11. Out-of-band notes

For roles unfilled or in transition.

## 12. Open questions

- Named Secrétaires d'État and Directeurs Centraux under Ferjani with currency verified.
- PDG CNAM, PDG PCT, Directeur DPM, Directeur Centre National de Pharmacovigilance with currency verified.
- Directeurs CHU La Rabta, Charles Nicolle, Sahloul Sousse, Fattouma Bourguiba Monastir, Hédi Chaker Sfax with currency verified.
- Présidents Commissions Santé ARP in the current Parliament.
- Président Conseil National de l'Ordre des Médecins, SNAP, Conseil de l'Ordre des Infirmiers with currency verified.
