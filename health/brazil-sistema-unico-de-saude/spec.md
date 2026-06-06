# spec.md — `leaders.yml`

Single source of truth for the structure, semantics, and update rules of `leaders.yml` for the Brazilian Sistema Único de Saúde (SUS). The YAML must conform to this spec; if they disagree, the spec wins and the YAML is fixed.

## 1. Purpose

`leaders.yml` is an engagement register of named individuals in and around the Brazilian SUS. The SUS, created by the 1988 Constitution and Lei 8.080/1990, is one of the largest public health systems in the world: universal, tax-financed, free at point of use. Operationally it is tripartite: União (federal Ministério da Saúde), 26 states + DF (Secretarias Estaduais de Saúde), and 5,570 municipalities (Secretarias Municipais de Saúde). Complementary private supplementary insurance covers ~25% of the population.

## 2. Scope

**In scope:** Presidente; Ministro/a da Saúde; Secretários-Executivos and Secretários of Atenção Especializada, Atenção Primária, Vigilância em Saúde, Ciência e Tecnologia, Saúde Indígena; Diretor-Presidente ANVISA (medicines); Diretor-Presidente ANS (supplementary insurance); Presidente Fiocruz; Presidente Instituto Butantan; Presidente CONASS (state secretaries); Presidente CONASEMS (municipal secretaries); Diretor INCA; Presidentes Comissões de Seguridade Social Câmara e Senado; Presidente CFM (Conselho Federal de Medicina); Presidente Cofen (enfermagem); Presidente CFF (farmacêuticos); Presidente AMB (Associação Médica Brasileira).

## 3. Structure

```
Sistema Único de Saúde brasileiro — partes interessadas:
  - {Organisation}:
      - {Person}:
          - Title: ...
          - Stakeholder engagement notes: [...]
          - Tone advice: [...]
```

Standard indentation. Ordering: Presidência → Ministério da Saúde → ANVISA → ANS → Fiocruz → Butantan → INCA → CONASS → CONASEMS → Câmara/Senado → conselhos profissionais.

## 4. Field definitions

Standard family conventions. Party affiliation using canonical Brazilian abbreviations: `PT`, `PL`, `PP`, `União Brasil`, `MDB`, `PSDB`, `PDT`, `PSB`, `PCdoB`, `Republicanos`, `Cidadania`, `PSD`, `Podemos`, `Novo`, `PSOL`, `Rede`, `Avante`, `Solidariedade`. Titles in Portuguese with English glosses.

## 5. Provenance and dating

Anchor facts to year, month or exact date. The Lula III government (PT-led coalition) was sworn in 1 January 2023. Alexandre Padilha (PT) replaced Nísia Trindade as Ministro da Saúde during the mandate; he is the current Minister in 2026 and previously held the post under Dilma Rousseff (2011-2014).

## 6. Update workflow

Verify against gov.br/saude, planalto.gov.br, anvisa.gov.br, ans.gov.br, fiocruz.br, butantan.gov.br, camara.leg.br, senado.leg.br, Folha de S.Paulo, O Globo, Estadão, Valor Econômico, UOL, G1.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating the SUS as federally managed — municipalities own delivery; the federal level co-finances and sets norms via Pactos Tripartite.
- Importing NHS framings unmodified — SUS is tax-financed Beveridgean but tripartite with constitutional fiscal-responsibility constraints.

## 9. Acronym glossary

- **ANS** — Agência Nacional de Saúde Suplementar.
- **ANVISA** — Agência Nacional de Vigilância Sanitária.
- **CFF / CFM / Cofen / AMB** — Conselho Federal de Farmácia / Medicina / Enfermagem; Associação Médica Brasileira.
- **CONASS** — Conselho Nacional de Secretários de Saúde.
- **CONASEMS** — Conselho Nacional de Secretarias Municipais de Saúde.
- **Fiocruz** — Fundação Oswaldo Cruz.
- **INCA** — Instituto Nacional de Câncer.
- **SAMU** — Serviço de Atendimento Móvel de Urgência.
- **SUS** — Sistema Único de Saúde.

## 10. Worked example

```yaml
      - Alexandre Padilha (PT):
          - Title: Ministro da Saúde (Minister of Health) (no governo Lula III)
          - Stakeholder engagement notes:
              - "Ministro da Saúde no governo Lula III (PT, coalizão); substituiu Nísia Trindade durante o mandato; PT; já havia sido Ministro da Saúde no governo Dilma Rousseff 2011-2014 — único brasileiro a ocupar a pasta em dois mandatos não consecutivos."
              - "Médico sanitarista, com formação em Saúde Coletiva; perfil PT-sanitarista, em linha com o consenso técnico-político do SUS."
              - "Owns o orçamento federal do SUS, a Política Nacional de Atenção Básica (PNAB), Mais Médicos e Mais Especialistas, Farmácia Popular, vigilância em saúde via Fiocruz e ANVISA, e a articulação tripartite com CONASS e CONASEMS."
              - "Posicionado publicamente na OMS (maio 2026) defendendo resposta global à crise climática e redução das desigualdades em saúde — projeção internacional brasileira no SUS."
              - "Hook: PNAB e Mais Médicos, Farmácia Popular, Fiocruz como ciência-e-tecnologia em saúde, ANVISA reform, mudanças climáticas e saúde indígena aterrissem; pitches que ignoram a estrutura tripartite SUS não aterrissem."
          - Tone advice:
              - "Abrir com PNAB, Mais Médicos, Farmácia Popular, Fiocruz e saúde climática — são suas linhas autorais e o frame PT-sanitarista do SUS."
              - "Não pitchear como se o Ministério decidisse a operação local — municípios são gestores plenos via Pactos Tripartite; centralização federal será recusada."
```

## 11. Out-of-band notes

For roles unfilled or interim.

## 12. Open questions

- Named Secretários-Executivos and Secretários de Atenção Especializada, Atenção Primária, Vigilância em Saúde, Ciência e Tecnologia, Saúde Indígena com vigência verificada.
- Diretor-Presidente ANVISA, ANS, Presidente Fiocruz, Butantan, INCA.
- Presidente CONASS e CONASEMS no ciclo atual.
- Presidentes Comissões de Seguridade Social Câmara e Senado.
- Presidente CFM, Cofen, CFF, AMB.
