# spec.md — `leaders.yml`

Single source of truth for the structure, semantics, and update rules of `leaders.yml` for the Austrian Gesundheitswesen. The YAML must conform to this spec; if they disagree, the spec wins and the YAML is fixed.

## 1. Purpose

`leaders.yml` is an engagement register of named individuals in and around Austrian health and social affairs. Each entry helps a reader inside the Bundesministerium für Arbeit, Soziales, Gesundheit, Pflege und Konsumentenschutz (Sozialministerium), the Dachverband der Sozialversicherungsträger, a Land government, or an adjacent body decide:

1. Who to engage for a given topic.
2. How to engage them — the angle that lands and the angle that fails.
3. Where to engage them — which public channels they use.

The Austrian Gesundheitswesen is a Bismarckian social-insurance system financed mainly through the Österreichische Gesundheitskasse (ÖGK, the merged statutory health fund created in 2020) plus separate funds for civil servants (BVAEB) and the self-employed (SVS). The Bund sets framework legislation; the nine Länder run the public-hospital pillar through their Landesgesundheitsfonds; the Bundesländer-Bund-Sozialversicherung Zielsteuerung Gesundheit (Z-G) coordinates planning. AGES regulates food and supports medicines; the BASG/Medizinmarktaufsicht regulates medicines and devices.

## 2. Scope

**In scope:** Bundeskanzler; Bundesministerin/Bundesminister für Arbeit, Soziales, Gesundheit, Pflege und Konsumentenschutz; the Sektionsleiter for Gesundheit, Pflege, Konsumentenschutz inside the Sozialministerium; Dachverband der Sozialversicherungsträger (Vorsitzender, Generaldirektor); ÖGK (Obmann, Generaldirektor); Gesundheit Österreich GmbH (GÖG, Geschäftsführung); Bundesamt für Sicherheit im Gesundheitswesen (BASG) and AGES (Geschäftsführung); the nine Landesgesundheitsfonds and the Landesräte für Gesundheit in each Bundesland; Österreichische Ärztekammer (Präsident); Österreichischer Apothekerverband (Präsident); Bundesvertretung Pflege; Nationalrat Ausschuss für Gesundheit Obmann/Obfrau.

**Out of scope:** operational staff below Sektionsleiter / Abteilungsleitung level; vendors; historical post-holders; non-Austrian counterparts.

## 3. Structure

```
Österreichisches Gesundheitswesen Stakeholder:
  - {Organisation}:
      - {Person}:
          - Title: ...
          - {optional contact fields}
          - Stakeholder engagement notes: [...]
          - Tone advice: [...]
```

Indentation: 2/6/10/14 spaces, no tabs, one blank line between sibling entries. Ordering: Bundesregierung → Sozialministerium → Sozialversicherung (Dachverband, ÖGK, BVAEB, SVS, AUVA, PVA) → Bundesinstitute (GÖG, BASG, AGES) → Länder Landeshauptleute/Landesräte für Gesundheit → Nationalrat Ausschuss für Gesundheit → professional bodies (Ärztekammer, Apothekerkammer, Pflege).

## 4. Field definitions

**Organisation name** — official German with English in parentheses (e.g. `Österreichische Gesundheitskasse (ÖGK)`).

**Person name** — uses academic titles (`Dr.`, `Mag.`, `Prof. Dr.`, `MMag.`); party affiliation in parentheses using canonical Austrian abbreviations (`ÖVP`, `SPÖ`, `FPÖ`, `NEOS`, `Grüne`, `KPÖ`).

**Title** — German, with English gloss where not obvious. Status flags: `interim`, `(seit {Datum})`, `(Aktualität prüfen)`.

**Contact fields** (optional, in order): `LinkedIn`, `X`, `Bluesky`, `Mastodon`, `Website`, `GitHub`, `Email`. Add only with public attribution.

**Stakeholder engagement notes** — 3-7 bullets covering career, ownership, public statements, hook. Anti-pattern: generic CV.

**Tone advice** — exactly two bullets. What to lead with; what to avoid. Specific to the person.

## 5. Provenance and dating

Anchor facts to year, month or exact date. The Stocker-Schumann-Babler coalition (ÖVP-SPÖ-NEOS) was sworn in 3 March 2025, ending the post-September-2024-election impasse. Treat any Sozialministerium or Bundesregierung entry pre-dating 3 March 2025 as warranting re-verification.

## 6. Update workflow

1. Identify the change. 2. Verify against bundeskanzleramt.gv.at, sozialministerium.gv.at, dachverband.gv.at, oegk.at, parlament.gv.at, Wiener Zeitung, Standard, Krone, Profil. 3. Apply minimum diff. 4. Confirm structure. 5. Re-validate cross-references.

