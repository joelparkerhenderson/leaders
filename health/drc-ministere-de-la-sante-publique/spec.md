# spec.md — `leaders.yml`

Single source of truth for the DRC health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Démocratique République du Congo Ministère de la Santé Publique, Hygiène et Prévoyance Sociale, Programme Élargi de Vaccination, Institut National de Recherche Biomédicale (INRB), Programme National de Lutte contre le Sida (PNLS), and adjacent bodies.

The Congolese system is donor-coordinated tax-funded with limited universal-coverage rollout; 26 provincial Divisions Provinciales de la Santé and ~520 Zones de Santé deliver services. Major ongoing burdens: Ebola (Bundibugyo outbreak declared 15 May 2026), mpox, measles, cholera, conflict-related health needs in eastern provinces.

## 2. Scope

In scope: Président; Premier Ministre; Ministre de la Santé Publique, Hygiène et Prévoyance Sociale; Vice-Ministre; Secrétaire Général; DG INRB; DG PNLS; Directeur PEV; Médecin-Chef Hôpital Général de Référence de Kinshasa; Médecins-Chefs Divisions Provinciales de la Santé (26 provinces); Présidents Commission Santé Assemblée Nationale et Sénat; Ordre des Médecins du Congo; Ordre des Pharmaciens.

## 3. Structure

Standard. Ordering: Présidence → Primature → MSPHP → INRB → PNLS → PEV → 26 DPS → hôpitaux → Parlement → Ordres.

## 4. Field definitions

Party affiliation: `UDPS` (Union pour la Démocratie et le Progrès Social — Tshisekedi), `Lamuka`, `Ensemble pour la République`, `Union sacrée de la Nation` (coalition). Titles in French / English.

## 5. Provenance and dating

Roger Kamba serves as Ministre de la Santé Publique, Hygiène et Prévoyance Sociale; cardiologist; pediatrician; appointed by President Félix Tshisekedi under PM Judith Suminwa Tuluka (since 2024). Active 2026 leading Bundibugyo Ebola response: cases rose to 381 with 63 deaths by 4 June 2026 per Xinhua; described US Ebola travel restrictions as 'discriminatory' (Washington Times); warned of 'very high' Ebola lethality rate (Al Jazeera May 2026).

## 6. Update workflow

Verify against minisantepublique.gouv.cd, presidence.cd, primature.cd, parliament.cd, Radio Okapi, Politico CD, AfricaNews, Reuters Africa, AP Africa, Xinhua DRC.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Ignoring conflict context — eastern provinces (Nord-Kivu, Sud-Kivu, Ituri) face M23 and other armed-group dynamics affecting health delivery.
- Importing US framings — DRC is donor-funded with strong WHO Africa, Africa CDC, MSF and Gavi roles.

## 9. Acronym glossary

- **DPS** — Division Provinciale de la Santé.
- **INRB** — Institut National de Recherche Biomédicale.
- **MSPHP** — Ministère de la Santé Publique, Hygiène et Prévoyance Sociale.
- **PNLS** — Programme National de Lutte contre le Sida.

## 10. Worked example

```yaml
      - Roger Kamba (UDPS / Union sacrée):
          - Title: Ministre de la Santé Publique, Hygiène et Prévoyance Sociale (under President Tshisekedi, PM Judith Suminwa Tuluka)
          - Stakeholder engagement notes:
              - "Ministre de la Santé Publique, Hygiène et Prévoyance Sociale sous le Président Félix Tshisekedi (UDPS / Union sacrée de la Nation) et la Première ministre Judith Suminwa Tuluka; cardiologue et pédiatre; profil médical-académique."
              - "Active May-June 2026: leads Bundibugyo Ebola disease outbreak response declared 15 May 2026 (WHO-DRC joint statement); cases rose to 381 with 63 deaths by 4 June 2026 (Xinhua, The Star); warned of 'very high' Ebola lethality rate as toll hit 80 (Al Jazeera May 2026); 136 deaths reported (New Vision); 'Health Leaders Endorse Coordinated Action and Continuity of Essential Services During Ebola Response' (Africa CDC); described US Ebola travel restrictions as 'discriminatory' (Washington Times, Breitbart Africa, June 2026)."
              - "Owns Ministère policy, INRB virology and biomedical research (DRC has the most experienced Ebola response infrastructure in the world), PEV vaccination, PNLS HIV programmes (DRC second-largest HIV cohort in WHO Africa region), 26 DPS coordination, hôpitaux généraux de référence network, MSF and donor partnership coordination, and DRC's WHO Africa, Africa CDC, CEEAC and SADC health positioning."
              - "Hook: Ebola Bundibugyo response, INRB virology research, PEV vaccination (including measles, polio, COVID legacy), HIV / PEPFAR continuity post-2025 USAID changes, eastern-provinces conflict-affected health response, mpox and Marburg preparedness, Africa CDC cooperation."
          - Tone advice:
              - "Open with Ebola response, INRB virology, HIV continuity post-USAID, eastern conflict-affected health and Africa CDC — these are his sustained 2026 lines."
              - "Do not pitch as if US-DRC engagement were unproblematic — the US Ebola travel restrictions framing as 'discriminatory' is his political-public line; US-aligned framings will require careful diplomatic acknowledgment."
```

## 11. Out-of-band notes

For roles unfilled or in transition.

## 12. Open questions

- Named Vice-Ministre, Secrétaire Général, DG INRB, DG PNLS, Directeur PEV with currency verified.
- Médecins-Chefs of major hôpitaux généraux de référence (Hôpital Général de Référence de Kinshasa, Centre Hospitalier Monkole, Hôpital Sendwe Lubumbashi).
- Médecins-Chefs Divisions Provinciales de la Santé of the 26 provinces — priorité Nord-Kivu, Sud-Kivu, Ituri (conflict-affected), Kinshasa, Haut-Katanga.
- Présidents Commission Santé Assemblée Nationale et Sénat in the current legislature.
- Présidents Ordre des Médecins du Congo, Ordre des Pharmaciens du Congo.
