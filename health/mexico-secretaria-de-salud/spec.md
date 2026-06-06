# spec.md — `leaders.yml`

Single source of truth for the structure, semantics, and update rules of `leaders.yml` for the Mexican sistema de salud. The YAML must conform to this spec; if they disagree, the spec wins and the YAML is fixed.

## 1. Purpose

`leaders.yml` is an engagement register of named individuals in and around the Mexican health system. Each entry helps a reader inside the Secretaría de Salud, IMSS, IMSS-Bienestar, ISSSTE, COFEPRIS, INSP, or an adjacent body decide who to engage, how, and where.

The Mexican system is segmented: IMSS (Instituto Mexicano del Seguro Social) covers formal-sector workers; ISSSTE covers federal civil servants; IMSS-Bienestar (created 2022 to absorb the former Seguro Popular/INSABI population) covers the uninsured population through federal-state agreements; private insurers cover the wealthier. The Secretaría de Salud sets policy, regulates through COFEPRIS, and runs federal-tertiary institutes. State health secretariats are the second sub-national tier.

## 2. Scope

**In scope:** Presidente/a de México; Secretario/a de Salud; Subsecretarios/as (Integración y Desarrollo del Sector Salud, Prevención y Promoción de la Salud); Director General IMSS; Director General IMSS-Bienestar; Director General ISSSTE; Comisionado/a Federal COFEPRIS; Director General CENAPRECE; Director General INSP; Directores Generales de los Institutos Nacionales de Salud (Cardiología, Cancerología, Pediatría, Nutrición, Neurología, Psiquiatría, Enfermedades Respiratorias, Perinatología, Geriatría, Genómica, Rehabilitación); Secretarios/as de Salud estatales for the 32 entidades; Presidente/a Comisión de Salud Cámara de Diputados; Presidente/a Comisión de Salud Senado; Presidentes de Academia Nacional de Medicina, Colegio Médico de México, Federación Mexicana de Enfermería.

**Out of scope:** operational staff below dirección general adjunta level; vendors; historical post-holders.

## 3. Structure

```
Sistema de salud mexicano — partes interesadas:
  - {Organisation}:
      - {Person}:
          - Title: ...
          - Stakeholder engagement notes: [...]
          - Tone advice: [...]
```

Indentation 2/6/10/14 spaces. Ordering: Presidencia → Secretaría de Salud → IMSS → IMSS-Bienestar → ISSSTE → COFEPRIS → INSP → Institutos Nacionales → 32 entidades federativas → Cámaras del Congreso → academias y colegios.

## 4. Field definitions

Standard family conventions. Party affiliation using canonical Mexican abbreviations: `Morena`, `PT` (Partido del Trabajo), `PVEM` (Partido Verde), `PAN` (Partido Acción Nacional), `PRI`, `MC` (Movimiento Ciudadano). Titles in Spanish with English glosses.

## 5. Provenance and dating

Anchor facts to year, month or exact date. Claudia Sheinbaum (Morena) was sworn in as Presidenta on 1 October 2024. David Kershenobich Stalnikowitz became Secretario de Salud on 1 October 2024.

## 6. Update workflow

1. Identify the change. 2. Verify against gob.mx/salud, gob.mx/presidencia, imss.gob.mx, imssbienestar.gob.mx, issste.gob.mx, gob.mx/cofepris, congreso.gob.mx, senado.gob.mx, Reforma, El Universal, La Jornada, Animal Político, Aristegui Noticias, Expansión. 3. Apply minimum diff. 4. Confirm structure. 5. Re-validate cross-references.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating the system as unitary — segmentation across IMSS, ISSSTE, IMSS-Bienestar and private is the defining feature; pitches that assume a single national buyer will be redirected.
- Importing US framings unmodified — Mexico has tax-financed and contributory tiers with strong federal-state political dynamics.

## 9. Acronym glossary

- **CENAPRECE** — Centro Nacional de Programas Preventivos y Control de Enfermedades.
- **COFEPRIS** — Comisión Federal para la Protección contra Riesgos Sanitarios (medicines, devices, food).
- **CONAMED** — Comisión Nacional de Arbitraje Médico.
- **DGE** — Dirección General de Epidemiología (within Secretaría de Salud).
- **IMSS** — Instituto Mexicano del Seguro Social.
- **IMSS-Bienestar** — federalised programme since 2022 covering the previously uninsured (replacing INSABI / former Seguro Popular).
- **INSABI** — former Instituto de Salud para el Bienestar (2020-2023), absorbed into IMSS-Bienestar.
- **INSP** — Instituto Nacional de Salud Pública.
- **ISSSTE** — Instituto de Seguridad y Servicios Sociales de los Trabajadores del Estado.
- **OPS / PAHO** — Organización Panamericana de la Salud / Pan American Health Organization.

## 10. Worked example

```yaml
      - David Kershenobich Stalnikowitz:
          - Title: Secretario de Salud (Secretary of Health) (desde 1 de octubre de 2024)
          - Stakeholder engagement notes:
              - "Secretario de Salud desde 1 de octubre de 2024, posesionado simultáneamente con el inicio del sexenio de Claudia Sheinbaum (Morena); médico internista, gastroenterólogo y hepatólogo; egresado de la Facultad de Medicina de la UNAM; doctor en Medicina por la Universidad de Londres."
              - "Carrera de referencia en hepatología — Director General del Instituto Nacional de Ciencias Médicas y Nutrición Salvador Zubirán durante muchos años; figura académica con alta credibilidad clínica, contraste con perfiles políticos del sexenio anterior."
              - "Equipo principal: Eduardo Clark García Dobarganes como Subsecretario de Integración y Desarrollo del Sector Salud; Alejandro Svarch Pérez como Director General — funcionarios reportados públicamente al inicio del gabinete."
              - "Owns la rectoría sanitaria, IMSS-Bienestar federal-estatal, política farmacéutica vía COFEPRIS y compras consolidadas, los Institutos Nacionales de Salud, vacunación universal, y la respuesta a sarampión y enfermedades emergentes — particularmente con el Mundial 2026 como evento sanitario centinela."
              - "Hook: IMSS-Bienestar federalización, política farmacéutica y desabasto, vacunación, Institutos Nacionales, salud mental, salud digital, Mundial 2026 como contingencia sanitaria aterrissent; pitchs centrados solo en IMSS o solo en el sector privado no aterrissent."
          - Tone advice:
              - "Abrir con IMSS-Bienestar, política farmacéutica, vacunación, Institutos Nacionales y la sanidad del Mundial 2026 — son sus líneas de mandato y su lengua clínico-académica."
              - "No proponer marcos que ignoren la segmentación IMSS / IMSS-Bienestar / ISSSTE — Kershenobich corregirá públicamente cualquier framing unitario; la segmentación es estructural y políticamente significativa."
```

## 11. Out-of-band notes

For roles unfilled or interim.

## 12. Open questions

- Named Subsecretarios with currency verified (Eduardo Clark García Dobarganes confirmed; Alejandro Svarch Pérez confirmed in DG role).
- Director General IMSS, IMSS-Bienestar, ISSSTE with currency verified.
- Comisionado/a Federal COFEPRIS, Director General CENAPRECE, INSP and the eleven Institutos Nacionales with currency verified.
- Secretarios/as de Salud de las 32 entidades federativas — prioritarios CDMX, Estado de México, Jalisco, Nuevo León, Puebla, Veracruz, Guanajuato.
- Presidente/a Comisión de Salud Cámara de Diputados and Senado en la LXVI Legislatura.
- Presidentes de Academia Nacional de Medicina, Colegio Médico de México, Federación Mexicana de Enfermería with currency verified.