## 7. Invariants

Standard register invariants: one Title, one engagement notes block, one Tone advice block (exactly two bullets); no `?` placeholders; one-line strings; HTTPS URLs; one organisation per person.

## 8. Anti-patterns

- Padding, speculation, vendor-flattering language, stale role titles, duplicate entries.
- Treating the Bund as the operational owner — hospitals sit with the Länder via Landesgesundheitsfonds; the Sozialversicherung sits in self-administration.
- Importing NHS framings unmodified — Austria's Sozialversicherungs-financed and Länder-delivered model has no NHS analog.

## 9. Acronym glossary

- **AGES** — Österreichische Agentur für Gesundheit und Ernährungssicherheit.
- **BASG** — Bundesamt für Sicherheit im Gesundheitswesen (medicines and devices regulator inside AGES Medizinmarktaufsicht).
- **BVAEB** — Versicherungsanstalt öffentlich Bediensteter, Eisenbahnen und Bergbau (statutory fund for civil servants).
- **Dachverband** — Dachverband der Sozialversicherungsträger (umbrella body of statutory insurance funds, successor to the former Hauptverband).
- **GÖG** — Gesundheit Österreich GmbH (national health-planning institute and ÖBIG).
- **Landesgesundheitsfonds** — Land-level health fund channelling federal-Land-insurance funding to public hospitals.
- **ÖGK** — Österreichische Gesundheitskasse (the main statutory health-insurance fund, created 1 January 2020 by merging the nine regional Gebietskrankenkassen).
- **PVA** — Pensionsversicherungsanstalt; **AUVA** — Allgemeine Unfallversicherungsanstalt; **SVS** — Sozialversicherung der Selbständigen.
- **Zielsteuerung Gesundheit (Z-G)** — Bund-Länder-Sozialversicherung joint planning and budgeting framework.

## 10. Worked example

```yaml
      - Korinna Schumann (SPÖ):
          - Title: Bundesministerin für Arbeit, Soziales, Gesundheit, Pflege und Konsumentenschutz (Federal Minister for Labour, Social Affairs, Health, Care and Consumer Protection) (seit 3. März 2025)
          - Stakeholder engagement notes:
              - "Bundesministerin im Stocker-Babler-Schumann-Kabinett seit dem 3. März 2025; SPÖ; vorher Vorsitzende der GPA-Gewerkschaft und Vizepräsidentin des ÖGB — Gewerkschaftshintergrund prägt das Pflege- und Arbeitsteil des Mandats."
              - "Verantwortet das gesamte Sozialministerium-Portfolio: Arbeit, Soziales, Gesundheit, Pflege, Konsumentenschutz; der Pflegeteil ist die größte politische Linie ihrer Amtszeit."
              - "Reformprozess Gesundheit Bund-Länder-Sozialversicherung soll laut Bundeskanzler Christian Stocker im Juni 2026 fertig sein; Schumann ist in einzelnen Punkten öffentlich anderer Ansicht als Stocker — koalitionäre Spannungen sind sichtbar."
              - "Hook: Pflegereform, Spitalsfinanzierung, Spitalsstruktur, ÖGK-Steuerung und Konsumentenschutz aterrissent; Pitches, die das Bund-Länder-Sozialversicherungs-Dreieck ignorieren, aterrissent nicht."
          - Tone advice:
              - "Mit Pflege, Spitalsfinanzierung, ÖGK-Reform und Arbeitsbedingungen einsteigen — das sind die SPÖ-Linien und ihr gewerkschaftlicher Hintergrund."
              - "Nicht zentralstaatlich pitchen, als wäre der Bund Operativer Träger — Spitäler sitzen bei den Ländern, Versicherung in der Selbstverwaltung."
```

## 11. Out-of-band notes

Used where a role is unfilled or interim. No Tone advice required.

## 12. Open questions

- Named Sektionsleiter for Gesundheit and Pflege inside the Sozialministerium under Schumann with currency verified.
- Named Vorsitzender and Generaldirektor of the Dachverband der Sozialversicherungsträger, Obmann and Generaldirektor of the ÖGK, and the BVAEB / SVS / AUVA / PVA leadership.
- Named Geschäftsführung of GÖG, BASG and AGES Medizinmarktaufsicht with currency verified.
- Landesräte/Landesrätinnen für Gesundheit of the nine Bundesländer (Wien, Niederösterreich, Burgenland, Steiermark, Oberösterreich, Salzburg, Kärnten, Tirol, Vorarlberg).
- Obmann/Obfrau of the Nationalrat Ausschuss für Gesundheit.
- Präsident/in der Österreichischen Ärztekammer, der Österreichischen Apothekerkammer and the major Pflege-Bundesvertretungen with currency verified.
