# spec.md — `leaders.yml`

Fonte unica di verità per il registro del sistema sanitario sammarinese. Il YAML deve essere conforme a questa specifica.

## 1. Purpose

Registro di coinvolgimento delle persone nominate presso il Segretariato di Stato per la Sanità e la Sicurezza Sociale della Repubblica di San Marino, l'Istituto per la Sicurezza Sociale (ISS) e organi adiacenti.

San Marino è una repubblica parlamentare con due Capitani Reggenti che servono come Capi di Stato per sei mesi a rotazione. Il sistema sanitario è pubblico, finanziato dall'ISS, centrato sull'Ospedale di Stato a Cailungo. Stato osservatore presso il Consiglio d'Europa, membro dell'OMS, in negoziati per Accordo di Associazione con l'UE.

## 2. Scope

In scope: Capitani Reggenti; Segretario di Stato per la Sanità e la Sicurezza Sociale; Direttore Generale ISS; Direttore Sanitario; Consiglio Grande e Generale Commissione Affari Interni, Sicurezza Pubblica, Servizi Sanitari.

Out of scope: capi di servizio ospedaliero.

## 3. Structure

Standard 2/6/10/14 indentation. Top-level key: `Stakeholder del sistema sanitario sammarinese:`. Ordine: Capitani Reggenti → Congresso di Stato → Segretariato Sanità → ISS → Ospedale di Stato → Consiglio.

## 4. Field definitions

Affiliazione partitica: `PDCS` (Partito Democratico Cristiano Sammarinese, storico maggioranza), `RF` (Repubblica Futura), `Domani Motus Liberi`, `PSD` (Partito Socialista e Democratico). Titoli in italiano.

## 5. Provenance and dating

Anchor to year, month or date. Mariella Mularoni è stata Segretaria di Stato per la Sanità nel Congresso di Stato dopo le elezioni politiche del 9 giugno 2024; verificare contro il Governo sammarinese.

## 6. Update workflow

Verify against esteri.sm, congresso.sm, consigliograndeegenerale.sm, libertas.sm (San Marino RTV), L'Informazione di San Marino, San Marino Fixing.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Confondere con l'Italia — San Marino è uno Stato sovrano con architettura propria, sebbene la lingua e numerose convenzioni bilaterali con l'Italia creino interdipendenza.
- Ignorare l'ISS — l'Istituto per la Sicurezza Sociale è il pagatore-fornitore unico; framings NHS-puro o assicurazione-pura saranno corretti.

## 9. Acronym glossary

- **ISS** — Istituto per la Sicurezza Sociale.
- **PDCS** — Partito Democratico Cristiano Sammarinese.

## 10. Worked example

```yaml
      - Mariella Mularoni (PDCS):
          - Title: Segretaria di Stato per la Sanità e la Sicurezza Sociale (Minister of Health and Social Security)
          - Stakeholder engagement notes:
              - "Segretaria di Stato per la Sanità nel Congresso di Stato post-elezioni del 9 giugno 2024; verificare contro esteri.sm."
              - "Owns la politica sanitaria, l'Ospedale di Stato a Cailungo via l'ISS (pagatore-fornitore), la rete dei centri di salute, le convenzioni con strutture italiane (Rimini, Cesena, Bologna) per spec specialistici, e diplomazia OMS Europa e UE-Accordo di Associazione."
              - "Hook: NCDs, longevità (San Marino ha una delle più alte aspettative di vita al mondo), salute mentale, salute digitale, e cooperazione transfrontaliera con l'Emilia-Romagna atterrano."
          - Tone advice:
              - "Aprire con NCDs, longevità, salute mentale, salute digitale e cooperazione con l'Emilia-Romagna."
              - "Non confondere con l'Italia né ignorare il modello pagatore-fornitore ISS."
```

## 11. Out-of-band notes

Per cariche vacanti o ad interim.

## 12. Open questions

- Direttore Generale ISS e Direttore Sanitario con titolarità verificata.
- Presidente Commissione Affari Interni del Consiglio Grande e Generale.
