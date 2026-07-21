# 📊 Diagrama de Casos de Uso (UML)

## Exemplo — Sistema de Conciliação

```mermaid
flowchart LR
    A((Analista)) --- UC1[Importar Extrato]
    A --- UC2[Conciliar Manualmente]
    A --- UC3[Consultar Divergências]
    G((Gestor)) --- UC4[Aprovar Divergência > R$ 10k]
    AU((Auditor)) --- UC5[Consultar Trilha]
    UC1 -.include.-> UC6[Validar Formato]
    UC2 -.extend.-> UC7[Marcar como Ajuste]
```

## Convenções
- **Ator** — círculo com nome
- **UC** — retângulo com verbo no infinitivo
- **Include** — UC obrigatoriamente executa outro
- **Extend** — UC pode opcionalmente executar outro
