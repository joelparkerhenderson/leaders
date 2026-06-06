# spec.md — `leaders.yml`

Single source of truth for the Costa Rican health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around Costa Rica's Ministerio de Salud and the CCSS (Caja Costarricense de Seguro Social), the universal-insurance-and-delivery body that is the operational heart of Costa Rican health.

Costa Rica operates a near-universal Bismarckian-style system run primarily by the CCSS, with the Ministerio de Salud as the rectoría / stewardship body. CCSS owns hospitals, finances and delivers care. INCIENSA is the public health institute.

## 2. Scope

In scope: Presidente; Ministro/a de Salud; Viceministros; Presidente Ejecutivo CCSS; Gerente Médico CCSS; Director INCIENSA; Director Nacional de Vigilancia de la Salud; Directores de los grandes hospitales (Hospital México, Calderón Guardia, San Juan de Dios, Nacional de Niños); Presidente Comisión Permanente de Asuntos Sociales Asamblea Legislativa; Colegio de Médicos y Cirujanos; Colegio de Enfermeras; Colegio de Farmacéuticos.

## 3. Structure

Standard. Ordering: Presidencia → Ministerio de Salud → CCSS → INCIENSA → grandes hospitales → Asamblea Legislativa → colegios profesionales.

## 4. Field definitions

Party affiliation using canonical Costa Rican abbreviations: `PPSD` (Progreso Social Democrático — Chaves), `PLN` (Liberación Nacional), `PUSC` (Unidad Social Cristiana), `PAC` (Acción Ciudadana), `FA` (Frente Amplio), `PNR` (Nueva República), `PLP` (Liberal Progresista). Titles in Spanish with English glosses.

## 5. Provenance and dating

Anchor facts to year, month or exact date. Laura Fernández (PPSD) became Presidenta el 8 de mayo de 2026 tras ganar la elección de febrero 2026; Rodrigo Chaves saliente fue nombrado Ministro de la Presidencia y Hacienda en su gobierno. La identidad de la nueva Ministra/o de Salud bajo Fernández aún debe verificarse formalmente; Mary Munive (Vicepresidenta y Ministra de Salud bajo Chaves, 2022-2026) terminó su período en mayo 2026.

## 6. Update workflow

Verify against presidencia.go.cr, ministeriodesalud.go.cr, ccss.sa.cr, inciensa.sa.cr, asamblea.go.cr, La Nación, La República, Semanario Universidad, CRHoy, Telenoticias.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating Ministerio de Salud as the operational owner — la CCSS es el pilar operativo del sistema; el Ministerio rectorea pero no provee.
- Importar NHS sin adaptar — Costa Rica es Bismarckiano puro con un solo asegurador-prestador integrado vertical.

## 9. Acronym glossary

- **CCSS** — Caja Costarricense de Seguro Social.
- **EBAIS** — Equipos Básicos de Atención Integral en Salud (basic primary-care teams).
- **INCIENSA** — Instituto Costarricense de Investigación y Enseñanza en Nutrición y Salud.

## 10. Worked example

```yaml
      - Notes on Ministerio de Salud:
          - Status: La administración de Laura Fernández (PPSD) asumió el 8 de mayo de 2026 tras la victoria en la elección de febrero 2026 (segunda vuelta en abril). El gabinete fue presentado pero la identidad confirmada del nuevo Ministro/a de Salud bajo Fernández no está aún registrada en este repositorio; comunicaciones oficiales de la Presidencia deben consultarse para confirmar la designación.
          - Implication: Hasta confirmar la designación, el engagement debe rutearse vía la Presidencia (donde Rodrigo Chaves ocupa Presidencia y Hacienda) y la Presidencia Ejecutiva de la CCSS, que mantiene el pilar operativo del sistema de salud costarricense.
```

## 11. Out-of-band notes

The Notes block above is used because the substantive identity of the current Minister of Health under the Fernández administration is not yet verifiable in this register.

## 12. Open questions

- Confirm identity and decreto de nombramiento del Ministro/a de Salud en el gobierno de Laura Fernández (mayo 2026).
- Named Viceministros bajo el nuevo Ministro/a.
- Presidente Ejecutivo CCSS y Gerente Médico CCSS bajo el nuevo gobierno.
- Director INCIENSA con vigencia verificada.
- Directores de los grandes hospitales nacionales (Hospital México, Calderón Guardia, San Juan de Dios, Nacional de Niños).
- Presidente Comisión Permanente de Asuntos Sociales de la Asamblea Legislativa.
- Presidente Colegio de Médicos y Cirujanos con vigencia verificada.
