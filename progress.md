# Progress — OBMEP Mirim 2 (5º ano)

## Estado (19/10/2026)
- **18/10:** desenho aprovado (`PLANO.md`) e regras (`CLAUDE.md`). Ritmo: 30–40 min nos dias de semana e prova inteira aos sábados.
- **19/10 — Fase 1 (pesquisa) feita:**
  - Regulamento: terça 10/11, 15 questões A–E, 1h30.
  - 18 PDFs oficiais do Mirim 2 baixados (2ª fase 2022–2025 e 1ª fase 2022–2026, com soluções), mais o Nível A.
  - 135 questões classificadas (`pesquisa/classif/`). Um revisor conferiu os 135 gabaritos contra as soluções oficiais.
  - Análise em `pesquisa/analise-2a-fase.md`: lógica 22%, visão espacial 20%, operações 15%. O difícil é ler e organizar.
- Provas de sábado: 24/10 = 2023 (diagnóstico) · 31/10 = 2024 · 07/11 = 2025.
- **Semana 1** (ter 20 a sáb 24): D1 lógica · D2 operações · D3 visão espacial · D4 tempo e "cerca e postes" · S1 prova 2023.
  - Dado e cubo ficou para a semana 2, porque todo o material oficial do tema está nas provas de sábado.
  - Cada dia foi escrito por um agente a partir de `pesquisa/molde-dia.md` (`pesquisa/dias/`) e montado no `roteiro/index.html`.

## Como montar
`roteiro/index.html` foi gerado uma vez a partir de `pesquisa/dias/*.html` + `*-cartas.js`. Daqui pra frente, editar direto o `index.html`.
O localStorage usa só o prefixo `mirim2:`.

## 29/10 — calendário refeito
A criança não fez a semana 1 e começou só hoje. Os 4 dias prontos e a prova 2023 foram remarcados sem mudar o conteúdo
(ver `PLANO.md`): D1 29/10 · D2 30/10 · S1 31/10 · D3 01/11 · D4 02/11. O card S1 foi movido para antes do D3 no HTML.
A página agora conta "Semana 1 de 3" a partir de 26/10, e as cartinhas tiveram o `desde` ajustado.

## Próximo passo
1. Sáb 31: o Diogo manda as respostas da prova 2023 (com "c" nas chutadas) → corrigir.
2. ⚠️ Até **dom 01/11**: montar e publicar a semana 2 (correção 2023 em seg 02, dado e cubo em ter 03, temas dos erros
   de qua 04 a sex 06, card da prova 2025 em sáb 07, correção em dom 08) e o seg 09. Sem isso, a página abre vazia em 03/11.
   Revisor separado antes de publicar.
