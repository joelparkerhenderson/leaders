# spec.md — `leaders.yml`

Single source of truth for the Salvadoran health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around El Salvador's Ministerio de Salud (MINSAL), Instituto Salvadoreño del Seguro Social (ISSS), Dirección Nacional de Medicamentos (DNM), and adjacent bodies.

The system has three segments: MINSAL (uninsured ~80%); ISSS (formal-sector workers); private clinics. The Bukele government has pursued visible health-infrastructure investments and digitalisation framings.

## 2. Scope

In scope: Presidente; Ministro/a de Salud; Viceministros (Servicios de Salud; Políticas de Salud); Director General ISSS; Director DNM; Director Instituto Nacional de Salud (INS El Salvador); Asamblea Legislativa Comisión de Salud; Colegio Médico de El Salvador.

## 3. Structure

Standard. Ordering: Presidencia → MINSAL → ISSS → DNM → INS → Asamblea → colegios.

## 4. Field definitions

Party affiliation using canonical Salvadoran abbreviations: `NI` (Nuevas Ideas — Bukele), `ARENA`, `FMLN`, `GANA`, `PCN`. Titles in Spanish with English glosses.

## 5. Provenance and dating

Anchor facts to year, month or exact date. Nayib Bukele (NI) was re-elected in February 2024 for a second term beginning 1 June 2024. Dr. Francisco José Alabi Montoya ha sido Ministro de Salud desde 2020 (pandemia), continuó en el segundo mandato Bukele.

## 6. Update workflow

Verify against salud.gob.sv, presidencia.gob.sv, isss.gob.sv, dnm.gob.sv, asamblea.gob.sv, La Prensa Gráfica, El Diario de Hoy, El Faro, El Salvador.com, Infobae El Salvador.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating MINSAL as única instancia — ISSS atiende segmento formal con red propia.
- Importar NHS sin adaptar — El Salvador es segmentado con MINSAL como red predominante.

## 9. Acronym glossary

- **DNM** — Dirección Nacional de Medicamentos.
- **ISSS** — Instituto Salvadoreño del Seguro Social.
- **MINSAL** — Ministerio de Salud.

## 10. Worked example

```yaml
      - Dr. Francisco José Alabi Montoya (NI):
          - Title: Ministro de Salud (Minister of Health) (en el segundo mandato Bukele desde 1 de junio de 2024; continuidad desde 2020)
          - Stakeholder engagement notes:
              - "Ministro de Salud desde 2020 (gestión de la pandemia COVID-19); continúa en el segundo mandato Bukele (Nuevas Ideas, NI) desde 1 de junio de 2024 — uno de los ministros de más larga continuidad en el gabinete."
              - "Según encuesta de Infobae mayo 2026, Defensa, Educación y Salud están entre los tres ministerios que impulsan la imagen del gabinete; Alabi tiene 39% de penetración y 31% de valoración favorable — figura visible del gabinete."
              - "Informó en junio 2026 que se adquirieron más equipos especializados para estudios diagnósticos en estos años que en toda la historia previa del MINSAL — narrativa de modernización tecnológica como eje del mandato."
              - "Polémicas: 'Salud con lupa' reportó controversia sobre una oficina ministerial de >US$50.000 en plena emergencia sanitaria — episodio que afectó la imagen pero no la posición política."
              - "Hook: digitalización del sistema, equipos médicos modernos, infraestructura hospitalaria nueva (Hospital El Salvador y otros), atención primaria comunitaria, salud materno-infantil aterrizan."
          - Tone advice:
              - "Abrir con modernización tecnológica, infraestructura hospitalaria y resultados visibles — son las líneas comunicacionales del gobierno Bukele en salud."
              - "No invocar críticas o cooperación con organismos opositores al gobierno — el contexto político está fuertemente polarizado y los framings críticos serán bloqueados."
```

## 11. Out-of-band notes

For roles unfilled or interim.

## 12. Open questions

- Named Viceministros de MINSAL bajo Alabi.
- Director General ISSS, Director DNM, Director INS El Salvador.
- Presidente Comisión de Salud de la Asamblea Legislativa.
- Presidente Colegio Médico de El Salvador.
