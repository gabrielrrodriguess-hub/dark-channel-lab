# Video Script

Skill para transformar uma ideia (ou uma pesquisa) em um roteiro gravável, cronometrado e fácil de editar.

## Entradas

Aceita qualquer um destes, e combina: tema/ângulo, briefing, transcrição de referência, research notes de outro skill (ex.: `youtube-research`), tom de voz da persona, duração-alvo e formato (long-form, Short, Reel, roteiro de live).

## Antes de escrever: fixar 5 decisões

1. **Promessa** — o que o espectador ganha ao terminar (uma frase, concreta).
2. **Público e nível** — pra quem é, e o que ele já sabe (evite jargão não explicado).
3. **Duração alvo** — se não vier, assuma: 8–12 min para long-form, 45–60s para Short, 20–30s para Reel.
4. **Formato de entrega** — falado em primeira pessoa (mais simples), narração em off, ou apresentação com slides.
5. **Tom** — o tom de voz da persona (tom, vocabulário, gírias permitidas, o que nunca faz).

Se o tema vier sem ângulo, proponha 2–3 ângulos e escolha o melhor segundo os critérios do briefing, ou pergunte se a decisão é do usuário — essa é uma escolha genuinamente dele quando muda a peça inteira.

## Estrutura do roteiro

Toda peça tem um **gancho** que entrega a promessa antes de qualquer contexto, e um **payoff** que a cumpre. A espinha dorsal:

| Beat | Tempo (% da duração) | Função |
|---|---|---|
| Gancho | 0–5% | Pattern interrupt + promessa específica + razão para ficar |
| Contexto | 5–15% | Só o mínimo para a promessa fazer sentido |
| Stakes | 15–25% | O que dá errado / o que está em jogo |
| Conteúdo | 25–85% | 2–4 blocos, cada um com uma ideia central |
| Payoff | 85–95% | Fecha a promessa, entrega o "e agora?" |
| CTA | 95–100% | Uma ação só (assinar, comentar, ver a parte 2) |

Regras de gancho: nunca "oi gente, bem-vindos ao canal"; nunca pergunta retórica óbvia; a promessa aparece até 8 segundos. Evite lista de 10 itens — 3 a 5 itens é o padrão que retém.

## Formato de saída

Para cada beat, entregue:

```text
[0:00–0:12]  GANCHO
FALA: "Eu testei [coisa específica] por 30 dias. Resultado: [gancho em 1 frase]."
TELA: close no rosto, sem texto
NOTA: se cortar em "resultado" e ir pro teaser de 0:40, prende melhor
```

Inclua sempre:

- **Coluna de fala** — o texto a ser dito, escrito para ser lido em voz alta (frases curtas, sem parênteses gramaticais, números por extenso quando lidos).
- **Coluna de tela/B-roll** — o que aparece.
- **Coluna de nota** — marcação de direção, cortes sugeridos, ênfases.
- **Tempo de cada beat** e o total estimado no fim.

Use timestamps `mm:ss` e mantenha o total coerente com a duração alvo. Estime ~150 palavras por minuto falado (mais lento, ~130, com pausas e B-roll).

## Variações por formato

- **Short/Reel**: um gancho de 0–2s, uma ideia só, loop ou payoff final que costura o início. Roteiro de ~120–160 palavras.
- **Long-form**: os beats da tabela, com cold open antes da intro e 2–3 "pattern interrupts" ao longo (troca de plano, pergunta ao espectador, mini-payoff).
- **Roteiro com referência**: se houver transcrição de referência, extraia a estrutura dela, não o texto — e reescreva na voz da persona, sem copiar frases.

## Checklist final (verifique antes de entregar)

- A promessa aparece no gancho e é cumprida no payoff.
- Todo beat tem fala, tela e tempo.
- Nenhuma frase leva mais de ~20 palavras (apenas em "tom curto").
- CTA: uma ação só, específica.
- Nenhum número ou dado sem origem declarada no roteiro (ou com a fonte em nota).
- O roteiro cabe na duração alvo ±10%.
- A primeira frase, lida em voz alta, soa natural — reescreva se soar a texto.

## Entrega

Roteiro em markdown, na conversa, pronto para copiar. Se o usuário quiser, ofereça também a versão em tabela (colunas: Tempo | Fala | Visual | Nota) para planilha de produção, ou em JSON estruturado para um gerador de vídeo.

Não invente estatísticas, estudos ou cifras. Se um dado sustenta um argumento e você não tem a fonte, escreva `[DADO A INSERIR — fonte]` no lugar.