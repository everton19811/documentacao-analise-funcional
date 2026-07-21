---

### 1.2 `docs/BFR_Documento_Especificacao_Funcional.md` (Arquivo com Modelo de Especificação)

```markdown
# 📄 Documento de Especificação Funcional (BFR)

**Projeto:** Automação e Integração de Conciliação Financeira  
**Código do Documento:** BFR-FIN-001  
**Autor:** Everton Pereira Santos  
**Versão:** 1.0  

---

## 1. Visão Geral
Este documento especifica os requisitos funcionais para a automação da rotina de conciliação entre o módulo de faturamento corporativo e a base de dados financeira (Oracle / Cognos TM1), visando mitigar inconsistências operacionais e automatizar alertas.

## 2. Partes Interessadas (Stakeholders)
- **Área Solicitante:** Controladoria / Financeiro
- **Time Técnico:** Arquitetura de Software, DBA Oracle, Analista Funcional

## 3. Requisitos Funcionais (RF)

| ID | Descrição do Requisito | Prioridade | Regra de Negócio Associada |
| :--- | :--- | :--- | :--- |
| **RF-001** | O sistema deve realizar a carga diária de dados via Job às 02:00. | Alta | RN-001: Job automático sem intervenção manual. |
| **RF-002** | O sistema deve aplicar validação de campos obrigatórios no arquivo de entrada. | Alta | RN-002: CNPJ, Valor e Data não podem ser nulos. |
| **RF-003** | O sistema deve gerar um log de inconsistências quando houver divergência > R$ 0,01. | Média | RN-003: Tolerância máxima de divergência de centavos. |

## 4. Fluxo Principal de Processo
1. Arquivo de faturamento é disponibilizado no repositório seguro.
2. O serviço de integração valida os tipos de dados e a integridade da estrutura.
3. Os registros válidos são inseridos na tabela temporária (`STG_CONCILIACAO`).
4. A procedure de conciliação é executada comparando a `STG_CONCILIACAO` com a tabela `FATURAMENTO_OFICIAL`.
5. Registros com divergência são gravados na tabela `LOG_ERROS_CONCILIACAO` e um e-mail é disparado ao time financeiro.
