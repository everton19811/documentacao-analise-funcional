# 📄 Catálogo de Regras de Negócio

> **Regra de Negócio (RN)** = política, restrição ou cálculo do negócio que independe da tecnologia. Deve ser rastreável ao FRD e à RTM.

---

## Estrutura de cada regra

| Campo | Descrição |
| :--- | :--- |
| **ID** | RN-XXX |
| **Nome** | Nome curto e claro |
| **Categoria** | Validação / Cálculo / Autorização / Restrição / Derivação |
| **Descrição** | Formulação clara em linguagem natural |
| **Fonte** | Documento, lei, entrevista, política |
| **Prioridade** | Obrigatória / Recomendada |
| **Requisitos associados** | RF-XXX, UC-XXX |
| **Data de vigência** | DD/MM/YYYY |
| **Status** | Ativa / Revogada / Em revisão |

---

## Exemplo preenchido

### RN-05 — Tolerância de data na conciliação

| Campo | Valor |
| :--- | :--- |
| **Categoria** | Cálculo |
| **Descrição** | Um lançamento contábil é conciliado com um lançamento bancário se: valor idêntico E diferença de data ≤ 3 dias úteis. |
| **Fonte** | Política Contábil Interna v3.2 |
| **Prioridade** | Obrigatória |
| **Requisitos** | RF-CON-002, UC-01 |
| **Vigência** | 01/01/2025 |
| **Status** | Ativa |

**Pseudocódigo:**
```
SE lancamento_contabil.valor == lancamento_banco.valor
E diferenca_dias_uteis(lancamento_contabil.data, lancamento_banco.data) <= 3
ENTAO conciliar()
SENAO marcar_como_divergencia()
```

---

## Catálogo (tabela mestra)

| ID | Nome | Categoria | Prioridade | Status |
| :--- | :--- | :--- | :--- | :--- |
| RN-01 | Formatos de arquivo aceitos | Validação | Obrigatória | Ativa |
| RN-02 | Perfil de acesso por área | Autorização | Obrigatória | Ativa |
| RN-05 | Tolerância de data ± 3 dias úteis | Cálculo | Obrigatória | Ativa |
| RN-08 | Divergência > R$ 10k requer aprovação dupla | Autorização | Obrigatória | Ativa |
| RN-12 | Retenção mínima de trilha: 5 anos | Restrição | Obrigatória | Ativa |
