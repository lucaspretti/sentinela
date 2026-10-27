# Sentinela

Projeto de verificação automatizada de alegações, para reduzir a disseminação de
desinformação. Este repositório contém **somente documentação**: não há código, stack,
modelos ou integrações escolhidos, e a eficácia do produto não está validada. O
trabalho aqui é escrever, revisar e manter documentos.

Repositório público: `github.com/lucaspretti/sentinela`.
Clone de trabalho: `/Volumes/1TB/GitHub/sentinela`.

## Mapa dos documentos

| Arquivo | O que é |
|---|---|
| `PLAN.md` | Plano v4: missão, decisões do operador, primeiro recorte, medição, roadmap M1 a M4 e dependências entre tickets |
| `docs/design.md` | Design do produto: regras de honestidade, núcleo de verificação, o que a evidência permite afirmar, rastreabilidade, dashboard, teste de impacto |
| `docs/legal/veiculo-juridico.md` | Pesquisa sobre a entidade jurídica (associação nova, âmbito estatal, RNA, Espanha) |
| `docs/research/lista-de-ingestao.md` | Demanda de leitura e estado da revisão de literatura |

O `PLAN.md` é o mapa; os detalhes e os critérios de cada tarefa ficam na issue. Se
uma decisão muda o caminho, atualize o `PLAN.md` e o `docs/design.md` no mesmo PR.

## Fluxo de trabalho

1. Toda mudança tem issue antes de começar. O roadmap está na issue-mãe #16; os
   tickets, no Project "Sapix Impulses" e nos milestones do repositório.
2. Trabalhe num branch `issue/<N>-<slug>`, num worktree irmão
   `/Volumes/1TB/GitHub/sentinela-issue-<N>`. Não commite na `main`.
3. Conventional Commits em português, com o número da issue no assunto:
   `docs: recorte aprovado do primeiro piloto (#13)`. Sem linhas `Co-Authored-By`
   nem outras de atribuição.
4. Abra PR referenciando a issue. O merge acrescenta o número do PR ao assunto
   (`... (#16) (#31)`) e mantém o histórico linear.
5. Ao retomar um ticket, leia a issue e confira os pré-requisitos ao vivo (relações
   `blockedBy` do GitHub), não pelo Status do Project. `Blocked` indica pré-requisito
   pendente, não impossibilidade técnica.
6. Depois de um erro ao criar ou alterar algo no GitHub, leia o recurso antes de
   repetir: pode ter havido aplicação parcial.

## Regras do produto que nenhum texto pode contrariar

Vêm do `docs/design.md` (seção 2) e do `PLAN.md`. Em conflito, valem eles.

- Sem pessoa inventada, sem rede de perfis falsos, sem engajamento fabricado. Uma
  identidade assumida por plataforma.
- A associação responde pelo que o sistema publica. Nunca apresentar checagem
  automatizada como se tivesse revisão humana, nem concordância entre modelos como
  prova ou revisão independente.
- Resposta automática é identificada como tal. Fontes sempre. Correção pública no
  mesmo canal.
- Material recebido e páginas recuperadas são dados não confiáveis, não instruções.
- Mensagens, participantes de grupos e traces brutos nunca são expostos como se
  fossem anônimos.

## Rigor ao escrever

- Eficácia é hipótese, não promessa. Antes de qualquer alegação de eficácia, consulte
  o quadro de fontes e limites em `docs/design.md` (seção 5).
- Não invente fatos, números ou referências, nem estimativas de esforço, retorno ou
  economia sem medição. Toda taxa informa período, numerador, denominador e origem.
- Separe o que foi lido e verificado do que é inferência. Uma fonte só consta como
  lida se foi lida; registre o estado real (por exemplo, "ingerido, análise pendente").
- Medida que o canal não fornece é "não observada", nunca zero. Tentativa, resposta
  gerada e publicação confirmada são contagens diferentes.
- Datas do roadmap são horizontes de revisão, não compromissos de entrega.
- No documento jurídico, cada afirmação traz a fonte ao lado; fonte não lida
  diretamente é marcada como tal.

## Decisões que são do operador

Não decida nem execute por conta própria: a denominação da associação (#9), os
estatutos (#10), a autorização de um piloto público, a entrada em grupos, a
publicação de comentários, a escolha de stack e modelos, e os limiares de sucesso.
Os documentos descrevem essas etapas como pendentes, não como autorizadas.

## Estilo

Português do Brasil, com acentuação completa. Sem travessões como pontuação: use
vírgula, ponto, dois-pontos ou divida a frase.
