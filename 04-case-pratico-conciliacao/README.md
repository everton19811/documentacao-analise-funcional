# 🎯 Case Prático — Sistema de Conciliação Financeira Automatizada

> **Case completo, ponta a ponta**, mostrando **como aplicar todos os templates deste repositório em um projeto real**. Baseado em experiência prática de sustentação e automação em Cognos TM1 + Oracle + ERP (anonimizado).

---

## 📋 Contexto

**Empresa:** "Alpha Retail" (fictícia — inspirada em varejo de grande porte)
**Setor:** Varejo alimentar, +500 lojas no Brasil
**Área demandante:** Controladoria / Contabilidade
**Problema:** conciliação bancária × contábil feita 100% em Excel, com 6h/dia por analista e ~8% de divergências não detectadas.

---

## 🎯 Objetivo do projeto

Automatizar 80% das conciliações bancárias, reduzir tempo de fechamento contábil de 5 → 2 dias úteis e gerar trilha de auditoria compatível com SOX.

---

## 🗂️ Artefatos deste case

Todos os artefatos abaixo foram produzidos usando os templates de [`../01-templates/`](../01-templates/):

| # | Artefato | Arquivo |
| :--- | :--- | :--- |
| 1 | Business Requirements Document | [`docs/01-BRD.md`](docs/01-BRD.md) |
| 2 | Functional Requirements Document | [`docs/02-FRD.md`](docs/02-FRD.md) |
| 3 | User Stories (10 exemplos) | [`docs/03-user-stories.md`](docs/03-user-stories.md) |
| 4 | Casos de Uso (UML) | [`docs/04-casos-de-uso.md`](docs/04-casos-de-uso.md) |
| 5 | Catálogo de Regras de Negócio | [`docs/05-regras-de-negocio.md`](docs/05-regras-de-negocio.md) |
| 6 | Matriz de Rastreabilidade | [`docs/06-RTM.md`](docs/06-RTM.md) |
| 7 | GAP Analysis As-Is × To-Be | [`docs/07-gap-analysis.md`](docs/07-gap-analysis.md) |
| 8 | Plano de Homologação (UAT) | [`docs/08-plano-homologacao.md`](docs/08-plano-homologacao.md) |
| 9 | Diagramas BPMN & Casos de Uso | [`diagramas/`](diagramas/) |

---

## 📈 Resultados atingidos (STAR)

- **S — Situation:** conciliação 100% manual em Excel, com 3 analistas dedicados full-time.
- **T — Task:** automatizar o processo com governança SOX e integração ao ERP.
- **A — Action:** conduzi elicitação com 7 stakeholders (2 workshops + 5 entrevistas), produzi BRD/FRD/RTM completos e liderei UAT com key user.
- **R — Result:** ✅ **-35% de erros de conciliação**, **-70% do tempo de execução** (6h → 30min), **fechamento contábil reduzido de 5 para 2 dias úteis**.

---

## 🛠️ Como estudar este case

1. Leia o `BRD` — entenda o **porquê** do projeto.
2. Leia o `FRD` — entenda **o quê** o sistema faz.
3. Compare `As-Is × To-Be` no GAP.
4. Veja como **cada RF vira US** com critérios de aceite em Gherkin.
5. Estude a **RTM** — perceba a rastreabilidade completa.
6. Termine no **plano de homologação** — veja como se prova que o requisito foi entregue.
