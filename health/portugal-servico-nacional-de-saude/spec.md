# spec.md — `leaders.yml`

Single source of truth for the structure, semantics, and update rules of `leaders.yml` for the Portuguese Serviço Nacional de Saúde (SNS). Treat this document as the canonical specification: the YAML must conform to it; if the YAML and this spec disagree, the spec wins and the YAML is fixed.

## 1. Purpose

`leaders.yml` is an engagement register of named individuals in and around the Portuguese SNS. Each entry exists so that a reader (typically inside the Ministério da Saúde, the Direção Executiva do SNS, an arm's-length agency, a Unidade Local de Saúde (ULS), a hospital, or an adjacent national body) can decide:

1. **Who to engage** for a given digital/transformation/policy topic.
2. **How to engage them** — the angle that lands and the angle that fails.
3. **Where to engage them** — which public channels they actually use.

It is not a phone book, not a CRM, and not a comms list. Entries that do not directly serve engagement decision-making are out of scope.

The Portuguese SNS is a tax-funded, universal Beveridgean system established in 1979 (Lei n.º 56/79). Since 2022 it is steered operationally by the Direção Executiva do SNS, a quasi-CEO function created to centralise SNS management; the Ministério da Saúde retains policy and budget. The 2024 reform replaced the previous combination of hospital centres, ACES and ARS with vertically integrated Unidades Locais de Saúde (ULS) covering each region's primary care plus hospital care. INFARMED regulates medicines and medical devices. Direção-Geral da Saúde (DGS) holds the chief medical-officer function and runs public-health programmes; the Instituto Nacional de Saúde Doutor Ricardo Jorge (INSA) is the national public-health research institute. ACSS (Administração Central do Sistema de Saúde) handles financial and human-resources system administration. The Entidade Reguladora da Saúde (ERS) is the cross-sector regulator (public, social, private).

## 2. Scope

**In scope:**
- Governo: Primeiro-Ministro; Ministro/a da Saúde; Secretário/a de Estado da Saúde and Secretário/a de Estado Adjunto/a e da Saúde where filled.
- Ministério da Saúde: Chefe de Gabinete da Ministra; Inspecção-Geral das Atividades em Saúde (IGAS); Secretaria-Geral do Ministério da Saúde.
- Direção Executiva do SNS (DE-SNS): Diretor/a Executivo/a, Conselho de Gestão.
- Direção-Geral da Saúde (DGS): Diretor/a-Geral da Saúde (the function combines national chief medical officer and head of the public-health authority).
- Other central state bodies: INFARMED (Presidente do Conselho Diretivo, Vice-Presidente, Vogal); Administração Central do Sistema de Saúde (ACSS, Presidente do Conselho Diretivo); SPMS — Serviços Partilhados do Ministério da Saúde (Presidente do Conselho de Administração); INSA — Instituto Nacional de Saúde Doutor Ricardo Jorge (Presidente do Conselho Diretivo); Instituto Português do Sangue e da Transplantação (IPST, Presidente); Entidade Reguladora da Saúde (ERS, Presidente).
- Unidades Locais de Saúde (ULS): Presidente do Conselho de Administração and Director Clínico of the largest ULS (ULS São José Lisboa, ULS Santa Maria Lisboa, ULS São João Porto, ULS Santo António Porto, ULS Coimbra, ULS Algarve, ULS Lisboa Ocidental).
- Regional autonomous health systems: Secretário Regional da Saúde of the Açores and Madeira regional governments.
- Assembleia da República: Comissão Parlamentar de Saúde Presidente and Vice-Presidente; party spokespeople (porta-vozes da Saúde).
- Statutory and oversight bodies: Tribunal de Contas where directly relevant; Provedor de Justiça where directly relevant; Comissão Nacional de Proteção de Dados (CNPD) on health-data matters; Conselho Nacional de Ética para as Ciências da Vida (CNECV).
- Related sector bodies of national significance: Ordem dos Médicos (Bastonário); Ordem dos Enfermeiros (Bastonária); Ordem dos Farmacêuticos (Bastonário); Ordem dos Médicos Dentistas; Conselho Nacional dos Médicos Internos; APAH (Associação Portuguesa de Administradores Hospitalares); Federação Nacional dos Médicos (Fnam) and Sindicato Independente dos Médicos (SIM); SEP (Sindicato dos Enfermeiros Portugueses); Confederação Nacional das Instituições de Solidariedade (CNIS) where the brief touches contracted social-care.
- For each organisation: only stakeholders senior enough that engagement with them shapes decisions across the organisation.

**Out of scope:**
- Operational staff below diretor/a-geral / vogal level inside agencies, and below conselho de administração inside hospitals and ULS.
- Suppliers, vendors, consultancies.
- Historical post-holders.
- Other Iberian counterparts unless they hold a Portugal-facing role.

## 3. Structure

The YAML is a single top-level mapping with one key.

```
SNS Portugal stakeholders:
  - {Organisation}:
      - {Person}:
          - Title: ...
          - {optional contact fields}
          - Stakeholder engagement notes: [...]
          - Tone advice: [...]
```

### Indentation rules

Standard 2/6/10/14 spaces; no tabs; one newline between sibling entries.

### Ordering

Organisations grouped by tier: Governo → Ministério da Saúde → Direção Executiva do SNS → central state bodies (DGS, INFARMED, ACSS, SPMS, INSA, IPST, ERS) → ULS (largest first, then alphabetical) → Açores and Madeira regional secretariats → Assembleia da República Comissão Parlamentar de Saúde → Ordens profissionais (Médicos, Enfermeiros, Farmacêuticos, Médicos Dentistas) → unions (Fnam, SIM, SEP) → APAH and Conselhos consultivos → oversight bodies.

Within an organisation: Ministro/a / Presidente / Diretor/a → Secretário/a de Estado / Vice-Presidente → Diretor/a Clínico/a → Diretor/a de Enfermagem → other directors → digital director → financial director.

## 4. Field definitions

### 4.1 Organisation name

Use the official Portuguese name with English in parentheses where the body is widely known by both (e.g. `Direção Executiva do Serviço Nacional de Saúde (DE-SNS)`, `INFARMED (Autoridade Nacional do Medicamento e Produtos de Saúde)`).

### 4.2 Person name

Academic titles `Dr.`, `Dra.`, `Prof.`, `Prof. Doutor/a`. Party affiliation in parentheses using canonical Portuguese abbreviations: `PSD` Partido Social Democrata, `PS` Partido Socialista, `Chega`, `IL` Iniciativa Liberal, `PCP` Partido Comunista Português, `BE` Bloco de Esquerda, `Livre`, `PAN` Pessoas-Animais-Natureza, `CDS-PP`. The Aliança Democrática (AD) brand is used for the PSD/CDS-PP coalition that has governed since March 2024.

### 4.3 `Title:` (required, one)

Portuguese title with English gloss where not self-evident. Status flags:
- `em exercício` or `interina/o` if not substantive.
- `(desde {data})` if newly in post.
- `(verificar atualidade)` if there is a known reason to re-check.

### 4.4 Contact fields (optional, zero or more)

`LinkedIn:`, `X:`, `Bluesky:`, `Mastodon:`, `Website:`, `GitHub:`, `Email:` — each at most once, only with public attribution.

### 4.5 `Stakeholder engagement notes:` (3-7 bullets)

Career background, ownership, public statements, hook. Anti-pattern: generic CV.

### 4.6 `Tone advice:` (exactly 2 bullets)

What to lead with; what to avoid. Portuguese reform frames such as Reforma do SNS, ULS-isação, Plano de Recuperação e Resiliência (PRR) Saúde, Estatuto do SNS (2022), médico de família para todos, plano nacional de saúde mental should be used where they fit.

### 4.7 Other fields

None.

## 5. Provenance and dating

- Anchor facts to year, month or exact date.
- The XXV Governo Constitucional was empossado in June 2025 following the snap election of 18 May 2025, with Luís Montenegro (PSD) reconducido as Primeiro-Ministro and Ana Paula Martins (PSD/AD) continuing as Ministra da Saúde. Treat the Ministério da Saúde tier as stable since 5 June 2025; treat agency leadership renewals (INFARMED, ACSS, SPMS) as on the same political cycle.

## 6. Update workflow

1. Identify the change.
2. Verify against portugal.gov.pt, sns.gov.pt, dgs.pt, infarmed.pt, acss.min-saude.pt, spms.min-saude.pt, insa.min-saude.pt, ers.pt, the Diário da República, Lusa, Público, Expresso, Jornal de Notícias, Diário de Notícias, Observador, Healthnews, Saúde Online, Just News.
3. Apply minimum diff; re-check Tone advice.
4. Confirm structure.
5. Re-validate cross-references.

## 7. Invariants

Standard register invariants apply.

## 8. Anti-patterns

- Padding; speculation; vendor-flattering language; stale role titles; duplicate entries; mixing facts and aspirations.
- Treating the DE-SNS as a Ministry sub-unit — it is a statutory operational steering body with Conselho de Gestão authority over the ULS network; routing engagement only through the Ministério leaves the operational layer untouched.
- Importing NHS or HSE framings unmodified — Portugal has a Beveridgean SNS like the UK but a strongly vertically integrated ULS model since 2024 that does not match either NHS England ICBs or the Irish HSE.

## 9. Acronym and term glossary (selective)

- **ACES** — Agrupamentos de Centros de Saúde (the previous primary-care groupings, largely absorbed into ULS in 2024).
- **ACSS** — Administração Central do Sistema de Saúde.
- **ARS** — Administrações Regionais de Saúde (regional health administrations; functions largely absorbed into ULS and DE-SNS since 2024).
- **CNECV** — Conselho Nacional de Ética para as Ciências da Vida.
- **CNPD** — Comissão Nacional de Proteção de Dados.
- **DE-SNS** — Direção Executiva do Serviço Nacional de Saúde.
- **DGS** — Direção-Geral da Saúde.
- **ERS** — Entidade Reguladora da Saúde.
- **Estatuto do SNS** — the 2022 SNS Statute (Decreto-Lei n.º 52/2022) that created the DE-SNS.
- **Fnam** — Federação Nacional dos Médicos.
- **IGAS** — Inspeção-Geral das Atividades em Saúde.
- **INEM** — Instituto Nacional de Emergência Médica.
- **INFARMED** — Autoridade Nacional do Medicamento e Produtos de Saúde, I.P.
- **INSA** — Instituto Nacional de Saúde Doutor Ricardo Jorge.
- **IPST** — Instituto Português do Sangue e da Transplantação.
- **Médico de Família para Todos** — flagship policy commitment to assign every resident a family doctor.
- **OPSS** — Observatório Português dos Sistemas de Saúde.
- **PRR** — Plano de Recuperação e Resiliência (Portuguese Recovery and Resilience Plan; substantial health-investment envelope).
- **SAM** — Sistema de Apoio ao Médico.
- **SEP** — Sindicato dos Enfermeiros Portugueses.
- **SIM** — Sindicato Independente dos Médicos.
- **SNS24** — the national health digital and call-centre service.
- **SPMS** — Serviços Partilhados do Ministério da Saúde (the digital and shared-services agency).
- **ULS** — Unidade Local de Saúde (vertically integrated regional health unit covering primary care plus hospital care, created sectorally from 2024).
- **XXIV / XXV Governo Constitucional** — the Montenegro I (2024-2025) and Montenegro II (from June 2025) governments.

## 10. Worked example

```yaml
      - Ana Paula Martins (PSD / AD):
          - Title: Ministra da Saúde (Minister of Health) (desde 2 de abril de 2024; reconduzida em 5 de junho de 2025)
          - Stakeholder engagement notes:
              - "Ministra da Saúde no XXIV Governo Constitucional desde a posse de 2 de abril de 2024 (governo Montenegro I); reconduzida no XXV Governo Constitucional empossado em 5 de junho de 2025 após a eleição antecipada de 18 de maio de 2025."
              - "Farmacêutica de formação; antiga Bastonária da Ordem dos Farmacêuticos; perfil técnico-profissional num pasta tradicionalmente médica — assinatura institucional é regulação profissional, farmácia e gestão hospitalar."
              - "Herda a reforma das Unidades Locais de Saúde (ULS) iniciada em 2024 e o Estatuto do SNS de 2022 que criou a Direção Executiva do SNS; deve articular com o Director Executivo Álvaro Almeida o equilíbrio política–operação."
              - "Desafios mandatários públicos: falta de médicos de família, listas de espera cirúrgicas, urgências e maternidades sob pressão, e execução do PRR Saúde — o orçamento da Saúde é politicamente exposto à fronteira esquerda (PS, BE, PCP, Livre) na Assembleia da República."
              - "Hook: ULS-isação, médico de família para todos, urgências, PRR Saúde, política do medicamento, e profissões da saúde aterrissam; pitches centrados em hospitais privados sem integração no SNS não aterrissam."
          - Tone advice:
              - "Liderar com ULS-isação, médico de família para todos, PRR Saúde e profissões da saúde — são as linhas mandatárias do governo Montenegro II e o seu background farmacêutico."
              - "Não enquadrar como ministra clínica — Martins é farmacêutica de formação e antiga Bastonária; framings clínico-hospitalares puros serão reformulados em chave reguladora e profissional."
```

## 11. Out-of-band notes

Used where a role is unfilled or in interim. Do not need Tone advice.

## 12. Open questions

- Named Secretário/a de Estado da Saúde and Secretário/a de Estado Adjunto/a e da Saúde under the XXV Governo Constitucional with currency verified to within six months.
- Named Diretor/a-Geral da Saúde currently in post (post-Graça Freitas; Rita Sá Machado was named afterwards; currency to verify in the XXV Governo Constitucional).
- Named Presidente do Conselho Diretivo of ACSS, SPMS, INSA, IPST and ERS with currency verified.
- Named Presidente do Conselho de Administração and Diretor Clínico of the seven largest ULS (ULS São José, ULS Santa Maria, ULS São João, ULS Santo António, ULS Coimbra, ULS Algarve, ULS Lisboa Ocidental).
- Named Secretário Regional da Saúde of the Açores and Madeira regional governments under the current legislaturas.
- Named Presidente of the Comissão Parlamentar de Saúde of the Assembleia da República in the current legislatura, plus party porta-vozes.
- Named Bastonário/a of the Ordem dos Médicos, Ordem dos Enfermeiros, Ordem dos Farmacêuticos and Ordem dos Médicos Dentistas with currency verified.
- Named leadership of Fnam, SIM and SEP through the current convenção colectiva cycles.
