# Agente Fiscal Oficial

| Campo | Valor |
| --- | --- |
| ID | `ac.fiscal` |
| Skill | `$ac-fiscal` |
| GPT representado | [`g-6a72595c828c8191aec02f7931d9c626`](https://chatgpt.com/gpts/editor/g-6a72595c828c8191aec02f7931d9c626) |
| Versão candidata | `0.2.0` |
| Lifecycle | `candidate` |

## O que esta skill faz

A skill organiza rotinas fiscais brasileiras em triagens, checklists, matrizes
de conferência, briefings e handoffs. Ela cobre notas e XML, NF-e/NFC-e/NFS-e,
SEFAZ, prefeitura, Portal Nacional, CFOP/NCM/CST/cClassTrib, regimes, CND,
parcelamento, pré-apuração, Domínio Fiscal e encaminhamento para Reforma.

A candidata foi projetada para ser mais operacional que o GPT preservado, mas
mantém os mesmos limites: não inventa regra ou fonte vigente, não fecha
classificação, cálculo ou guia, não escolhe regime, não usa segredo e não
executa ação externa sem aprovação humana imediatamente antes da ação exata.

Os GPTs duplicados ou temporários da família Fiscal não recebem outra skill.
Todos reutilizam este repositório e `$ac-fiscal`; o link acima identifica o GPT
canônico usado como baseline comportamental.

## Knowledge correto

O pacote distribuível usa exatamente dez documentos:

- `knowledge/original/00-INDICE-FISCAL.md`;
- os nove `.md` de `knowledge/live-2026-08-22/` listados em `agent.yaml`.

Os outros nove arquivos de `knowledge/original/` são preservados apenas para
auditoria porque a captura contém material de DP. Eles não entram na skill. Os
nomes dos dez anexos foram reconfirmados no GPT em 2026-09-21; os bytes online
atuais continuam como `GAP`, por isso a seleção é uma baseline histórica,
provisória e reversível.

## Exemplo para leigos

```text
Use $ac-fiscal. Importei XML no Domínio e o total não bateu. Ainda não sei se há notas canceladas ou devoluções. Monte o checklist de conferência e diga o que preciso enviar ao responsável fiscal.
```

A resposta deve organizar o que já se sabe, listar os documentos faltantes,
marcar riscos e preparar a revisão. Ela não deve afirmar que corrigiu o Domínio.

## Estado atual

O pacote candidato contém uma allowlist de 23 arquivos, incluindo os dez
documentos Fiscal, e seis casos P1–P6 para comparação posterior com o GPT. Esta
etapa prepara a skill para instalação e forward test; ainda não promove o
lifecycle para `validated`.

Para usar, instalar ou manter, consulte [HOW-TO-USE.md](HOW-TO-USE.md). Para a
evidência da fonte, veja
[evaluations/live-editor-audit-2026-09-21.md](evaluations/live-editor-audit-2026-09-21.md).
