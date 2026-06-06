# spec.md — `leaders.yml`

Single source of truth for the Mozambican health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Mozambican Ministério da Saúde (MISAU), Central de Medicamentos e Artigos Médicos (CMAM), Instituto Nacional de Saúde, Hospital Central de Maputo, and adjacent bodies.

The Mozambican system is tax-funded with significant donor coordination; MISAU runs the public network through Provincial and District Health Directorates; northern provinces (Cabo Delgado, Nampula, Niassa) face insurgency-related health-service disruption.

## 2. Scope

In scope: President; PM; Ministro da Saúde; Vice-Ministros; Secretário Permanente; DG INS; DG CMAM; Director Hospital Central de Maputo; Director Hospital Central de Beira; Directors Provincial Health Directorates (10 provinces); Assembleia da República Comissão de Política Social; Ordem dos Médicos.

## 3. Structure

Standard. Ordering: President → PM → MISAU → CMAM → INS → Hospitais Centrais → 10 DPS → Assembleia → Ordem.

## 4. Field definitions

Party affiliation: `Frelimo` (ruling), `Renamo` (opposition), `MDM`. Titles in Portuguese / English.

## 5. Provenance and dating

Dr. Ussene Hilário Isse serves as Ministro da Saúde; surgeon by specialty; active 2026 on medicines-management rigor, anti-corruption in the medicines chain (CMAM), and system-resilience messaging amid Cabo Delgado insurgency and post-Idai-Daniel-cyclone reconstruction.

## 6. Update workflow

Verify against misau.gov.mz, portaldogoverno.gov.mz, parlamento.mz, cmam.gov.mz, Notícias, O País Moçambique, MMO News, AIM News, Mediafax.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Importing US framings — Mozambique is highly donor-coordinated.
- Ignoring Cabo Delgado context — northern-provinces health response requires specific framings.

## 9. Acronym glossary

- **CMAM** — Central de Medicamentos e Artigos Médicos.
- **DPS** — Direcção Provincial de Saúde.
- **INS** — Instituto Nacional de Saúde.
- **MISAU** — Ministério da Saúde.

## 10. Worked example

```yaml
      - Dr. Ussene Hilário Isse (Frelimo):
          - Title: Ministro da Saúde de Moçambique
          - Stakeholder engagement notes:
              - "Ministro da Saúde de Moçambique; médico cirurgião especialista; perfil no portaldogoverno.gov.mz; biografia médico-académica."
              - "Active 2026: 'O Ministro da Saúde, Ussene Isse, afirmou que o sistema continua a responder apesar dos desafios' (Parlamento.mz, O País); 'Ussene Isse exige maior rigor na gestão de medicamentos em Moçambique' (MMO); 'MINISTRO DA SAÚDE USSENE ISSE INSURGE-SE CONTRA CORRUPÇÃO NA CADEIA DE MEDICAMENTOS' (CMAM)."
              - "Governo de Moçambique institui 'mês da planificação' para maior eficiência e transparência no sector da saúde (AIM News, outubro 2025) — reforma de planeamento institucional."
              - "Owns MISAU policy, CMAM medicines-supply-chain reform, INS public-health institute, Hospital Central de Maputo and Hospital Central de Beira, 10 DPS coordination, Cabo Delgado / northern-provinces health response, post-Idai / post-Daniel cyclone reconstruction, and Mozambique's WHO Africa, SADC and CPLP positioning."
              - "Hook: medicines anti-corruption (a defining mandate line), Cabo Delgado health response, mpox preparedness, HIV / TB / malaria post-PEPFAR-changes continuity (Mozambique has the highest HIV adult prevalence in SADC), cyclone-recovery health-infrastructure, CPLP cooperation."
          - Tone advice:
              - "Open with medicines anti-corruption, Cabo Delgado response, HIV continuity and CPLP cooperation — these are his sustained 2026 lines."
              - "Do not assume nationwide uniformity — Cabo Delgado, Nampula, Niassa require specific insurgency-context framings."
```

## 11. Out-of-band notes

For roles unfilled or in transition.

## 12. Open questions

- Named Vice-Ministros and Secretário Permanente under Isse with currency verified.
- DG INS, DG CMAM with currency verified.
- Directors of Hospital Central de Maputo, Hospital Central de Beira, Hospital Provincial de Nampula.
- Directors of the 10 Direcções Provinciais de Saúde — priority Cabo Delgado, Maputo, Nampula.
- Assembleia da República Comissão de Política Social Chair with currency verified.
- Bastonário Ordem dos Médicos with currency verified.
