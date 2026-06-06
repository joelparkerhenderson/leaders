# spec.md — `leaders.yml`

Fonte única de verdade para o registo do sistema de saúde timorense. O YAML deve estar em conformidade com esta especificação.

## 1. Purpose

Registo de envolvimento das pessoas nomeadas no Ministério da Saúde de Timor-Leste (República Democrática de Timor-Leste, RDTL) e organismos adjacentes.

Timor-Leste é uma República semipresidencialista lusófona pós-2002 com sistema de saúde público dominante centrado no Hospital Nacional Guido Valadares (HNGV) em Díli e centros de saúde comunitários. Membro da CPLP, ASEAN observador-em-via-de-adesão (admissão prevista 2025-2026), PALOP-TL.

## 2. Scope

In scope: Presidente; Primeiro-Ministro; Ministro da Saúde; Diretor-Geral HNGV; Comissão de Saúde do Parlamento Nacional.

Out of scope: diretores municipais; chefes de serviço.

## 3. Structure

Standard 2/6/10/14 indentation. Top-level key: `Partes interessadas do sistema de saúde timorense:`. Ordem: Presidência → Governo → Ministério → HNGV → Parlamento Nacional.

## 4. Field definitions

Filiação partidária: `CNRT` (Congresso Nacional da Reconstrução Timorense, no poder com Xanana Gusmão PM), `Fretilin` (Frente Revolucionária do Timor-Leste Independente, oposição principal), `PD` (Partido Democrático), `KHUNTO`. Títulos em português.

## 5. Provenance and dating

Anchor to year, month or date. O Ministro da Saúde no governo CNRT-PD-KHUNTO de Xanana Gusmão (desde julho 2023) é a verificar contra a Presidência do Governo e a Tatoli (Agência Noticiosa de Timor-Leste).

## 6. Update workflow

Verify against moh.gov.tl, timor-leste.gov.tl, parlamento.tl, Tatoli (ANTL), Jornal Independente, RTTL (Rádio e Televisão de Timor-Leste).

## 7. Invariants

Standard.

## 8. Anti-patterns

- Confundir com Timor Oeste (parte da Indonésia) — Timor-Leste é Estado soberano lusófono distinto.
- Ignorar a inserção CPLP-PALOP — a cooperação portuguesa, brasileira, cabo-verdiana e angolana é uma alavanca técnica significativa em formação de recursos humanos de saúde.
- Ignorar a próxima adesão à ASEAN — a adesão completa muda o quadro de cooperação regional.

## 9. Acronym glossary

- **CNRT** — Congresso Nacional da Reconstrução Timorense.
- **CPLP** — Comunidade dos Países de Língua Portuguesa.
- **Fretilin** — Frente Revolucionária do Timor-Leste Independente.
- **HNGV** — Hospital Nacional Guido Valadares.
- **PALOP-TL** — Países Africanos de Língua Oficial Portuguesa e Timor-Leste.

## 10. Worked example

```yaml
      - Dr [Nome a verificar] (CNRT-PD-KHUNTO):
          - Title: Ministro da Saúde (Minister of Health)
          - Stakeholder engagement notes:
              - "Ministro da Saúde no governo CNRT-PD-KHUNTO de Xanana Gusmão (PM desde julho 2023); verificar titularidade contra timor-leste.gov.tl e Tatoli."
              - "Owns a política e o orçamento do MS, o HNGV em Díli, hospitais municipais (Baucau, Maliana, Suai, Oecusse), rede de centros de saúde comunitários, e diplomacia OMS WPRO, ASEAN (próxima adesão), CPLP, PALOP-TL e G7+ (estados frágeis)."
              - "Hook: TB (Timor tem alta carga), malária (progressos para eliminação), MCH (mortalidade infantil em queda mas elevada), nutrição (stunting prevalente), NCDs emergentes, cobertura CSU e cooperação CPLP-ASEAN aterram."
          - Tone advice:
              - "Abrir com TB, malária, MCH, nutrição, NCDs, CSU e cooperação CPLP-ASEAN."
              - "Não confundir com Timor Oeste indonésio nem ignorar a próxima adesão ASEAN."
```

## 11. Out-of-band notes

Para cargos vagos ou interinos.

## 12. Open questions

- Identidade do Ministro da Saúde em titularidade verificada.
- Diretor-Geral HNGV.
- Presidente Comissão de Saúde Parlamento Nacional.
