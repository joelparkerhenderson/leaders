# spec.md — `leaders.yml`

Source unique de vérité pour le registre des parties prenantes du système de santé mauritanien. Le YAML doit se conformer à cette spécification.

## 1. Purpose

Registre d'engagement des personnes nommées au sein du Ministère de la Santé de la République Islamique de Mauritanie et corps adjacents.

La Mauritanie est membre du G5 Sahel (historique), de la CEDEAO observateur, de l'Union du Maghreb Arabe et de la Ligue Arabe. Le système est public-dominant avec un Centre Hospitalier National (CHN) à Nouakchott, des hôpitaux régionaux, et un réseau de structures primaires.

## 2. Scope

In scope: Président; Ministre de la Santé; Secrétaire Général MS; Directeur Général CHN; Directeur de la Pharmacie; Assemblée Nationale Commission Affaires Sociales et Santé.

Out of scope: directeurs régionaux; chefs de service.

## 3. Structure

Standard 2/6/10/14 indentation. Top-level key: `Parties prenantes du système de santé mauritanien:`. Ordre: Présidence → MS → CHN → Pharmacie → Assemblée.

## 4. Field definitions

Affiliation partisane: `INSAF` (parti au pouvoir d'El Insaf — Equity), `Tawassoul`, `RFD` (Rassemblement des Forces Démocratiques), `UPR` legacy. Titres en français et arabe.

## 5. Provenance and dating

Anchor to year, month or date. Le Ministre de la Santé sous la présidence de Mohamed Ould Cheikh El Ghazouani est à vérifier contre la Présidence de la République et l'Agence Mauritanienne d'Information (AMI).

## 6. Update workflow

Verify against sante.gov.mr, presidence.mr, ami.mr, Sahara Media, Cridem, Mauriweb, Alakhbar.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Importer les framings sénégalais ou maliens — la Mauritanie a une identité arabo-berbère et africaine distincte, et un système institutionnel propre.
- Négliger la dimension arabophone et la coopération du Golfe — Mauritanie est membre de la Ligue Arabe et reçoit un appui des partenaires arabes.

## 9. Acronym glossary

- **AMI** — Agence Mauritanienne d'Information.
- **CHN** — Centre Hospitalier National.
- **INSAF** — El Insaf (parti au pouvoir).
- **MS** — Ministère de la Santé.

## 10. Worked example

```yaml
      - Dr [Nom à vérifier] (INSAF):
          - Title: Ministre de la Santé (Minister of Health)
          - Stakeholder engagement notes:
              - "Ministre de la Santé du gouvernement de Mohamed Ould Cheikh El Ghazouani; vérifier la titularité contre la Présidence et l'AMI."
              - "Owns la politique et le budget MS, le Centre Hospitalier National à Nouakchott, l'Hôpital de l'Amitié (chinois), les hôpitaux régionaux des wilayas, la pharmacie centrale, et la diplomatie OMS AFRO, UA, Ligue Arabe et UMA."
              - "Hook: paludisme, santé maternelle et infantile, NCDs, nutrition (Mauritanie touchée par la sécheresse), couverture universelle, et coopération arabe-africaine atterrissent."
          - Tone advice:
              - "Ouvrir avec paludisme, santé maternelle et infantile, NCDs, nutrition et couverture universelle."
              - "Ne pas importer des framings sénégalais ou maliens et reconnaître la dimension arabe et africaine."
```

## 11. Out-of-band notes

Pour les postes vacants ou intérimaires.

## 12. Open questions

- Identité du Ministre de la Santé en titre avec titularité vérifiée.
- Secrétaire Général MS et Directeur Général CHN.
- Président Commission Affaires Sociales et Santé à l'Assemblée Nationale.
