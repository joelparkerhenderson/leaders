# spec.md — `leaders.yml`

Single source of truth for the Angolan health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Angolan Ministério da Saúde (MINSA), Direcção Nacional de Medicamentos e Equipamentos (DNME), Instituto Nacional de Saúde Pública (INSP), Hospital Josina Machel and Hospital Maria Pia, and adjacent bodies.

The Angolan system is tax-funded with significant donor coordination; MINSA runs the public network; 18 provincial Direcções Provinciais de Saúde manage operational delivery; significant private and church-affiliated health-services sector.

## 2. Scope

In scope: Presidente; Vice-Presidente; Ministro/a da Saúde; Secretários de Estado; DG INSP; DG DNME; Director Hospital Josina Machel; Directores Provinciais de Saúde (18 provinces); Assembleia Nacional Comissão de Política Social, Ambiente, Saúde e Educação; Ordem dos Médicos de Angola.

## 3. Structure

Standard. Ordering: Presidência → Vice-Presidência → MINSA → INSP → DNME → Hospital Josina Machel → 18 DPS → Assembleia → Ordem.

## 4. Field definitions

Party affiliation: `MPLA` (Movimento Popular de Libertação de Angola — Lourenço), `UNITA` (União Nacional para a Independência Total de Angola). Titles in Portuguese / English.

## 5. Provenance and dating

Dra. Sílvia Paula Valentim Lutucuta has served as Ministra da Saúde de Angola since 2017 (with appointment formally renewed 16 September 2022); long-tenured; cardiologist; represented Angola at the World Health Summit Regional Meeting 2026 in Nairobi (April 2026); reaffirmed Angola's commitment to dracunculiasis eradication at WHA79 (21 May 2026).

## 6. Update workflow

Verify against minsa.gov.ao, governo.gov.ao, parlamento.ao, ANGOP, Jornal de Angola, O País Angola, Novo Jornal.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Importing US framings — Angola is oil-revenue funded with significant CPLP and Chinese partnerships.
- Ignoring provincial heterogeneity — 18 provinces vary widely in health-service access.

## 9. Acronym glossary

- **DNME** — Direcção Nacional de Medicamentos e Equipamentos.
- **INSP** — Instituto Nacional de Saúde Pública.
- **MINSA** — Ministério da Saúde.

## 10. Worked example

```yaml
      - Dra. Sílvia Paula Valentim Lutucuta (MPLA):
          - Title: Ministra da Saúde de Angola (since 2017; appointment formally renewed 16 September 2022)
          - Stakeholder engagement notes:
              - "Ministra da Saúde de Angola desde 2017 no governo MPLA do Presidente João Lourenço; appointment formally renewed 16 September 2022; cardiologista; longa tenure no portfolio."
              - "Active 2026: representou Angola na Cúpula Mundial da Saúde 2026 / World Health Summit Regional Meeting em Nairobi (27-29 April 2026, OPaís Angola); reafirmou o compromisso de Angola em erradicar a dracunculíase numa reunião ministerial de alto nível no dia 21 de maio de 2026 na Assembleia Mundial da Saúde (WHA79); discursou na aula inaugural da Universidade de São Paulo sobre avanços na formação de quadros de saúde."
              - "Apresentou tolerância zero a actos de mau-uso na campanha do Cunene (UNICEF Angola)."
              - "Owns MINSA policy, INSP public-health institute, DNME pharmaceuticals and equipment, Hospital Josina Machel and Hospital Maria Pia, 18 Direcções Provinciais de Saúde, formação de quadros de saúde (parcerias com USP Brasil), e Angola's WHO Africa, CPLP, SADC e cooperação China-Angola no sector da saúde."
              - "Hook: erradicação da dracunculíase (uma das doenças negligenciadas), MPLA Plano Nacional de Saúde, oncologia nacional, formação de quadros, parcerias CPLP e BRICS+ atterissem."
          - Tone advice:
              - "Abrir com erradicação da dracunculíase, formação de quadros, MPLA Plano Nacional de Saúde e cooperação CPLP — são as linhas autoréais sostenidas de Lutucuta em 2026."
              - "Não pitchear em framings que ignorem a cooperação China-Angola — China é um parceiro maior na infra-estrutura de saúde angolana."
```

## 11. Out-of-band notes

For roles unfilled or in transition.

## 12. Open questions

- Named Secretários de Estado da Saúde under Lutucuta with currency verified.
- DG INSP e DG DNME with currency verified.
- Director Hospital Josina Machel and outros hospitais centrais.
- Directores Provinciais de Saúde of 18 provinces — priority Luanda, Huambo, Benguela, Huíla, Cabinda.
- Assembleia Nacional Comissão de Política Social, Ambiente, Saúde e Educação Chair with currency verified.
- Bastonário Ordem dos Médicos de Angola with currency verified.
