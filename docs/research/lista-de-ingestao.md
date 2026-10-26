# Lista de ingestão de pesquisa

Documento vivo. Cada obra entra com: o que é, por que importa para o plano do
Sentinela, e o que extrair dela. Toda leitura deve virar pelo menos um card ou
uma decisão no `PLAN.md`.

## Diagnóstico do acervo atual

Já no cortex (bom, mas cobrindo o inimigo): *Digital Astroturfing in Politics*,
*Global Disinformation Order 2019* (Oxford), *Architects of Networked
Disinformation* (Filipinas), *Social Bots Distort the 2016 Election*,
*Detection and Characterization of Coordinated Online Behavior*, *Content
Moderation Remedies*, transparência de plataforma, *Wanting* (Burgis), *Nexus*
(Harari), *Thinking Fast and Slow*, *Attensity!*.

Esta lista é uma demanda de leitura, não comprovação de que os estudos foram
lidos ou de que a intervenção proposta reduz disseminação. Crença, intenção de
compartilhar e compartilhamento observado são resultados diferentes.

## Estado da revisão de intervenção (26/10/2026, issue #6)

| Fonte | Ledger de fontes | Estado e limite |
|---|---|---|
| *Fact-checking information from large language models can decrease headline discernment*, arXiv:2308.10800 | #118 | Ingerido; resumo, desenho experimental, efeitos adversos e prompt lidos nas passagens 1, 10, 21 e 39. Contraponto à hipótese de benefício automático. Mede crença e intenção, não circulação real no WhatsApp. |
| *The Perils & Promises of Fact-checking with Large Language Models*, arXiv:2310.13549 | #119 | Ingerido; análise detalhada pendente. Não usar como validação já lida. |
| *Shifting attention to accuracy can reduce misinformation online*, DOI 10.1038/s41586-021-03344-2 | #120 | Metadados localizados; o resolvedor não encontrou cópia aberta. Não usado como evidência lida nesta revisão. |
| *Psychological interventions countering misinformation in social media: A scoping review*, DOI 10.3389/fpsyt.2022.974782 | #121 | Ingerido; passagem 43 lida sobre categorias e viabilidade. Não fornece estimativa causal única para o Sentinela. |

Canais consultados: cortex (interpretações e passagens), catálogo de livros com
texto armazenado e ledger `sapix sources` com busca OpenAlex. Os pedidos foram
registrados com justificativa e referência a `lucaspretti/sentinela#6` antes da
ingestão. Detalhes e posição de cada fonte em `../design.md`, seções 5 e 10.

Não foi verificado um estudo que avalie exatamente a combinação proposta de
orquestração com ferramentas, chatbot de WhatsApp e comentários por timestamp.
Uma lacuna de evidência não prova ineficácia; exige testar sem prometer o resultado.

## Prioridade 1: intervenção (o que testar)

### Foolproof: Why Misinformation Infects Our Minds and How to Build Immunity
- Autor: Sander van der Linden (2023)
- Área: inoculação / prebunking
- Por que: é a tese que muda o conteúdo de "desmentir o fato" para "vacinar
  contra a técnica". Card que ensina o truque protege contra a próxima mentira.
- Onde: livro; material aberto em inoculation.science
- Extrair: como estruturar um card que expõe a técnica da manipulação; comparar
  prebunking e debunking por resultado e contexto, sem presumir superioridade geral.

### The Debunking Handbook
- Autores: Stephan Lewandowsky, John Cook e outros (2020)
- Área: correção prática
- Por que: vira o template direto do card.
- Onde: gratuito, debunkinghandbook.org (PDF)
- Extrair: liderar com a verdade, não repetir o mito; explicar como a pessoa foi
  enganada; oferecer a explicação alternativa; o "truth sandwich".

### The Conspiracy Theory Handbook
- Autores: Lewandowsky & Cook
- Área: como falar com quem crê em conspiração
- Onde: gratuito (PDF)
- Extrair: os traços do pensamento conspiratório e respostas que não afastam.

## Prioridade 2: evidência

### The Elusive Backfire Effect
- Autores: Thomas Wood & Ethan Porter (Political Behavior, 2019)
- Área: correção funciona?
- Extrair: por que o "backfire effect" é raro em replicação, e por que corrigir
  vale a pena. Desfaz o medo de que corrigir piore.

### Fighting COVID-19 Misinformation on Social Media (accuracy nudge)
- Título completo localizado: *Fighting COVID-19 Misinformation on Social Media:
  Experimental Evidence for a Scalable Accuracy-Nudge Intervention* (2020).
- DOI localizado via OpenAlex em 26/10/2026: 10.1177/0956797620939054.
- A atribuição anterior a Nature foi retirada; não confundir esta referência com
  o paper de 2021, DOI 10.1038/s41586-021-03344-2, pedido #120 do ledger.
- Área: empurrão de precisão.
- Estado: metadados conferidos; resultados não lidos nesta revisão.
- Extrair: mecanismo, resultados medidos e limites de aplicação a canais e grupos.
  Não tratar intenção de compartilhamento como redução observada de disseminação.

### Concentração do consumo de desinformação
- Autores: Andrew Guess, Brendan Nyhan e outros (2023)
- Área: quem realmente consome
- Extrair: o problema é pequeno, denso e concentrado em poucos super
  espalhadores. Foca a ambição: reduzir amplificação de poucos, não convencer
  todo mundo.

### Correção e o continued influence effect
- Autora: Briony Swire-Thompson e colaboradores
- Área: limites da correção
- Extrair: por que corrigir tarde é fraco e por que agir cedo tem vantagem.

## Prioridade 3: Brasil e distribuição

### O mundo do avesso: verdade e política na era digital
- Autora: Letícia Cesarino (2022)
- Área: contexto brasileiro
- Extrair: como a política brasileira circula de fato; vocabulário e enquadres.

### Pesquisa sobre WhatsApp e as eleições brasileiras de 2018
- Área: canal real
- Por que: é onde a fake news política BR mora.
- Extrair: como grupos e encaminhamento funcionam; o que faz um conteúdo
  circular dentro do WhatsApp.

### Twitter and Tear Gas: The Power and Fragility of Networked Protest
- Autora: Zeynep Tufekci (2017)
- Área: movimentos em rede
- Extrair: por que rede sem organização desinfla; o que dá sustentação a uma
  causa ao longo do tempo.

### Personal Influence (two-step flow)
- Autores: Elihu Katz & Paul Lazarsfeld (1955)
- Área: difusão via líderes de opinião
- Extrair: informação se espalha por intermediários de confiança, não por
  broadcast. Base para a estratégia do canal.

## Prioridade 4: voz e credibilidade

### Influence: The Psychology of Persuasion
- Autor: Robert Cialdini
- Área: persuasão
- Extrair: os princípios de influência que tornam um apelo eficaz ou repelente.

### Age of Propaganda
- Autores: Anthony Pratkanis & Elliot Aronson
- Área: propaganda e persuasão cotidiana
- Extrair: como mensagens convencem e como se defendem delas.

### The Elements of Journalism
- Autores: Bill Kovach & Tom Rosenstiel
- Área: ofício e credibilidade
- Extrair: o que sustenta a confiança de quem checa fatos. Base do tom do
  Sentinela.

## Regra de ingestão

- Ingerir no Sapix e deixar o refinamento destilar.
- Cada obra deve produzir pelo menos um card ou uma decisão registrada no
  `PLAN.md`. Leitura que não muda nada não precisava ser lida.