# spec.md — `leaders.yml`

Single source of truth for the Cameroonian health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Ministère de la Santé Publique (MINSANTE), Programme Élargi de Vaccination, Centres Pasteur du Cameroun, hôpitaux centraux et CHU, and adjacent bodies.

The Cameroonian system has Couverture Santé Universelle (CSU) implementation ongoing; MINSANTE runs the public network; regional Délégations de Santé Publique manage 10 regions. France-cooperation and AFD financing significant; Anglophone-crisis-affected regions require specific framings.

## 2. Scope

In scope: Président; Premier Ministre; Ministre de la Santé Publique; Secrétaires d'État; Secrétaire Général; Inspecteurs Généraux; Directeur PEV (Programme Élargi de Vaccination); Directeur Centre Pasteur du Cameroun; Directeurs hôpitaux centraux (Yaoundé, Douala, Laquintinie); Délégués Régionaux de la Santé Publique (10 régions); Présidents Commissions Santé Assemblée Nationale et Sénat; Ordre National des Médecins; Ordre des Pharmaciens.

## 3. Structure

Standard. Ordering: Présidence → Premier Ministre → MINSANTE → CPC → PEV → hôpitaux centraux → 10 délégations → Parlement → Ordres.

## 4. Field definitions

Party affiliation: `RDPC` (Rassemblement Démocratique du Peuple Camerounais — Biya), `SDF` (Social Democratic Front), `MRC` (Mouvement pour la Renaissance du Cameroun), `UNDP`, `CPP`. Titles in French / English.

## 5. Provenance and dating

Dr. Manaouda Malachie serves as Ministre de la Santé Publique under President Paul Biya / Premier Ministre Joseph Dion Ngute; long tenure; 3rd Vice-President of WHO Executive Board (honoured at Geneva 2026); 389 billion FCFA Ministry budget for 2026 placed under the sign of performance.

## 6. Update workflow

Verify against minsante.cm, spm.gov.cm, prc.cm, ena.cm, ActuCameroun, News du Cameroun, Cameroun-Info.Net, Cameroon Tribune, AfriqueMedia.tv, Yaoundeinfo.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating MINSANTE as the only counterparty — regional Délégations de Santé Publique manage operational delivery; donor coordination (AFD, KfW, USAID, Gavi, Global Fund) is structurally embedded.
- Importing US framings — Cameroon is universal-coverage-implementing with significant donor coordination.

## 9. Acronym glossary

- **CPC** — Centre Pasteur du Cameroun.
- **CSU** — Couverture Santé Universelle.
- **MINSANTE** — Ministère de la Santé Publique.
- **PEV** — Programme Élargi de Vaccination.

## 10. Worked example

```yaml
      - Dr. Manaouda Malachie (RDPC):
          - Title: Ministre de la Santé Publique du Cameroun
          - Stakeholder engagement notes:
              - "Ministre de la Santé Publique sous le Président Paul Biya et le Premier ministre Joseph Dion Ngute; RDPC; profil sur spm.gov.cm; longue tenure au portefeuille."
              - "Active 2026: lancement de l'exécution du budget ministériel 2026 (389 milliards FCFA) le 29 janvier à Yaoundé sous le signe de la performance (News du Cameroun, ActuCameroun); a présidé la session stratégique du PEV pour 2026 (Afrique Media); a déclaré que le système de santé camerounais a enregistré une avancée majeure, jamais vue en Afrique (ActuCameroun mars 2026); à Genève, sortie remarquée sur l'injustice sanitaire (mai 2026, ActuCameroun); honoré à Genève pour l'engagement du Cameroun au sein de l'OMS comme 3ème Vice-Président du Conseil exécutif de l'OMS (Yaoundeinfo)."
              - "Visite à l'hôpital Laquintinie de Douala (avril 2026); proximité avec figures de la culture camerounaise (MINSANTE)."
              - "Owns MINSANTE policy, CSU implementation, CPC vaccine science (Centre Pasteur de Yaoundé), PEV, hôpitaux centraux et régionaux, 10 délégations régionales, et la diplomatie sanitaire du Cameroun à l'OMS, CEMAC et Africa CDC."
              - "Hook: CSU, performance budgétaire, PEV, vaccination COVID legacy, CPC programmes, gestion crises Anglophone et insécurité, OMS Conseil exécutif présidence et leadership africain à l'OMS land."
          - Tone advice:
              - "Ouvrir avec CSU, performance budgétaire, PEV, vaccination et leadership OMS — sont ses lignes autorales sostenues."
              - "Ne pas pitcher en framings qui ignorent la crise anglophone — les régions du Nord-Ouest et du Sud-Ouest nécessitent des cadres spécifiques."
```

## 11. Out-of-band notes

For roles unfilled or in transition.

## 12. Open questions

- Named Secrétaires d'État, Secrétaire Général, Inspecteurs Généraux du MINSANTE.
- Directeur Centre Pasteur du Cameroun et Directeur PEV.
- Directeurs hôpitaux Laquintinie Douala, Hôpital Général Yaoundé, Hôpital Central Yaoundé.
- Délégués Régionaux de la Santé Publique des 10 régions.
- Présidents Commissions Santé Assemblée Nationale et Sénat.
- Présidents Ordre National des Médecins, Ordre des Pharmaciens.
