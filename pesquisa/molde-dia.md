# Molde de um dia (para quem escreve os cards)

Para quem é: uma criança de 10 anos (5º ano) que estuda sozinha, com um adulto por perto, para a 2ª fase da Olimpíada
Mirim 2. A prova é em 10/11/2026: 15 questões A–E, 1h30. O dia tem de 30 a 40 minutos.

## Como ela aprende (vindo do CMB)
- Ela pensa a conta certo, mas tropeça na anotação, perde de vista o que a questão pede e esquece de conferir.
- O que funciona: escrever no canto o que a questão quer, uma conta por linha, testar alternativa por alternativa,
  resolução em balões, "refaz agora".
- Na Mirim, a dificuldade é ler e organizar, não fazer conta. As armadilhas são "NÃO", "com certeza",
  "o menor/maior possível" e o dado que só aparece na figura.

## Regras de texto
- Linguagem de 10 anos, frases curtas e tom calmo. Nada de "fácil": errar faz parte.
- **Cada dia se explica sozinho.** Não mandar "lembrar do dia X" sem repetir o resumo.
- Nunca usar "escada" nem "degrau" para a tabela das unidades. "Degrau" pode ser usado para nível de dificuldade.
- Questão oficial: a página não copia a figura. Ela manda abrir o PDF na página certa:
  `<a href="../provas/AAAA-Nfase-prova.pdf#page=P" target="_blank">prova AAAA, Nª fase, página P</a>`, com o **número da questão**.
- Gabarito **somente** da solução oficial (`provas/AAAA-Nfase-solucao.pdf`). A resolução usa a ideia da solução
  oficial, reescrita para criança.
- Sem LaTeX: usar ×, ÷, − e frações como 1/2 em texto.
- Nenhum dado pessoal da criança.

## HTML (copiar exatamente estas classes)
```html
<section class="dia" data-dia="D1" data-data="2026-10-20">
  <h2>Dia 1 — Título curto <span class="tag">Tema</span></h2>
  <p class="quando">terça, 20/10 · ⏱ 30 a 40 min</p>

  <div class="passo"><input type="checkbox" id="d1c"><label for="d1c">🃏 <b>Cartinhas</b> (3 min): abre as <a href="#cartas">🃏 Cartinhas</a> lá em cima, faz a rodada e volta pra cá.</label></div>

  <div class="passo"><input type="checkbox" id="d1i"><div class="corpo"><label for="d1i">🧠 <b>A ideia de hoje</b> (5 a 8 min): …</label>
    <div class="check"><ol style="margin:6px 0 0 20px;padding:0"><li>…</li></ol></div>
    <details class="res" open><summary>👀 Olha eu pensando em voz alta</summary> … (exemplo resolvido, inventado e simples, com balões passo-r) </details>
  </div></div>

  <div class="passo"><input type="checkbox" id="d1q1"><div class="corpo"><label for="d1q1">✏️ <b>1ª questão</b> (5 min) — abre a <a href="../provas/2022-2fase-prova.pdf#page=2" target="_blank">prova 2022, 2ª fase, página 2</a> e faz a <b>questão 7</b>.</label>
    <details><summary>💡 Dica (só se travar)</summary>…uma dica que não entrega a resposta…</details>
    <details class="res"><summary>Resolução (só depois de tentar!)</summary>
      <div class="quer">🎯 O que ela quer: …</div>
      <div class="passo-r"><span class="n">1</span><div>…</div></div>
      <div class="passo-r"><span class="n">2</span><div>…</div></div>
      <div class="resp">✅ Resposta: letra D</div>
      <div class="atalho">💡 <b>Atalho de prova:</b> <em>…</em></div>
      <div class="esc">⚠️ <b>Escorregão comum:</b> <em>…</em></div>
    </details>
  </div></div>
  <!-- As primeiras questões têm a dica 💡; as últimas são 💪 "sem ajuda" (sem o details da dica, label começando com 💪). -->

  <div class="passo"><input type="checkbox" id="d1e"><label for="d1e">⭐ <b>Marca no caderno</b> a questão que achou mais difícil e por quê (1 linha). Errou alguma? Anota o número e conta pro Diogo.</label></div>

  <div class="dica"><b>Dica do dia 1</b>…uma frase…</div>
  <p class="prog" id="prog1"></p>
</section>
```
- Os ids de checkbox seguem o prefixo do dia (`d1…`, `d2…`) e são únicos.
- `<p class="prog" id="progN">` é obrigatório.
- Some os minutos: o dia todo deve caber em 30 a 40 min.
