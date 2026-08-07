---
title: Fontes canonicas - Fiscal
type: knowledge-sources
status: draft
produto: Mentoria de Contadora a CEO
pilar: agentes
departamento: Fiscal
fonte_tipo: curadoria
origem: agents/knowledge/fiscal
data_criacao: 2026-07-04
data_consulta: 2026-08-06
entra_no_rag: reference_only
confiabilidade: interna_curada
tags:
  - academia-contadores/dcceo/agentes
---

# Fontes canonicas - Fiscal

| ID | Fonte | Status | Uso |
|---|---|---|---|
| FIS-FONTE-001 | agents/fiscal/_curated/03-prompt-v0-extraido.md | reference_only | prompt legado importado |
| FIS-FONTE-002 | agents/fiscal/_curated/09-prompt-v2-thread.md | sim_candidato | prompt operacional atual |
| FIS-FONTE-003 | 01_CONTABILIDADE_ESTRUTURADA_PROCESSOS/04_EXTRACOES_MD_LIMPAS/Fiscal/lote-01 | sim_candidato_com_guardrails | POPs fiscais extraidos |
| FIS-FONTE-004 | 01_CONTABILIDADE_ESTRUTURADA_PROCESSOS/05_SINTESES_POR_DEPARTAMENTO/sintese-fiscal-lote-01.md | reference_only | mapa de rotina |
| FIS-FONTE-005 | 01_CONTABILIDADE_ESTRUTURADA_PROCESSOS/06_PARECER_CONTADOR_SENIOR/parecer-contador-senior-fiscal-lote-01.md | reference_only | limites e prioridade |
| FIS-FONTE-006 | 04_PESQUISA_EXTERNA_DEEP_SEARCH/08_REFORMA_TRIBUTARIA_DAY_RAG | reference_only | Reforma, usar com fonte vigente |
| FIS-FONTE-007 | manuais longos/regimes/IRPF/planejamento | reference_only | nao usar como decisao final |
| FIS-FONTE-008 | PDFs com OCR pendente | bloqueado_ate_revisao | avisar confiabilidade parcial |

## Politica de fonte
- POP curto validado pode orientar checklist.
- Manual longo nao vira resposta final sem revisao.
- OCR pendente exige aviso de confiabilidade.
- Reforma exige fonte vigente e guardrails do agente Reforma.

## Fontes oficiais revalidadas em 2026-08-06

| Fonte oficial | URL | Aplicacao segura |
|---|---|---|
| Portal SPED | https://www.gov.br/sped/pt-br | Escrituracoes e documentos fiscais; consultar o modulo e a versao aplicavel antes de orientar |
| Receita Federal - Declaracoes e Escrituracoes | https://www.gov.br/receitafederal/pt-br/servicos/declaracoes-e-escrituracoes | Porta oficial para servicos de declaracoes e SPED; nao equivale a comprovacao de transmissao |
| Portal Nacional da NFS-e | https://www.gov.br/nfse/pt-br | Situacao, noticias e documentacao vigente da NFS-e nacional |
| NFS-e - Documentacao de producao restrita | https://www.gov.br/nfse/pt-br/biblioteca/documentacao-tecnica/producao-restrita | Layouts e schemas de homologacao, inclusive grupos IBS/CBS; nao tratar homologacao como producao |
| NFS-e - Atualizacoes e implantacoes | https://www.gov.br/nfse/pt-br/biblioteca/documentacao-tecnica/atualizacoes-e-implantacoes | Confirmar cronograma e mudancas do ambiente antes de orientar ERP ou emissor |

Alteracoes de NFS-e, DFe, IBS/CBS, cClassTrib ou cronograma da Reforma devem ser tratadas como tema temporal e encaminhadas para a IA de Reforma quando exigirem interpretacao tecnica.
