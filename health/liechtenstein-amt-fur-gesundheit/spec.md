# spec.md — `leaders.yml`

Einzige Quelle der Wahrheit für das Verzeichnis der Stakeholder des liechtensteinischen Gesundheitssystems. Die YAML muss dieser Spezifikation entsprechen.

## 1. Purpose

Engagement-Verzeichnis der namentlich genannten Personen im Liechtensteinischen Ministerium für Gesellschaft, Bildung, Sport und Kultur (mit Gesundheitsressort) und angrenzenden Organen.

Liechtenstein ist eine konstitutionelle Erbmonarchie auf demokratisch-parlamentarischer Grundlage unter dem Fürsten Hans-Adam II. (Staatsoberhaupt, mit Erbprinz Alois als Stellvertreter). Das Gesundheitssystem basiert auf gesetzlicher Krankenversicherung (KVG-System); enge Kooperation mit Schweizer Spitälern (insbesondere Kantonsspital Graubünden, Universitätsspital Zürich, St. Galler Spitalverbund). Mitglied im EWR und in der WHO Europa.

## 2. Scope

In scope: Fürst; Regierungschef; Ministerin/Minister für Gesellschaft, Bildung, Sport und Kultur (zuständig für Gesundheit); Leiter Amt für Gesundheit; Landtag Kommission für Soziales und Gesundheit.

Out of scope: Spitalleitungen; Krankenkassenleitungen.

## 3. Structure

Standard 2/6/10/14 indentation. Top-level key: `Stakeholder des liechtensteinischen Gesundheitssystems:`. Reihenfolge: Fürstenhaus → Regierung → Ministerium → Amt für Gesundheit → Landtag.

## 4. Field definitions

Parteizugehörigkeit: `VU` (Vaterländische Union), `FBP` (Fortschrittliche Bürgerpartei), `FL` (Freie Liste), `DpL` (Demokraten pro Liechtenstein). Titel in Deutsch.

## 5. Provenance and dating

Anchor to year, month or date. Manuel Frick (FBP) war Minister für Gesellschaft, Bildung, Sport und Kultur (mit Gesundheitsressort) in der Regierung Risch (VU-FBP-Koalition); die Parlamentswahlen am 9. Februar 2025 haben die VU als stärkste Kraft bestätigt mit Regierungschef Brendan Wanger; das Gesundheitsressort ist in der neuen Regierung neu zugeteilt — Titelinhaber gegen die Regierung Liechtenstein verifizieren.

## 6. Update workflow

Verify against regierung.li, landtag.li, llv.li (Liechtensteinische Landesverwaltung), Liechtensteiner Vaterland, Liechtensteiner Volksblatt, Radio Liechtenstein.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Liechtenstein mit der Schweiz verwechseln — souveräner Staat mit eigenständiger Architektur, obwohl die Zollunion mit der Schweiz und die enge Spitalkooperation Interdependenz schaffen.
- Den EWR ignorieren — Liechtenstein ist EWR-Mitglied (nicht EU), was die Anwendbarkeit von EU-Gesundheitsrecht regelt.

## 9. Acronym glossary

- **EWR** — Europäischer Wirtschaftsraum.
- **FBP** — Fortschrittliche Bürgerpartei.
- **KVG** — Krankenversicherungsgesetz.
- **VU** — Vaterländische Union.

## 10. Worked example

```yaml
      - Notes on Minister für Gesundheit von Liechtenstein nach den Wahlen 2025:
          - Status: Verify against regierung.li for the post-9 February 2025 portfolio holder.
          - Implication: Liechtenstein engagement requires recognition of monarchy framework, EWR membership and Swiss cooperation.
          - Hook: NCDs, mental health, longevity, EWR-EU regulatory alignment, Swiss-spital cooperation.
          - Tone: Open with NCDs, longevity, EWR alignment and Swiss-spital cooperation.
```

## 11. Out-of-band notes

Für vakante oder interimistische Ämter.

## 12. Open questions

- Bestätigung des aktuellen Gesundheitsministers nach den Wahlen 2025.
- Leiter Amt für Gesundheit mit verifizierter Amtszeit.
