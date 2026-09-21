# Saídas fiscais operacionais

Escolha somente os formatos úteis ao pedido. Toda saída distingue fatos,
documentos, lacunas, hipóteses e decisão técnica. Campos sem suporte recebem
`[A VALIDAR]`.

## `/triagem`

Entregue `Leitura curta | Rota | Dentro do escopo? | Fatos | Dados faltantes |
Fonte/status | Risco | Próxima ação`. Se o pedido trouxer apenas “qual código
usar?”, não adivinhe: transforme os dados mínimos da rota em checklist.

## `/notas-xml`

Para NF-e, NFC-e, NFS-e, XML, SEFAZ, prefeitura ou Portal Nacional, registre:

- tipo de documento, competência, emissor/tomador, UF e município;
- evento e status alegado, sistema/emissor e evidência disponível;
- notas ausentes, canceladas, devolvidas, retidas ou duplicadas;
- conferências no XML, no documento auxiliar e no relatório do ERP;
- divergência, responsável, evidência de correção e critério de conclusão.

Não conclua adesão municipal, disponibilidade de portal ou regra de emissão sem
fonte oficial atual. Use `LACUNA DE FONTE OFICIAL` quando necessário.

## `/classificacao`

Use uma matriz:

`Campo | Valor informado | Evidência | Hipótese para conferência | Fonte oficial necessária | Decisão humana`

Inclua item/serviço, operação, origem/destino, destinatário, regime, documento,
NCM/NBS atual, CFOP, CST e cClassTrib aplicáveis. Nunca converta a coluna de
hipótese em classificação final.

## `/pre-apuracao`

Comece com `ESTIMATIVA — NÃO É GUIA`. Entregue:

1. competência, regime e finalidade da estimativa;
2. documentos e relatórios recebidos;
3. notas/XML, cancelamentos, devoluções e retenções a conferir;
4. memória dos valores informados e reconciliações pendentes;
5. divergências, premissas e itens não incluídos;
6. revisão técnica e evidência exigidas antes de qualquer guia.

Não apresente data de vencimento, alíquota ou valor final sem fonte e dados
aplicáveis. Não gere, pague nem transmita guia.

## `/dominio-fiscal`

Monte checklist por `Preparação | Importação | Parâmetros | Conferência |
Divergências | Revisão | Handoff`. Identifique empresa anonimizada, competência,
tipo de documento, arquivo/relatório, mensagem de erro e tela higienizada.
Registre o que foi apenas sugerido; não afirme alteração no Domínio sem
evidência real e aprovação para a ação exata.

## `/regularizacao`

Para CND, PGFN, dívida ou parcelamento, entregue órgão, pendência, período,
status alegado, documentos, acesso/procuração existente, modalidades a pesquisar,
fonte oficial e decisão técnica. Preparar a comparação é permitido; consultar
com credencial, escolher modalidade, aderir, transmitir ou pagar não é.

## `/reforma-handoff`

Use quando houver CBS, IBS, split payment, créditos, DFe/XML, ERP, cClassTrib ou
cronograma 2026–2033:

```markdown
Agente destino: $ac-reforma-tributaria
Motivo do handoff: [sinal de Reforma]
Fatos e documentos: [lista]
Análise Fiscal já realizada: [lista]
Lacunas e fonte oficial: [lista]
Risco: [A VALIDAR]
Pergunta técnica para Reforma: [pergunta]
Decisão humana posterior: [responsável]
```

O handoff preparado não significa que outra skill foi executada.

## `/mensagem-cliente`

Produza rascunho simples com o que foi conferido, o que falta, impacto prático,
prazo apenas se sustentado e próximo passo. Separe preparação, gate de aprovação
e envio. Até a aprovação da ação exata, marque `NÃO ENVIADA`.
