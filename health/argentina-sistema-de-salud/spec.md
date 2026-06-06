# spec.md — `leaders.yml`

Single source of truth for the structure, semantics, and update rules of `leaders.yml` for the Argentine sistema de salud. The YAML must conform to this spec; if they disagree, the spec wins and the YAML is fixed.

## 1. Purpose

`leaders.yml` is an engagement register of named individuals in and around the Argentine health system. The system is highly fragmented: federal Ministerio de Salud sets policy; 24 provinces and CABA own public-hospital delivery; the Obras Sociales (~300 union-managed funds) and PAMI (the elderly pension fund) cover formal-sector workers and pensioners respectively; prepaid plans (EMP/Prepagas) cover the wealthier population; an uninsured ~30-35% rely on public provincial hospitals.

## 2. Scope

**In scope:** Presidente; Ministro de Salud; Secretarios; Director PAMI; Superintendente de Servicios de Salud (SSSalud); Administrador ANMAT; Director Malbrán Institute; Ministros de Salud provinciales (CABA, Buenos Aires, Córdoba, Santa Fe, Mendoza, Tucumán, Salta); Presidente Comisión de Salud Cámara de Diputados and Comisión de Salud Senado; Presidente AMA, COMRA, FEMECA, FACME.

## 3. Structure

```
Sistema de salud argentino — partes interesadas:
  - {Organisation}:
      - {Person}:
          - Title: ...
          - Stakeholder engagement notes: [...]
          - Tone advice: [...]
```

Standard indentation. Ordering: Presidencia → Ministerio de Salud → ANMAT → SSSalud → PAMI → Malbrán → 24 provincias → Congreso → asociaciones profesionales.

## 4. Field definitions

Standard family conventions. Party affiliation using canonical Argentine abbreviations: `LLA` (La Libertad Avanza), `PRO`, `UCR`, `UP` (Unión por la Patria, ex-Frente de Todos / Peronismo), `PJ`, `MC`, `CC-ARI`, `FIT-U`, `Hacemos por Nuestro País`. Titles in Spanish with English glosses.

## 5. Provenance and dating

Anchor facts to year, month or exact date. The Milei government (LLA) was sworn in 10 December 2023. Mario Lugones replaced Mario Russo as Ministro de Salud during the Milei administration; he is the current Minister in 2026. Argentina formally withdrew from the WHO in 2026 — a decision Lugones publicly defended.

## 6. Update workflow

Verify against argentina.gob.ar/salud, casarosada.gob.ar, anmat.gob.ar, sssalud.gob.ar, pami.org.ar, Infobae, Clarín, La Nación, Página/12, Perfil, Ámbito Financiero.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating the system as unitary — fragmentation across federal, provincial, Obras Sociales and PAMI is the defining feature.
- Importing NHS framings unmodified — Argentina is one of the world's most fragmented mixed systems.

## 9. Acronym glossary

- **ANMAT** — Administración Nacional de Medicamentos, Alimentos y Tecnología Médica.
- **COMRA** — Confederación Médica de la República Argentina.
- **Obras Sociales** — union-managed statutory funds (~300 nationally).
- **PAMI** — Programa de Atención Médica Integral (Instituto Nacional de Servicios Sociales para Jubilados y Pensionados).
- **Prepagas / EMP** — empresas de medicina prepaga.
- **SSSalud** — Superintendencia de Servicios de Salud.

## 10. Worked example

```yaml
      - Mario Iván Lugones (LLA):
          - Title: Ministro de Salud (Minister of Health) (en el gobierno de Javier Milei, LLA)
          - Stakeholder engagement notes:
              - "Ministro de Salud en el gobierno de Javier Milei (LLA); médico, especialista en Cardioangiología y Salud Pública; egresado de la Universidad de Buenos Aires (1972); miembro de la Sociedad Argentina de Cardiología."
              - "Defendió públicamente la salida formal de Argentina de la Organización Mundial de la Salud — decisión emblemática del gobierno Milei en política sanitaria internacional."
              - "Anunció en mayo 2026 un programa nacional para diagnóstico y tratamiento del ACV (accidente cerebrovascular); participó en Argentina Week en Nueva York presentando propuestas argentinas en investigación clínica, producción farmacéutica y servicios de salud de alta calidad."
              - "Hook: política farmacéutica, PAMI, Obras Sociales, salida de la OMS, programas verticales (ACV, oncología), inversión extranjera en salud aterrizan; pitches centrados en sistema público integrado no aterrizan dentro del marco de desregulación."
          - Tone advice:
              - "Abrir con desregulación, inversión privada, programas focalizados y reforma de PAMI / Obras Sociales — son las líneas del gobierno Milei."
              - "No pitchear como si la OMS o el sistema público fueran el marco — el gobierno se ha alejado explícitamente de ambos; framings de 'cobertura universal' al estilo OPS serán políticamente disonantes."
```

## 11. Out-of-band notes

For roles unfilled or interim.

## 12. Open questions

- Named Secretarios de Salud bajo Lugones with currency verified.
- Administrador ANMAT, Superintendente SSSalud, Director PAMI with currency verified.
- Ministros de Salud de las provincias grandes (Buenos Aires, CABA, Córdoba, Santa Fe, Mendoza).
- Presidentes Comisión de Salud Cámara y Senado en el actual período legislativo.
- Presidentes AMA, COMRA, FEMECA, FACME with currency verified.
