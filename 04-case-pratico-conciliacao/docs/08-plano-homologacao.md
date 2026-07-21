# 📄 Plano de Homologação (UAT) — Case CFA

## 1. Objetivo
Validar, com o key user Ana (Contábil Sr.), que o CFA atende 100% dos RF "Must" antes do go-live em 30/09/2025.

## 2. Escopo
- Todos os RF "Must" (9 RFs)
- Trilha SOX (validação KPMG separada em 20/07)
- 3 bancos representativos (Banco 1 API, Banco 3 OFX, Banco 5 CNAB240)

## 3. Ambiente
- **URL:** https://cfa-hml.alpharetail.local
- **Usuários de teste:**
  - `ana.contabil` (perfil Analista)
  - `carlos.coord` (perfil Coord.)
  - `diretor.fin` (perfil Diretor)
  - `auditor.kpmg` (perfil Auditor)
- **Dados:** massa de 5.000 lançamentos de junho/2025 (anonimizada)

## 4. Cronograma

| Dia | Atividade |
| :--- | :--- |
| 08/07 | Treinamento (2h) |
| 09–11/07 | Execução guiada (AF + Ana) |
| 14/07 | Consolidação de bugs |
| 15/07 | Retest de bugs corrigidos |
| 16/07 | Sign-off |

## 5. Casos de Teste (extrato)

| CT | Descrição | RF | Resultado esperado | Executado | Resultado |
| :--- | :--- | :--- | :--- | :--- | :--- |
| CT-01 | Upload OFX válido | RF-CON-001 | Import ok, X lançamentos | 09/07 | ✅ Passou |
| CT-02 | Upload TXT inválido | RF-CON-001 | Erro "Formato não suportado" | 09/07 | ✅ Passou |
| CT-05 | Conciliação R$ 1500 · datas próximas | RF-CON-003 | Marcado "Conciliado" | 10/07 | ✅ Passou |
| CT-06 | Conciliação · Δ = 5 dias úteis | RF-CON-003 | Marcado "Divergência" | 10/07 | ✅ Passou |
| CT-08 | Tratar divergência com justificativa curta | RF-CON-004 | Erro "min. 20 chars" (RN-20) | 11/07 | ✅ Passou |
| CT-09 | Tentar aprovar própria divergência | RF-CON-004 | Bloqueio SoD (RN-15) | 11/07 | ✅ Passou |
| CT-11 | Divergência R$ 15.000 | RF-CON-005 | E-mail ao Coord | 11/07 | ✅ Passou |
| CT-14 | Consultar trilha 30 dias atrás | RF-CON-008 | Retorno < 3s, imutável | 14/07 | ✅ Passou |

## 6. Critérios de Aceite (go/no-go)

| Critério | Meta | Real | Status |
| :--- | :--- | :--- | :--- |
| RF "Must" homologados | 100% | 100% | ✅ |
| Bugs críticos abertos | 0 | 0 | ✅ |
| Bugs altos abertos | ≤ 2 | 1 | ✅ |
| Sign-off KPMG | Sim | 20/07 | ✅ |
| Treinamento executado | Sim | 08/07 | ✅ |

## 7. Sign-off

| Papel | Nome | Assinatura | Data |
| :--- | :--- | :--- | :--- |
| Key User | Ana (Contábil Sr.) | _________ | 16/07/2025 |
| PO | Coord. Controladoria | _________ | 16/07/2025 |
| Sponsor | Diretor Financeiro | _________ | 16/07/2025 |
| Auditoria | KPMG | _________ | 20/07/2025 |
| GP/AF | Everton P. Santos | _________ | 16/07/2025 |

**Status geral: 🟢 APROVADO PARA GO-LIVE**
