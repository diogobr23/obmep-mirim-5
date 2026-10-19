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

## Próximo passo
1. ✅ 19/10: 2 revisores separados (24 questões: links, páginas, gabaritos e resoluções ok; 1 erro de conta num escorregão do D2 + 7 ajustes aplicados). Publicado: **https://diogobr23.github.io/obmep-mirim-5/**
   ⚠️ A semana 2 precisa estar no ar até **seg 26/10**: sem ela, a página abre vazia.
2. Sáb 24: o Diogo manda as respostas da prova 2023 (com "c" nas chutadas) → corrigir → montar a correção de seg 26 e a semana 2 (dado e cubo + temas dos erros).
