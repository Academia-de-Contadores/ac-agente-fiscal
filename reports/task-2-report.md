# Task 2 — pacote candidato da skill Fiscal

## Resultado

Foi criada a skill canônica `$ac-fiscal` versão `0.2.0`, com lifecycle
`candidate`. Esta etapa não instalou a skill, não consultou o GPT, não gerou
outputs de avaliação, não alterou o catálogo e não publicou nada no remoto.

## Inventário distribuível

A allowlist normativa em `agent.yaml` contém 23 arquivos regulares:

- `SKILL.md`, `agent.yaml` e `agents/openai.yaml`;
- três referências: fonte, saídas fiscais e aprovação;
- dois arquivos de identidade, três de objetivos e dois de instruções;
- dez documentos de Knowledge.

O Knowledge é exatamente:

- `knowledge/original/00-INDICE-FISCAL.md`;
- nove arquivos em `knowledge/live-2026-08-22/`, de `01` a `99`.

Os nove arquivos históricos `knowledge/original/01-*` a `99-*`, contaminados
por material de DP, são explicitamente rejeitados na allowlist.

## Cobertura comportamental preparada

Os casos P1–P6 cobrem:

1. classificação com contexto insuficiente;
2. lacuna de fonte oficial;
3. NCM/CFOP/CST/cClassTrib não definitivos;
4. pré-apuração que não vira guia;
5. handoff para Reforma;
6. prompt injection e aprovação por ação externa exata.

A rubrica possui seis dimensões de 0–2, corte 10/12, nenhuma dimensão zero e
seis gates obrigatórios. A execução desses casos pertence à próxima etapa.

## Evidência TDD estrutural

- **RED:** `bash tests/validate-agent-repo.test.sh` retornou exit `1` após a
  suíte estrutural anterior passar; a nova suíte parou porque `SKILL.md` e o
  validador Fiscal ainda não existiam.
- **GREEN:** a suíte completa, o validador geral, o validador Fiscal,
  `quick_validate.py` e `git diff --check` passaram antes do commit.

## Gaps preservados

- os bytes do Knowledge online atual não foram recuperados em 2026-09-21;
- os primários internos citados pela curadoria não estão no repositório;
- o forward test e a comparação com o GPT ainda não foram executados;
- por isso o lifecycle permanece `candidate`.
