# spec.md — `leaders.yml`

Single source of truth for the structure, semantics, and update rules of `leaders.yml` for the Bolivian sistema de salud. The YAML must conform to this spec; if they disagree, the spec wins and the YAML is fixed.

## 1. Purpose

`leaders.yml` is an engagement register of named individuals in and around the Bolivian health system. The system combines a public subsystem run by the Ministerio de Salud y Deportes (MSyD) and Servicios Departamentales de Salud (SEDES), the social-security subsystem (Caja Nacional de Salud and other Cajas), and a small private sector. The Sistema Único de Salud (SUS) was launched 2019 as a universal-coverage scheme for the uninsured.

## 2. Scope

**In scope:** Presidente; Ministro/a de Salud y Deportes; Viceministros (Gestión del Sistema Sanitario; Promoción, Vigilancia Epidemiológica y Medicina Tradicional); Director General Caja Nacional de Salud; Director AGEMED (medicines agency); Director INLASA (national health institute); Directores SEDES of the nine departments (La Paz, Santa Cruz, Cochabamba, Potosí, Oruro, Chuquisaca, Tarija, Beni, Pando); Presidente Comisión de Política Social Cámara de Diputados; Colegio Médico de Bolivia.

## 3. Structure

```
Sistema de salud boliviano — partes interesadas:
  - {Organisation}:
      - {Person}:
          - Title: ...
          - Stakeholder engagement notes: [...]
          - Tone advice: [...]
```

Standard indentation. Ordering: Presidencia → MSyD → AGEMED → INLASA → Cajas → SEDES → Asamblea Legislativa → Colegio Médico.

## 4. Field definitions

Standard family conventions. Party affiliation using canonical Bolivian abbreviations: `MAS-IPSP`, `CC` (Comunidad Ciudadana), `Creemos`, `PDC`. Titles in Spanish with English glosses.

## 5. Provenance and dating

Anchor facts to year, month or exact date. Marcela Flores Zambrana is Ministra de Salud y Deportes as of June 2026. Vice-Ministers Dr. José Luis Ríos Cambeses (Gestión del Sistema Nacional de Salud) and Dr. Roxana Elizabeth Salamanca Kacic (Promoción, Vigilancia Epidemiológica y Medicina Tradicional). The Ministry presented the Plan de Salud 2026-2030.

## 6. Update workflow

Verify against minsalud.gob.bo, gob.bo, asambleadiputados.gob.bo, La Razón, Página Siete, Los Tiempos, El Deber.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating SEDES as Ministry subunits — they are departmental-government bodies under departmental autonomy.
- Importing NHS framings unmodified — Bolivia is segmented (public + Cajas + SUS) with strong tradicional-medicine recognition.

## 9. Acronym glossary

- **AGEMED** — Agencia Estatal de Medicamentos y Tecnologías en Salud.
- **CNS** — Caja Nacional de Salud.
- **INLASA** — Instituto Nacional de Laboratorios de Salud.
- **MSyD** — Ministerio de Salud y Deportes.
- **SEDES** — Servicio Departamental de Salud.
- **SUS** — Sistema Único de Salud (Bolivia 2019).

## 10. Worked example

```yaml
      - Marcela Flores Zambrana:
          - Title: Ministra de Salud y Deportes (Minister of Health and Sports) (en funciones, 2026)
          - Stakeholder engagement notes:
              - "Ministra de Salud y Deportes con presencia activa en mayo-junio 2026 — iniciativas sobre donación de sangre y recomendaciones sanitarias publicadas en la web institucional."
              - "Posesionó a dos viceministros: Dr. José Luis Ríos Cambeses (Vicemininstro de Gestión del Sistema Nacional de Salud) y Dra. Roxana Elizabeth Salamanca Kacic (Vicemininstra de Promoción, Vigilancia Epidemiológica y Medicina Tradicional)."
              - "Presentó el Plan de Salud 2026-2030 como marco estratégico del Ministerio; impulsa el Sistema Único de Salud (SUS) y la integración con la Caja Nacional de Salud."
              - "Hook: SUS, Plan de Salud 2026-2030, atención primaria, medicina tradicional, recursos humanos, donación de sangre y enfermedades vectoriales aterrizan."
          - Tone advice:
              - "Abrir con SUS, Plan 2026-2030, atención primaria y medicina tradicional — son las líneas vigentes del Ministerio."
              - "No pitchear como si la salud fuese federal-centralizada — los nueve SEDES tienen autoridad departamental significativa."
```

## 11. Out-of-band notes

For roles unfilled or interim.

## 12. Open questions

- Confirm Marcela Flores Zambrana's biographical data and partido político.
- Director General Caja Nacional de Salud, AGEMED, INLASA with currency verified.
- Directores de SEDES de los nueve departamentos.
- Presidente Comisión de Política Social Cámara de Diputados.
- Presidente Colegio Médico de Bolivia.
