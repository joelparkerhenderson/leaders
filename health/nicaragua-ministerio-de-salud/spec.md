# spec.md — `leaders.yml`

Single source of truth for the Nicaraguan health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around Nicaragua's Ministerio de Salud (MINSA), Instituto Nicaragüense de Seguridad Social (INSS), and adjacent bodies.

The Nicaraguan health system is centralised under MINSA with the Ortega-Murillo regime exercising strong political control. Cuban medical cooperation remains active. The country has had significant political-emigration of medical professionals since 2018 and faces persistent international isolation. Health information transparency is constrained.

## 2. Scope

In scope: Co-Presidentes Daniel Ortega and Rosario Murillo; Ministro/a de Salud; Vice-Ministros; Director INSS; Director Instituto de Medicamentos (DIGEMID-equivalent); Directors of major SILAIS (departmental health systems); Asamblea Nacional Comisión de Salud, Seguridad Social y Bienestar; FMN (Federación Médica Nicaragüense). Note: regime structure dominates institutional ownership.

## 3. Structure

Standard. Ordering: Co-Presidencia → MINSA → INSS → SILAIS → Asamblea → FMN.

## 4. Field definitions

Party affiliation using canonical Nicaraguan abbreviations: `FSLN` (Frente Sandinista de Liberación Nacional), `Alianza por la República` (PLC + others), opposition parties largely banned or in exile. Titles in Spanish with English glosses.

## 5. Provenance and dating

Anchor facts to year, month or exact date. Martha Verónica Reyes Álvarez served as Ministra de Salud from April 2020 until her "resignation" was officially published on 23 October 2024 — Reyes was the fifth functionary to depart the regime in four months. The Health Ministry has been under uncertain leadership since; substantive successor identity must be verified. The 2014 constitutional reform and 2025 power-sharing produced the co-presidency of Ortega and Murillo. Cuban-mission cooperation continues.

## 6. Update workflow

Verify against minsa.gob.ni, el19digital.com, presidencia.gob.ni, asamblea.gob.ni, Confidencial (en exilio), Despacho 505, La Prensa (Nicaragua, en exilio), Nicaragua Investiga, Infobae Centroamérica, Coyuntura.co.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating institutional channels as politically neutral — el régimen Ortega-Murillo controla institucionalmente cualquier engagement.
- Importar NHS sin adaptar — Nicaragua es centralizado-FSLN con dependencia importante de cooperación cubana.

## 9. Acronym glossary

- **FSLN** — Frente Sandinista de Liberación Nacional.
- **INSS** — Instituto Nicaragüense de Seguridad Social.
- **MINSA** — Ministerio de Salud.
- **SILAIS** — Sistema Local de Atención Integral en Salud (regional / departmental).

## 10. Worked example

```yaml
      - Notes on Ministerio de Salud:
          - Status: Martha Verónica Reyes Álvarez fue Ministra de Salud desde abril 2020 hasta octubre 2024, cuando el régimen oficializó su "renuncia" — Reyes fue la quinta funcionaria en abandonar el régimen en cuatro meses. Desde entonces el cargo de Ministro/a titular ha estado en transición o vacante; la identidad sustantiva del sucesor/a debe verificarse en comunicaciones oficiales del régimen (El 19 Digital, La Gaceta, Asamblea Nacional).
          - Implication: El engagement debe rutearse vía Casa Presidencial (Ortega-Murillo) y direcciones operativas del MINSA hasta confirmación oficial de un Ministro/a titular. La política sanitaria operativa está controlada políticamente por el régimen; cualquier framing técnico debe respetar la centralización institucional.
```

## 11. Out-of-band notes

For roles unfilled or in transition. The political environment (closure of opposition NGOs, restrictions on independent press, persecution of opposition figures) limits independent verification.

## 12. Open questions

- Confirm identity, fecha de toma de posesión y partido del actual Ministro/a de Salud bajo la co-presidencia Ortega-Murillo.
- Named Vice-Ministros de MINSA con vigencia verificada.
- Director General INSS con vigencia verificada.
- Directores de los SILAIS departamentales.
- Presidente Comisión de Salud, Seguridad Social y Bienestar de la Asamblea Nacional.
- FMN (Federación Médica Nicaragüense) directiva con vigencia verificada.
- Coordinador/a Misión Médica Cubana en Nicaragua.
