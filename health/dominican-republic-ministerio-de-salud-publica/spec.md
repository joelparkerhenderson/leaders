# spec.md — `leaders.yml`

Single source of truth for the Dominican Republic health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Dominican Ministerio de Salud Pública y Asistencia Social (MSP), Servicio Nacional de Salud (SNS), Seguro Nacional de Salud (SENASA), Superintendencia de Salud y Riesgos Laborales (SISALRIL), and adjacent bodies.

The Dominican system implemented Ley 87-01 in 2001 separating financing (SDSS / Sistema Dominicano de Seguridad Social) from delivery (SNS). SENASA administers the subsidised regime; ARS contributory regime; private insurance for the wealthier. SNS operates public hospitals through nine Regional Health Services. MSP sets policy and rectoría.

## 2. Scope

In scope: Presidente; Ministro/a de Salud Pública y Asistencia Social; Viceministros; Director Ejecutivo SNS; Director Ejecutivo SENASA; Superintendente SISALRIL; Director DIGEPRES (medicines); Director Servicio Nacional de Salud regional directors; Senado Comisión Permanente de Salud; Cámara de Diputados Comisión Permanente de Salud; Presidente Colegio Médico Dominicano (CMD); Colegio Dominicano de Enfermería; Colegio Dominicano de Farmacéuticos.

## 3. Structure

Standard 2/6/10/14. Ordering: Presidencia → MSP → SNS → SENASA → SISALRIL → DIGEPRES → Congreso → colegios profesionales.

## 4. Field definitions

Party affiliation using canonical Dominican abbreviations: `PRM` (Partido Revolucionario Moderno — Abinader), `PLD` (Partido de la Liberación Dominicana), `FP` (Fuerza del Pueblo — Leonel Fernández), `PRD`, `PRSC`, `Alianza País`. Titles in Spanish with English glosses.

## 5. Provenance and dating

Dr. Víctor Atallah was designated Ministro de Salud Pública y Asistencia Social by Decreto 36-24 in January 2024 by President Luis Abinader (PRM), replacing Dr. Daniel Rivera. Cardiologist, with postgraduate training at Lenox Hill Hospital and Cornell Medical School. In May 2026, Atallah assumed the Presidency of the 79th World Health Assembly — first time the Dominican Republic has held this role. Continues active through mid-2026.

## 6. Update workflow

Verify against msp.gob.do, presidencia.gob.do, sns.gob.do, senasa.gob.do, sisalril.gob.do, senado.gob.do, camaradediputados.gob.do, Diario Libre, Listín Diario, El Caribe, Acento, Hoy.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating MSP as the only counterparty — SNS, SENASA and ARS together form the operational architecture.
- Importing NHS framings unmodified — Dominican Republic separates financing and delivery formally under Ley 87-01.

## 9. Acronym glossary

- **ARS** — Administradoras de Riesgos de Salud (private and public health-insurance administrators).
- **CMD** — Colegio Médico Dominicano.
- **MSP** — Ministerio de Salud Pública y Asistencia Social.
- **SDSS** — Sistema Dominicano de Seguridad Social.
- **SENASA** — Seguro Nacional de Salud.
- **SISALRIL** — Superintendencia de Salud y Riesgos Laborales.
- **SNS** — Servicio Nacional de Salud.

## 10. Worked example

```yaml
      - Dr. Víctor Atallah (PRM):
          - Title: Ministro de Salud Pública y Asistencia Social (Minister of Public Health and Social Assistance) (desde enero de 2024 por Decreto 36-24)
          - Stakeholder engagement notes:
              - "Ministro de Salud Pública y Asistencia Social designado por Decreto Presidencial 36-24 en enero de 2024 por el Presidente Luis Abinader (PRM), reemplazando al Dr. Daniel Rivera; PRM."
              - "Graduado Magna Cum Laude en Medicina del Instituto Tecnológico de Santo Domingo (INTEC); posgrado en Medicina Interna, Cardiología, Cardiología Nuclear y Cardiología Intervencionista en Lenox Hill Hospital, afiliado a Cornell Medical School en Nueva York; diplomados del American Board of Internal Medicine y Nuclear Cardiology, y certificaciones del American College of Cardiology."
              - "Fundador y presidente de la Fundación Víctor Atallah, entidad sin fines de lucro; participó en la construcción del centro de asistencia médica para víctimas de la tragedia de Jimaní (2004), que también atendió en el terremoto de Haití de 2010 (cobertura del New York Times, Wall Street Journal, People Magazine)."
              - "En mayo de 2026 asumió la Presidencia de la 79ª Asamblea Mundial de la Salud (WHA79) — primera vez que la República Dominicana asume esta presidencia; destacó en Roma los avances dominicanos en nutrición y sistemas alimentarios sostenibles."
              - "Owns la rectoría MSP, articulación con SNS / SENASA / SISALRIL, juramentó a Julio César Landrón como director del SNS; coordina con UNICEF, OPS y Plan Internacional de Alimentación Escolar."
              - "Hook: presidencia WHA, nutrición y sistemas alimentarios, articulación SNS-SENASA-SISALRIL, atención primaria, política farmacéutica, infraestructura hospitalaria aterrizan."
          - Tone advice:
              - "Abrir con presidencia WHA, nutrición, atención primaria y articulación financiera-delivery — son sus líneas de mandato y proyección internacional."
              - "No tratar MSP como el único actor — SNS es prestador, SENASA y ARS son aseguradores; framings deben respetar la separación financiera-delivery de Ley 87-01."
```

## 11. Out-of-band notes

For roles unfilled or in transition.

## 12. Open questions

- Named Viceministros del MSP bajo Atallah con vigencia verificada.
- Director Ejecutivo SENASA y Superintendente SISALRIL con vigencia verificada.
- Director DIGEPRES con vigencia verificada.
- Directores de las nueve Direcciones Regionales del SNS.
- Presidentes Comisión Permanente de Salud Senado y Cámara de Diputados.
- Presidente CMD, Colegio Dominicano de Enfermería, Colegio Dominicano de Farmacéuticos.
