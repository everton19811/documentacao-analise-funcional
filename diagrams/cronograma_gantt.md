# 📅 Cronograma Macro do Projeto (Gantt)

Este documento apresenta a distribuição temporal das fases do projeto, marcos principais e entregáveis planejados para as Sprints.

---

## 📊 Visualização do Cronograma

```mermaid
gantt
    title Cronograma de Execução e Entregas
    dateFormat  YYYY-MM-DD
    axisFormat  %d/%m

    section 1. Iniciação & Planejamento
    Termo de Abertura (Project Charter)   :done,    m1, 2026-08-01, 2026-08-05
    Mapeamento de Stakeholders            :done,    m2, 2026-08-03, 2026-08-07
    EAP e Espec. de Requisitos            :active,  m3, 2026-08-08, 2026-08-15

    section 2. Execução (Sprints)
    Sprint 1 - Configuração & Backend     :         s1, 2026-08-16, 2026-08-29
    Sprint 2 - Frontend & Integrações     :         s2, 2026-08-30, 2026-09-12
    Sprint 3 - Testes & Homologação       :         s3, 2026-09-13, 2026-09-22

    section 3. Encerramento
    Treinamento & Handover                :         e1, 2026-09-23, 2026-09-27
    Post-Mortem & Lições Aprendidas       :         e2, 2026-09-28, 2026-09-30
