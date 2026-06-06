# spec.md — `leaders.yml`

Single source of truth for the Côte d'Ivoire health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Côte d'Ivoire Ministère de la Santé, de l'Hygiène Publique et de la Couverture Maladie Universelle (MSHPCMU), Caisse Nationale d'Assurance Maladie (CNAM), Pharmacie de la Santé Publique de Côte d'Ivoire (PSP), Direction de la Pharmacie et du Médicament, and adjacent bodies.

The Ivorian system implemented Couverture Maladie Universelle (CMU) through the Caisse Nationale d'Assurance Maladie (CNAM); MSHPCMU sets policy; CHU centres hospitaliers universitaires (Cocody, Treichville, Yopougon, Bouaké) provide tertiary care.

## 2. Scope

In scope: Président; Vice-Président; Premier Ministre; Ministre de la Santé, de l'Hygiène Publique et de la CMU; Secrétaires d'État; Directeurs Généraux; DG CNAM; DG PSP; Directeur Pharmacie et Médicament; Directeurs CHU Cocody, Treichville, Yopougon, Bouaké; Directeur Institut Pasteur de Côte d'Ivoire (IPCI); Présidents Commissions Santé Assemblée Nationale et Sénat; Ordre National des Médecins; Ordre National des Pharmaciens.

## 3. Structure

Standard. Ordering: Présidence → Primature → MSHPCMU → CNAM → PSP → DPM → CHU → IPCI → Parlement → Ordres.

## 4. Field definitions

Party affiliation: `RHDP` (Rassemblement des Houphouëtistes pour la Démocratie et la Paix — Ouattara), `PDCI-RDA`, `PPA-CI` (Gbagbo), `FPI`, `MGC`. Titles in French / English.

## 5. Provenance and dating

Pierre N'Gou Dimba serves as Ministre de la Santé, de l'Hygiène Publique et de la Couverture Maladie Universelle in the Patrick Achi / Robert Beugré Mambé / Robert Beugré Mambé government under President Alassane Ouattara; active 2026 on quality of care, sovereignty in health and technological innovation, maternal and child health and nutrition.

## 6. Update workflow

Verify against sante.gouv.ci, presidence.ci, primature.ci, gouv.ci, AIP (Agence Ivoirienne de Presse), Abidjan.net, Connection Ivoirienne, Fraternité Matin.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating MSHPCMU as buyer — CNAM administers CMU.
- Importing US framings — Côte d'Ivoire is universal-insurance-rolling-out with significant donor and partner coordination.

## 9. Acronym glossary

- **CMU** — Couverture Maladie Universelle.
- **CNAM** — Caisse Nationale d'Assurance Maladie.
- **IPCI** — Institut Pasteur de Côte d'Ivoire.
- **PSP** — Pharmacie de la Santé Publique.

## 10. Worked example

```yaml
      - Pierre N'Gou Dimba (RHDP):
          - Title: Ministre de la Santé, de l'Hygiène Publique et de la Couverture Maladie Universelle de Côte d'Ivoire
          - Stakeholder engagement notes:
              - "Ministre de la Santé, de l'Hygiène Publique et de la CMU de Côte d'Ivoire sous le Président Alassane Ouattara (RHDP) et le Premier ministre Robert Beugré Mambé; biographie sur sante.gouv.ci."
              - "Active 2026: a souhaité faire de la qualité des soins la priorité de 2026 (AIP, février 2026); appelle à construire des systèmes de santé inclusifs avec les nouvelles technologies et les innovations dans le cadre de la souveraineté sanitaire (Abidjan.net, mai 2026); a présenté la nouvelle Direction des Ressources Humaines de la Santé comme un levier de modernisation du système (AIP); depuis Genève (mai 2026), a réaffirmé l'engagement de la Côte d'Ivoire à faire de la nutrition un pilier central de sa politique de santé maternelle et infantile (Connection Ivoirienne); incident sécuritaire à Bôdô avec exfiltration."
              - "A partagé l'expérience ivoirienne avec la 5e cohorte du stage résidentiel du Programme Kofi Annan en Leadership en santé mondiale (Abidjan.net)."
              - "Owns Ministère policy, CNAM CMU administration, PSP pharmaceutical supply, IPCI public-health research, CHU network, et la diplomatie sanitaire de la Côte d'Ivoire à l'OMS Afrique, CEDEAO et UEMOA."
              - "Hook: CMU expansion, qualité des soins, ressources humaines de la santé, souveraineté sanitaire et innovations technologiques, nutrition maternelle et infantile, CEDEAO cooperation, Pasteur-IPCI mRNA-Africa programmes aterrissent."
          - Tone advice:
              - "Ouvrir avec CMU, qualité des soins, souveraineté sanitaire et nutrition maternelle-infantile — sont ses lignes autorales 2026."
              - "Ne pas pitcher en framings exclusivement Nord-Sud — la souveraineté sanitaire et la coopération africaine intra-régionale sont des cadres explicites."
```

## 11. Out-of-band notes

For roles unfilled or in transition.

## 12. Open questions

- Named Secrétaires d'État et Directeurs Généraux du Ministère.
- DG CNAM, DG PSP, Directeur Pharmacie et Médicament with currency verified.
- Directeurs CHU Cocody, Treichville, Yopougon, Bouaké with currency verified.
- Directeur IPCI with currency verified.
- Présidents Commissions Santé Assemblée Nationale et Sénat.
- Présidents Ordre National des Médecins, Ordre National des Pharmaciens.
