# 📄 RTM — Matriz de Rastreabilidade de Requisitos

> **Objetivo:** garantir que **cada requisito de negócio** foi transformado em requisito funcional, implementado em um caso de uso, testado e homologado.
> A RTM é o **coração da governança funcional** — sem ela, não há como provar que "o que foi pedido foi entregue".

---

## Estrutura básica

| Objetivo BRD | Req. Funcional | Regra Negócio | Caso de Uso / US | Caso de Teste | Status | Sign-off |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| OB-01 | RF-CON-001 | RN-01 | UC-01 / US-101 | CT-01, CT-02 | 🟢 Homologado | ✅ 12/06 |
| OB-01 | RF-CON-002 | RN-05 | UC-01 / US-102 | CT-03, CT-04, CT-05 | 🟢 Homologado | ✅ 12/06 |
| OB-01 | RF-CON-003 | — | UC-02 / US-103 | CT-06 | 🟡 Em teste | — |
| OB-02 | RF-CON-004 | — | US-104 | CT-07 | 🔴 Pendente dev | — |
| OB-02 | RF-CON-005 | RN-08 | UC-03 / US-105 | CT-08, CT-09 | 🟢 Homologado | ✅ 12/06 |

**Legenda de status:**
- 🔴 Pendente
- 🟡 Em desenvolvimento / teste
- 🟢 Homologado

---

## Como preencher

1. **Uma linha por requisito funcional** (nível mais granular).
2. **Objetivo BRD** deve existir — se não existir, o requisito está fora do escopo.
3. **Casos de teste** devem cobrir happy path + pelo menos 1 exceção.
4. **Sign-off** só é marcado após UAT com termo assinado.

---

## Cobertura (%)

$$\text{Cobertura} = \frac{\text{RF com sign-off}}{\text{Total de RF}} \times 100\%$$

Meta para go-live: **100% dos RF "Must" com sign-off**.
