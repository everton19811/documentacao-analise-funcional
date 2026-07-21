# 📄 Catálogo de Regras — Case Conciliação

| ID | Nome | Categoria | Descrição | RF | Prioridade | Status |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| RN-01 | Formatos aceitos | Validação | Aceitar apenas OFX, CSV e CNAB240 | RF-CON-001 | Obrigatória | Ativa |
| RN-02 | Perfis de acesso | Autorização | Analista, Coord., Diretor, Auditor, Admin | RF-CON-011 | Obrigatória | Ativa |
| RN-05 | Tolerância de conciliação | Cálculo | Valor idêntico E \|Δdias úteis\| ≤ 3 | RF-CON-003 | Obrigatória | Ativa |
| RN-08 | Aprovação > R$ 10k | Autorização | Divergência > R$ 10k requer Coord. | RF-CON-005 | Obrigatória | Ativa |
| RN-09 | Aprovação > R$ 100k | Autorização | Divergência > R$ 100k requer Diretor | RF-CON-006 | Obrigatória | Ativa |
| RN-12 | Retenção de trilha | Restrição | Trilha imutável por 5 anos (SOX) | RF-CON-008 | Obrigatória | Ativa |
| RN-15 | Segregação de função | Autorização | Usuário NÃO pode aprovar sua própria divergência | RF-CON-004 | Obrigatória | Ativa |
| RN-20 | Justificativa mínima | Validação | Justificativa de divergência ≥ 20 chars | RF-CON-004 | Obrigatória | Ativa |

## Detalhe — RN-05
```
SE lancamento_contabil.valor == lancamento_banco.valor
E dias_uteis(lancamento_contabil.data, lancamento_banco.data) <= 3
ENTAO status = "Conciliado"
SENAO status = "Divergência"
```

## Detalhe — RN-15 (SoD)
```
SE aprovador.id == criador.id DA divergencia
ENTAO bloquear
    E logar tentativa
    E notificar administrador
```
