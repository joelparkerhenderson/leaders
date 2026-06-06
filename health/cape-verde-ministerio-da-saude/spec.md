# spec.md — `leaders.yml`

Fonte única de verdade para o registo do sistema de saúde cabo-verdiano. O YAML deve estar em conformidade com esta especificação.

## 1. Purpose

Registo de envolvimento das pessoas nomeadas no Ministério da Saúde de Cabo Verde e organismos adjacentes.

Cabo Verde é um arquipélago atlântico, membro da CEDEAO e da CPLP, com um sistema de saúde público predominante organizado por ilhas, e um forte engajamento com a OMS AFRO, PALOP-TL e parceiros lusófonos.

## 2. Scope

In scope: Primeiro-Ministro; Ministro da Saúde; Diretor Nacional de Saúde; Diretor ARFA (regulador de medicamentos); Comissão de Saúde da Assembleia Nacional.

Out of scope: delegados de saúde concelhios; diretores hospitalares.

## 3. Structure

Standard 2/6/10/14 indentation. Top-level key: `Partes interessadas do sistema de saúde cabo-verdiano:`. Ordem: Governo → Ministério → Direção Nacional → ARFA → Assembleia.

## 4. Field definitions

Filiação partidária: `MpD` (Movimento para a Democracia, no poder sob José Maria Neves PR e Ulisses Correia e Silva PM transitando 2026), `PAICV` (Partido Africano da Independência de Cabo Verde, oposição principal), `UCID` (União Caboverdiana Independente e Democrática). Títulos em português.

## 5. Provenance and dating

Anchor to year, month or date. O Ministro da Saúde do governo MpD de Ulisses Correia e Silva deve ser verificado contra a Presidência do Governo e a comunicação social cabo-verdiana.

## 6. Update workflow

Verify against minsaude.gov.cv, governo.cv, parlamento.cv, A Nação, Expresso das Ilhas, Inforpress.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Tratar Cabo Verde como Estado continental — é um arquipélago de dez ilhas com logística inter-ilhas particular; framings continentais serão filtrados.
- Ignorar a comunidade PALOP-TL — Cabo Verde participa ativamente na CPLP e em mecanismos PALOP, com cooperação técnica recíproca; framings que ignoram a lusofonia desperdiçam alavancagem.

## 9. Acronym glossary

- **ARFA** — Agência de Regulação e Supervisão dos Produtos Farmacêuticos e Alimentares.
- **CPLP** — Comunidade dos Países de Língua Portuguesa.
- **MpD** — Movimento para a Democracia.
- **PAICV** — Partido Africano da Independência de Cabo Verde.
- **PALOP-TL** — Países Africanos de Língua Oficial Portuguesa e Timor-Leste.

## 10. Worked example

```yaml
      - Dr [Nome a verificar] (MpD):
          - Title: Ministro da Saúde (Minister of Health)
          - Stakeholder engagement notes:
              - "Ministro da Saúde no governo MpD; verificar titularidade contra governo.cv e Inforpress."
              - "Owns a política e o orçamento do MS, o Hospital Dr. Agostinho Neto (Praia) e o Hospital Baptista de Sousa (Mindelo), a rede hospitalar regional e centros de saúde por ilha, a ARFA, a coordenação inter-ilhas, e a diplomacia OMS AFRO, CEDEAO, CPLP e PALOP-TL."
              - "Hook: cobertura universal, doenças não transmissíveis, saúde mental, dengue e arboviroses, saúde materno-infantil, e cooperação CPLP aterram."
          - Tone advice:
              - "Abrir com cobertura universal, NCDs, saúde mental, dengue e cooperação CPLP."
              - "Não importar framings continentais nem ignorar a lusofonia."
```

## 11. Out-of-band notes

Para cargos vagos ou interinos.

## 12. Open questions

- Identidade do Ministro da Saúde em titularidade verificada.
- Diretor Nacional de Saúde e Diretor ARFA.
- Presidente da Comissão de Saúde da Assembleia Nacional.
