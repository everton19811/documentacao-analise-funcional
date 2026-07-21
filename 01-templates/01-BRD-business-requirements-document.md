# 📄 BRD — Business Requirements Document

> **Objetivo:** documentar o **PORQUÊ** do projeto — problema de negócio, objetivos, benefícios e escopo macro. Aprovado pelo sponsor antes de qualquer desenvolvimento.

---

## 1. Identificação

| Campo | Valor |
| :--- | :--- |
| **Projeto** | `<Nome do projeto>` |
| **Código** | `PRJ-YYYY-NNN` |
| **Sponsor** | `<Nome — cargo>` |
| **Product Owner** | `<Nome>` |
| **Analista Funcional** | `<Nome>` |
| **Versão** | 1.0 |
| **Data** | `DD/MM/YYYY` |
| **Status** | 🟡 Rascunho / 🟢 Aprovado |

---

## 2. Contexto e Problema de Negócio

`<Descrever o cenário atual e a dor que motiva o projeto. Use dados: volumes, custos, tempo perdido, riscos.>`

**Exemplo de estrutura:**
- **Situação atual:** ...
- **Problema:** ...
- **Impacto se nada for feito:** ...

---

## 3. Objetivos de Negócio (SMART)

| # | Objetivo | Métrica | Meta | Prazo |
| :--- | :--- | :--- | :--- | :--- |
| OB-01 | Reduzir tempo de fechamento contábil | Dias úteis | De 5d → 2d | 6 meses |
| OB-02 | Reduzir erros de conciliação | % divergências | De 8% → <2% | 6 meses |

---

## 4. Escopo

### 4.1 Está no escopo (In-Scope)
- ✅ ...
- ✅ ...

### 4.2 Fora do escopo (Out-of-Scope)
- ❌ ...
- ❌ ...

### 4.3 Premissas
- ...

### 4.4 Restrições
- ...

---

## 5. Stakeholders (Matriz RACI resumida)

| Stakeholder | Área | Papel | R/A/C/I |
| :--- | :--- | :--- | :--- |
| Sponsor | Diretoria Financeira | Aprovador | A |
| Key user | Contabilidade | Consultor | R |
| PO | TI | Responsável | R |
| Dev Lead | TI | Executor | C |
| Auditoria | Compliance | Informado | I |

---

## 6. Benefícios Esperados

| Benefício | Tipo | Valor estimado |
| :--- | :--- | :--- |
| Redução de horas de trabalho manual | Tangível | R$ 120k/ano |
| Aumento da confiabilidade contábil | Intangível | — |

---

## 7. Riscos de Negócio (top 5)

| # | Risco | Probabilidade | Impacto | Resposta |
| :--- | :--- | :--- | :--- | :--- |
| R-01 | Baixa adesão dos usuários | Média | Alto | Treinamento + gestão de mudança |
| R-02 | Regulação bancária mudar | Baixa | Alto | Arquitetura flexível |

---

## 8. Alto nível de Cronograma & Orçamento

| Fase | Duração | Marco |
| :--- | :--- | :--- |
| Análise & Desenho | 6 sem | Assinatura FRD |
| Desenvolvimento | 12 sem | Sistema em homologação |
| UAT & Go-live | 4 sem | Sign-off do sponsor |

**Orçamento estimado:** R$ `<valor>`

---

## 9. Aprovações (Sign-off)

| Papel | Nome | Assinatura | Data |
| :--- | :--- | :--- | :--- |
| Sponsor | | | |
| Product Owner | | | |
| Gerente de Projetos | | | |

---

## 10. Histórico de Revisões

| Versão | Data | Autor | Mudança |
| :--- | :--- | :--- | :--- |
| 1.0 | DD/MM/YYYY | `<Nome>` | Versão inicial |
