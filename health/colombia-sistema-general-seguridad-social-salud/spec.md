# spec.md — `leaders.yml`

Single source of truth for the structure, semantics, and update rules of `leaders.yml` for the Colombian Sistema General de Seguridad Social en Salud (SGSSS). The YAML must conform to this spec; if they disagree, the spec wins and the YAML is fixed.

## 1. Purpose

`leaders.yml` is an engagement register of named individuals in and around the Colombian health system. The SGSSS, created by Ley 100/1993, is a regulated-market model in which the EPS (Entidades Promotoras de Salud) compete for affiliates in the contributory and subsidised regimes and contract with the IPS (Instituciones Prestadoras de Servicios de Salud). MinSalud sets policy; ADRES is the central financial pool; INVIMA regulates medicines and devices. The Petro government's health reform proposes a structural transformation of the EPS / ADRES / IPS architecture; the reform has produced significant political conflict.

## 2. Scope

**In scope:** Presidente; Ministro/a de Salud y Protección Social; Viceministros (Salud Pública y Prestación de Servicios; Protección Social); Director ADRES; Director INVIMA; Director INS (Instituto Nacional de Salud); Superintendente Nacional de Salud (Supersalud); Secretarios Departamentales y Distritales de Salud (priorizar Bogotá, Antioquia, Valle del Cauca, Atlántico, Cundinamarca); Presidentes Comisión Séptima Cámara y Senado; Presidente Federación Médica Colombiana, Asociación Colombiana de Hospitales y Clínicas (ACHC), Colegio Médico Colombiano.

## 3. Structure

```
Sistema General de Seguridad Social en Salud (Colombia) — partes interesadas:
  - {Organisation}:
      - {Person}:
          - Title: ...
          - Stakeholder engagement notes: [...]
          - Tone advice: [...]
```

Standard indentation. Ordering: Presidencia → Minsalud → ADRES → INVIMA → INS → Supersalud → entidades territoriales → Congreso (Comisión Séptima) → asociaciones gremiales.

## 4. Field definitions

Standard family conventions. Party affiliation using canonical Colombian abbreviations: `Pacto Histórico` (coalición), `Colombia Humana`, `Polo`, `Verdes` (Alianza Verde), `Centro Democrático`, `Cambio Radical`, `Conservador`, `Liberal`, `La U`, `Comunes`, `MIRA`, `Salvación Nacional`, `Dignidad`. Titles in Spanish with English glosses.

## 5. Provenance and dating

Anchor facts to year, month or exact date. The Petro government (Pacto Histórico) was sworn in 7 August 2022. Guillermo Alfonso Jaramillo Martínez (médico, ex-ministro de Salud bajo Samper, ex-alcalde de Ibagué) ha sido Ministro de Salud y Protección Social desde 1 de mayo de 2023 después de la salida de Carolina Corcho. En 2026 enfrenta múltiples investigaciones (Procuraduría por participación en política, denuncias por nepotismo, cuestionamientos por gestión irregular). Confirmó públicamente que no renunciará y que no podrá ser candidato presidencial en 2026.

## 6. Update workflow

Verify against minsalud.gov.co, presidencia.gov.co, adres.gov.co, invima.gov.co, ins.gov.co, supersalud.gov.co, camara.gov.co, senado.gov.co, El Tiempo, El Espectador, Semana, La Silla Vacía, Vorágine, Infobae Colombia, Vanguardia.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Tratar las EPS como intermediarios prescindibles — la reforma Petro las desafía pero el régimen vigente las mantiene como ordenadoras del gasto.
- Importar marcos NHS sin modificar — Colombia es regulated-market con EPS competitivas.

## 9. Acronym glossary

- **ADRES** — Administradora de los Recursos del Sistema General de Seguridad Social en Salud.
- **EPS** — Entidades Promotoras de Salud.
- **INS** — Instituto Nacional de Salud.
- **INVIMA** — Instituto Nacional de Vigilancia de Medicamentos y Alimentos.
- **IPS** — Instituciones Prestadoras de Servicios de Salud.
- **MinSalud / Minsalud** — Ministerio de Salud y Protección Social.
- **Régimen Contributivo / Régimen Subsidiado** — los dos regímenes principales del SGSSS.
- **SGSSS** — Sistema General de Seguridad Social en Salud (Ley 100/1993).
- **Supersalud** — Superintendencia Nacional de Salud.
- **UPC** — Unidad de Pago por Capitación.

## 10. Worked example

```yaml
      - Guillermo Alfonso Jaramillo Martínez (Pacto Histórico / Colombia Humana):
          - Title: Ministro de Salud y Protección Social (Minister of Health and Social Protection) (desde 1 de mayo de 2023)
          - Stakeholder engagement notes:
              - "Ministro de Salud y Protección Social desde el 1 de mayo de 2023, sucediendo a Carolina Corcho durante la primera gran crisis de la reforma de salud Petro; Pacto Histórico / Colombia Humana; médico, ex-Ministro de Salud bajo Ernesto Samper, ex-Gobernador de Tolima, ex-Alcalde de Ibagué."
              - "Bajo investigaciones múltiples en 2026: la Procuraduría abrió investigación por presunta participación en política en evento del 31 de mayo en Coyaima (Tolima); investigaciones por nepotismo en contratos familiares (~3 mil millones de pesos según denuncias); presuntas irregularidades en la gestión ministerial."
              - "Confirmó públicamente que no renuncia al Ministerio y que no podrá ser candidato presidencial en 2026 — anclaje firme en la gestión Petro hasta el fin del mandato."
              - "Owns la implementación operativa del nuevo modelo de gestión de la salud (intervención EPS, fortalecimiento ADRES como pagador único, transformación territorial), UPC, política farmacéutica, y la mediación con las EPS intervenidas (Sanitas, EPS Sura, Nueva EPS, etc.)."
              - "Hook: reforma de salud, intervención EPS, ADRES como pagador, modelo preventivo y territorial, UPC, política farmacéutica, gestión COVID legacy aterrizan; pitches que defienden el statu quo de EPS no aterrizan."
          - Tone advice:
              - "Abrir con reforma de salud Petro, modelo preventivo y territorial, ADRES y UPC — son los frames discursivos del Ministerio."
              - "No abordar como interlocutor de bajo perfil — Jaramillo opera en un contexto político conflictivo y de alta exposición mediática; cualquier framing debe anticipar el escrutinio público."
```

## 11. Out-of-band notes

For roles unfilled or interim.

## 12. Open questions

- Named Viceministros bajo Jaramillo with currency verified.
- Director ADRES, INVIMA, INS, Supersalud with currency verified.
- Secretarios de Salud de Bogotá, Antioquia, Valle del Cauca, Atlántico, Cundinamarca.
- Presidente Comisión Séptima Cámara y Senado en el período legislativo actual.
- Presidentes de Federación Médica Colombiana, ACHC, Colegio Médico Colombiano.
