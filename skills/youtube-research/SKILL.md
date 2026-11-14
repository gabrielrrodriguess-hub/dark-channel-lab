# YouTube Research

Skill para pesquisar vídeos no YouTube e transformar isso em insumo acionável (roteiro, ângulo editorial, referências).

## Princípio

Nunca invente dados do YouTube. Se não conseguiu buscar, diga explicitamente que não conseguiu e entregue o que sabe + como buscar. Dados de visualizações/desempenho só entram com fonte (URL ou título do vídeo).

## Fluxo

### 1. Definir o escopo

Antes de buscar, extraia do pedido: tema ou palavra-chave, o que a pessoa quer aprender com os vídeos (estrutura, gancho, dados de nicho, formato, monetization), público-alvo, idioma, janela de tempo (recência).

Se o tema for amplo, estreite por: ângulo (ex.: "como negociar salário"), formato (ex.: "formato lista vs. história"), faixa de canal (micro/médio/grande). Não pergunte tudo — assuma defaults razoáveis (idioma do usuário, últimos 12 meses, vídeos com tração acima da mediana do canal) e diga o que assumiu.

### 2. Buscar

Priorize, nesta ordem:

1. **Busca web com filtro de domínio**: `WebSearch` com `allowed_domains: ["youtube.com", "youtu.be"]` e termos em pt-BR e en. Ex.: `tutorial altura de planta site:youtube.com`.
2. **Busca web aberta** para achar listas, blogs de análise, threads e posts que apontem vídeos específicos (às vezes o vídeo não ranqueia na busca do YouTube).
3. **YouTube via `yt-dlp`** quando estiver disponível no ambiente — é o caminho mais confiável para metadados e legendas:
   - `yt-dlp "ytsearch10:<termo>" --flat-playlist --print "%(id)s|%(title)s|%(channel)s|%(duration)s|%(view_count)s|%(upload_date)s"`
   - Legendas: `yt-dlp "<url>" --write-auto-sub --sub-langs "pt,en" --skip-download -o "%(id)s.%(ext)s"`
   - Sem yt-dlp? Use `web_fetch` na URL do vídeo para pegar metadados que o HTML expõe (title, description, view count aproximado, upload date).
4. **Canais** via `yt-dlp "https://www.youtube.com/@canal/videos"` ou a aba Videos/Shorts do canal — útil para mapear o que um concorrente publica com regularidade.

### 3. Extrair (por vídeo)

Capture apenas o que interessa, nesta ordem de prioridade:

- **Estrutura** (mais valiosa): gancho (primeiros 15s), promessa, beats/outline, CTA, tensão/payoff.
- **Ângulo editorial**: a tese central que o vídeo prova, e o que ele deixa de fora.
- **Formato**: duração, ritmo, cortes, uso de B-roll, presença de rosto, legendas queimadas, formato de thumbnail.
- **Prova**: números citados, fontes usadas, autoridade de quem apresenta.
- **Engagement**: contagem de views, comentários relevantes (quais perguntas/dúvidas o público leva), duração média de retenção se exposta.
- **Transcrição**: sempre que disponível. Em vídeos > 15 min, resuma por timestamp (mm:ss) em blocos, em vez de despejar o texto bruto.

### 4. Sintetizar

Devolva uma leitura transversal, não uma lista de resumos. O que o usuário quer é o padrão:

- O que 3+ vídeos grandes fazem igual (as "regras" do formato).
- Onde o nicho está saturado (mesma estrutura, mesmo ângulo, mesmo tipo de thumbnail).
- Lacunas: um subângulo que quase ninguém cobre, um formato que funciona e ninguém replica, um erro recorrente que você pode inverter.
- O que é específico do vídeo (métrica pontual) versus padrão (regra).

### 5. Entregar

Formato padrão de resposta:

```markdown
## Resumo do que foi encontrado
- N vídeos analisados: [tema] (links das fontes-chave)
- Padrões que se repetem
- Lacunas / oportunidades

## Estrutura vencedora (template)
[beats em ordem, com o que funciona em cada um]

## Ângulos subexplorados
1. ...

## Dados de referência
[tabela: vídeo, canal, views, duração, gancho em uma frase]
```

## Regras

- Máximo ~8 vídeos detalhados por rodada, com outros citados só em uma linha. Volume sem leitura não serve.
- Sempre inclua links. Vídeo sem link é inútil para o usuário revisar.
- Separar fato observado ("o vídeo X tem 42s de gancho antes do contexto") de inferência ("gancho longo funcionou porque...").
- Se a busca falhar (sem rede, sem yt-dlp, sem permissão), diga o que falhou e ofereça o caminho manual: lista de links para o usuário abrir ou paste das transcrições.