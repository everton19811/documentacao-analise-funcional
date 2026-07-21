# ✅ Checklist — Revisão de Documento Funcional

Antes de submeter para sign-off, marque cada item:

## Estrutura
- [ ] Documento tem cabeçalho com ID, versão, autor e data
- [ ] Histórico de revisões preenchido
- [ ] Índice/sumário legível
- [ ] Referências a outros documentos linkadas

## Requisitos
- [ ] Cada RF tem ID único (`RF-XXX-###`)
- [ ] Cada RF tem prioridade MoSCoW
- [ ] Cada RF é atômico (não combina 2 comportamentos)
- [ ] Cada RF é testável (dá para escrever CT)
- [ ] Cada RF rastreável a um objetivo do BRD

## Regras de negócio
- [ ] Toda regra citada no texto tem entrada no catálogo
- [ ] Nenhuma regra é ambígua (5W2H aplicado)
- [ ] Regras conflitantes foram resolvidas

## Diagramas
- [ ] Diagrama de contexto presente
- [ ] BPMN As-Is e To-Be (se aplicável)
- [ ] Fluxo principal ilustrado (sequência ou UC)

## NFR
- [ ] Performance quantificada (não "rápido")
- [ ] Segurança e auditoria descritas
- [ ] Compliance identificado (LGPD, SOX, etc.)

## Rastreabilidade
- [ ] RTM iniciada (BRD → RF → UC/US)

## Qualidade textual
- [ ] Sem ambiguidades ("aceitável", "amigável", "razoável")
- [ ] Sem duplicidade
- [ ] Glossário atualizado
