# 📄 User Stories — Case Conciliação

> 10 histórias representativas, derivadas dos RF do FRD. Todas seguem formato Connextra + Gherkin.

---

## US-101 — Importar extrato OFX (RF-CON-001)

> **Como** Analista Contábil,
> **Eu quero** fazer upload de um extrato bancário no formato OFX,
> **Para que** o sistema possa ler os lançamentos automaticamente sem digitação manual.

**Sprint:** 3 · **Story Points:** 5 · **Prioridade:** Must

### Critérios de Aceite (Gherkin)
```gherkin
Cenário: Upload de OFX válido
  Dado que estou na tela "Nova Conciliação"
  E selecionei o banco "Banco 3"
  Quando faço upload de um arquivo .ofx válido
  Então o sistema exibe a mensagem "Arquivo importado com sucesso"
  E lista os lançamentos encontrados
  E registra a operação na trilha de auditoria

Cenário: Upload de arquivo inválido
  Dado que estou na tela "Nova Conciliação"
  Quando faço upload de um arquivo .txt
  Então o sistema exibe "Formato não suportado. Aceitos: OFX, CSV, CNAB240"
  E não registra nenhum lançamento
```

**RN:** RN-01 · **UC:** UC-01

---

## US-102 — Conciliar automaticamente (RF-CON-003)

> **Como** Analista Contábil,
> **Eu quero** que o sistema concilie automaticamente lançamentos com mesmo valor e datas próximas,
> **Para que** eu só precise tratar as exceções.

**Sprint:** 4 · **SP:** 8 · **Prioridade:** Must

```gherkin
Cenário: Conciliação por valor exato + data ±3 dias úteis
  Dado que existe um lançamento contábil de R$ 1.500,00 em 10/06/2025
  E existe um lançamento bancário de R$ 1.500,00 em 12/06/2025
  Quando o sistema executar a conciliação
  Então os dois lançamentos são marcados como "Conciliados"
  E aparecem na aba "Conciliados"

Cenário: Fora da tolerância de data
  Dado que existe um lançamento contábil de R$ 1.500,00 em 10/06/2025
  E existe um lançamento bancário de R$ 1.500,00 em 17/06/2025 (5 dias úteis depois)
  Quando o sistema executar a conciliação
  Então os dois lançamentos aparecem em "Divergências"
```

**RN:** RN-05 · **UC:** UC-01

---

## US-103 — Tratar divergência manualmente (RF-CON-004)

> **Como** Analista Contábil,
> **Eu quero** classificar cada divergência como "Ajuste", "Estorno" ou "Pendente",
> **Para que** o processo de fechamento fique auditável.

```gherkin
Cenário: Marcar divergência como Ajuste
  Dado que existe uma divergência de R$ 200,00
  Quando marco como "Ajuste" e informo justificativa
  Então a divergência sai da fila de pendentes
  E é gravada na trilha de auditoria com meu usuário, timestamp e justificativa
```

**RN:** RN-15 · **UC:** UC-02

---

## US-104 — Alertar coord. sobre divergência > R$ 10k (RF-CON-005)

> **Como** Sistema,
> **Eu quero** enviar e-mail ao Coordenador de Controladoria sempre que uma divergência ultrapassar R$ 10.000,
> **Para que** ele possa aprovar rapidamente.

```gherkin
Cenário: Divergência acima do limite
  Dado que uma divergência de R$ 12.500 é gerada
  Quando o sistema finalizar a conciliação
  Então envia e-mail ao Coordenador com assunto "[CFA] Divergência R$ 12.500 requer aprovação"
  E cria uma tarefa "Aprovação pendente" no dashboard do coordenador
```

**RN:** RN-08

---

## US-105 — Gerar relatório PDF (RF-CON-007)
> Como Coord., quero gerar relatório de conciliação em PDF, para arquivar no fechamento mensal.

---

## US-106 — Dashboard de KPIs (RF-CON-009)
> Como Diretor Financeiro, quero ver dashboard com % conciliado, tempo médio e divergências pendentes por banco.

---

## US-107 — Login SSO (RF-CON-011)
> Como Usuário, quero logar com minha conta corporativa (Azure AD), para não gerenciar senha adicional.

---

## US-108 — Export trilha SOX (RF-CON-012)
> Como Auditor KPMG, quero exportar trilha em CSV assinado, para evidência SOX 404.

---

## US-109 — Configurar tolerância (RF-CON-010)
> Como Administrador, quero parametrizar a tolerância de dias por banco, para acomodar bancos que compensam em D+5.

---

## US-110 — Aprovar minha própria divergência (regra SoD)
> Como Analista, NÃO devo poder aprovar divergências que eu mesmo criei — o sistema deve bloquear (RN-15).

```gherkin
Cenário: Segregação de função (SoD)
  Dado que criei uma divergência
  Quando tento aprová-la
  Então o sistema exibe "Ação bloqueada por segregação de função (RN-15)"
  E registra tentativa na trilha
```
