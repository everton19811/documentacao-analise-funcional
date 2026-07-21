# 📊 BPMN — Notação e Exemplos

> BPMN 2.0 (Business Process Model and Notation) é o padrão **OMG** para modelar processos de negócio de forma legível por negócio e técnico.

## Elementos básicos (em Mermaid — aproximação)

| Elemento BPMN | Símbolo | Uso |
| :--- | :--- | :--- |
| Evento início | ⭕ | Início do processo |
| Atividade | ▭ | Tarefa a ser executada |
| Gateway (decisão) | 🔷 | Ponto de decisão |
| Evento fim | 🔴 | Fim do processo |

## Exemplo — Processo de aprovação de despesa

```mermaid
flowchart LR
    S((Início)) --> A[Colaborador solicita reembolso]
    A --> V[Gestor valida nota fiscal]
    V --> G{Valor > R$ 500?}
    G -->|Sim| D[Diretor aprova]
    G -->|Não| P[Pagar direto]
    D --> P
    P --> F((Fim))
```

## Exemplo com raia (swimlane conceitual)

```mermaid
flowchart TB
    subgraph Colaborador
        A[Preenche solicitação]
    end
    subgraph Gestor
        B[Valida & aprova]
    end
    subgraph Financeiro
        C[Efetua pagamento]
    end
    A --> B --> C
```

## Boas práticas
- Nome de atividade sempre começa com **verbo no infinitivo** (Aprovar, Enviar).
- Todo gateway deve ter **saída de sim/não claramente rotulada**.
- Um processo tem **1 início e ao menos 1 fim** (pode ter múltiplos fins).
- Se o processo tem mais de 20 atividades, quebre em subprocessos.
