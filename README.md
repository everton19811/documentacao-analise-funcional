# 📘 Documentação de Análise Funcional — Material Didático

> Repositório-modelo com **templates, técnicas, checklists e um case prático completo** de Análise Funcional / Análise de Negócio.
> Construído para ser **material de estudo** e **modelo reutilizável** em projetos reais.

[![BABOK v3](https://img.shields.io/badge/BABOK-v3-025E73?style=flat-square)](https://www.iiba.org/career-resources/a-business-analysis-professional-s-foundation-for-success/babok/)
[![IIBA](https://img.shields.io/badge/IIBA-Aligned-0077B5?style=flat-square)](https://www.iiba.org/)
[![PMBOK](https://img.shields.io/badge/PMBOK-7ed-000000?style=flat-square)](https://www.pmi.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg?style=flat-square)](LICENSE)

---

## 🎯 Objetivo

Fornecer um **kit completo do Analista Funcional / Analista de Negócio** com:

1. **Fundamentos** — o que é AF, papel do profissional, ciclo de vida da análise, glossário.
2. **Templates prontos** — BRD, FRD, SRS, User Story, Caso de Uso, RTM, Regras de Negócio, GAP Analysis, Change Request.
3. **Técnicas de elicitação** — entrevistas, workshops, MoSCoW, 5W2H, SIPOC, BPMN.
4. **Case prático ponta a ponta** — projeto "Sistema de Conciliação Financeira" com **todos** os artefatos preenchidos.
5. **Checklists de qualidade** — revisão de documentação, homologação (UAT), sign-off.

---

## 🗂️ Como este repositório está organizado

```text
documentacao-analise-funcional/
├── 00-fundamentos/           ← O que é AF, papel, ciclo, glossário
├── 01-templates/             ← Modelos em branco (BRD, FRD, SRS, US, UC, RTM...)
├── 02-diagramas/             ← Exemplos de BPMN, fluxos e casos de uso em Mermaid
├── 03-tecnicas-elicitacao/   ← Entrevistas, workshops, MoSCoW, 5W2H, SIPOC
├── 04-case-pratico-conciliacao/  ← Case COMPLETO preenchido (referência prática)
├── 05-checklists/            ← Revisão, homologação, UAT, sign-off
├── 06-referencias/           ← BABOK, IIBA, livros, cursos e links úteis
└── .github/                  ← Templates de issue (US, bug funcional, regra, CR) e PR
```

---

## 🚀 Como usar este material

### 👨‍🎓 Se você está **estudando** Análise Funcional
1. Comece por [`00-fundamentos/01-o-que-e-analise-funcional.md`](00-fundamentos/01-o-que-e-analise-funcional.md).
2. Estude as **técnicas** em `03-tecnicas-elicitacao/`.
3. Leia o **case prático** em `04-case-pratico-conciliacao/` — veja como cada técnica vira artefato.
4. Refaça o case mudando o domínio (ex.: e-commerce, RH, logística).

### 👨‍💼 Se você é **Analista Funcional** trabalhando em um projeto
1. Copie os arquivos de `01-templates/` para o seu projeto.
2. Preencha seguindo o exemplo em `04-case-pratico-conciliacao/`.
3. Use os `05-checklists/` antes de submeter para sign-off.

### 🎓 Se você é **recrutador / avaliador**
- Este repositório demonstra **domínio prático** de: BABOK v3, PMBOK, Scrum, BPMN, UML (Casos de Uso), regras de negócio, RTM (Requirements Traceability Matrix) e homologação.

---

## 📚 Índice completo de artefatos

### 00 — Fundamentos
- [O que é Análise Funcional](00-fundamentos/01-o-que-e-analise-funcional.md)
- [Papel do Analista Funcional](00-fundamentos/02-papel-do-analista-funcional.md)
- [Ciclo de vida da Análise](00-fundamentos/03-ciclo-de-vida-da-analise.md)
- [Glossário de termos](00-fundamentos/04-glossario.md)

### 01 — Templates (em branco, prontos para preencher)
- [BRD — Business Requirements Document](01-templates/01-BRD-business-requirements-document.md)
- [FRD — Functional Requirements Document](01-templates/02-FRD-functional-requirements-document.md)
- [SRS — Software Requirements Specification (IEEE 830)](01-templates/03-SRS-software-requirements-specification.md)
- [User Story (formato Connextra + INVEST)](01-templates/04-user-story.md)
- [Caso de Uso (UML)](01-templates/05-caso-de-uso.md)
- [Regra de Negócio](01-templates/06-regra-de-negocio.md)
- [RTM — Requirements Traceability Matrix](01-templates/07-RTM-matriz-rastreabilidade.md)
- [GAP Analysis (As-Is × To-Be)](01-templates/08-gap-analysis.md)
- [Especificação Funcional Detalhada](01-templates/09-especificacao-funcional.md)
- [Change Request (Solicitação de Mudança)](01-templates/10-change-request.md)

### 02 — Diagramas (Mermaid)
- [BPMN — Notação e exemplos](02-diagramas/01-bpmn-exemplos.md)
- [Fluxo de tela / navegação](02-diagramas/02-fluxo-de-tela.md)
- [Diagrama de Casos de Uso](02-diagramas/03-diagrama-casos-de-uso.md)

### 03 — Técnicas de Elicitação
- [Entrevista com stakeholder](03-tecnicas-elicitacao/01-entrevista-stakeholder.md)
- [Workshop de requisitos](03-tecnicas-elicitacao/02-workshop-requisitos.md)
- [MoSCoW — priorização](03-tecnicas-elicitacao/03-priorizacao-moscow.md)
- [5W2H aplicado a requisitos](03-tecnicas-elicitacao/04-5w2h.md)
- [SIPOC — visão de processo](03-tecnicas-elicitacao/05-sipoc.md)

### 04 — Case Prático Completo 🎯
**Projeto: Sistema de Conciliação Financeira Automatizada**
- [Visão geral do case](04-case-pratico-conciliacao/README.md)
- [BRD preenchido](04-case-pratico-conciliacao/docs/01-BRD.md)
- [FRD preenchido](04-case-pratico-conciliacao/docs/02-FRD.md)
- [User Stories](04-case-pratico-conciliacao/docs/03-user-stories.md)
- [Casos de Uso](04-case-pratico-conciliacao/docs/04-casos-de-uso.md)
- [Regras de Negócio](04-case-pratico-conciliacao/docs/05-regras-de-negocio.md)
- [Matriz de Rastreabilidade (RTM)](04-case-pratico-conciliacao/docs/06-RTM.md)
- [GAP Analysis As-Is × To-Be](04-case-pratico-conciliacao/docs/07-gap-analysis.md)
- [Plano de Homologação (UAT)](04-case-pratico-conciliacao/docs/08-plano-homologacao.md)
- [Diagramas BPMN & Casos de Uso](04-case-pratico-conciliacao/diagramas/)

### 05 — Checklists de Qualidade
- [Checklist de revisão de documento funcional](05-checklists/01-revisao-documento.md)
- [Checklist de homologação (UAT)](05-checklists/02-homologacao-uat.md)
- [Checklist de sign-off](05-checklists/03-sign-off.md)

### 06 — Referências
- [BABOK v3, PMBOK, livros e cursos](06-referencias/README.md)

---

## 👤 Autor

**Everton Pereira Santos** — Gerente de Projetos | Analista Funcional Sênior | Analista de Negócios

- 🌐 [github.com/everton19811](https://github.com/everton19811)
- 💼 [LinkedIn](https://linkedin.com/in/evertonpereirasantos)
- 📧 everton1981@gmail.com

---

## 📜 Licença

MIT — sinta-se livre para reutilizar em projetos pessoais, profissionais ou acadêmicos, citando a fonte.
