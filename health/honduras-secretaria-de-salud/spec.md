# spec.md — `leaders.yml`

Single source of truth for the Honduran health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around Honduras's Secretaría de Salud (SESAL), Instituto Hondureño de Seguridad Social (IHSS), and adjacent bodies.

Honduras has a segmented system: SESAL provides care for the uninsured majority; IHSS covers formal-sector workers; private clinics serve the wealthier; military and police have separate systems. The new Asfura government (January 2026) took the unusual step of having the President personally take direct charge of the Health portfolio.

## 2. Scope

In scope: Presidente; Vicepresidentes (three); Secretario/a de Salud or coordinating vice-presidents; Vice-Ministros; Director IHSS; Director Agencia de Regulación Sanitaria (ARSA); Comisión de Salud Pública del Congreso Nacional; Colegio Médico de Honduras.

## 3. Structure

Standard. Ordering: Presidencia → SESAL → IHSS → ARSA → Comisión del Congreso → Colegio Médico.

## 4. Field definitions

Party affiliation using canonical Honduran abbreviations: `Partido Nacional` (PN), `Libre` (Libertad y Refundación — Castro), `Partido Liberal` (PL), `PINU`, `Salvador de Honduras`. Titles in Spanish with English glosses.

## 5. Provenance and dating

Anchor facts to year, month or exact date. Nasry "Tito" Asfura (Partido Nacional) was sworn in 27 January 2026 after the November 2025 election; he personally assumed direct charge of the Secretaría de Salud and announced no separate Health Minister, instead operating with three Vice-Presidents (María Antonieta Mejía, Diana Herrera, Carlos Flores Guifarro) and Vice-Ministers Ángel Midence (Redes Integradas de Servicios de Salud) and José Miguel Castillo (Proyectos e Inversión).

## 6. Update workflow

Verify against salud.gob.hn, presidencia.gob.hn, ihss.hn, congreso.gob.hn, La Prensa Honduras, El Heraldo, La Tribuna, Tiempo, Proceso Digital.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Asumir que existe Secretario/a de Salud titular — la administración Asfura optó por que el Presidente la ejerza directamente.
- Importar NHS sin adaptar — Honduras enfrenta crisis sanitaria sostenida y dependencia de cooperación.

## 9. Acronym glossary

- **ARSA** — Agencia de Regulación Sanitaria.
- **IHSS** — Instituto Hondureño de Seguridad Social.
- **SESAL** — Secretaría de Salud (sometimes written as Secretaría de Salud Pública).

## 10. Worked example

```yaml
      - Nasry Juan "Tito" Asfura Zablah (Partido Nacional):
          - Title: Presidente de la República y Secretario de Salud (in-charge) (desde 27 de enero de 2026)
          - Stakeholder engagement notes:
              - "Presidente de la República desde 27 de enero de 2026; Partido Nacional; ex-Alcalde de Tegucigalpa; tomó la decisión inusual de asumir personalmente la cartera de Salud, sin designar un Secretario titular."
              - "Justificación pública: control directo sobre los servicios sanitarios; los tres Vicepresidentes (María Antonieta Mejía, Diana Herrera, Carlos Flores Guifarro) acompañan la cartera; Ángel Midence como Vice-Ministro de Redes Integradas de Servicios de Salud y José Miguel Castillo como Sub-Secretario de Proyectos e Inversión."
              - "Owns la rectoría operativa de SESAL, IHSS coordinación, ARSA, redes hospitalarias departamentales, e inicio del Plan Asfura de Salud — política sanitaria definida directamente desde la Presidencia."
              - "Hook: infraestructura hospitalaria nueva, salud materno-infantil, dengue y vectores, cobertura sanitaria universal, IHSS reform aterrizan; pitches deben canalizarse vía Vice-Ministros y Casa Presidencial."
          - Tone advice:
              - "Abrir con infraestructura hospitalaria, IHSS, dengue, y prioridades del Plan Asfura de Salud — son las líneas explícitas del Presidente."
              - "No buscar Secretario/a titular — la estructura es presidencial con Vice-Ministros operativos; cualquier framing que asuma una jefatura ministerial separada será corregido."
```

## 11. Out-of-band notes

The above explains why a Secretario/a titular is not listed.

## 12. Open questions

- Confirmar continuidad del arreglo presidencial-directo durante el mandato Asfura.
- Director IHSS, Director ARSA con vigencia verificada.
- Presidente Comisión de Salud Pública del Congreso Nacional.
- Presidente Colegio Médico de Honduras.
