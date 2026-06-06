# spec.md — `leaders.yml`

Single source of truth for the structure, semantics, and update rules of `leaders.yml` for the Chilean sistema de salud. The YAML must conform to this spec; if they disagree, the spec wins and the YAML is fixed.

## 1. Purpose

`leaders.yml` is an engagement register of named individuals in and around the Chilean health system. The system has two main segments: FONASA (Fondo Nacional de Salud, public single payer for ~78% of the population) and ISAPRES (private insurance for the wealthier ~17%); the SNSS (Sistema Nacional de Servicios de Salud) operates public hospitals through 29 regional Servicios de Salud. Minsal sets policy; the Superintendencia de Salud regulates; ISP (Instituto de Salud Pública) regulates medicines and devices.

## 2. Scope

**In scope:** Presidente; Ministra/o de Salud; Subsecretarios (Salud Pública; Redes Asistenciales); Director FONASA; Superintendente de Salud; Director ISP; Director Cenabast; Directores de los 29 Servicios de Salud (priorizar Servicios Metropolitanos y los grandes regionales); Presidente Comisión de Salud Cámara de Diputados; Presidente Comisión de Salud Senado; Presidente Colegio Médico de Chile; Presidente Colegio de Enfermeras; Presidente Colegio de Químicos Farmacéuticos.

## 3. Structure

```
Sistema de salud chileno — partes interesadas:
  - {Organisation}:
      - {Person}:
          - Title: ...
          - Stakeholder engagement notes: [...]
          - Tone advice: [...]
```

Standard indentation. Ordering: Presidencia → Minsal → Subsecretarías → FONASA → Superintendencia → ISP → Cenabast → 29 Servicios de Salud → Congreso → colegios profesionales.

## 4. Field definitions

Standard family conventions. Party affiliation using canonical Chilean abbreviations: `RN`, `UDI`, `Republicano`, `Evópoli`, `PSCh`, `PPD`, `PRSD`, `PC`, `CS` (Convergencia Social), `RD` (Revolución Democrática), `FA` (Frente Amplio), `DC`, `Demócratas`, `PdG` (Partido de la Gente). Titles in Spanish with English glosses.

## 5. Provenance and dating

Anchor facts to year, month or exact date. José Antonio Kast (Partido Republicano) won the December 2025 presidential runoff against the continuing-coalition candidate. His government was sworn in 11 March 2026. Dr. May Chomalí Garib (Independent) assumed as Ministra de Salud on 11 March 2026; she had been Executive Director of CENS (National Centre for Health Information Systems) until January 2026. She succeeded Dr. Ximena Aguilera Sanhueza (independent, in the Boric government 2022-2026).

## 6. Update workflow

Verify against minsal.cl, gob.cl, fonasa.cl, supersalud.gob.cl, ispch.gob.cl, camara.cl, senado.cl, El Mercurio, La Tercera, El Mostrador, BioBioChile, Cooperativa, T13, CIPER.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating Servicios de Salud as Ministry subunits — they are statutory entities under the SNSS framework.
- Importing NHS framings unmodified — Chile is mixed FONASA-ISAPRES with strong private participation; reform proposals must engage both pillars.

## 9. Acronym glossary

- **AUGE / GES** — Acceso Universal a Garantías Explícitas / Garantías Explícitas en Salud (the explicit-guarantees system from 2005).
- **Cenabast** — Central Nacional de Abastecimiento.
- **CENS** — Centro Nacional en Sistemas de Información en Salud.
- **FONASA** — Fondo Nacional de Salud.
- **ISAPRES** — Instituciones de Salud Previsional.
- **ISP** — Instituto de Salud Pública de Chile.
- **Minsal** — Ministerio de Salud.
- **SNSS** — Sistema Nacional de Servicios de Salud.
- **Superintendencia de Salud** — Superintendencia que regula FONASA, ISAPRES y prestadores.

## 10. Worked example

```yaml
      - Dra. May Chomalí Garib (Ind.):
          - Title: Ministra de Salud (Minister of Health) (desde el 11 de marzo de 2026, gobierno de José Antonio Kast)
          - Stakeholder engagement notes:
              - "Ministra de Salud desde el 11 de marzo de 2026 en el gobierno de José Antonio Kast (Partido Republicano); designada como independiente; cirujana egresada de la Facultad de Medicina de la Universidad de Chile, con posgrados en Epidemiología y Salud Pública y diplomado en Gestión en Salud."
              - "Hasta enero de 2026 fue Directora Ejecutiva del Centro Nacional en Sistemas de Información en Salud (CENS), institución dedicada a la interoperabilidad y modernización digital del sistema de salud chileno — perfil técnico-digital inusual para un Ministerio históricamente dominado por epidemiólogos o gestores clínicos."
              - "Hija del odontólogo Juan Chomalí; hermana del Cardenal Fernando Chomalí, Arzobispo de Santiago — perfil familiar con conexiones eclesiales relevantes en la política chilena."
              - "Owns el ciclo presupuestario 2026-2030 del Minsal, las redes asistenciales SNSS, FONASA, Superintendencia de Salud, ISP, Cenabast, GES, salud mental, listas de espera quirúrgicas y la agenda de transformación digital del sistema (Chomalí es especialista en este último campo)."
              - "Hook: transformación digital, interoperabilidad, listas de espera, GES, reforma ISAPRES post-fallos Corte Suprema, Cenabast, salud mental aterrizan; pitches que ignoran el segmento ISAPRES no aterrizan."
          - Tone advice:
              - "Abrir con transformación digital, interoperabilidad, listas de espera y reforma de ISAPRES — son su campo de especialización (CENS) y las prioridades políticas del gobierno Kast en salud."
              - "No pitchear como si FONASA fuera el único pagador — el sistema dual FONASA-ISAPRES es estructural y políticamente sensible; framings unitarios serán corregidos."
```

## 11. Out-of-band notes

For roles unfilled or interim.

## 12. Open questions

- Named Subsecretarios de Salud Pública y de Redes Asistenciales bajo Chomalí with currency verified.
- Director FONASA, Superintendente de Salud, Director ISP, Director Cenabast with currency verified.
- Directores de los 29 Servicios de Salud, priorizando los Metropolitanos y grandes regionales.
- Presidente Comisión de Salud Cámara y Senado en el período legislativo actual.
- Presidente Colegio Médico, Colegio de Enfermeras, Colegio de Químicos Farmacéuticos.
