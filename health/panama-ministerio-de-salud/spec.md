# spec.md — `leaders.yml`

Single source of truth for the Panamanian health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around Panama's Ministerio de Salud (MINSA), Caja de Seguro Social (CSS), and adjacent bodies.

The Panamanian system is segmented: MINSA provides care for the uninsured ~30% and runs public health programmes; CSS covers formal-sector workers and dependants (~65%); private providers serve the wealthier. Both MINSA and CSS operate their own hospital networks. The Mulino government has prioritised integration of the two segments.

## 2. Scope

In scope: Presidente; Ministro/a de Salud; Vice-Ministros; Director General CSS; Director CSS Hospitalario; Director Caja de Seguro Social Plan de Salud; Director Instituto Conmemorativo Gorgas de Estudios de la Salud (ICGES); Director Direccion General de Salud Pública; Directors of large hospitals (Santo Tomás, CSS Complejo Hospitalario, Hospital del Niño, San Miguel Arcángel, Anita Moreno, Hospital Regional Aquilino Tejeira, Hospital de Especialidades Pediátricas); Asamblea Nacional Comisión de Salud; Colegio Médico de Panamá.

## 3. Structure

Standard. Ordering: Presidencia → MINSA → CSS → ICGES → grandes hospitales → Asamblea → Colegio Médico.

## 4. Field definitions

Party affiliation using canonical Panamanian abbreviations: `RM` (Realizando Metas — Mulino / Martinelli), `PRD` (Partido Revolucionario Democrático), `Alianza`, `Cambio Democrático` (CD), `Panameñista`, `MOLIRENA`, `Vamos`, `Otro Camino`. Titles in Spanish with English glosses.

## 5. Provenance and dating

Anchor facts to year, month or exact date. José Raúl Mulino (Realizando Metas) was sworn in 1 July 2024. Dr. Fernando Boyd Galindo es Ministro de Salud desde el inicio del gobierno Mulino — cirujano dental, especialidad en Periodoncia por la Universidad de Pennsylvania (1983); graduado de la Universidad de Panamá (1979).

## 6. Update workflow

Verify against minsa.gob.pa, presidencia.gob.pa, css.gob.pa, gorgas.gob.pa, asamblea.gob.pa, La Prensa Panamá, La Estrella de Panamá, Panamá América, El Siglo, Telemetro, TVN-2.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Tratar MINSA y CSS como una sola red — son sistemas paralelos con redes hospitalarias propias; la integración es agenda política.
- Importar NHS sin adaptar — Panamá es segmentado con dos pilares públicos paralelos.

## 9. Acronym glossary

- **CSS** — Caja de Seguro Social.
- **ICGES** — Instituto Conmemorativo Gorgas de Estudios de la Salud.
- **MINSA** — Ministerio de Salud.

## 10. Worked example

```yaml
      - Dr. Fernando Boyd Galindo (Realizando Metas):
          - Title: Ministro de Salud (Minister of Health) (en el gobierno de José Raúl Mulino desde 1 de julio de 2024)
          - Stakeholder engagement notes:
              - "Ministro de Salud desde el 1 de julio de 2024 en el gobierno de José Raúl Mulino (Realizando Metas, sucesor de Cortizo); cirujano dental, Doctor of Dental Surgery por la Universidad de Panamá (1979); especialidad en Periodoncia por la University of Pennsylvania (1983)."
              - "Defiende públicamente la integración del sistema de salud (MINSA + CSS), una agenda política central del mandato; en intervenciones recientes ha hablado de 'llevar al patio de la casa la atención de salud' en la transformación de la atención primaria."
              - "Bajo presión presupuestal: 'En muchos hospitales tenemos solo para avanzar 6 meses' (declaración a La Prensa) — el ciclo de gestión 2026 está marcado por la urgencia fiscal y la priorización de medicamentos, especialidades y vacantes."
              - "Owns la rectoría del sistema, integración con CSS, política farmacéutica, vacancias para internos médicos, ICGES, atención primaria, y articulación con OPS / OMS en respuesta a brotes (dengue, malaria fronteriza)."
              - "Hook: integración MINSA-CSS, atención primaria comunitaria, medicamentos, ICGES research, salud fronteriza (Darién), salud materno-infantil aterrizan."
          - Tone advice:
              - "Abrir con integración MINSA-CSS, atención primaria y presión presupuestal — son los frames discursivos del mandato Boyd Galindo."
              - "No proponer marcos que ignoren la CSS — los pitches deben respetar la dualidad operativa del sistema."
```

## 11. Out-of-band notes

For roles unfilled or interim.

## 12. Open questions

- Named Vice-Ministros bajo Boyd Galindo con vigencia verificada.
- Director General CSS con vigencia verificada (la CSS es estatutariamente autónoma).
- Director ICGES, Director General de Salud Pública con vigencia verificada.
- Directores de los grandes hospitales (Santo Tomás, CSS Complejo Hospitalario Arnulfo Arias Madrid, Hospital del Niño, San Miguel Arcángel).
- Presidente Comisión de Salud de la Asamblea Nacional en el período actual.
- Presidente Colegio Médico de Panamá con vigencia verificada.
