# Trend Scout

Skill para encontrar temas com tração ascendente e convertê-los em pautas concretas, antes que o nicho sature.

## Princípio central: momento > volume

Um tema com 5 milhões de buscas anuais e pico há dois anos vale menos que um tema com 80 mil buscas que dobrou nos últimos 30 dias. O scout não busca o que é popular — busca o que está **subindo agora** e ainda não está saturado.

## Fluxo

### 1. Enquadrar o nicho

Defina (ou assuma): o nicho/categoria, o público, o idioma e o geography de interesse, o canal (para saber o que já foi coberto), e o horizonte (temporada, 30/60/90 dias). Sem nicho, o radar é inútil — se o usuário não disser, assuma pelo contexto da conversa ou pelo nicho do canal e declare a suposição.

### 2. Coletar sinais (em paralelo, sempre mais de uma fonte)

Sinais fortes de subida:

- **YouTube**: `yt-dlp "ytsearch20:<termo>" --flat-playlist --print "%(id)s|%(title)s|%(view_count)s|%(upload_date)s"` — vídeos com upload recente e views desproporcionais ao canal são sinal forte de tendência. Compare a velocidade de views de vídeos novos do tema contra a média do canal.
- **Busca web**: `WebSearch` por News / recência. Termos como "novo", "2026", "tendência", "explodiu", "em alta" em pt-BR/en.
- **Google Trends**: via `web_fetch` em `trends.google.com/trends/explore?q=<termo>&hl=pt-BR` — leia o interest/tempo real, ou use a aba "Trending" por país quando disponível.
- **Reddit**: subreddits do nicho, ordenados por "Top — Este mês" (`reddit.com/r/<sub>/top/?t=month`). É onde a tendência aparece 2–4 semanas antes.
- **Twitter/X, TikTok Creative Center, Hacker News, forums**: sinal de conversa, menos de busca — mas indica o que está sendo compartilhado agora.
- **Notícias e lançamentos**: `WebSearch` com filtro de domínio para veículos do setor e para a fonte primária (changelog, release notes, preprint, anúncio oficial). Uma tendência quase sempre tem um gatilho datável.

Sinais fracos (não usar como prova): post isolado sem data, SEO blogspam de 2023, volume alto sem variação temporal.

### 3. Filtrar o ruído

Descarta qualquer tema que:

- Já tenha o pico há mais de ~3 meses e esteja em queda ou estável há muito tempo.
- Tenha a discussão dominada por um único evento datado e já encerrado.
- Seja genérico demais ("marketing", "produtividade") — sem gancho de urgência.
- Não tenha nenhum vídeo recente com tração no YouTube (sinal de que o formato não respira na plataforma).

### 4. Pontuar

Dê a cada tema survivors quatro notas de 1 a 5, com justificativa curta:

| Critério | Pergunta |
|---|---|
| Momentum | A busca/atenção subiu nas últimas 4 semanas? |
| Saturação | Quantos vídeos recentes e bons já existem sobre isso? (5 = saturado) |
| Adequação ao canal | Dá para fazer um vídeo que seja sobre *esse* canal? |
| Durabilidade | Continua interessante em 30 dias, ou morre na semana? |

**Score = (Momentum + Durabilidade + Adequação) − Saturação.** Use a saturação como redutora, não como aditiva. Classifique: ≥9 fazer agora; 6–8 preparar (roteiro pronto, publicar em 1–2 semanas); ≤5 descartar ou parkar.

### 5. Entregar como pauta, não como trend

O entregável de um scout é um **ângulo de entrada**, não uma palavra-chave. Um tema vira pauta quando tem: o fato novo (datado, verificável), a tensão (por que isso importa agora), a promessa (o que o espectador sai sabendo), e o formato (como se prova: análise, teste, tutorial, comparação).

## Formato de saída

```markdown
## Radar de tendências — [nicho] | [data]
Fontes consultadas: YouTube, Reddit, web, Trends

### FAZER AGORA
1. [Tema] — Score 9/10
   Gatilho: [fato datado + link]
   Por que agora: [tensão]
   Ângulo: [promessa em 1 frase]
   Formato sugerido: [tipo de vídeo]
   Janela: ~2 semanas antes de saturar
   Risco: [o que pode dar errado / quem pode copiar]

### PREPARAR
2. ...

### DESCARTADO (e por quê)
- [Tema] — sem momentum, pico em [mês/ano]
```

## Regras

- Sempre com link e data. Tendência sem data é opinião.
- Cite 2+ fontes independentes por tema no topo do radar. Se o tema só aparece em uma fonte, marque como hipótese.
- Converta sazonalidade em agenda, não em notícia: "finanças" não é tendência, "declaração de IR 2026 com novas deduções" é.
- Se a busca falhar, diga o que falhou e entregue os temas com base no que foi possível coletar, marcando o nível de confiança de cada um (alto/médio/baixo).
- Ofereça no final: "quer o roteiro do #1?" — o encadeamento natural com `video-script`.
- Nunca invente volume de busca, custo de anúncio ou métrica de engagement. Se não tem o número, qualifique ("poucos vídeos recentes com tração") ou marque `[VALIDAR]`.