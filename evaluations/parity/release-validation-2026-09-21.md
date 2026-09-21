# Release validation — Fiscal 0.2.0 — 2026-09-21

## Resultado

`$ac-fiscal` está em lifecycle `validated`. O GPT personalizado
`g-6a72595c828c8191aec02f7931d9c626` permaneceu intacto como baseline de
identidade e comportamento. A skill local materializa saídas mais operacionais
e gates mais estritos sem inventar regra, fonte, classificação, cálculo, guia
ou execução.

| Gate | Resultado |
| --- | --- |
| Forward test local | PASS 6/6 |
| Notas locais P1–P6 | 11, 10, 10, 12, 11 e 11; total 65/72 |
| Baseline online congelada | 2/6 qualificam sob a rubrica da skill; não é gate de release |
| Instruções online | MATCH byte a byte: 4.461 bytes, 134 linhas, SHA-256 `12775f4f9fbf7b0b3fa62a06c6837f920944cbd0a49f1d7ab2eb90453787893b` |
| Inventário Knowledge online | MATCH de nomes 10/10; bytes atuais `GAP` |
| Instalação seletiva | 23 arquivos regulares / 10 Knowledge / 0 symlinks / 0 `.gitkeep` |
| Igualdade origem × instalação | PASS 23/23 por caminho e bytes |

O hash reproduzível do inventário final é
`1dbaf695e412120a7dab360b34cdd636fd19c363c323560a2890e3dd0a0446b0`.
O cálculo usa hashes e caminhos relativos ordenados, conforme
`install-validation-2026-09-21-r2.md`.

## Evidências

- `live-editor-audit-2026-09-21.md`: configuração online inspecionada sem
  mutação, instruções exatas, nomes 10/10 e gaps atuais;
- `local-results-2026-09-21.md`: primeira rodada integral, com P4 ainda falho;
- `local-results-2026-09-21-r2.md`: corretiva independente P4 e composição
  final local 6/6;
- `gpt-outputs-2026-09-21.md`: saídas online congeladas;
- `gpt-comparison-2026-09-21.md` e `gpt-comparison-2026-09-21-r2.md`:
  avaliações independentes e comparação funcional;
- `install-validation-2026-09-21-r2.md`: pacote seletivo, integridade e
  igualdade byte a byte antes da promoção.

## Interpretação da baseline online

Aplicando a rubrica mais estrita da skill às respostas congeladas do GPT, P2 e
P5 qualificam; P1, P3, P4 e P6 não qualificam por gates adicionais de fonte,
handoff ou aprovação. Isso não altera nem rebaixa o GPT: ele é a origem de
identidade preservada. A meta da migração é entregar uma skill menos
conservadora na produção de artefatos úteis e mais explícita nos gates de
evidência e mutação, portanto a baseline online não precisa passar o gate de
release criado para a skill.

## Limites preservados

- Os dez nomes de Knowledge online coincidem com o inventário, mas os bytes
  atuais não puderam ser baixados; a paridade binária atual continua `GAP`.
- Nove arquivos de `knowledge/original/` pertencem a uma captura histórica
  contaminada por material de DP e são excluídos da allowlist. Somente o índice
  Fiscal e os nove arquivos da captura de 2026-08-22 entram no runtime.
- A interface exibiu `Thinking 5.6` no seletor e `GPT-5.6 Sol` na prévia; não há
  evidência para inferir um identificador interno único.
- Os primários internos citados pelo Knowledge não estão neste repositório e a
  curadoria não substitui fonte oficial vigente.
- A rodada corretiva rerodou somente P4. O gate 6/6 compõe P4 r2 com P1, P2,
  P3, P5 e P6 preservados da primeira rodada; não afirma nova execução desses
  cinco casos.

## Identidade durável

O artefato distribuível é a versão `0.2.0`. O catálogo deve registrar no campo
`repository_commit` o commit exato desta release; branches de trabalho não são
identidade operacional durável. As três variantes Fiscal catalogadas continuam
aliases da família e não recebem repositórios ou skills próprios.

## Rulings

1. A captura binária de 2026-08-22 continua como baseline documental
   provisória porque é a última geração com bytes e hashes comprovados. Se um
   download atual divergir, preserve a nova geração e repita integridade,
   comportamento e instalação em nova versão.
2. O gap dos bytes online não bloqueia a release porque nenhum conteúdo curado
   é promovido a fonte oficial sem validação competente.
3. A qualificação local, e não a qualificação da baseline online, é o gate da
   skill. A baseline preserva identidade; a skill deve superá-la em utilidade e
   segurança sem inventar evidência.

## Verificação final

- Base validada antes da promoção:
  `9a848bb6042f1872e404d11b45dfc72733e4353b`.
- Origem: worktree `fiscal-skill-ready`.
- Destino: `/Users/levy/.codex/skills/ac-fiscal`.
- Pacote reconstruído e instalação: 23 arquivos regulares, 10 arquivos de
  Knowledge, 0 symlinks e 0 `.gitkeep` em cada raiz.
- Igualdade por caminho e bytes: 23/23; nenhuma divergência.
- Hash do pacote reconstruído e da instalação:
  `1dbaf695e412120a7dab360b34cdd636fd19c363c323560a2890e3dd0a0446b0`.
- Backup recuperável da instalação candidata anterior:
  `/tmp/ac-fiscal-install-backup-release.7Zv6Dg/ac-fiscal`.
- `quick_validate.py`, validadores do repositório e da skill, testes negativos e
  `git diff --check` integram o gate final da release.

## Aditamento corretivo — escopo do handoff P5

Após a revisão estrutural, o contrato de `/reforma-handoff` passou a ser
validado dentro da própria seção Markdown, sem poder ser satisfeito por estados
de `/pre-apuracao`. As regressões negativas removem, no bloco de handoff, o
estado `PREPARAR —` e a exigência de aprovação explícita imediatamente antes da
ação exata; ambas devem ser rejeitadas pelo validador. A redação das lacunas foi
delimitada ao ramo com execução pedida ou prevista, preservando a saída de
análise pura sem gate operacional. Esta evidência é estrutural; não afirma nova
execução do forward test comportamental.
