# spec.md — `leaders.yml`

Source unique de vérité pour le registre des parties prenantes du système de santé béninois. Le YAML doit se conformer à cette spécification.

## 1. Purpose

Registre d'engagement des personnes nommées au sein du Ministère de la Santé (MS) de la République du Bénin et corps adjacents.

Le Bénin est sous la présidence de Patrice Talon (depuis 2016, second mandat depuis 2021) avec un cabinet à orientation technocratique. Membre de la CEDEAO, UEMOA, Francophonie.

## 2. Scope

In scope: Président; Ministre de la Santé; Secrétaire Général; Directeur CNHU-HKM (Centre National Hospitalier Universitaire Hubert Koutoukou Maga); Directeur ABMETS (Agence Béninoise des Médicaments et autres produits de santé); Assemblée Nationale Commission Santé.

Out of scope: directeurs départementaux; chefs de service.

## 3. Structure

Standard 2/6/10/14 indentation. Top-level key: `Parties prenantes du système de santé béninois:`. Ordre: Présidence → MS → CNHU → ABMETS → Assemblée.

## 4. Field definitions

Affiliation partisane: `BR` (Bloc Républicain, mouvance présidentielle), `UPR` (Union Progressiste le Renouveau, mouvance présidentielle), `Les Démocrates` (opposition, parti de Boni Yayi). Titres en français.

## 5. Provenance and dating

Anchor to year, month or date. Prof. Benjamin Hounkpatin a été Ministre de la Santé sous Talon; la titularité actuelle est à vérifier contre le Secrétariat Général du Gouvernement.

## 6. Update workflow

Verify against gouv.bj, sante.gouv.bj, assemblee-nationale.bj, ABP (Agence Béninoise de Presse), La Nation, Matin Libre.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Ignorer la nouvelle Agence Béninoise des Médicaments (ABMETS) — réforme régulatoire récente; framings basés sur l'ancienne architecture pharmaceutique seront désalignés.
- Importer des framings nigérians — le Bénin est francophone, dans la zone CFA UEMOA, et institutionnellement distinct du Nigeria voisin anglophone.

## 9. Acronym glossary

- **ABMETS** — Agence Béninoise des Médicaments et autres produits de santé.
- **ABP** — Agence Béninoise de Presse.
- **CNHU-HKM** — Centre National Hospitalier Universitaire Hubert Koutoukou Maga.
- **MS** — Ministère de la Santé.

## 10. Worked example

```yaml
      - Prof. Benjamin Hounkpatin (BR-mouvance présidentielle):
          - Title: Ministre de la Santé (Minister of Health)
          - Stakeholder engagement notes:
              - "Ministre de la Santé sous Patrice Talon; médecin; profil technocratique compatible avec la doctrine de gouvernance Talon; vérifier la titularité courante contre le Secrétariat Général du Gouvernement."
              - "Owns la politique et le budget MS, le CNHU-HKM à Cotonou, l'hôpital Mère-Enfant de la Lagune (HOMEL), les Centres Hospitaliers Départementaux des douze départements, l'ABMETS, ARCH (Assurance pour le Renforcement du Capital Humain) volet santé, et la diplomatie OMS AFRO, CEDEAO et UEMOA."
              - "Hook: ARCH-Vie volet santé (CUS-cible), paludisme, santé maternelle et infantile, NCDs, mpox et préparation aux urgences, et structuration ABMETS atterrissent."
          - Tone advice:
              - "Ouvrir avec ARCH-santé, paludisme, MCH, NCDs et structuration régulatoire."
              - "Ne pas ignorer l'ABMETS ni importer des framings nigérians."
```

## 11. Out-of-band notes

Pour les postes vacants ou intérimaires.

## 12. Open questions

- Confirmation de la titularité actuelle du Ministre de la Santé.
- Directeur Général ABMETS et Directeur Général CNHU-HKM.
- Président Commission Santé Assemblée Nationale.
