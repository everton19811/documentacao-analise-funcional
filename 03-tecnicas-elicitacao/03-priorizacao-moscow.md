# 🎯 MoSCoW — Priorização

| Categoria | Significado | % típico do escopo |
| :--- | :--- | :--- |
| **M**ust have | Sem isso o produto NÃO vai a produção | 60% |
| **S**hould have | Importante, mas dá para postergar 1 release | 20% |
| **C**ould have | Se sobrar tempo, entregar | 15% |
| **W**on't have (this time) | Fora do escopo desta release | 5% |

## Como aplicar
1. Liste todos os requisitos
2. Peça a cada stakeholder para classificar
3. Consolide — se houver conflito, sponsor decide
4. Reveja a cada sprint (prioridade muda)

## Exemplo aplicado ao case de conciliação
| RF | MoSCoW |
| :--- | :--- |
| RF-CON-001 (import extrato) | Must |
| RF-CON-002 (conciliação automática) | Must |
| RF-CON-003 (conciliação manual) | Must |
| RF-CON-004 (export relatório) | Should |
| RF-CON-005 (alerta e-mail) | Could |
| RF-CON-006 (integração WhatsApp) | Won't |

## Anti-padrão
❌ Cliente marca 100% como "Must" — force a distribuição real.
