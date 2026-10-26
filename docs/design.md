# Sentinela: design do produto

Status: direção de produto definida; desenho proposto, sem implementação ou eficácia validada.
Atualizado em 26/10/2026.
Rastreabilidade: [issue #6](https://github.com/lucaspretti/sentinela/issues/6).
Plano: [`../PLAN.md`](../PLAN.md).

## 1. Missão, identidade e escopo

Reduzir a disseminação de desinformação em geral. Política brasileira é um recorte
inicial de maior impacto para o operador, não a missão nem um limite do produto.
Fact-checking automatizado é uma primeira intervenção; outras poderão ser testadas.

Sentinela é o projeto editorial, operado por Lucas Pretti sob pseudônimo, sem
biografia inventada. Uma identidade por plataforma, claramente o mesmo projeto.
Quem quiser saber quem está por trás não deve receber uma identidade fictícia.

Esta revisão trata do produto e do software. Não altera os estatutos, não escolhe
a denominação da associação e não estabelece um órgão editorial externo.

## 2. Decisões e regras de honestidade

### Confirmadas pelo operador

- O fluxo editorial pretendido é automatizado por uma orquestração de modelos
  com ferramentas de consulta a fontes fidedignas.
- Não há revisão ou aprovação humana obrigatória por publicação nesse fluxo.
  A associação conserva responsabilidade; modelos não são sujeitos responsáveis.
- A medição faz parte do produto desde o começo, com dashboard operacional e
  futura divulgação pública de dados agregados.

### Regras preservadas

1. Nada de pessoa inventada ou rede de perfis falsos.
2. Uma identidade assumida por plataforma, sem simular pessoas diferentes.
3. Nenhum engajamento fabricado, likes, follows ou comentários coordenados para
   simular apoio. Uma resposta automática de verificação, se permitida pelo canal,
   deve ser identificada como tal, não como comentário espontâneo de uma pessoa.
4. Fontes sempre. Pode haver checagem própria fundamentada em evidências, além de
   reutilização atribuída de checagens existentes. Não inventar fatos ou referências.
5. Corrigir publicamente no mesmo canal; distinguir edição de conteúdo e nova
   distribuição da correção. Alcance equivalente é objetivo, não dado garantido.
6. Não chamar concordância entre modelos de prova ou de revisão humana independente.

## 3. Recorte inicial e hipóteses de evolução

### Primeiro recorte aprovado (26/10/2026, issue #13)

O primeiro núcleo atenderá **texto e links sobre alegações brasileiras com fontes
documentais**, sob demanda. Esse limite é do piloto, não da missão. WhatsApp é um
canal candidato, sujeito à confirmação de viabilidade em interfaces oficiais.
Vídeo, comentários públicos e participação em grupos ficam para etapas posteriores.

A aprovação deste recorte não define stack, modelos, corpus, limiares de sucesso
ou formato final de resposta, nem autoriza implantação ou publicação real.
As capacidades abaixo permanecem hipóteses de evolução, não integrações confirmadas.

### 3.1. Checagem sob demanda no WhatsApp

Receber texto, link, áudio ou vídeo. Extrair alegações e responder com conclusão,
fontes, contexto e limitações. O usuário consulta antes de compartilhar, quando
possível. Não verificar automaticamente a identidade ou todo o discurso da pessoa.

### 3.2. Bot em grupos, quando chamado

O comportamento pretendido é participar como bot identificado, mediante convite e
autorização, e responder a uma solicitação explícita. Não entrar indiscriminadamente
em grupos nem monitorar toda a conversa por padrão. Viabilidade e permissões das
interfaces oficiais do WhatsApp ainda precisam ser verificadas.

### 3.3. Vídeo e resposta por timestamp

Transcrever preservando offsets, separar alegações verificáveis de opinião e ligar
cada uma ao trecho original. Exemplo de contrato de resposta:

> 02:14: alegação X. O documento Y, referente ao período Z, informa W.
> 05:38: a evidência consultada não é suficiente para confirmar a alegação.

A produção dessa checagem e sua publicação como comentário são capacidades
separadas. Comentários automáticos dependem de API, autorização e limites de cada
plataforma; não estão confirmados nesta documentação.

### 3.4. Página e conteúdo próprio

Publicar páginas de checagem, respostas curtas e, se útil, carrosséis. Um mesmo
núcleo de evidências pode sustentar os formatos. Instagram, WhatsApp e outras
plataformas são canais possíveis, não uma ordem definitiva de implementação.

## 4. Núcleo de verificação proposto

1. **Receber:** registrar canal, formato, consentimento pertinente e identificador.
2. **Extrair:** delimitar alegações, entidades, datas, escopo e timestamps.
3. **Consultar:** localizar fontes primárias e checagens atribuídas; verificar
   procedência, atualidade, contexto e se a fonte realmente sustenta a alegação.
4. **Confrontar:** avaliar evidências favoráveis, contrárias e lacunas. Modelos não
   substituem as fontes nem podem decidir apenas por votação entre si.
5. **Decidir:** confirmado, contradito, enganoso por contexto ou inconclusivo.
   Esses estados são proposta de contrato, ainda sujeitos a avaliação offline.
6. **Responder:** citar evidências e explicar a conclusão sem julgar a pessoa.
7. **Entregar:** distinguir resposta gerada, tentativa de publicação e entrega
   confirmada. Se a confirmação não existir, não contar como publicação confirmada.
8. **Corrigir:** versionar evidências, conclusão e publicações relacionadas,
   mantendo o histórico necessário para explicar mudanças.

Uma fonte reputada não torna toda afirmação verdadeira. Não concluir ausência de
um acontecimento apenas porque uma busca não o encontrou. Datas, recortes e
fidelidade da transcrição integram a avaliação.

Conteúdo recebido e documentos recuperados são dados não confiáveis, não instruções
para a orquestração. Os controles de permissões, execução e proteção contra
instruções maliciosas nas fontes precisam de decisão e testes próprios antes de
implementação. Nenhuma stack ou composição de modelos é escolhida aqui.

## 5. O que a evidência permite afirmar

### 5.1. Principal contraponto: checagem de LLM não implica benefício ao usuário

*Fact-checking information from large language models can decrease headline
discernment*, arXiv:2308.10800, foi solicitado no ledger (#118), ingerido e consultado
em trechos exatos. Localizadores: passagens 1 (resumo), 10 (condições do experimento),
21 (efeitos adversos) e 39 (prompt de checagem).

- Experimento aleatorizado e pré-registrado sobre crença e intenção de compartilhar
  manchetes políticas, não observação de encaminhamentos reais no WhatsApp.
- As condições incluíram controle, checagens humanas e exposição obrigatória ou
  opcional a checagens de ChatGPT.
- Não houve melhora significativa geral no discernimento de veracidade ou no
  discernimento de intenção de compartilhamento com a intervenção de ChatGPT.
- Nos casos de manchetes verdadeiras incorretamente rotuladas como falsas, a crença
  caiu; em manchetes falsas com resposta incerta do modelo, a crença aumentou.
- Na condição opcional, participantes que escolheram consultar a checagem ficaram
  mais propensos a compartilhar tanto notícias verdadeiras quanto falsas. A escolha
  de consultar deve ser considerada ao interpretar essa comparação.

**Posição da fonte:** contraria a suposição de benefício automático. Não prova que
uma orquestração atual com ferramentas falhará, nem que funcionará. Justifica medir
a interação usuário-resposta, não só a acurácia do componente.

### 5.2. Revisão de intervenções: apoio contextual, não validação deste produto

*Psychological interventions countering misinformation in social media: A scoping
review*, DOI 10.3389/fpsyt.2022.974782, ledger #121. Passagem 43 lida: a revisão
classifica intervenções e aponta como viáveis avaliação de fonte, mensagem de
organização confiável, alterações de UX e rotulagem. Também assinala diferenças
entre populações e a necessidade de diversificar a pesquisa.

**Posição da fonte:** apoia estudar apresentação, confiança e contexto, em vez de
apenas emitir um selo. Viabilidade não equivale a eficácia causal. Não autoriza
extrapolar um efeito único a grupos brasileiros, vídeos ou respostas automáticas.

### 5.3. Lacunas preservadas

- *The Perils & Promises of Fact-checking with Large Language Models*,
  arXiv:2310.13549, ledger #119: ingerido, análise detalhada ainda pendente.
- *Shifting attention to accuracy can reduce misinformation online*,
  DOI 10.1038/s41586-021-03344-2, ledger #120: o resolvedor não encontrou cópia aberta;
  título e metadados não foram usados como prova de eficácia nesta revisão.
- Não foi verificado um estudo que teste exatamente o produto proposto: modelos
  com ferramentas, WhatsApp sob demanda e comentários de vídeo por timestamp.
- As obras da lista de ingestão são demandas de leitura, não evidência de que
  tenham sido lidas. Não publicar números de redução a partir dessa lista.

**Conclusão:** o produto é uma hipótese de intervenção que exige validação técnica
e comportamental. Não prometer redução da disseminação com base em automação,
fontes reputadas, número de modelos, alcance ou volume de checagens.

## 6. Rastreabilidade: o que registrar

Proposta de registros estruturados, ainda sem escolha de banco ou stack:

- `request_id`: solicitação recebida e canal, sem expor contatos privados.
- `claim_id`: alegação delimitada; duplicatas não viram automaticamente novos fatos.
- `check_id` e versão: checagem, conclusão, evidências e vínculo com alegações.
- `run_id`: execução da orquestração; modelo, versão de prompt e configuração,
  chamadas de ferramentas, tempos, custos, falhas e decisão de abstenção.
- Evidências: URL, instante de consulta, data da fonte, trecho que sustenta a
  conclusão, localização na mídia e referência preservável quando permitido.
- Entrega: destino, identificador externo, tentativas, confirmação e correções.
- Avaliação: referência externa, conjunto de teste e rótulo; não usar o consenso
  do próprio sistema como verdade de referência.

Registrar evidências e decisões reproduzíveis, não exigir exposição de raciocínio
interno privado dos modelos. Corrigir gera nova versão ligada à anterior.

## 7. Dashboard operacional desde o início

| Camada | Indicadores propostos | Leitura correta |
|---|---|---|
| Atividade | Solicitações, alegações distintas, checagens concluídas, respostas geradas, posts confirmados | Trabalho realizado |
| Qualidade | Precisão por classe contra referência externa, alegações verdadeiras rejeitadas, falsas confirmadas, suporte das citações, transcrição, abstenção e cobertura | Desempenho do sistema avaliado |
| Operação | Latência ponta a ponta e por etapa, falhas de ferramentas e entrega, disponibilidade, custo por checagem, fila | Saúde e custo do serviço |
| Correções | Solicitações recebidas, erros confirmados, versões corrigidas, tempo até correção e destinos alcançados | Capacidade de autocorreção |
| Impacto | Discernimento e comportamento de compartilhamento comparados a controle | Efeito observado, com desenho e limites declarados |

Cada indicador deve ter definição, período, numerador, denominador, origem e versão.
Separar tentativas de resultados e alegações distintas de reaproveitamentos. Taxas
por canal e formato ajudam a não esconder falhas numa média global.

Não transformar ausência de telemetria em zero. Não pressupor acesso a
encaminhamentos de WhatsApp ou identificação de quem mudou de comportamento.
Curtidas e comentários não comprovam persuasão; mais compartilhamentos do Sentinela
não comprovam menos compartilhamentos de desinformação.

## 8. Como testar redução, não apenas produção

Proposta metodológica a fechar antes de piloto público:

1. Definir domínio e população, canal, período, hipótese e resultado principal.
2. Construir avaliação offline separada do desenvolvimento, incluindo verdade,
   falsidade, contexto enganoso, evidência insuficiente e falhas de extração.
3. Usar referência externa, com fontes e critérios verificáveis. Revisão de um
   corpus de avaliação não equivale a revisão humana obrigatória por publicação.
4. Comparar controle e intervenção num teste consentido e pré-especificado.
   Seleção voluntária de quem consulta o bot não basta para inferir efeito causal.
5. Considerar aleatorização por grupo quando houver interação e contaminação entre
   participantes; unidade e desenho dependem do piloto, não estão definidos aqui.
6. Medir separadamente crença, intenção de compartilhar e ação observada. Se só
   houver intenção, nomear a medida como intenção.
7. Medir também dano: rejeição de informação verdadeira, aceitação de informação
   falsa e exposição adicional ao boato. Não publicar falsidades para montar o teste.
8. Definir amostra, critérios de interrupção, retenção e aprovação do piloto antes
   de executá-lo. Nenhum limiar numérico é fixado sem dados de referência.

Os procedimentos controlados do experimento de arXiv:2308.10800 sustentam a
separação de condições e desfechos; a adaptação a grupos e eventos reais é proposta
nossa, não resultado daquele estudo. Não declarar efeito global a partir de um
piloto restrito nem prometer acesso a métricas não confirmadas pela plataforma.

## 9. Página pública de resultados

Hipótese futura de transparência, não dashboard já existente:

- Total de checagens concluídas, alegações distintas e posts confirmados, por período.
- Distribuição de conclusões, abstenções e correções, com denominadores.
- Metodologia, grau de automação e limites de cada medida.
- Indicadores de eficácia somente quando estudados, com população, método,
  comparação, incerteza e resultados adversos.
- Não usar frases como "N fake news evitadas" ou "N pessoas convencidas" sem
  desenho e dados capazes de sustentá-las.
- Não publicar mensagens privadas, contatos, participantes de grupos ou traces
  brutos. Agregações pequenas também precisam de avaliação de privacidade.

Antes de coleta, definir finalidade, base aplicável, dados mínimos, acesso, retenção
e exclusão. Remover nomes ou fazer hash de telefones não torna todo o conteúdo
anônimo. A página pública deve derivar de indicadores definidos, não de trackers
adicionais em cada visualização.

## 10. Fontes das decisões de medição e dados

| Fonte e localizador lido | Decisão que sustenta | Limite ou contraponto |
|---|---|---|
| *Site Reliability Engineering*, 2nd Edition, capítulo "The Greenfield Design: Engineering Reliability from Day Zero", âncora "SLIs are not an afterthought. Monitoring and observability hooks are built into"; zettel-124783cd491a, passagem conferida | Instrumentação e dashboards junto com as funcionalidades | Trata de confiabilidade operacional, não prova impacto contra desinformação |
| *The Art of SEO*, 4th Edition, "Optimizing Web Pages for Performance", âncora "The effect of having one such program running is not"; zettel-042dce2c05d8, passagem conferida | Evitar trackers sobrepostos; medir o custo da coleta | Fonte sobre trackers em páginas web; aplicação ao pipeline é extrapolação, não medição de overhead do Sentinela |
| *Practical Data Privacy*, passagem 981, âncora "Dropping identifiers to anonymize data is not a real approach" | Não expor logs privados como supostamente anônimos | Não define sozinha nossa base legal, prazo de retenção ou mecanismo de anonimização |
| arXiv:2308.10800, passagens 1, 10, 21 e 39 | Avaliar usuário e resposta, controle, intenção versus ação, erros em conteúdo verdadeiro | Contraponto à promessa de eficácia automática; não avalia esta implementação |
| DOI 10.3389/fpsyt.2022.974782, passagem 43 | Considerar fonte, apresentação, confiança e diferenças de população | Revisão de escopo e viabilidade, não estimativa única de efeito |

Trechos exatos foram consultados pelo cortex. Demandas adicionais constam do
ledger de fontes #118 a #121 e da issue #6. Um status de ingestão não significa
que todos os resultados do paper tenham sido revisados.

## 11. Refinamentos anteriores preservados (2026-10-25)

Estes itens vieram da rodada anterior de pesquisa; não são novos resultados desta
revisão. As referências permanecem para rastrear sua origem:

1. Correção oferece explicação alternativa, não apenas negação (zettel-2380c5563456).
2. Reduzir circulação é o alvo, não prometer eliminar mentiras (zettel-54d0119ef2d3).
3. Data, fonte e origem declaradas; correções públicas (zettel-42e4b315c2e9,
   zettel-6665643e4258).
4. Ensinar como conferir, não só citar (zettel-09bc6d6de5b1).
5. Distribuição por nós de confiança, não broadcast frio (zettel-f104821f952e,
   zettel-3acbff87526c).
6. Grupos peer-to-peer como hipótese de confiança, não garantia (zettel-5f79aff68ee5).
7. Tempo é qualidade; resposta a rumores em circulação (zettel-17a30c45738b,
   zettel-c0fd69923b62).
8. Liderar com o fato, sem julgar quem acreditou (zettel-c23d8151b549).
9. Não exagerar conclusões ou resultados (zettel-8db56e296563).

## 12. Próximos passos e limites

- Primeiro caso de uso aprovado: texto e links sobre alegações brasileiras com
  fontes documentais. Próximo: especificar contrato de resposta e corpus de avaliação.
- Verificar interfaces oficiais e medidas observáveis por canal.
- Abrir issues próprias para núcleo, ferramentas, corpus, telemetria, dashboard e
  avaliação; esta issue registra direção e evidência, não implementa os componentes.
- Definir política de correções, reclamações e suspensão da automação, sem atribuir
  a modelos a responsabilidade jurídica da associação.
- Continuar a revisão dos papers, incluindo o contraponto sobre efeitos adversos.
- Nome jurídico (issue #9) e estatutos (issue #10) seguem em trilhas separadas.

Não-objetivos desta revisão: farm de contas, engajamento simulado, postagem real,
entrada em grupos, deploy, escolha de stack, limiares de sucesso sem referência ou
alteração dos estatutos.
