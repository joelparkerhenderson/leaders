# spec.md — `leaders.yml`

Single source of truth for the Guatemalan health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around Guatemala's Ministerio de Salud Pública y Asistencia Social (MSPAS), Instituto Guatemalteco de Seguridad Social (IGSS), and adjacent bodies.

The Guatemalan system is highly fragmented and underfunded. MSPAS attends to the uninsured majority through three levels of care; IGSS covers formal-sector workers (~17%); private clinics serve the wealthier (~10%); military and police have separate systems.

## 2. Scope

In scope: Presidente; Ministro/a MSPAS; Viceministros (Atención Primaria; Hospitales; Administrativo; Tecnología y Salud); Gerente IGSS; Director Laboratorio Nacional de Salud; Áreas de Salud directors; Congreso Comisión de Salud y Asistencia Social; Colegio de Médicos y Cirujanos de Guatemala; Colegio de Farmacéuticos y Químicos.

## 3. Structure

Standard. Ordering: Presidencia → MSPAS → IGSS → Laboratorio Nacional → Áreas de Salud → Congreso → colegios.

## 4. Field definitions

Party affiliation using canonical Guatemalan abbreviations: `Semilla` (Movimiento Semilla — Arévalo), `Vamos`, `UNE`, `Cabal`, `VOS`, `Valor`, `Todos`, `Viva`. Titles in Spanish with English glosses.

## 5. Provenance and dating

Anchor facts to year, month or exact date. Bernardo Arévalo de León (Semilla) was sworn in 14 January 2024. Dr. Joaquín Barnoya Pérez fue designado Ministro de Salud Pública y Asistencia Social en julio 2024, sustituyendo a Óscar Cordón Cruz quien renunció por motivos personales.

## 6. Update workflow

Verify against mspas.gob.gt, presidencia.gob.gt, igssgt.org, congreso.gob.gt, Prensa Libre, elPeriódico, La Hora, eP Investiga, Agencia Guatemalteca de Noticias (AGN), Soy502.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Tratar al MSPAS como entidad funcional plena — el sistema enfrenta desnutrición crónica infantil, brechas presupuestales severas y dependencia de cooperación OPS / USAID históricamente.
- Importar NHS sin adaptar — Guatemala es fragmentado y constrainted por ingresos fiscales bajos.

## 9. Acronym glossary

- **IGSS** — Instituto Guatemalteco de Seguridad Social.
- **MSPAS** — Ministerio de Salud Pública y Asistencia Social.
- **OPS/OMS** — Organización Panamericana de la Salud / OMS.

## 10. Worked example

```yaml
      - Dr. Joaquín Barnoya Pérez (Semilla / no partidario):
          - Title: Ministro de Salud Pública y Asistencia Social (Minister of Public Health and Social Assistance) (desde julio de 2024)
          - Stakeholder engagement notes:
              - "Ministro de Salud Pública y Asistencia Social desde julio de 2024 en el gobierno de Bernardo Arévalo de León (Movimiento Semilla); designado tras la renuncia de Óscar Cordón Cruz por motivos personales el 13 de junio."
              - "Médico, investigador de prestigio internacional en control del tabaco — la OPS / OMS Guatemala reconoció en febrero 2026 su liderazgo en la decisión de Estado que consolida la posición internacional de Guatemala en control del tabaco."
              - "Mensaje inaugural al personal: 'Solo soy una persona más del equipo y vengo a trabajar con ustedes' — perfil técnico y horizontal, contrastante con perfiles políticos previos."
              - "Sobrevivió interpelación en el Congreso con nueve acuerdos que pusieron fin al proceso — superó un momento de tensión política temprano en el mandato."
              - "En junio 2026 desarrolló con apoyo de OPS / OMS misión técnica para acelerar el fortalecimiento de la atención primaria para respuesta a enfermedades no transmisibles."
              - "Hook: control del tabaco, NCDs y atención primaria, salud materno-infantil y desnutrición crónica, infraestructura hospitalaria, cooperación OPS aterrizan."
          - Tone advice:
              - "Abrir con control del tabaco, NCDs, atención primaria y cooperación OPS — son las líneas autorales y los reconocimientos internacionales de Barnoya."
              - "No buscar atajos políticos — Barnoya opera como técnico-académico y rechaza framings partidarios o de captura."
```

## 11. Out-of-band notes

For roles unfilled or interim.

## 12. Open questions

- Named Viceministros bajo Barnoya con vigencia verificada.
- Gerente IGSS y Director Laboratorio Nacional de Salud con vigencia verificada.
- Directores de Áreas de Salud regionales.
- Presidente Comisión de Salud y Asistencia Social del Congreso.
- Presidente Colegio de Médicos y Cirujanos de Guatemala.
