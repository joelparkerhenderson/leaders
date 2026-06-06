# spec.md — `leaders.yml`

Single source of truth for the Cuban health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Cuban Ministerio de Salud Pública (MINSAP), CECMED (medicines authority), the Cuban network of policlínicos and hospitals, and adjacent bodies.

The Cuban system is fully public, universal, free at point of use, and government-managed. Primary care via family medicine (médico de familia) and policlínicos; secondary and tertiary care through provincial and national hospitals; tertiary research via Instituto Pedro Kourí (IPK), Cardiocentro, Hermanos Ameijeiras and others. Cuban medical brigades operate internationally (currently in dozens of countries) as a major foreign-exchange and diplomatic asset. The system is in severe crisis as of 2025-2026 with shortages of medicines, equipment and personnel attributed by the government to the US embargo.

## 2. Scope

In scope: Presidente Miguel Díaz-Canel; First Secretary PCC; Vice-Presidente; Ministro de Salud Pública; Viceministros; Director CECMED; Director Centros de Investigación y Desarrollo de Medicamentos (CIDEM); Director Instituto Pedro Kourí (IPK); Directors of major hospitals (Hermanos Ameijeiras, Cardiocentro, CIMEQ, William Soler); Asamblea Nacional Comisión de Salud y Deporte; FETSS (sindicato); BioCubaFarma (state biopharmaceutical holding) leadership.

## 3. Structure

Standard 2/6/10/14. Ordering: Presidencia → MINSAP → CECMED → IPK → CIDEM → BioCubaFarma → grandes hospitales → Asamblea Nacional Comisión → sindicato.

## 4. Field definitions

Party affiliation: PCC (Partido Comunista de Cuba) is the single legal party; senior MINSAP officials are PCC members. Titles in Spanish with English glosses.

## 5. Provenance and dating

Dr. José Ángel Portal Miranda has served as Ministro de Salud Pública since 2018. In February 2026 he told AP that the Cuban healthcare system is 'on the brink of collapse' due to the US embargo on oil; in March 2026 he addressed US efforts to deprive the Cuban people of medical care; in May 2026 he toured rehabilitating hospitals in Santiago de Cuba. Cuba launched 'Plan por la Salud y la Vida 2026'.

## 6. Update workflow

Verify against minsap.gob.cu, cubadebate.cu, granma.cu, cibercuba.com, prensa-latina.cu, MINREX (mid.gov.cu / minrex.gob.cu), AFP, AP and Reuters Latin America bureau.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating the system as functional at pre-2017 levels — current operational reality involves significant shortages.
- Ignoring the international cooperation dimension — Cuban medical brigades in dozens of countries (Venezuela, Algeria, Mexico, Italy, Honduras, Belize and others) are structural to MINSAP and Cuban foreign policy.

## 9. Acronym glossary

- **BioCubaFarma** — state biopharmaceutical holding (vaccines including SOBERANA, Abdala; cancer treatments including CIMAvax; biotechnology).
- **CECMED** — Centro para el Control Estatal de Medicamentos, Equipos y Dispositivos Médicos.
- **CIMEQ** — Centro de Investigaciones Médico-Quirúrgicas.
- **IPK** — Instituto Pedro Kourí (tropical medicine and infectious diseases).
- **MINSAP** — Ministerio de Salud Pública.
- **PCC** — Partido Comunista de Cuba.

## 10. Worked example

```yaml
      - Dr. José Ángel Portal Miranda (PCC):
          - Title: Ministro de Salud Pública (Minister of Public Health) (desde 2018)
          - Stakeholder engagement notes:
              - "Ministro de Salud Pública desde 2018; PCC; médico de profesión; ha encabezado MINSAP a lo largo del periodo de crisis sostenida del sistema sanitario cubano, agudizado por el bloqueo estadounidense y la pandemia."
              - "Declaró a AP en febrero de 2026 que el sistema de salud cubano está 'al borde del colapso' por el bloqueo estadounidense sobre suministros petroleros; en marzo de 2026 (Pravda ES vía Victor Ternovsky) abordó los esfuerzos estadounidenses por dejar al pueblo cubano sin atención médica; en mayo de 2026 recorrió hospitales en rehabilitación en Santiago de Cuba (Cubadebate)."
              - "Owns la rectoría del sistema, las brigadas médicas internacionales (Venezuela, Honduras, Belize, Italia, México, Argelia, etc., como activo diplomático y de divisas), la articulación con BioCubaFarma para producción nacional de medicamentos y vacunas (SOBERANA, Abdala, CIMAvax), la formación médica en ELAM, y representación en OMS / OPS."
              - "Intervino en la 79ª Asamblea Mundial de la Salud y en la sesión especial; activo en la diplomacia sanitaria del Sur Global."
              - "Hook: brigadas médicas, BioCubaFarma vacunas y biotecnología, formación médica ELAM, bloqueo y acceso a medicamentos, atención primaria 'modelo cubano', diplomacia OMS/OPS aterrizan."
          - Tone advice:
              - "Abrir con brigadas médicas, BioCubaFarma, atención primaria, formación ELAM y bloqueo — son los frames sostenidos de MINSAP en el contexto político actual."
              - "No proponer marcos comerciales o de cooperación con organismos vinculados al bloqueo — la posición política es explícita y los framings vinculados a Washington serán rechazados; cooperación Sur-Sur, ALBA, BRICS+, ONU sistemas, OPS son las vías legítimas."
```

## 11. Out-of-band notes

For roles unfilled or in transition.

## 12. Open questions

- Named Viceministros de MINSAP bajo Portal Miranda con vigencia verificada.
- Director CECMED, Director IPK, Director CIDEM con vigencia verificada.
- Presidente BioCubaFarma con vigencia verificada.
- Directores de los principales hospitales (Hermanos Ameijeiras, Cardiocentro, CIMEQ, William Soler).
- Presidente Comisión de Salud y Deporte de la Asamblea Nacional del Poder Popular.
- Secretario General Federación de Trabajadores de la Salud (FTSS) con vigencia verificada.
