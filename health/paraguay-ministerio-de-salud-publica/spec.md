# spec.md — `leaders.yml`

Single source of truth for the Paraguayan health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Paraguayan Ministerio de Salud Pública y Bienestar Social (MSPBS), IPS (Instituto de Previsión Social), DINAVISA (medicines agency), and adjacent bodies.

The Paraguayan system has three sub-systems: MSPBS provides care for the uninsured ~75%; IPS covers formal-sector workers (~20%); private clinics serve the wealthier. Paraguay launched a Digital Health Agenda and is running PAHO's imPACT mission against cancer.

## 2. Scope

In scope: Presidente; Ministro/a de Salud Pública y Bienestar Social; Viceministros; Director IPS; Director DINAVISA; Director Servicio Nacional de Erradicación del Paludismo (SENEPA); Cámara de Diputados Comisión de Salud Pública; Cámara de Senadores Comisión de Salud Pública; Círculo Paraguayo de Médicos.

## 3. Structure

Standard 2/6/10/14 indentation. Ordering: Presidencia → MSPBS → IPS → DINAVISA → SENEPA → Congreso → asociaciones profesionales.

## 4. Field definitions

Party affiliation using canonical Paraguayan abbreviations: `ANR-PC` (Asociación Nacional Republicana — Partido Colorado), `PLRA` (Partido Liberal Radical Auténtico), `Partido Encuentro Nacional`, `Cruzada Nacional`, `Frente Guasu`, `Patria Querida`. Titles in Spanish with English glosses.

## 5. Provenance and dating

Anchor facts to year, month or exact date. Dr. María Teresa Barán Wasilchuk (Colorada) ha sido Ministra de Salud Pública y Bienestar Social desde el 15 de agosto de 2023, posesión simultánea con el inicio del gobierno de Santiago Peña (ANR-PC).

## 6. Update workflow

Verify against mspbs.gov.py, presidencia.gov.py, ips.gov.py, dinavisa.gov.py, diputados.gov.py, senado.gov.py, ABC Color, Última Hora, La Nación, IP Paraguay.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating MSPBS as único responsable — IPS atiende una fracción significativa de la población con red propia.
- Importar NHS sin adaptar — Paraguay es segmentado.

## 9. Acronym glossary

- **DINAVISA** — Dirección Nacional de Vigilancia Sanitaria (agencia de medicamentos).
- **IPS** — Instituto de Previsión Social (seguridad social paraguaya).
- **MSPBS** — Ministerio de Salud Pública y Bienestar Social.
- **SENEPA** — Servicio Nacional de Erradicación del Paludismo (también dengue, chikungunya).

## 10. Worked example

```yaml
      - Dra. María Teresa Barán Wasilchuk (ANR-PC):
          - Title: Ministra de Salud Pública y Bienestar Social (Minister of Public Health and Social Welfare) (desde el 15 de agosto de 2023)
          - Stakeholder engagement notes:
              - "Ministra de Salud Pública y Bienestar Social desde el 15 de agosto de 2023 en el gobierno de Santiago Peña (ANR Partido Colorado); cirujana, especialista en Medicina Familiar, con extensa experiencia en salud pública; nacida el 25 de agosto de 1970."
              - "Anteriormente había sido Encargada de Despacho del MSPBS, lo que le dio continuidad institucional al asumir el cargo titular."
              - "Owns la rectoría del sistema, la articulación con IPS, DINAVISA y SENEPA, el Sistema de Protección Social, la Agenda de Salud Digital (Conectatón 2026), y la Misión imPACT 2026 de la IAEA / OMS para respuesta nacional al cáncer."
              - "Hook: salud digital y interoperabilidad, atención primaria, cáncer (imPACT 2026), enfermedades vectoriales (dengue), articulación intersectorial con MEC y MTESS, IPS reform aterrizan."
          - Tone advice:
              - "Abrir con salud digital, interoperabilidad, cáncer (imPACT), atención primaria y articulación intersectorial — son las prioridades visibles del Ministerio en 2026."
              - "No pitchear como si MSPBS fuera el único pagador — el IPS tiene autonomía y arquitectura institucional propia; framings unitarios serán corregidos."
```

## 11. Out-of-band notes

For roles unfilled or interim.

## 12. Open questions

- Named Viceministros bajo Barán with currency verified.
- Director IPS, DINAVISA, SENEPA with currency verified.
- Presidente Comisión de Salud Pública Cámara de Diputados y Senado.
- Círculo Paraguayo de Médicos and other professional bodies.
