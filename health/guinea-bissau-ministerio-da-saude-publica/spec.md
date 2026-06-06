# spec.md — `leaders.yml`

Fonte única de verdade para o registo do sistema de saúde da Guiné-Bissau. O YAML deve estar em conformidade com esta especificação.

## 1. Purpose

Registo de envolvimento das pessoas nomeadas no Ministério da Saúde Pública da República da Guiné-Bissau e organismos adjacentes.

A Guiné-Bissau é um pequeno Estado da África Ocidental, membro da CEDEAO, da UEMOA, da CPLP e dos PALOP, com uma política instável caracterizada por sucessivas crises e mudanças de governo sob o Presidente Umaro Sissoco Embaló (Madem G15).

## 2. Scope

In scope: Presidente; Primeiro-Ministro; Ministro da Saúde Pública; Secretário-Geral; Diretor Hospital Nacional Simão Mendes; Diretor INASA (Instituto Nacional de Saúde Pública); Comissão de Saúde da Assembleia Nacional Popular.

Out of scope: diretores regionais; chefes de serviço.

## 3. Structure

Standard 2/6/10/14 indentation. Top-level key: `Partes interessadas do sistema de saúde guineense:`. Ordem: Presidência → Governo → MSP → INASA → ANP.

## 4. Field definitions

Filiação partidária: `Madem G15` (Movimento para a Alternância Democrática G15, no poder com Embaló), `PAIGC` (Partido Africano da Independência da Guiné e Cabo Verde), `PRS` (Partido da Renovação Social). Títulos em português.

## 5. Provenance and dating

Anchor to year, month or date. O Ministro da Saúde sob o governo de transição/Embaló deve ser verificado contra a Presidência e a Agência de Notícias da Guiné (ANG); a rotação ministerial é elevada.

## 6. Update workflow

Verify against presidenciarepublica.gw, anpaisesemconstrucao.org, ANG (Agência de Notícias da Guiné), O Democrata.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Assumir estabilidade política prolongada — a Guiné-Bissau tem ciclo político notavelmente instável e rotação ministerial elevada; framings que assumem continuidade institucional falham.
- Confundir com a República da Guiné (Conakry) — Estados distintos com história colonial, língua oficial (português vs. francês) e arquitetura institucional próprios.

## 9. Acronym glossary

- **ANG** — Agência de Notícias da Guiné.
- **CPLP** — Comunidade dos Países de Língua Portuguesa.
- **INASA** — Instituto Nacional de Saúde Pública.
- **MSP** — Ministério da Saúde Pública.
- **PAIGC** — Partido Africano da Independência da Guiné e Cabo Verde.

## 10. Worked example

```yaml
      - Dr [Nome a verificar]:
          - Title: Ministro da Saúde Pública (Minister of Public Health)
          - Stakeholder engagement notes:
              - "Ministro da Saúde Pública num gabinete com rotação elevada sob a presidência de Embaló; verificar titularidade contra ANG e O Democrata."
              - "Owns a política e o orçamento do MSP, o Hospital Nacional Simão Mendes (Bissau), o Hospital Raoul Follereau, a rede regional de hospitais e centros de saúde, INASA, e a diplomacia OMS AFRO, CEDEAO, UEMOA, CPLP e PALOP."
              - "Hook: paludismo, saúde materno-infantil, NCDs, surto de cólera periódico, cooperação CPLP-PALOP e apoio dos parceiros (OMS, UNICEF, Banco Mundial, Fundo Global, Gavi) aterram."
          - Tone advice:
              - "Abrir com paludismo, saúde materno-infantil, NCDs, surto e cooperação CPLP."
              - "Não confundir com Guiné-Conakry nem assumir estabilidade prolongada."
```

## 11. Out-of-band notes

Para cargos vagos ou interinos.

## 12. Open questions

- Identidade do Ministro da Saúde Pública em titularidade verificada.
- Diretor Hospital Nacional Simão Mendes e Diretor INASA.
- Presidente Comissão de Saúde Assembleia Nacional Popular.
