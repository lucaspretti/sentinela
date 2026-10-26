# Sentinela: plano do produto (v4)

Status: direção de produto definida; eficácia e integrações ainda por validar.
Atualizado em 26/10/2026. Rastreabilidade: [issue #6](https://github.com/lucaspretti/sentinela/issues/6).
Design e fontes: [`docs/design.md`](docs/design.md).

## Missão

Reduzir a disseminação de desinformação em geral. A política brasileira é um
recorte inicial de maior impacto para o operador, não a definição da missão.
Fact-checking é uma primeira intervenção; outros mecanismos poderão ser avaliados.

O nome jurídico da associação permanece pendente. Esta revisão documenta produto,
software e medição, não altera os estatutos nem resolve sua governança.

## Decisões do operador

- Operação editorial automatizada por uma orquestração de modelos conectados a
  ferramentas de consulta a fontes fidedignas. Não há aprovação humana obrigatória
  por publicação no modelo pretendido.
- A associação continua responsável pelo que o sistema publica. Não apresentar
  checagens automatizadas como se tivessem revisão humana.
- Rastreabilidade, observabilidade e dashboard fazem parte do produto desde o
  início. Uma página pública poderá futuramente mostrar resultados agregados.
- Uma identidade assumida por plataforma; pseudônimo sem pessoa inventada;
  nenhuma conta falsa, nenhum engajamento fabricado; fontes e correções públicas.

## Mudança em relação à v3

A v3 já havia abandonado o farm de contas falsas. A v4 mantém esse abandono e
substitui o plano limitado a repacotar checagens políticas em carrosséis por um
serviço de verificação automatizada baseado em evidências, com diferentes canais.
O carrossel continua como formato possível, não como único produto. A sequência
antiga de fases de distribuição não é uma decisão atual de prioridade.

## Hipóteses de produto

1. **Checagem sob demanda no WhatsApp:** receber texto, link, áudio ou vídeo e
   responder sobre alegações específicas, com evidências e referências.
2. **Resposta em grupos quando chamado:** bot claramente identificado, convidado
   e autorizado pelo grupo. Viabilidade em interfaces oficiais ainda não verificada.
3. **Checagem de vídeo por timestamp:** extrair alegações preservando o contexto,
   vincular cada uma ao trecho e produzir resposta com fontes. Publicação automática
   como comentário depende das permissões e limites oficiais da plataforma.
4. **Conteúdo próprio:** página de checagem, carrossel ou resposta curta, a partir
   do mesmo núcleo de evidências.

Nada disso autoriza entrar em grupos, publicar comentários ou executar um piloto
público nesta etapa de documentação.

## Núcleo compartilhado proposto

Material recebido → extração de alegações → consulta às fontes → avaliação das
evidências → decisão de responder ou abster-se → resposta rastreável → correção.

Modelos são instrumentos de análise, não fontes primárias. Concordância entre
modelos não demonstra veracidade. Cada conclusão precisa estar sustentada por
fontes que realmente apoiem a alegação, considerando data, escopo e contexto.
Material recebido e páginas recuperadas são dados não confiáveis, não instruções
para o sistema. Os controles de execução das ferramentas precisam de validação
própria antes da implementação.

## Eficácia: hipótese, não promessa

A literatura consultada não demonstra que esta combinação de orquestração,
respostas no WhatsApp e comentários por timestamp reduza a disseminação.

O experimento de arXiv:2308.10800 não encontrou melhora significativa geral no
discernimento de manchetes ou no discernimento de intenção de compartilhamento
com as checagens de ChatGPT. Encontrou também efeitos adversos em condições
específicas. Isso contraria a suposição de que adicionar um verificador automático
seja, por si só, benéfico. O estudo não testa o sistema proposto do Sentinela.

A revisão DOI 10.3389/fpsyt.2022.974782 organiza intervenções e sua viabilidade;
não fornece uma estimativa causal única para nosso produto. Consultar o quadro
de fontes e limites em `docs/design.md` antes de fazer alegações de eficácia.

## Medição desde o primeiro piloto

| Camada | Exemplos | O que não prova |
|---|---|---|
| Atividade | Solicitações, alegações distintas, checagens concluídas, posts publicados | Redução de desinformação |
| Qualidade | Correção contra referência externa, suporte das citações, erros em fatos verdadeiros, abstenções | Mudança no comportamento do público |
| Operação | Latência por etapa, custo, falhas de ferramentas, disponibilidade, falhas de entrega | Eficácia social |
| Impacto | Discernimento e comportamento de compartilhamento comparados a controle | Efeito fora da população e do canal estudados |

- Cada execução terá identificadores de solicitação, alegação, checagem e entrega.
- Tentativas, respostas geradas e publicações confirmadas são contagens diferentes.
- Cada taxa precisa de período, numerador, denominador e origem do dado.
- Intenção de compartilhar não será apresentada como compartilhamento real.
- Alcance e compartilhamentos do Sentinela não serão apresentados como circulação
  de desinformação evitada.
- Se um canal não fornecer determinada medida, registrar como não observada,
  não como zero. Não pressupor acesso a encaminhamentos de WhatsApp.
- Dashboard público: agregados, metodologia, período, limitações e correções;
  nunca mensagens privadas, participantes de grupos ou traces brutos.

## Plano de validação

1. Fechar domínio inicial, contrato de resposta e limites das ferramentas.
2. Construir corpus externo de referência com alegações verdadeiras, falsas,
   enganosas e casos sem evidência suficiente. Separar avaliação e desenvolvimento.
3. Medir o núcleo offline, incluindo falhas de transcrição e de suporte das fontes.
4. Instrumentar junto com a funcionalidade e verificar impacto da própria coleta
   sobre latência e custo; não acumular trackers sobrepostos.
5. Antes de piloto público, definir hipóteses, amostra, período, medida principal,
   critérios de interrupção e tratamento de dados. Não fixar números sem evidência.
6. Comparar intervenções num teste consentido e controlado. Se houver grupos,
   considerar contaminação entre participantes ao escolher a unidade de comparação.
7. Só declarar redução quando houver evidência compatível com essa afirmação.

## Pendências

- [ ] Escolher o primeiro produto a implementar; ordem ainda não aprovada.
- [ ] Validar APIs oficiais, formatos de mídia, permissões, rate limits e eventos
  realmente observáveis em cada canal.
- [ ] Definir corpus, métricas, retenção de dados e contrato de resposta.
- [ ] Avaliar contestação, correções e condições de suspensão da automação.
- [ ] Definir componentes técnicos em issues próprias antes de escrever software.
- [ ] Confirmar disponibilidade de nomes em etapa separada (issue #9).

## Referências e estado de leitura

- arXiv:2308.10800: experimento e resultados lidos; principal contraponto à promessa
  de eficácia automática.
- DOI 10.3389/fpsyt.2022.974782: trechos da revisão lidos; apoio contextual, não prova
  do fluxo proposto.
- *Site Reliability Engineering*, 2nd Edition: passagem verificada que sustenta
  instrumentação e dashboard desenvolvidos junto com as funcionalidades.
- *The Art of SEO*, 4th Edition: passagem verificada sobre custo de múltiplos
  trackers; aplicação à página pública, extrapolação prudente ao pipeline.
- *Practical Data Privacy*: passagem verificada que adverte que remover
  identificadores não basta para proteger dados compartilhados.
- arXiv:2310.13549: ingerido pelo ledger; análise detalhada pendente.
- DOI 10.1038/s41586-021-03344-2: pedido #120 do ledger de fontes; o resolvedor não
  encontrou cópia aberta. Não usado como evidência lida nesta revisão.
