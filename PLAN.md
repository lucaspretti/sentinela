# Projeto de checagem política BR (v3)

## O que mudou e por quê

A v2 descrevia um farm de contas falsas coordenadas ("anti-fake-news army").
A v3 abandona esse desenho por decisão explícita.

O motivo está registrado: a literatura e as notas do cortex mostram que
comportamento inautêntico coordenado (a) é detectável pela uniformidade dos
sinais, (b) se volta contra quem o pratica quando a coordenação é descoberta,
e (c) é a mesma técnica usada pelo adversário. O método destruiria o objetivo.

O projeto agora é um veículo de checagem **assumido**, com identidade real. A
escala vem de conteúdo bom e de gente real compartilhando, não de volume de
perfis falsos.

## Objetivo

Fazer a checagem de fatos sobre política brasileira circular mais e mais rápido
entre pessoas reais, dentro das regras das plataformas e da lei.

## Princípios (não negociáveis)

1. **Identidade real.** Nada de persona falsa. O projeto tem nome, rosto e
   responsável identificável.
2. **Fonte sempre.** Todo conteúdo cita a checagem original (Comprova, Aos
   Fatos, Lupa, Estadão Verifica, UOL Confere). O projeto repacota, não inventa.
3. **Correção pública.** Errou, corrige no mesmo canal, com o mesmo alcance.
4. **Sem comportamento fabricado.** Nenhuma conta, nenhum engajamento, nenhum
   seguidor artificial. Automação só para o que você publica na sua própria
   página, via canal oficial.
5. **Transparência de origem.** O projeto diz de onde fala e quem o opera.

## Conteúdo

- **Público-alvo:** política brasileira.
- **Formato Fase 1:** carrossel de 6 a 8 slides, um claim por carrossel, pt-BR.
- **Voz:** pessoa comum explicando, não veículo jornalístico.
- **Método de checagem (Debunking Handbook):** liderar com a verdade, não repetir
  o mito no título, explicar como a pessoa foi enganada, oferecer a explicação
  alternativa.
- **Cadência:** 2 a 3 posts/dia é o teto humano; começar com 1 post/dia bem feito
  e ajustar pelo dado.
- [ ] `[?]` Ferramenta de produção dos carrosséis (template + render).

## Distribuição (a alavanca real, não o volume)

Em ordem de custo:

1. **Perfil próprio do projeto**, conteúdo orgânico.
2. **Compartilhamento por pessoas reais** que concordam com a pauta. Isso se
   conquista, não se automatiza.
3. **Checagem comunitária no WhatsApp**, onde a fake news política realmente
   circula no Brasil. O papel do projeto é dar munição pronta (card, link,
   fonte) para quem está no grupo.
4. **Impulsionamento pago** do conteúdo que funciona, dentro das regras.
- [ ] `[?]` Existe alguém no Brasil para operar isto presencialmente, ou o
  operador é você da Europa? A origem do operador precisa ser dita com clareza.

## Tecnologia (mínima de propósito)

- Gerador de carrossel a partir de template (imagem + texto + fonte).
- Agendamento de post na própria página via **API oficial do Instagram**
  (conta Business/Creator). Nada de automação de engajamento, nada de proxy,
  nada de fingerprint.
- [ ] `[?]` Stack do gerador (Python/Pillow, HTML/CSS, outro).

## Métricas do POC (30 dias)

- Alcance vindo de contas reais (impressões, contas alcançadas).
- Compartilhamentos (o sinal que mais importa).
- Crescimento orgânico de seguidores.
- Quantos cards foram reusados por gente de fora do projeto.
- Sem métrica definida o teste não prova nada.

## Base de evidência

Síntese da literatura em `research/`:
- Inoculação / prebunking protege mais que correção tardia (van der Linden,
  *Foolproof*).
- O "backfire effect" é quase mito em replicação (Wood & Porter, 2019).
- Correção funciona se bem feita (Lewandowsky, Cook et al., *Debunking
  Handbook*).
- O problema é concentrado, não difuso (Guess, Nyhan et al., *Nature*, 2023).
- Empurrão de precisão reduz compartilhamento (Pennycook et al., *Nature*, 2020).
- Comportamento inautêntico coordenado falha (Digital astroturfing, 2018;
  Oxford Internet Institute, 2019).

## Riscos

- Publicar sem fonte credível destrói a confiança do projeto.
- Tom de púlpito moralista afasta o público que precisa ouvir.
- Automação de engajamento (mesmo com boa intenção) reintroduz o problema da v2.
- Origem do operador (Europa) versus público (Brasil) pode ser lida como
  interferência se não for transparente.

## Roadmap

1. **Fase 0** — fechar as decisões `[?]`, montar a base de evidência.
2. **Fase 1** — perfil único, 30 posts, medir alcance e compartilhamento.
3. **Fase 2** — dobrar no que funcionou, cortar o que não funcionou.
4. **Fase 3** — se houver tração, recorrer a impulsionamento pago e rede de
   pessoas reais.