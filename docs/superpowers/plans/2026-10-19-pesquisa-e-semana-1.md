# Pesquisa + Semana 1 — Plano de execução

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:executing-plans. Steps use checkbox (`- [ ]`) syntax.

**Goal:** Fechar a Fase 1 (pesquisa) e a Fase 2 (semana 1 publicada) do `PLANO.md`.

**Architecture:** Os PDFs oficiais ficam em `provas/`. A análise de temas fica em `pesquisa/analise-2a-fase.md`, com o gabarito
de cada questão. A página `roteiro/index.html` é copiada da estrutura do `estudo-cmb` (cards por dia, cartinhas, checagem
de KaTeX) com prefixo `mirim2:`.

**Tech Stack:** HTML/CSS/JS estático, KaTeX auto-hospedado, GitHub Pages, Python (PyMuPDF via `pdf_read.py`) para ler PDFs.

**Spec:** `PLANO.md` + `CLAUDE.md`

## Global Constraints
- Nenhum dado pessoal da criança no repo, nos commits, nos prompts ou na memória.
- Toda resposta de questão oficial vem do gabarito oficial.
- Nada fora do que cai na prova.
- Linguagem de criança de 10 anos.
- Na página: "tabela das unidades", nunca "escada"/"degrau".
- Prefixo do localStorage: `mirim2:`.
- Prompts de subagente terminam com "Responda em português brasileiro".

## Review Focus
1. Prova de sábado usada em dia de semana: deve ser impossível (checar por número de questão).
2. Gabarito copiado errado (letra trocada): confrontar com o PDF de solução.
3. Página aberta no celular: sem rolagem horizontal; tabela das unidades cabe.
4. Progresso do Mirim 2 apagando o do CMB/Mirim 1: as chaves precisam começar com `mirim2:`.
5. Dia fora da semana atual aparecendo: testar a lógica de semana com datas simuladas.

---

### Task 1: Regulamento e provas oficiais
**Files:** Create `provas/*.pdf`, `pesquisa/fontes.md`
- [ ] Buscar no site da Olimpíada Mirim (olimpiadamirim.obmep.org.br) o regulamento 2026 e as provas de 2ª fase do Mirim 2 com solução (todos os anos disponíveis).
- [ ] Baixar para `provas/AAAA-2fase-prova.pdf` e `provas/AAAA-2fase-solucao.pdf`; também as de 1ª fase do Mirim 2 (banco de treino).
- [ ] Anotar em `pesquisa/fontes.md`: data da 2ª fase, nº de questões, duração, local, URL de cada PDF.
- [ ] Commit.

### Task 2: Análise "o que cai"
**Files:** Create `pesquisa/analise-2a-fase.md`
- [ ] Ler cada prova de 2ª fase (texto; se escaneada, PNG a 80 dpi e apagar depois).
- [ ] Tabela: ano · questão · tema · gabarito oficial · dificuldade (fácil/média/difícil).
- [ ] Peso por tema (% das questões), ordenado.
- [ ] Reservar as 3 provas mais recentes para os sábados (24/10, 31/10, 07/11); as demais e a 1ª fase viram banco.
- [ ] Escolher os 4 temas da semana 1 (fortes no peso e leves para a retomada pós-CMB).
- [ ] Revisor separado confere tema e gabarito de uma amostra contra os PDFs.
- [ ] Commit; relatório curto para o Diogo (temas, peso e os 4 da semana 1) antes da Task 3.

### Task 3: Página-base
**Files:** Create `roteiro/index.html`, `roteiro/check_katex.js`, `roteiro/vendor/katex/`, `index.html`, `robots.txt`
- [ ] Copiar do `estudo-cmb` a estrutura (CSS, lógica da semana, cartinhas, progresso), sem nenhum conteúdo de dia.
- [ ] Trocar todas as chaves do localStorage para `mirim2:` (`grep -n "localStorage" roteiro/index.html` → só `mirim2:`).
- [ ] Testar a lógica de semana com datas simuladas (19/10, 24/10, 26/10, 10/11).
- [ ] Commit.

### Task 4: Semana 1 (ter 20 a sáb 24)
**Files:** Modify `roteiro/index.html`
- [ ] 4 cards de tema (ideia do dia + escadinha de 4–6 questões oficiais do banco, com resolução em balões e gabarito oficial).
- [ ] Card de sábado: prova 1 (link do PDF, 1h30, como passar as respostas pro Diogo).
- [ ] Cartinhas iniciais (`quero`, `unid`, `parsai`, `ordop` se couberem nos temas + 1 por tema da semana).
- [ ] `node roteiro/check_katex.js` com 0 erros; HTML balanceado; ids únicos.
- [ ] Revisor separado (contas, gabarito, linguagem); aplicar ajustes.
- [ ] Commit.

### Task 5: Publicar
- [ ] `gh repo create diogobr23/obmep-mirim-5 --public --source . --push`; ativar Pages (branch main, raiz).
- [ ] `curl` na URL de `roteiro/` retorna 200; Diogo abre no celular.
- [ ] `progress.md` com estado e próximo passo; commit e push.
