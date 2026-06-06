# spec.md — `leaders.yml`

Single source of truth for the Peruvian health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around Peru's Ministerio de Salud (MINSA), EsSalud (Seguridad Social en Salud), DIGEMID (medicines), Susalud (regulator), Instituto Nacional de Salud, and adjacent bodies.

The Peruvian system is segmented: MINSA serves the uninsured ~25% through SIS (Seguro Integral de Salud); EsSalud covers formal-sector workers ~30%; private clinics serve ~10%; armed-forces and police have separate sub-systems. Political instability since 2016 has produced ten Presidents in eight years and even more rapid Health Minister turnover.

## 2. Scope

In scope: Presidente; Ministro/a de Salud; Viceministros (Salud Pública; Prestaciones y Aseguramiento en Salud); Presidente EsSalud; Director DIGEMID; Superintendente Susalud; Director Instituto Nacional de Salud; Directores Regionales de Salud (Lima, Arequipa, La Libertad, Piura, Cusco); Presidente Comisión de Salud y Población Congreso; Decano Colegio Médico del Perú.

## 3. Structure

Standard 2/6/10/14 indentation. Ordering: Presidencia → MINSA → EsSalud → DIGEMID → Susalud → INS → DIRESAS → Congreso → Colegio Médico.

## 4. Field definitions

Party affiliation using canonical Peruvian abbreviations: `FP` (Fuerza Popular), `APP` (Alianza para el Progreso), `RP` (Renovación Popular), `Avanza País`, `Acción Popular`, `Somos Perú`, `Perú Libre`, `Cambio Democrático`, `Honor y Democracia`, `Podemos Perú`, `Bloque Magisterial`. Titles in Spanish with English glosses.

## 5. Provenance and dating

Anchor facts to year, month or exact date. Following the December 2022 Pedro Castillo impeachment, Dina Boluarte's government held to October 2024, when she fell and José Jerí (Avanza País) was sworn in briefly, then José María Balcázar took the presidency in early 2026 after further parliamentary maneuvering. Health Minister rotations have been frequent: Luis Quiroz Avilés was ratified Health Minister under Balcázar's PCM in late 2025 / early 2026, then Juan Carlos Velasco Guerrero was sworn in March 2026 after Quiroz's resignation. Treat any Ministerio entry as warranting re-verification.

## 6. Update workflow

Verify against gob.pe/minsa, gob.pe/presidencia, gob.pe/essalud, gob.pe/susalud, congreso.gob.pe, El Comercio, La República, Infobae Perú, RPP, IDL-Reporteros, Ojo Público.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Tratar MINSA como única entidad — EsSalud y FF.AA./PNP son sub-sistemas paralelos importantes.
- Importar NHS sin adaptar — Perú es segmentado y políticamente inestable.

## 9. Acronym glossary

- **DIGEMID** — Dirección General de Medicamentos, Insumos y Drogas.
- **DIRESA** — Dirección Regional de Salud.
- **EsSalud** — Seguro Social de Salud (Seguridad Social del Perú).
- **INS** — Instituto Nacional de Salud.
- **MINSA** — Ministerio de Salud.
- **PCM** — Presidencia del Consejo de Ministros.
- **SIS** — Seguro Integral de Salud.
- **Susalud** — Superintendencia Nacional de Salud.

## 10. Worked example

```yaml
      - Dr. Juan Carlos Velasco Guerrero:
          - Title: Ministro de Salud (Minister of Health) (desde marzo de 2026, gobierno de José María Balcázar)
          - Stakeholder engagement notes:
              - "Ministro de Salud desde marzo de 2026 en el gobierno del Presidente José María Balcázar, jurando tras la renuncia del Ministro Luis Quiroz Avilés; cirujano, con doctorado en Salud Pública por la Universidad Nacional Federico Villarreal."
              - "Trayectoria reciente: Presidente Ejecutivo del Instituto Nacional de Salud (INS) entre noviembre 2025 y marzo 2026; Superintendente Nacional de Salud (Susalud) entre noviembre 2021 y noviembre 2025 — cinco años en el regulador del sistema."
              - "Asume en un contexto de extrema inestabilidad política: diez Presidentes en ocho años (incluyendo Castillo, Boluarte, Jerí, Balcázar), rotación ministerial alta, desabasto de medicamentos en establecimientos públicos, listas de espera prolongadas."
              - "Owns la rectoría del sistema, EsSalud (coordinación, no control directo), SIS, DIGEMID, Susalud, INS, y la coordinación con DIRESAS regionales en un país con fuerte heterogeneidad geográfica."
              - "Hook: medicamentos y desabasto, EsSalud reform, SIS expansion, primer nivel, atención materno-infantil en Sierra y Selva, sustancias controladas y enfermedades emergentes aterrizan; pitches estratégicos de largo plazo son difíciles."
          - Tone advice:
              - "Abrir con desabasto de medicamentos, EsSalud, SIS, primer nivel y atención regional — son los problemas operativos en un ciclo ministerial corto."
              - "No proponer reformas estructurales — el ciclo político hace inviables compromisos de largo plazo; framings de continuidad institucional fallarán."
```

## 11. Out-of-band notes

For roles unfilled or interim.

## 12. Open questions

- Confirm Juan Carlos Velasco Guerrero's exact decreto supremo de nombramiento y composición ministerial actual del Premier Balcázar.
- Named Viceministros bajo Velasco with currency verified.
- Presidente Ejecutivo EsSalud, Director DIGEMID, Superintendente Susalud with currency verified.
- Directores Regionales de Salud de regiones grandes (Lima, Arequipa, La Libertad, Piura, Cusco).
- Presidente Comisión de Salud y Población del Congreso en el actual período.
- Decano Colegio Médico del Perú with currency verified.
