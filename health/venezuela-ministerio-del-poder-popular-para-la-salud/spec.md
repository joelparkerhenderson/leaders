# spec.md — `leaders.yml`

Single source of truth for the Venezuelan health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Venezuelan Ministerio del Poder Popular para la Salud (MPPS), IVSS (Instituto Venezolano de los Seguros Sociales), and adjacent bodies.

The Venezuelan system is in deep humanitarian crisis since 2015-2017. The Bolivarian government's Sistema Público Nacional de Salud (SPNS) operates through the Misión Barrio Adentro (Cuban-Venezuelan medical mission), a deteriorated network of state hospitals and ambulatorios, and an under-funded IVSS. Many indicators (medicine availability, maternal mortality, infectious disease control) have regressed dramatically. The Maduro government and opposition contest political legitimacy after the 2024 election cycle.

## 2. Scope

In scope: Presidente; Vicepresidenta Ejecutiva; Ministro/a del Poder Popular para la Salud; Viceministros; Presidente IVSS; INHRR (Instituto Nacional de Higiene Rafael Rangel — vaccines, medicines); Coordinador Misión Barrio Adentro; Directores de los grandes hospitales (HUC, JM de los Ríos, Vargas, IVSS Pérez Carreño); Asamblea Nacional Comisión Permanente de Desarrollo Social Integral (Salud); FMV (Federación Médica Venezolana).

## 3. Structure

Standard 2/6/10/14 indentation. Ordering: Presidencia → Vicepresidencia Ejecutiva → MPPS → IVSS → INHRR → Misión Barrio Adentro → hospitales → AN → FMV.

## 4. Field definitions

Party affiliation: `PSUV` (Partido Socialista Unido de Venezuela), `PCV` (Partido Comunista de Venezuela), `MAS`, `Tupamaro`, `PCV`, `Somos Venezuela`; opposition: `MUD` (Mesa de la Unidad Democrática), `UNT`, `VPV`, `Primero Justicia`, `Voluntad Popular`. Titles in Spanish with English glosses.

## 5. Provenance and dating

Anchor facts to year, month or exact date. In January 2026, Vice-President Delcy Rodríguez designated Dra. Nuramy Josefa Gutiérrez González as Ministra de Salud, replacing Magaly Gutiérrez Viña (who had served since February 2022 and continues as Presidenta del IVSS). The Bolivarian government launched the "Plan por la Salud y la Vida 2026" in January 2026 emphasising Misiones in the streets.

## 6. Update workflow

Verify against mpps.gob.ve, presidencia.gob.ve, ivss.gob.ve, asambleanacional.gob.ve, Prensa Latina, Telesur, Tal Cual, Efecto Cocuyo, Armando.info, Bloomberg Línea.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Tratar al sistema como funcional al nivel pre-2014 — la crisis humanitaria ha redefinido la operación.
- Ignorar la dimensión geopolítica — Cuba (Misión Barrio Adentro), Rusia, Irán, China son socios sanitarios relevantes.

## 9. Acronym glossary

- **IVSS** — Instituto Venezolano de los Seguros Sociales.
- **INHRR** — Instituto Nacional de Higiene Rafael Rangel.
- **MPPS** — Ministerio del Poder Popular para la Salud.
- **SPNS** — Sistema Público Nacional de Salud.

## 10. Worked example

```yaml
      - Dra. Nuramy Josefa Gutiérrez González (PSUV):
          - Title: Ministra del Poder Popular para la Salud (Minister of Health) (designada en enero de 2026)
          - Stakeholder engagement notes:
              - "Designada Ministra del Poder Popular para la Salud en enero de 2026 por la Vicepresidenta Ejecutiva Delcy Rodríguez, reemplazando a Magaly Gutiérrez Viña (en el cargo desde febrero de 2022)."
              - "Magaly Gutiérrez Viña continúa como Presidenta del IVSS — la rotación interna del PSUV mantiene un equipo coherente en el sector salud-seguridad social."
              - "Asume bajo el lanzamiento del 'Plan por la Salud y la Vida 2026' del Gobierno Bolivariano, enfocado en el despliegue de Misiones en las calles para fortalecer atención integral."
              - "Contexto: emergencia humanitaria compleja persistente; deterioro de infraestructura hospitalaria; éxodo de personal médico; cooperación cubana mantenida vía Misión Barrio Adentro; sanciones estadounidenses afectando importación de medicamentos."
              - "Hook: Plan por la Salud y la Vida 2026, Misiones, atención primaria, medicamentos básicos, vacunación, cooperación con Cuba/Rusia/Irán/China, presencia internacional en AMS aterrizan."
          - Tone advice:
              - "Abrir con el Plan por la Salud y la Vida 2026, Misiones, atención primaria — son las líneas oficiales del gobierno bolivariano y los marcos discursivos del PSUV en salud."
              - "No proponer cooperación con organismos estadounidenses o vinculados a sanciones — la política sanitaria está politizada y los framings vinculados a Washington serán rechazados; la cooperación va por OMS, OPS, Cuba, Rusia, Irán y China."
```

## 11. Out-of-band notes

For roles unfilled or interim. Note that political legitimacy is contested between the Maduro government and the opposition coalition led by María Corina Machado (de jure recognised by some governments).

## 12. Open questions

- Confirm Dra. Nuramy Gutiérrez González biographical detail and partido political affiliation.
- Named Viceministros del MPPS bajo Gutiérrez González.
- INHRR Director with currency verified.
- Coordinador Misión Barrio Adentro and Cuban-side medical-mission counterparts.
- Directores de los grandes hospitales (HUC, JM de los Ríos, Vargas, IVSS Pérez Carreño).
- AN Comisión Permanente de Desarrollo Social Integral (Salud) Presidente.
- FMV Presidente with currency verified.
