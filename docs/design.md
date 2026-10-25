# Sentinela — Design

Status: rascunho para revisão
Data: 2026-10-25
Issue: (a criar)

## 1. Identidade

- O Sentinela é um projeto de checagem de fatos sobre política brasileira,
  operado por Lucas Pretti sob pseudônimo.
- **Pseudônimo, não pessoa falsa.** Não há biografia inventada. Quando
  perguntado quem está por trás, o operador assume o projeto.
- **Uma identidade por plataforma** (um Instagram, um X, um canal de WhatsApp),
  todas assumidamente o mesmo projeto. Nunca várias contas fingindo ser pessoas
  diferentes.

## 2. Regras de honestidade (não negociáveis)

1. Nada de persona falsa. Anônimo sim, pessoa inventada não.
2. Uma identidade por plataforma, nunca contas múltiplas se passando por gente.
3. Nada de engajamento fabricado (likes, follows, comentários coordenados).
4. Fonte sempre. O projeto repacota checagem existente, não inventa fato.
5. Correção pública no mesmo canal e com o mesmo alcance.

## 3. Objetivo e público

- Público: brasileiro que consome política, incluindo quem ainda não tem
  posição formada. Não é converter o convertido.
- Objetivo: reduzir a circulação de desinformação política, não ganhar debate.
  O que se mede é alcance e compartilhamento, não razão.

## 4. Conteúdo

- **Formato Fase 1:** carrossel de 6 a 8 slides, um claim por carrossel, pt-BR.
- **Método (Debunking Handbook):** liderar com a verdade; não repetir o mito no
  título; explicar como a pessoa foi enganada; oferecer a explicação
  alternativa; citar a fonte.
- **Fonte:** Comprova, Aos Fatos, Lupa, Estadão Verifica, UOL Confere.
- **Voz:** pessoa comum explicando, não veículo jornalístico.
- **Cadência:** 1 post/dia para começar. Teto humano 2 a 3. Ajustar pelo dado.

## 5. Distribuição

- **Fase 1:** Instagram (motor de descoberta) + canal de WhatsApp (onde a fake
  news política circula). Custam o mesmo conteúdo, então valem juntos.
- **Fase 2:** grupo ou comunidade de WhatsApp para o lado de confiança.
- **Fase 3:** bot que responde a mensagem encaminhada com a checagem, só depois
  de existir acervo e voz.
- **Semeadura por pessoas reais** (two-step flow): o conteúdo se espalha por
  intermediários de confiança, não por broadcast frio.

## 6. Tecnologia

- **Gerador de carrossel:** template para PNG, a partir de texto e fonte.
- **Publicação:** manual no início; depois API oficial do Instagram (conta
  Business/Creator). Nada de canal não-oficial.
- **Proibido por desenho:** proxy, fingerprint, automação de engajamento,
  contas múltiplas. É o que separa o Sentinela do que ele combate.
- **Repo:** github.com/lucaspretti/sentinela.

## 7. Métricas do POC (30 dias)

- Alcance: contas alcançadas e impressões.
- Compartilhamentos: o sinal principal, é o que mede se o conteúdo viaja.
- Crescimento orgânico de seguidores.
- Cards reusados por gente de fora do projeto.
- Sobrevivência: nenhum bloqueio de conta no período.
- Tempo de resposta: intervalo entre um boato aparecer e a checagem sair.
  Chegar tarde vale como não chegar.

## 8. Não-objetivos

- Não é farm, não é swarm, não é exército de perfis.
- Não é veículo jornalístico novo: repacota checagem que já existe.
- Não monetiza no POC.

## 9. Riscos

- Tom de púlpito moralista afasta justamente quem precisa ouvir.
- Publicar sem fonte credível destrói a confiança do projeto de uma vez.
- Operador na Europa versus público no Brasil: precisa ser dito com clareza.
- Recaída na tentação de automatizar engajamento (reintroduz o problema da v2).

## 10. Próximos passos

- Gerador de carrossel (issue própria).
- Escolha do nome/handle do Instagram.
- Canal de WhatsApp com número dedicado (anonimato do operador).
- Ingestão da lista de pesquisa (`docs/research/lista-de-ingestao.md`).

## 11. Refinamentos da pesquisa (2026-10-25)

Cada item veio de uma nota do cortex e virou regra do projeto.

1. **Correção substitui, não só nega.** Todo card oferece a explicação
   alternativa, não apenas o selo de falso. (zettel-2380c5563456)
2. **Teto realista.** O alvo é reduzir a circulação, não eliminar a produção
   de mentira. (zettel-54d0119ef2d3)
3. **Marca de responsabilidade.** Data e fonte assinadas em cada card;
   identidade de quem opera declarada; seção pública "erramos" para correções.
   (zettel-42e4b315c2e9, zettel-6665643e4258)
4. **Regra de verificação no próprio card.** Ensinar como conferir, não só
   citar a fonte. (zettel-09bc6d6de5b1)
5. **Distribuição por nós de confiança, não broadcast frio.** Alinhar às
   organizações de checagem já existentes e aceitar que quem compartilha adapta
   a mensagem. (zettel-f104821f952e, zettel-3acbff87526c)
6. **O grupo peer-to-peer vale mais para confiança que o canal de mão única.**
   (zettel-5f79aff68ee5)
7. **Tempo é qualidade.** Trilha reativa para rumor em circulação, além da
   cadência editorial. (zettel-17a30c45738b, zettel-c0fd69923b62)
8. **Sem alarme de identidade.** Liderar com o fato, sem julgar quem
   acreditou; o julgamento ativa a defesa do leitor. (zettel-c23d8151b549)
9. **Nunca exagerar.** O exagero queima a credibilidade, que é o ativo do
   projeto. (zettel-8db56e296563)