# spec.md — `leaders.yml`

Fuente única de verdad para el registro del sistema de salud de Guinea Ecuatorial. El YAML debe ajustarse a esta especificación.

## 1. Purpose

Registro de involucramiento de personas nombradas en el Ministerio de Sanidad y Bienestar Social de la República de Guinea Ecuatorial y entidades adyacentes.

Guinea Ecuatorial es el único Estado africano hispanohablante (oficiales: español, francés, portugués); productor de petróleo del Golfo de Guinea bajo la presidencia de Teodoro Obiang Nguema Mbasogo (PDGE, en el poder desde 1979). Sistema de salud público con apoyo cubano significativo en recursos humanos clínicos.

## 2. Scope

In scope: Presidente; Vicepresidente; Ministro de Sanidad y Bienestar Social; Secretario General; Director Hospital General de Malabo; Director Hospital Regional de Bata; Comisión de Sanidad de la Cámara de los Diputados.

Out of scope: directores provinciales; jefes de servicio.

## 3. Structure

Standard 2/6/10/14 indentation. Top-level key: `Partes interesadas del sistema de salud ecuatoguineano:`. Orden: Presidencia → Ministerio → Hospitales → Cámara.

## 4. Field definitions

Afiliación partidaria: `PDGE` (Partido Democrático de Guinea Ecuatorial, partido único de facto en el poder). Títulos en español.

## 5. Provenance and dating

Anchor to year, month or date. El Ministro de Sanidad bajo Obiang se verifica contra la Presidencia y la Agencia de Prensa de Guinea Ecuatorial (APGE).

## 6. Update workflow

Verify against guineaecuatorialpress.com, presidenciage.com, APGE.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Ignorar el sistema partido-único — Guinea Ecuatorial opera un sistema PDGE-dominante y los framings de pluralismo competitivo serán filtrados.
- Importar framings cameruneses o gaboneses — Estado distinto, hispanohablante, con dos territorios principales (Río Muni continental y Bioko insular) y arquitectura institucional propia.

## 9. Acronym glossary

- **APGE** — Agencia de Prensa de Guinea Ecuatorial.
- **PDGE** — Partido Democrático de Guinea Ecuatorial.

## 10. Worked example

```yaml
      - Dr [Nombre a verificar] (PDGE):
          - Title: Ministro de Sanidad y Bienestar Social (Minister of Health and Social Welfare)
          - Stakeholder engagement notes:
              - "Ministro de Sanidad bajo Obiang; verificar contra la Presidencia y APGE."
              - "Owns la política y el presupuesto del Ministerio, el Hospital General de Malabo, el Hospital Regional de Bata, la red provincial entre Río Muni continental e Bioko insular, la cooperación cubana en recursos humanos clínicos, y la diplomacia OMS AFRO, CEMAC y CPLP."
              - "Hook: paludismo, salud materno-infantil, NCDs, cooperación cubana, y CPLP-OMS aterrizan; framings de gran reforma estructural se filtran a través de la dirección presidencial."
          - Tone advice:
              - "Abrir con paludismo, MCH, NCDs y cooperación cubana."
              - "No ignorar el sistema PDGE ni importar framings cameruneses o gaboneses."
```

## 11. Out-of-band notes

Para cargos vacantes o interinos.

## 12. Open questions

- Identidad del Ministro de Sanidad en titularidad verificada.
- Directores hospitalarios y Presidente Comisión de Sanidad.
