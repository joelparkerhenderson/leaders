# spec.md — `leaders.yml`

Source unique de vérité pour le registre des parties prenantes du système de santé burundais. Le YAML doit se conformer à cette spécification.

## 1. Purpose

Registre d'engagement des personnes nommées au sein du Ministère de la Santé Publique et de la Lutte contre le SIDA (MSPLS) de la République du Burundi et corps adjacents.

Le Burundi est sous la présidence d'Évariste Ndayishimiye (CNDD-FDD, depuis 2020), avec un système de santé public-dominant à forte présence missionnaire, supporté par les partenaires (OMS, UNICEF, Banque Mondiale, Fonds Mondial, Gavi, Coopération Belge, UE) et marqué par la stratégie de gratuité ciblée pour enfants de moins de 5 ans et femmes enceintes.

## 2. Scope

In scope: Président; Premier Ministre; Ministre de la Santé Publique et de la Lutte contre le SIDA; Secrétaire Permanent; Directeur Général INSP; Directeur ABREMA; Assemblée Nationale Commission Santé.

Out of scope: directeurs provinciaux; chefs de service.

## 3. Structure

Standard 2/6/10/14 indentation. Top-level key: `Parties prenantes du système de santé burundais:`. Ordre: Présidence → MSPLS → INSP → ABREMA → Assemblée.

## 4. Field definitions

Affiliation partisane: `CNDD-FDD` (Conseil National pour la Défense de la Démocratie — Forces de Défense de la Démocratie, au pouvoir), `CNL` (Congrès National pour la Liberté, opposition), `UPRONA`. Titres en français.

## 5. Provenance and dating

Anchor to year, month or date. Le Ministre de la Santé Publique et de la Lutte contre le SIDA sous Ndayishimiye est à vérifier contre la Présidence et l'Agence Burundaise de Presse.

## 6. Update workflow

Verify against presidence.gov.bi, minisante.bi, parlement.bi, ABP (Agence Burundaise de Presse), Iwacu, SOS Médias Burundi.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Importer des framings rwandais — Burundi et Rwanda partagent géographie et histoire mais ont des trajectoires politiques et sanitaires distinctes; framings croisés seront filtrés.
- Ignorer la gratuité ciblée — la politique de gratuité pour enfants de moins de 5 ans et femmes enceintes est politiquement protégée.

## 9. Acronym glossary

- **ABP** — Agence Burundaise de Presse.
- **ABREMA** — Autorité Burundaise de Régulation des Médicaments et Aliments.
- **CNDD-FDD** — Conseil National pour la Défense de la Démocratie — Forces de Défense de la Démocratie.
- **INSP** — Institut National de Santé Publique.
- **MSPLS** — Ministère de la Santé Publique et de la Lutte contre le SIDA.

## 10. Worked example

```yaml
      - Dr [Nom à vérifier] (CNDD-FDD):
          - Title: Ministre de la Santé Publique et de la Lutte contre le SIDA (Minister of Public Health and the Fight against AIDS)
          - Stakeholder engagement notes:
              - "Ministre du MSPLS sous Ndayishimiye; vérifier contre la Présidence et ABP."
              - "Owns la politique et le budget MSPLS, le CHU de Kamenge, l'Hôpital Prince Régent Charles, le réseau provincial et missionnaire (catholique, protestant), INSP, ABREMA, et la diplomatie OMS AFRO, EAC, CIRGL et UA."
              - "Hook: paludisme, VIH (gratuité ARV), MCH, NCDs, gratuité ciblée et préparation aux urgences (mpox, Marburg régional) atterrissent."
          - Tone advice:
              - "Ouvrir avec paludisme, VIH, MCH, gratuité ciblée et préparation aux urgences."
              - "Ne pas importer des framings rwandais ni négliger la gratuité ciblée."
```

## 11. Out-of-band notes

Pour les postes vacants ou intérimaires.

## 12. Open questions

- Identité du Ministre en titre avec titularité vérifiée.
- Directeur Général INSP et Directeur ABREMA.
- Président Commission Santé Assemblée Nationale.
