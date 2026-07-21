# 📄 Especificação Funcional Detalhada

> Documento de nível técnico-funcional que serve de referência para desenvolvimento e teste. Combina UC + regras + protótipo.

## EF-XXX — `<Nome da funcionalidade>`

### 1. Metadados
| Campo | Valor |
| :--- | :--- |
| ID | EF-XXX |
| Módulo | `<Nome>` |
| Versão | 1.0 |
| AF | `<Nome>` |

### 2. Objetivo
`<O que essa funcionalidade resolve>`

### 3. Atores & Perfis
| Perfil | Permissão |
| :--- | :--- |

### 4. Pré-condições

### 5. Fluxo Principal (passo a passo por tela)

**Tela 1 — `<Nome>`**
- Campos:
  - `Campo A` — Texto, obrigatório, máx. 100 chars
  - `Campo B` — Data, obrigatório, formato DD/MM/YYYY
- Ações: `[Salvar]` `[Cancelar]`
- Validações: `<RN-XX>`

**Tela 2 — ...**

### 6. Fluxos Alternativos e Exceções

### 7. Regras de Negócio Aplicadas
- RN-XX, RN-YY

### 8. Mensagens do Sistema
| Código | Tipo | Mensagem |
| :--- | :--- | :--- |
| MSG-001 | Erro | "Campo obrigatório" |
| MSG-002 | Info | "Registro salvo com sucesso" |

### 9. Layout / Wireframe
`<Anexar imagem / link Figma>`

### 10. Impactos
| Sistema | Tipo de impacto |
| :--- | :--- |
| ERP | Consumo de API |
| BI | Nova fonte de dados |

### 11. Cenários de Teste (Gherkin)
```gherkin
Cenário: Salvar com dados válidos
  Dado que o usuário preencheu Campo A e Campo B
  Quando clicar em Salvar
  Então o sistema exibe MSG-002
```
