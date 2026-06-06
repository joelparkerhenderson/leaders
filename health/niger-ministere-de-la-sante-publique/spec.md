# spec.md — `leaders.yml`

Single source of truth for the Nigerien health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Niger Ministère de la Santé Publique, Hygiène Publique et Lutte contre les Endémies, ONPPC (Office National des Produits Pharmaceutiques et Chimiques), Centre National de Référence Hôpital National de Niamey, and adjacent bodies.

The Nigerien system is donor-coordinated tax-funded with limited universal coverage; MSP runs the public network through 8 régions médicales; the CNSP (Comité National pour la Sauvegarde de la Patrie) transition government emphasises souveraineté sanitaire and pharmaceutical localisation; Niger is in AES with Burkina Faso and Mali.

## 2. Scope

In scope: Président CNSP / Général Tiani; Premier Ministre; Ministre de la Santé Publique, Hygiène Publique et Lutte contre les Endémies; Secrétaire Général; Directeurs Centraux; DG ONPPC; Directeur Hôpital National de Niamey; Directeur Hôpital de l'Amitié Niger-Türkiye; Directeurs Régionaux Santé (8 régions); CNT Commission Santé; Ordre des Médecins du Niger.

## 3. Structure

Standard. Ordering: Présidence CNSP → Premier Ministre → MSP → ONPPC → Hôpitaux nationaux → 8 DRS → CNT → Ordre.

## 4. Field definitions

Transition government — no formal party affiliations; military and technocratic. Titles in French / English.

## 5. Provenance and dating

Médecin Colonel-Major Garba Hakimi serves as Ministre de la Santé Publique, Hygiène Publique et Lutte contre les Endémies in the CNSP transition government; military medical officer; active 2026 on souveraineté sanitaire, 7 milliards FCFA tariff reduction compensation, 6,000+ contractual health workers recruitment, Hajj 2026 health team, malaria mobilisation.

## 6. Update workflow

Verify against santé.gouv.ne, presidence.ne, anp.ne (Agence Nigérienne de Presse), Le Sahel, Niger Inter, NigerDiaspora.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Importing French / CEDEAO framings — Niger withdrew from CEDEAO January 2024.
- Ignoring AES context.

## 9. Acronym glossary

- **AES** — Alliance des États du Sahel.
- **CNSP** — Comité National pour la Sauvegarde de la Patrie.
- **CNT** — Conseil Consultatif de la Refondation (transitional).
- **MSP** — Ministère de la Santé Publique, Hygiène Publique et Lutte contre les Endémies.
- **ONPPC** — Office National des Produits Pharmaceutiques et Chimiques.

## 10. Worked example

```yaml
      - Médecin Colonel-Major Garba Hakimi:
          - Title: Ministre de la Santé Publique, Hygiène Publique et Lutte contre les Endémies (in the CNSP transition government)
          - Stakeholder engagement notes:
              - "Ministre de la Santé Publique dans le gouvernement de transition CNSP sous le Général Abdourahamane Tiani (au pouvoir depuis le coup d'État du 26 juillet 2023); médecin militaire (Colonel-Major); profil officiel via ANP."
              - "Active 2026 priorities: gouvernement a injecté près de 7 milliards de francs CFA pour compenser la réduction des tarifs de prestations dans les formations sanitaires publiques en 2025 (Le Sahel entretien exclusif); recrutement en 2026 de plus de 6,000 agents contractuels de santé annoncé à la Journée internationale des infirmiers (ANP, 11 mai 2026); appel à mobilisation contre le paludisme (ANP, Journée mondiale de lutte contre le Paludisme); missions de terrain dans les régions de Zinder, Diffa (N'Guigmi), Tillabéri (Chical, Wagou); visite Hôpital de l'Amitié Niger-Türkiye; équipe d'encadrement sanitaire du Hadj 2026."
              - "Owns MSP policy, souveraineté sanitaire strategy (NigerDiaspora coverage), ONPPC pharmaceutical management, Hôpital National de Niamey, 8 régions médicales, insurgency-affected régions (Tillabéri, Diffa, Tahoua), and AES diplomacy."
              - "Hook: souveraineté sanitaire, tariff reduction (7 milliards FCFA compensation), 6,000+ recruitment, malaria mobilisation, insurgency-affected regions, AES cooperation."
          - Tone advice:
              - "Ouvrir avec souveraineté sanitaire, recrutement, tariff reduction et coopération AES — sont les lignes autorales du gouvernement de transition."
              - "Ne pas pitcher en framings français traditionnels — CNSP government emphasises souveraineté and BRICS+ / Russie partnerships."
```

## 11. Out-of-band notes

For roles unfilled or in transition.

## 12. Open questions

- Named Secrétaire Général et Directeurs Centraux du MSP.
- DG ONPPC, Directeur Hôpital National de Niamey with currency verified.
- Directeurs Régionaux Santé des 8 régions — priorité Tillabéri, Diffa, Tahoua (insurgency-affected).
- CNT Commission Santé Chair with currency verified.
- Président Ordre des Médecins du Niger with currency verified.
