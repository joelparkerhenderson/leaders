# spec.md — `leaders.yml`

Single source of truth for the Malian health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Mali Ministère de la Santé et du Développement Social, Caisse Nationale d'Assurance Maladie (CNAM), Pharmacie Populaire du Mali, Institut National de Santé Publique (INSP), and adjacent bodies.

The Malian system is donor-coordinated tax-funded with limited universal coverage; MSDS runs the public network through 19 régions médicales; transition government under Colonel Assimi Goïta emphasises souveraineté sanitaire and AES cooperation.

## 2. Scope

In scope: Président Goïta; Premier Ministre; Ministre de la Santé et du Développement Social; Secrétaire Général; DG CNAM; DG Pharmacie Populaire; Directeur INSP; Directeurs CHU (Point G, Gabriel Touré); Directeurs régionaux santé; CNT Commission Santé; Ordre des Médecins du Mali.

## 3. Structure

Standard.

## 4. Field definitions

Transition government — military and technocratic. Titles in French / English.

## 5. Provenance and dating

Médecin Colonel-major Assa Badiallo Touré serves as Ministre de la Santé et du Développement Social since 4 July 2023 in the Goïta transition government; military medical officer; reported as WHO Africa regional president; active 2026 on Mali-China cooperation, UN and World Bank partnerships, INPS reform, sovereignty.

## 6. Update workflow

Verify against sante.gouv.ml, primature.gov.ml, presidence.ml, maliweb, bamada.net, EchosMedias, Malikunafoni.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Importing French / CEDEAO framings — Mali withdrew CEDEAO January 2024 and pivoted to Russia / AES.

## 9. Acronym glossary

- **AES** — Alliance des États du Sahel.
- **CNAM** — Caisse Nationale d'Assurance Maladie.
- **INPS** — Institut National de Prévoyance Sociale.
- **MSDS** — Ministère de la Santé et du Développement Social.

## 10. Worked example

```yaml
      - Médecin Colonel-major Assa Badiallo Touré:
          - Title: Ministre de la Santé et du Développement Social (in the Goïta transition government, since 4 July 2023)
          - Stakeholder engagement notes:
              - "Ministre de la Santé et du Développement Social depuis le 4 juillet 2023 dans le gouvernement de transition du Colonel Assimi Goïta; médecin militaire de rang Colonel-major; profil 'Vertus : Sens élevé du travail, intégrité morale et amour pour la patrie' (Maliweb)."
              - "Active 2026: coopération sanitaire Mali-Chine à Taiyuan (Maliweb); renforcement axes humanitaires et sanitaires avec l'ONU et la Banque mondiale (Maliweb communiqué 391); lancement Journée Nationale de la Souveraineté Retrouvée à Kalaban-Coro (Bamada); présentation de vœux 2026 sous le sceau de la reconnaissance et de l'engagement collectif (Bamada); feuille de route INPS appelant à une restructuration profonde de la sécurité sociale; lancement DEF 2026 examens; rapportée comme présidente régionale OMS Afrique."
              - "Owns MSDS policy, CNAM CMU/RAMED, Pharmacie Populaire pharmaceutical supply, INSP, CHU Point G et Gabriel Touré, 19 régions médicales, sécurité sociale (INPS), insurgency-affected régions (Centre, Nord, GATIA / JNIM / ISGS dynamics), and Mali's WHO Africa, AES, BRICS+ diplomacy."
              - "Hook: souveraineté sanitaire, Mali-Chine cooperation, INPS sécurité sociale reform, OMS Afrique leadership, AES."
          - Tone advice:
              - "Ouvrir avec souveraineté, Mali-Chine, OMS Afrique et AES — sont les lignes de la transition."
              - "Ne pas pitcher en framings français / CEDEAO — Mali en AES et coopération Russie / Chine."
```

## 11. Out-of-band notes

For roles unfilled or interim.

## 12. Open questions

- Named Secrétaire Général MSDS, DG CNAM, DG Pharmacie Populaire, Directeur INSP.
- Directeurs CHU Point G, CHU Gabriel Touré, et CHU Mère-Enfant Le Luxembourg.
- Directeurs régionaux santé des 19 régions.
- CNT Commission Santé Chair et Président Ordre des Médecins du Mali.
