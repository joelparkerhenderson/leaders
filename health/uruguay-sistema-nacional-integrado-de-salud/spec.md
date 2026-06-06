# spec.md — `leaders.yml`

Single source of truth for the Uruguayan Sistema Nacional Integrado de Salud (SNIS) register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around Uruguay's Ministerio de Salud Pública (MSP), ASSE (Administración de los Servicios de Salud del Estado), Junta Nacional de Salud (JUNASA), and adjacent bodies.

The SNIS, created by the Frente Amplio reform of 2007-2008, combines a public sub-system run by ASSE and a private not-for-profit IAMC (Instituciones de Asistencia Médica Colectiva) network, all under uniform FONASA (Fondo Nacional de Salud) financing. JUNASA contracts both networks under a per-capita-adjusted-for-risk payment.

## 2. Scope

In scope: Presidente; Ministra/o de Salud Pública; Subsecretario/a; Director General ASSE; Director MEVOS or Salud Mental; JUNASA Presidencia; MSP Direcciones Generales (Salud, Coordinación); CCSS (Cámara) Comisión de Salud; Senado Comisión de Salud Pública; Sindicato Médico del Uruguay (SMU); Federación Uruguaya de la Salud (FUS); FEMI (federación de gremios médicos del interior); Federación Médica del Interior.

## 3. Structure

Standard 2/6/10/14 indentation. Ordering: Presidencia → MSP → ASSE → JUNASA → IAMC representatives → Congreso → sindicatos profesionales.

## 4. Field definitions

Party affiliation using canonical Uruguayan abbreviations: `FA` (Frente Amplio), `PN` (Partido Nacional), `PC` (Partido Colorado), `Cabildo Abierto`, `PI` (Partido Independiente), `Identidad Soberana`. Titles in Spanish with English glosses.

## 5. Provenance and dating

Anchor facts to year, month or exact date. The Yamandú Orsi government (Frente Amplio) was sworn in 1 March 2025 after the FA's November 2024 election win. Cristina Lustemberg ha sido Ministra de Salud Pública desde 1 de marzo de 2025.

## 6. Update workflow

Verify against gub.uy/ministerio-salud-publica, presidencia.gub.uy, asse.com.uy, parlamento.gub.uy, El Observador, La Diaria, Búsqueda, Brecha, El País Uruguay.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Tratar ASSE como única entidad — el sistema IAMC mutual atiende la mayoría de la población urbana.
- Importar marcos NHS sin adaptar — el SNIS es público-privado mixto bajo financiamiento FONASA unificado.

## 9. Acronym glossary

- **ASSE** — Administración de los Servicios de Salud del Estado.
- **FONASA** — Fondo Nacional de Salud.
- **IAMC** — Instituciones de Asistencia Médica Colectiva (mutualistas).
- **JUNASA** — Junta Nacional de Salud.
- **MSP** — Ministerio de Salud Pública.
- **SMU** — Sindicato Médico del Uruguay.
- **SNIS** — Sistema Nacional Integrado de Salud.

## 10. Worked example

```yaml
      - Dra. Cristina Lustemberg (FA):
          - Title: Ministra de Salud Pública (Minister of Public Health) (desde el 1 de marzo de 2025)
          - Stakeholder engagement notes:
              - "Ministra de Salud Pública desde el 1 de marzo de 2025 en el gobierno de Yamandú Orsi (Frente Amplio); pediatra de profesión; previamente diputada del Frente Amplio."
              - "Definió equipo completo del MSP y de ASSE al asumir el cargo — uno de los primeros gabinetes técnicos articulados del gobierno Orsi."
              - "Presentó conjuntamente con OPS el Informe Anual 2025 destacando avances en salud en Uruguay (abril 2026) — alto perfil regional."
              - "Owns SNIS, FONASA, ASSE, JUNASA, IAMC contracts, primera infancia (su especialidad pediátrica), salud mental, programa de medicamentos."
              - "Hook: SNIS reform, primera infancia, salud mental, FONASA sustainability, IAMC contratos, medicamentos de alto costo aterrizan."
          - Tone advice:
              - "Abrir con SNIS, primera infancia, salud mental y FONASA — son las líneas FA y su especialización pediátrica."
              - "No tratar ASSE e IAMC como si fueran lo mismo — son dos pilares con cultura institucional distinta dentro del SNIS."
```

## 11. Out-of-band notes

For roles unfilled or interim.

## 12. Open questions

- Named Subsecretario/a, Director General ASSE, Presidencia JUNASA bajo Lustemberg.
- Direcciones Generales del MSP (Salud, Coordinación).
- Presidentes Comisiones de Salud Cámara y Senado en la actual legislatura.
- Presidente SMU, FUS, FEMI, Federación Médica del Interior.
