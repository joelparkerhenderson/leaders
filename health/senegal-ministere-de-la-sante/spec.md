# spec.md — `leaders.yml`

Single source of truth for the Senegalese health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Sénégal Ministère de la Santé et de l'Action Sociale, Agence Nationale de la Couverture Maladie Universelle (ANACMU), Direction de la Pharmacie et du Médicament, Institut Pasteur Dakar, and adjacent bodies.

The Sénégal system has Couverture Maladie Universelle (CMU) covering the previously uninsured population; civil servants and formal-sector workers have other arrangements (IPM); Ministry runs national hospitals and regional structures. Pasteur Institute Dakar is a regional reference and pioneer of mRNA-Africa manufacturing.

## 2. Scope

In scope: Président; Premier Ministre; Ministre de la Santé et de l'Action Sociale; Directeurs Centraux; DG ANACMU; Directeur Pharmacie et Médicament; Directeur Institut Pasteur Dakar; Directeurs CHU (Aristide Le Dantec — currently being rebuilt; Fann; Le Dantec); Médecins-Chefs Régions Médicales (14 regions); Assemblée Nationale Commission Santé Chair; Ordre National des Médecins; Ordre National des Pharmaciens.

## 3. Structure

Standard. Ordering: Présidence → Primature → Ministère → ANACMU → DPM → Institut Pasteur Dakar → CHU → 14 régions médicales → Ordres.

## 4. Field definitions

Party affiliation: `Pastef-Les Patriotes` (Sonko / Diomaye), `APR` (Alliance pour la République, Macky Sall), `PS`, `AFP`, opposition coalitions. Titles in French / Wolof / English.

## 5. Provenance and dating

Dr. Ibrahima Sy serves as Ministre de la Santé, Hygiène Publique et de l'Action Sociale; reconfirmed in the new government formed 1 June 2026 under PM Ahmadou Al Aminou Lo (Pastef-Les Patriotes / Diomaye Faye government); academic public health expert; Master Assistant since 2017 at the Department of Geography of UCAD Dakar; associate researcher at CSE; previous research experience in Mauritania, Côte d'Ivoire and Switzerland.

## 6. Update workflow

Verify against sante.gouv.sn, primature.sn, presidence.sn, assemblee-nationale.sn, APS Sénégal, Le Soleil, Sud Quotidien, Pressafrik.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating Ministère as buyer — ANACMU manages CMU.
- Importing US framings — Sénégal is mixed-coverage with significant donor coordination.

## 9. Acronym glossary

- **ANACMU** — Agence Nationale de la Couverture Maladie Universelle.
- **CMU** — Couverture Maladie Universelle.
- **CSE** — Centre de Suivi Écologique.
- **IPM** — Institutions de Prévoyance Maladie.
- **UCAD** — Université Cheikh Anta Diop, Dakar.

## 10. Worked example

```yaml
      - Dr. Ibrahima Sy (Pastef-Les Patriotes / Diomaye):
          - Title: Ministre de la Santé, de l'Hygiène publique et de l'Action sociale (reconfirmed in the new government of 1 June 2026)
          - Stakeholder engagement notes:
              - "Ministre de la Santé reconfirmed in the new government formed 1 June 2026 under Premier ministre Ahmadou Al Aminou Lo in the Bassirou Diomaye Faye (Pastef-Les Patriotes) presidency; academic public health expert; Master Assistant since 2017 at the Department of Geography of UCAD Dakar; associate researcher at CSE (Centre de Suivi Écologique); prior research experience at institutions in Mauritania, Côte d'Ivoire and Switzerland."
              - "Owns Ministère policy, ANACMU coordination of CMU, Direction de la Pharmacie et du Médicament regulation, Institut Pasteur Dakar (Pasteur Institute Dakar — mRNA-Africa Madiba vaccine manufacturing initiative), CHU and régional hospital network, 14 régional medical offices, and Sénégal's WHO Africa, ECOWAS and OIF positioning."
              - "Hook: CMU expansion, Pasteur Institute Dakar mRNA-vaccine manufacturing (Madiba), CHU Aristide Le Dantec reconstruction, public-health research integration (his academic background), mpox / Lassa / Marburg outbreak preparedness, and ECOWAS regional cooperation land."
          - Tone advice:
              - "Open with CMU, Pasteur Institute Madiba mRNA initiative, CHU Le Dantec reconstruction and public-health research — these align with his academic background and the Diomaye-Pastef souveraineté sanitaire framing."
              - "Do not pitch France-aligned defaults — the Pastef government has emphasised souveraineté and BRICS+ / Sahel partnerships; France-aligned defaults will be politically misaligned."
```

## 11. Out-of-band notes

For roles unfilled or in transition.

## 12. Open questions

- Named Directeurs Centraux du Ministère under Sy with currency verified.
- DG ANACMU, Directeur Pharmacie et Médicament, Directeur Institut Pasteur Dakar with currency verified.
- Directeurs of CHU (Aristide Le Dantec, Fann, Dalal Jamm, Albert Royer, Principal de Dakar) with currency verified.
- Médecins-Chefs of the 14 régions médicales.
- Assemblée Nationale Commission Santé Chair.
- Présidents Ordre National des Médecins, Ordre National des Pharmaciens with currency verified.
