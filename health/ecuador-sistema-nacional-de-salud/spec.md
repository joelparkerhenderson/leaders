# spec.md — `leaders.yml`

Single source of truth for the structure, semantics, and update rules of `leaders.yml` for the Ecuadorian Sistema Nacional de Salud (SNS). The YAML must conform to this spec; if they disagree, the spec wins and the YAML is fixed.

## 1. Purpose

`leaders.yml` is an engagement register of named individuals in and around the Ecuadorian health system. The SNS is institutionally tripartite: Ministerio de Salud Pública (MSP) provides care for the uninsured ~50%; IESS (Instituto Ecuatoriano de Seguridad Social) covers formal-sector workers; ISSFA / ISSPOL cover military and police. Private clinics serve the wealthier. The Noboa government has had unusually rapid Health Minister turnover — seven Ministers in two years as of April 2026.

## 2. Scope

**In scope:** Presidente; Ministro/a de Salud Pública; Viceministros; Director General IESS; Director General ARCSA (medicines agency); Director ACESS (health quality and accreditation); Director INEC health statistics; Directores Zonales de Salud; Asamblea Nacional Comisión Especializada de Salud; Federación Médica Ecuatoriana; Colegio Médico de Pichincha; Federación de Enfermeras y Enfermeros.

## 3. Structure

```
Sistema Nacional de Salud (Ecuador) — partes interesadas:
  - {Organisation}:
      - {Person}:
          - Title: ...
          - Stakeholder engagement notes: [...]
          - Tone advice: [...]
```

Standard indentation. Ordering: Presidencia → MSP → ARCSA → ACESS → IESS → ISSFA / ISSPOL → coordinaciones zonales → Asamblea → colegios profesionales.

## 4. Field definitions

Party affiliation using canonical Ecuadorian abbreviations: `ADN` (Acción Democrática Nacional — partido de Noboa), `RC` (Revolución Ciudadana — correísmo), `Pachakutik`, `PSC` (Partido Social Cristiano), `Construye`, `MD` (Movimiento Democrático). Titles in Spanish with English glosses.

## 5. Provenance and dating

Anchor facts to year, month or exact date. The Noboa government (ADN) was sworn in 23 November 2023; Noboa was re-elected in April 2025 for a full term to 2029. Ministerial turnover in Health has been extreme: by 27 April 2026 Jaime Bernabé Erazo was designated as the seventh Minister of Health, replacing Edgar José Lama von Buchwald (Feb 2025-May 2025, who left to chair IESS) and several intermediate Ministers. Treat any Ministerio entry as warranting re-verification.

## 6. Update workflow

Verify against salud.gob.ec, presidencia.gob.ec, iess.gob.ec, arcsa.gob.ec, asambleanacional.gob.ec, El Universo, El Comercio Ecuador, Primicias, Plan V, La Posta.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Tratar el MSP como única instancia operativa — el IESS atiende ~25% de la población con red propia.
- Importar NHS sin adaptar — Ecuador es segmentado con cobertura desigual entre regiones.

## 9. Acronym glossary

- **ACESS** — Agencia de Aseguramiento de la Calidad de los Servicios de Salud y Medicina Prepagada.
- **ARCSA** — Agencia Nacional de Regulación, Control y Vigilancia Sanitaria.
- **IESS** — Instituto Ecuatoriano de Seguridad Social.
- **ISSFA / ISSPOL** — Instituto de Seguridad Social de las Fuerzas Armadas / Policía Nacional.
- **MSP** — Ministerio de Salud Pública.

## 10. Worked example

```yaml
      - Jaime Bernabé Erazo (ADN):
          - Title: Ministro de Salud Pública (Minister of Public Health) (desde el 27 de abril de 2026, séptimo Ministro de Salud del gobierno Noboa)
          - Stakeholder engagement notes:
              - "Designado Ministro de Salud Pública el 27 de abril de 2026 por el Presidente Daniel Noboa Azín — séptimo Ministro de Salud en menos de dos años de gobierno; precedió Edgar José Lama von Buchwald (febrero 2025-mayo 2025; renunció para presidir el Consejo Directivo del IESS) y varios ministros intermedios."
              - "Asume en un contexto de severa volatilidad institucional del MSP: desabasto de medicamentos en la red pública, brote de violencia en hospitales públicos, deuda histórica con prestadores, y crisis financiera del IESS."
              - "Owns la rectoría del SNS, la coordinación con IESS, ARCSA, ACESS, política farmacéutica, redes integradas de servicios de salud, y la respuesta a emergencias sanitarias regionales."
              - "Hook: medicamentos y desabasto, deuda hospitalaria, IESS reform, fortalecimiento de primer nivel, dengue y vectores, vacunación rutinaria aterrizan; pitches estratégicos de largo plazo serán difíciles dado el ciclo ministerial corto."
          - Tone advice:
              - "Abrir con desabasto de medicamentos, deuda hospitalaria, primer nivel y emergencias — son las prioridades operativas en un ciclo ministerial corto y altamente politizado."
              - "No proponer reformas estructurales de largo plazo — el ciclo de rotación ministerial reciente sugiere que asuntos estratégicos serán postergados a un ministro futuro."
```

## 11. Out-of-band notes

For roles unfilled or interim.

## 12. Open questions

- Confirm Jaime Bernabé Erazo's biographical detail and exact decreto de nombramiento (Decreto Ejecutivo).
- Named Viceministros bajo Erazo with currency verified.
- Director General IESS, ARCSA, ACESS with currency verified.
- Directores Zonales de Salud de las nueve zonas.
- Presidente Comisión Especializada de Salud de la Asamblea Nacional en el período actual.
- Federación Médica Ecuatoriana y colegios profesionales con vigencia verificada.
