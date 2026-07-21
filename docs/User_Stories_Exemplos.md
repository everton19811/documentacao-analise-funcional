# 📌 Modelos de Histórias de Usuário (User Stories)

---

### 🔹 US-01: Visualização de Divergências Orçamentárias

**História:**
> **Como** Analista Financeiro,  
> **Quero** visualizar um dashboard com a lista de divergências de conciliação agrupadas por centro de custo,  
> **Para que** eu possa corrigir os lançamentos incorretos antes do fechamento mensal.

**Critérios de Aceite (Dado / Quando / Então):**
- **Cenário 1: Filtro por Período Valido**
  - **Dado** que estou autenticado na plataforma com perfil "Financeiro",
  - **Quando** seleciono o mês de competência e clico em "Filtrar",
  - **Então** o sistema exibe a lista de registros divergentes com coluna de valor esperado x valor realizado.

- **Cenário 2: Exportação do Relatório**
  - **Dado** que a lista de divergências contém registros,
  - **Quando** clico no botão "Exportar Excel",
  - **Então** o arquivo `.xlsx` é baixado mantendo a formatação numérica padrão do sistema.

---

### 🔹 US-02: Notificação de Falha de Integração

**História:**
> **Como** Administrador de TI / Sustentação,  
> **Quero** receber um alerta por e-mail quando a carga de dados de importação falhar,  
> **Para que** eu possa atuar na causa raiz sem impactar a operação matinal.
