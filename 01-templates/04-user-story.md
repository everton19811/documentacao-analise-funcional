# 📄 User Story — Template

## Formato Connextra
> **Como** `<persona>`
> **Eu quero** `<ação/funcionalidade>`
> **Para que** `<benefício de negócio>`

---

## US-XXX — `<Título curto e claro>`

| Campo | Valor |
| :--- | :--- |
| **ID** | US-XXX |
| **Épico** | EP-YY |
| **Feature** | FT-YY |
| **Sprint** | `<n>` |
| **Estimativa** | `<story points>` |
| **Prioridade** | Must / Should / Could |
| **Autor** | `<AF>` |

### História
> Como **`<persona>`**, eu quero **`<ação>`** para que **`<benefício>`**.

### Contexto / Regra de negócio
`<Explicação adicional, links para RN-XX>`

### Critérios de Aceite (Gherkin)

```gherkin
Cenário: <descrição do cenário feliz>
  Dado que <pré-condição>
  E que <outra pré-condição>
  Quando <ação>
  Então <resultado esperado>
  E <outro resultado>

Cenário: <exceção / erro>
  Dado que <pré-condição inválida>
  Quando <ação>
  Então <mensagem de erro esperada>
```

### Definition of Ready (DoR)
- [ ] História escrita no formato Connextra
- [ ] Critérios de aceite definidos
- [ ] Regras de negócio linkadas
- [ ] Mockup/protótipo anexado (se aplicável)
- [ ] Estimada pelo time
- [ ] Dependências identificadas

### Definition of Done (DoD)
- [ ] Código revisado (code review)
- [ ] Testes unitários ≥ 80%
- [ ] Testes de integração passando
- [ ] Documentação atualizada
- [ ] Deploy em homologação
- [ ] UAT aprovado pelo key user
- [ ] Sem bugs bloqueantes

---

## Checklist INVEST (qualidade da US)

- [ ] **I**ndependent — pode ser entregue isoladamente
- [ ] **N**egotiable — não é um contrato rígido
- [ ] **V**aluable — entrega valor ao usuário
- [ ] **E**stimable — o time consegue estimá-la
- [ ] **S**mall — cabe em uma sprint
- [ ] **T**estable — tem critérios claros de aceite
