# CLAUDE.md — OBMEP Mirim 2 (5º ano)

Roteiro para uma criança do **5º ano** classificada para a **2ª fase da Olimpíada Mirim – OBMEP,
nível Mirim 2** (4º e 5º anos). Prova provavelmente na **terça, 10/11/2026**, na escola. A data e o
formato serão confirmados na pesquisa. É um projeto pessoal do Diogo, irmão de `estudo-cmb` (é a mesma
criança, que fez o CMB em 18/10) e de `obmep-mirim-3` (outra criança, que não deve ser misturada aqui).
**Não é Belo Coffee nem UCS.**

## Idioma
Sempre responder em português brasileiro.

## Ao abrir uma sessão aqui
1. Ler `progress.md` (estado atual e próximo passo) antes de responder qualquer coisa.
2. Ler `PLANO.md` (desenho aprovado e critério de "pronto").

## Quem usa o quê
- **A criança** usa `roteiro/index.html`. Há um adulto por perto, mas a página é feita para ela se virar
  sozinha (máximo de autonomia, como no CMB).
- **Diogo** prepara o material com o Claude e manda fotos das folhas e o resultado dos sábados.
- `pesquisa/` é a "cozinha" e nunca é mostrada à criança.

## Regras do material
- Linguagem de criança de 10 anos em tudo que vai para o roteiro.
- **Nada fora do que cai na prova** (ver a tabela em `pesquisa/analise-2a-fase.md`). Não inventar assunto.
- Fontes de questão, nesta ordem:
  1. **Oficiais OBMEP Mirim 2.** As provas de 2ª fase reservadas aos sábados não entram em dia de semana.
  2. **Questões inventadas**, só como variação de uma questão que ela errou ou como degrau-ponte. Recebem a
     etiqueta ✏️ TREINO e são resolvidas às cegas por um 2º agente; se as respostas divergirem, a questão é descartada.
  Não usar sites de "simulado" de terceiros.
- Toda questão oficial traz a resposta do **gabarito oficial** e uma resolução no padrão do CMB:
  🎯 o que ela quer → balões numerados → ✅ resposta → 💡 atalho → ⚠️ escorregão.
- **Cada dia se explica sozinho.** A página mostra só a semana atual, então nunca mandar "lembrar" algo de outro dia
  sem trazer o resumo dentro do próprio dia.
- Troca de unidade → **tabela das unidades** (`div.escada` no código). Na página, diz-se "tabela das unidades" e
  "casa", nunca "escada" nem "degrau". "Degrau" fica reservado para os níveis de dificuldade.
- Todo vídeo e todo link é conferido antes de entrar (abre, assunto certo, duração anotada).
- Toda tarefa tem "como sei que terminei".
- **Nenhum dado pessoal da criança em lugar nenhum**: nem nome, apelido, escola, turma, foto ou letra.
  Isso vale para arquivos, memória, commits e prompts de agente. Referir-se a ela como "a criança".
  Fotos das folhas são só analisadas; as imagens renderizadas são apagadas do scratchpad ao fim.

## Freios (risco baixo: não gasta dinheiro, não fala com terceiros)
- Toda resposta é conferida contra o gabarito oficial.
- O roteiro é revisado por um agente separado antes de ir para a criança.
- Prompt de subagente termina com "Responda em português brasileiro".

## Git e publicação
Repo **público** `diogobr23/obmep-mirim-5` + GitHub Pages, com `noindex` e `robots.txt`.
O localStorage usa o prefixo `mirim2:`, porque a origem github.io é a mesma do `mirim1:` e do CMB.
⚠️ Por ser público: **nenhum dado da criança** no repo.
