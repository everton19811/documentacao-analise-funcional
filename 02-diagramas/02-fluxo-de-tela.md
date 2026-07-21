# 📊 Fluxo de Tela / Navegação

Modela como o usuário navega entre telas do sistema.

## Exemplo — Fluxo de login e dashboard

```mermaid
flowchart LR
    T1[Tela Login] -->|Credencial válida| T2[Dashboard]
    T1 -->|Credencial inválida| T1
    T2 --> T3[Nova conciliação]
    T2 --> T4[Relatórios]
    T3 --> T5[Upload extrato]
    T5 --> T6[Resultado conciliação]
    T6 --> T2
```

## Como usar em documentação
1. Cada nó = **1 tela real**
2. Rótulo da seta = **ação do usuário** ou **condição**
3. Vincule cada tela a um **wireframe/Figma** em anexo
