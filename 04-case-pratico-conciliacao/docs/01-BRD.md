# 📄 BRD — Sistema de Conciliação Financeira Automatizada

## 1. Identificação
| Campo | Valor |
| :--- | :--- |
| Projeto | Conciliação Financeira Automatizada (CFA) |
| Código | PRJ-2025-014 |
| Sponsor | Diretor Financeiro — Alpha Retail |
| Product Owner | Coordenador de Controladoria |
| Analista Funcional | Everton Pereira Santos |
| Versão | 1.2 |
| Data | 15/03/2025 |
| Status | 🟢 Aprovado |

## 2. Contexto e Problema de Negócio

Atualmente, a **conciliação bancária × contábil** da Alpha Retail é realizada por **3 analistas full-time** utilizando planilhas Excel. O processo envolve:

- Download manual de extratos de 8 bancos (formato PDF e CSV)
- Digitação de lançamentos ausentes
- Cruzamento visual valor a valor com o razão contábil (SAP)
- Registro de divergências em planilha compartilhada

**Situação atual:**
- Tempo: **6 horas/dia × 3 analistas** = 18h/dia
- Erros: **~8% dos lançamentos** com divergência não detectada
- Fechamento contábil: **5 dias úteis**
- Auditoria (KPMG) apontou **risco material em SOX 404** por ausência de trilha automatizada

**Impacto se nada for feito:**
- Persistência de risco de compliance (SOX)
- Impossibilidade de escalar (Alpha planeja +200 lojas em 2026)
- Custo anual estimado: **R$ 540k** em horas + risco de multa

## 3. Objetivos de Negócio (SMART)

| # | Objetivo | Métrica | Meta | Prazo |
| :--- | :--- | :--- | :--- | :--- |
| OB-01 | Reduzir tempo de conciliação | Horas/dia | De 18h → 3h | 6 meses |
| OB-02 | Reduzir divergências não detectadas | % | De 8% → < 2% | 6 meses |
| OB-03 | Reduzir prazo de fechamento contábil | Dias úteis | De 5 → 2 | 9 meses |
| OB-04 | Atender SOX 404 (trilha auditoria) | Compliance | 100% | Go-live |

## 4. Escopo

### In-Scope ✅
- Importação automática de extratos dos **8 bancos** (OFX, CSV, CNAB240, API)
- Motor de conciliação com regra de tolerância
- Tela de tratamento de divergências
- Trilha de auditoria com retenção de 5 anos
- Integração de leitura com SAP (razão contábil)
- Relatórios (PDF e Excel)
- Alertas por e-mail
- SSO via Azure AD

### Out-of-Scope ❌
- Contabilização automática (permanece no SAP)
- Conciliação de cartão de crédito (fase 2)
- App mobile
- Chatbot/WhatsApp

### Premissas
- Bancos manterão o mesmo layout dos arquivos por 24 meses
- SAP disponibilizará view de leitura (`V_RAZAO_CONTABIL`)
- Azure AD já provisionado

### Restrições
- Prazo: go-live até 30/09/2025
- Orçamento: R$ 480k
- Compliance: LGPD + SOX 404
- Infraestrutura: on-premise (regra corporativa)

## 5. Stakeholders (RACI resumido)

| Stakeholder | Área | Papel | RACI |
| :--- | :--- | :--- | :--- |
| Diretor Financeiro | Financeiro | Sponsor | A |
| Coordenador de Controladoria | Controladoria | PO | R |
| Analista Contábil Sr. (Ana) | Contabilidade | Key User | R |
| Gerente de Auditoria Interna | Compliance | Aprovador SOX | C |
| Everton P. Santos | TI | AF/GP | R |
| Arquiteto de Soluções | TI | Design técnico | C |
| KPMG | Auditoria externa | Validador | I |

## 6. Benefícios Esperados

| Benefício | Tipo | Valor estimado |
| :--- | :--- | :--- |
| Realocação de 2 analistas para atividades analíticas | Tangível | R$ 360k/ano |
| Redução de risco SOX (multa evitada) | Tangível | R$ 800k (potencial) |
| Aumento da confiabilidade dos números | Intangível | — |
| Base para expansão (+200 lojas) | Estratégico | — |

**ROI estimado:** payback em **11 meses**.

## 7. Riscos de Negócio (top 5)

| # | Risco | Prob. | Impacto | Resposta |
| :--- | :--- | :--- | :--- | :--- |
| R-01 | Bancos mudarem layout do arquivo | Média | Alto | Módulo parametrizável |
| R-02 | Baixa adesão dos analistas | Média | Alto | Gestão de mudança + treinamento |
| R-03 | Atraso na entrega da view SAP | Alta | Médio | Escalar para CTO |
| R-04 | Divergência SOX na auditoria de UAT | Baixa | Alto | Envolver KPMG desde a fase de FRD |
| R-05 | Orçamento insuficiente para fase 2 (cartão) | Média | Baixo | Escopo faseado |

## 8. Cronograma & Orçamento macro

| Fase | Duração | Marco |
| :--- | :--- | :--- |
| Análise & FRD | 6 sem | Sign-off FRD |
| Desenvolvimento | 14 sem | Sistema em HML |
| UAT & Sign-off SOX | 4 sem | Aceite KPMG |
| Go-live & estabilização | 4 sem | Encerramento |

**Total:** 28 semanas · **Orçamento:** R$ 480k

## 9. Aprovações
| Papel | Nome | Data |
| :--- | :--- | :--- |
| Sponsor | Diretor Financeiro | 15/03/2025 |
| PO | Coord. Controladoria | 15/03/2025 |
| GP/AF | Everton P. Santos | 15/03/2025 |

## 10. Histórico
| v | Data | Autor | Mudança |
| :--- | :--- | :--- | :--- |
| 1.0 | 01/03/2025 | Everton | Versão inicial |
| 1.1 | 10/03/2025 | Everton | Ajustes após workshop |
| 1.2 | 15/03/2025 | Everton | Inclusão de SOX 404 (obs KPMG) |
