# spec.md — `leaders.yml`

Single source of truth for the Moroccan health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Moroccan Ministère de la Santé et de la Protection Sociale, ANAM (Agence Nationale de l'Assurance Maladie), CNSS, CNOPS (now AMO), Direction du Médicament et de la Pharmacie, Régions Sanitaires, CHU centres hospitaliers universitaires, and adjacent bodies.

Morocco has rolled out universal social health insurance (AMO — Assurance Maladie Obligatoire) covering the formal-sector workers via CNSS and civil servants via CNOPS, plus AMO Tadamon for the previously uninsured (formerly RAMED). The Royal Reform 2021-2025 announced universal coverage. The 2024 Health Reform Law (Loi-cadre 06.22) created Groupements Sanitaires Territoriaux (GST) — regional health authorities under decentralisation. Five CHU networks operate as tertiary backbone.

## 2. Scope

In scope: Roi (King Mohammed VI); Chef du Gouvernement; Ministre de la Santé et de la Protection Sociale; Secrétaires d'État; Secrétaire Général; Directeur de la Médecine; Directeur Hôpitaux et Soins Ambulatoires; Directeur ANAM; DG CNSS; DG CNOPS; Directeur DMP; Directeurs des Groupements Sanitaires Territoriaux (12 regions); Directeurs CHU (Ibn Sina Rabat, Ibn Rochd Casablanca, Hassan II Fès, Mohammed VI Marrakech, Mohammed VI Oujda, Souss-Massa Agadir); Présidents Commissions Parlementaires Santé Chambre des Représentants et Chambre des Conseillers; Conseil National de l'Ordre des Médecins; Ordre des Pharmaciens; Ordre des Infirmiers.

## 3. Structure

Standard. Ordering: Royal Cabinet → Gouvernement → Ministère de la Santé → ANAM → CNSS / CNOPS → DMP → GST → CHU → Parlement → Ordres.

## 4. Field definitions

Party affiliation using canonical Moroccan abbreviations: `RNI` (Rassemblement National des Indépendants — Akhannouch), `PAM` (Parti Authenticité et Modernité), `Istiqlal`, `USFP`, `PJD`, `MP`, `UC`, `PPS`. Titles in French / Arabic with English glosses.

## 5. Provenance and dating

Amine Tahraoui (RNI-aligned technocrat) has served as Ministre de la Santé et de la Protection Sociale since October 2024 in the second Akhannouch government, succeeding Khalid Aït Taleb. Pre-political background: chief of staff to the Minister of Agriculture under Akhannouch; investment banker at Attijari; Director General of Aksal Group; Secretary General of the Prime Minister's Office.

## 6. Update workflow

Verify against sante.gov.ma, cg.gov.ma, anam.ma, cnss.ma, cnops.org.ma, parlement.ma, Médias24, Yabiladi, L'Opinion, La Nouvelle Tribune, Le Matin (Maroc), Hespress.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating the Ministère as the only counterparty — AMO architecture distributes financing across CNSS, CNOPS and ANAM.
- Importing NHS framings unmodified — Morocco is universal mandatory insurance with public provider expansion.

## 9. Acronym glossary

- **AMO** — Assurance Maladie Obligatoire.
- **AMO Tadamon** — solidarity-financed coverage for previously RAMED population.
- **ANAM** — Agence Nationale de l'Assurance Maladie.
- **CHU** — Centre Hospitalier Universitaire.
- **CNOPS** — Caisse Nationale des Organismes de Prévoyance Sociale (civil-servant scheme).
- **CNSS** — Caisse Nationale de Sécurité Sociale.
- **DMP** — Direction du Médicament et de la Pharmacie.
- **GST** — Groupement Sanitaire Territorial (regional health authority under Loi-cadre 06.22).
- **RAMED** — Régime d'Assistance Médicale (former subsidised regime now AMO Tadamon).

## 10. Worked example

```yaml
      - Amine Tahraoui (RNI-aligned technocrat):
          - Title: Ministre de la Santé et de la Protection Sociale (since October 2024, in the second Akhannouch government)
          - Stakeholder engagement notes:
              - "Ministre de la Santé et de la Protection Sociale since October 2024 in the second Aziz Akhannouch (RNI) government, succeeding Pr Khalid Aït Taleb; pre-political background as chief of staff to the Minister of Agriculture under Akhannouch; investment banker at Attijari; Director General of Aksal Group; Secretary General of the PM's Office before the ministerial appointment — corporate-and-finance background unusual for a Moroccan Health Minister."
              - "Active 2026: announced 15 hospital projects to be delivered in 2026 across regions (La Nouvelle Tribune); launched new generation of hospitals and health centres in Drâa-Tafilalet south-east region in April 2026 to extend access to remote areas (Médias24); defended reforms before Parliament in March 2026 (Médias24, Yabiladi); promised a more modern health system."
              - "Owns the Loi-cadre 06.22 implementation creating Groupements Sanitaires Territoriaux as decentralised health authorities; AMO universalisation including AMO Tadamon; pharmacy and medicine reform via DMP; the five CHU network expansion (including Tanger CHU planned); coordination with CNSS and CNOPS; pharmaceutical local-manufacturing initiative."
              - "Hook: AMO universalisation, GST regional decentralisation, hospital infrastructure (15 new in 2026), CHU expansion, local pharmaceutical manufacturing, mental health and digital health land."
          - Tone advice:
              - "Open with AMO universalisation, GST decentralisation, hospital infrastructure delivery and CHU expansion — these are Tahraoui's sustained authored lines and the Royal Reform priorities."
              - "Do not pitch with a technocrat-only frame — Tahraoui is RNI-aligned and operates within the Akhannouch government's political logic; framings that ignore RNI political priorities (employment, investment, regional equality) will not resonate."
```

## 11. Out-of-band notes

For roles unfilled or in transition.

## 12. Open questions

- Named Secrétaire Général and Directeurs (Médecine, Hôpitaux et Soins Ambulatoires) of the Ministère with currency verified.
- Directeur ANAM, DG CNSS, DG CNOPS, Directeur DMP with currency verified.
- Directeurs des 12 GST with currency verified.
- Directeurs of CHU Ibn Sina Rabat, Ibn Rochd Casablanca, Hassan II Fès, Mohammed VI Marrakech, Mohammed VI Oujda, Souss-Massa Agadir.
- Présidents Commissions Parlementaires Santé Chambre des Représentants et Chambre des Conseillers.
- Présidents Ordre National des Médecins, Ordre des Pharmaciens, Ordre des Infirmiers with currency verified.
