# spec.md — `leaders.yml`

Font única de veritat per al registre del sistema de salut andorrà. El YAML ha de complir aquesta especificació.

## 1. Purpose

Registre d'involucració de persones nomenades al Ministeri de Salut del Principat d'Andorra i organismes adjacents.

Andorra és un coprincipat parlamentari amb dos coprínceps (President de la República Francesa i Bisbe d'Urgell). Sistema de salut públic amb cobertura via la CASS (Caixa Andorrana de Seguretat Social) i l'Hospital Nostra Senyora de Meritxell com a centre principal. Membre de l'OMS i de l'Acord d'Associació amb la UE en negociació.

## 2. Scope

In scope: Cap de Govern; Ministre de Salut; Director SAAS (Servei Andorrà d'Atenció Sanitària); Director CASS; Consell General Comissió Legislativa d'Afers Socials, Joventut i Igualtat.

Out of scope: directors de serveis hospitalaris.

## 3. Structure

Standard 2/6/10/14 indentation. Top-level key: `Stakeholders del sistema de salut andorrà:`. Order: Govern → Ministeri → SAAS → CASS → Consell General.

## 4. Field definitions

Afiliació partidària: `DA` (Demòcrates per Andorra), `Concòrdia` (centre), `Acció Liberal`, `PS` (Partit Socialdemòcrata). Títols en català.

## 5. Provenance and dating

Anchor to year, month or date. Helena Mas Cucurull ha estat Ministra de Salut al Govern de Xavier Espot Zamora (Demòcrates per Andorra, des de 2019, reelegit 2023); verificar contra el Govern d'Andorra.

## 6. Update workflow

Verify against govern.ad, salut.govern.ad, consell.ad, ANA (Agència de Notícies Andorrana), Diari d'Andorra, Bondia, Andorra Difusió.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Importar framings espanyols o francesos — Andorra és sobirana amb arquitectura institucional pròpia.
- Ignorar la CASS — el finançament és asseguradora-públic; framings d'NHS-pur són inexactes.

## 9. Acronym glossary

- **CASS** — Caixa Andorrana de Seguretat Social.
- **DA** — Demòcrates per Andorra.
- **SAAS** — Servei Andorrà d'Atenció Sanitària.

## 10. Worked example

```yaml
      - Helena Mas Cucurull (DA):
          - Title: Ministra de Salut (Minister of Health)
          - Stakeholder engagement notes:
              - "Ministra de Salut al Govern Espot II (DA, des de 2023); verificar contra govern.ad."
              - "Owns la política i pressupost de Salut, l'Hospital Nostra Senyora de Meritxell via SAAS, la xarxa de centres de salut, CASS finançament, i diplomàcia OMS Europa i UE-Acord d'Associació."
              - "Hook: salut digital, NCDs, salut mental, longevitat (Andorra té una de les esperances de vida més altes), cobertura transfronterera UE, i acord d'associació UE aterren."
          - Tone advice:
              - "Obrir amb salut digital, NCDs, salut mental, longevitat i Acord UE."
              - "No importar framings espanyols o francesos ni ignorar la CASS."
```

## 11. Out-of-band notes

Per a càrrecs vacants o interins.

## 12. Open questions

- Director SAAS i Director CASS amb titularitat verificada.
- President Comissió Afers Socials Consell General.
