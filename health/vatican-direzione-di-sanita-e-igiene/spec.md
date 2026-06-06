# spec.md — `leaders.yml`

Fonte unica di verità per il registro del sistema sanitario dello Stato della Città del Vaticano. Il YAML deve essere conforme a questa specifica.

## 1. Purpose

Registro di coinvolgimento delle persone nominate presso la Direzione di Sanità e Igiene del Governatorato dello Stato della Città del Vaticano e organi adiacenti, nonché i dicasteri della Santa Sede competenti per la pastorale della salute.

Lo Stato della Città del Vaticano è il più piccolo Stato sovrano del mondo (~0,49 km²; ~800 abitanti). Il sistema sanitario interno è gestito dalla Direzione di Sanità e Igiene del Governatorato. La cittadinanza vaticana è funzionale (limitata a chi vi risiede per ragioni di servizio). I servizi sanitari complessi sono erogati prevalentemente tramite convenzioni con strutture italiane (Policlinico Gemelli, Bambino Gesù, San Giovanni di Dio).

## 2. Scope

In scope: Sommo Pontefice; Segretario di Stato; Presidente del Governatorato dello Stato della Città del Vaticano; Direttore della Direzione di Sanità e Igiene; Prefetto del Dicastero per il Servizio dello Sviluppo Umano Integrale (competente per la pastorale della salute a livello universale).

Out of scope: cappellani ospedalieri; medici dell'Ospedale Bambino Gesù (struttura della Santa Sede ma sotto diversa governance).

## 3. Structure

Standard 2/6/10/14 indentation. Top-level key: `Stakeholder del sistema sanitario vaticano:`. Ordine: Sommo Pontefice → Segretario di Stato → Governatorato → Direzione di Sanità e Igiene → Dicasteri.

## 4. Field definitions

Lo Stato della Città del Vaticano non ha partiti politici; la governance è ecclesiastica. Titoli in italiano e latino come appropriato; usare titoli ecclesiastici (Em.za Card., Mons., Sua Santità).

## 5. Provenance and dating

Anchor to year, month or date. Sua Santità Papa Leone XIV è stato eletto il 8 maggio 2025 (succedendo a Papa Francesco, deceduto il 21 aprile 2025). Le nomine ai vertici del Governatorato sono soggette al pontificato Leone XIV.

## 6. Update workflow

Verify against vatican.va, press.vatican.va, vaticanstate.va, L'Osservatore Romano, Vatican News.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Confondere Stato della Città del Vaticano con Santa Sede — sono due soggetti giuridici distinti (la Santa Sede è la persona giuridica universale della Chiesa Cattolica; lo Stato è il territorio fisico). Per la salute interna è competente lo Stato; per la pastorale universale i Dicasteri della Santa Sede.
- Ignorare la rete sanitaria cattolica globale — la Chiesa Cattolica gestisce circa il 26% delle strutture sanitarie mondiali; la pastorale della salute via Dicasteri è una scala diversa dalla sanità interna del Vaticano.

## 9. Acronym glossary

- **SCV** — Stato della Città del Vaticano.

## 10. Worked example

```yaml
      - Suor [Nome a verificare]:
          - Title: Direttrice della Direzione di Sanità e Igiene del Governatorato dello SCV
          - Stakeholder engagement notes:
              - "Direzione di Sanità e Igiene del Governatorato dello SCV; verificare contro vaticanstate.va."
              - "Owns la sanità interna dello SCV per i residenti (clero, religiose, Guardia Svizzera, dipendenti laici), convenzioni con strutture italiane, e profilassi sanitaria interna."
              - "Hook: anziani (la popolazione vaticana è invecchiata), longevità, salute occupazionale, gestione eventi di massa (pellegrinaggi Anno Santo 2025)."
          - Tone advice:
              - "Distinguere sempre Stato della Città del Vaticano (sanità interna) da Santa Sede (pastorale universale via Dicasteri)."
```

## 11. Out-of-band notes

Per cariche vacanti o ad interim.

## 12. Open questions

- Direttore Direzione di Sanità e Igiene con titolarità verificata.
- Prefetto del Dicastero per il Servizio dello Sviluppo Umano Integrale.
