# SubEquipe_02 — IA Generativa

## Descrição

Registro do **FOCO_03 — IA Generativa** da SubEquipe_02. Reúne os pontos de vista de cada integrante sobre as lições aprendidas e o uso de IA Generativa na entrega.

## Objetivo

Registrar, com senso crítico, como cada membro utilizou IA Generativa no trabalho e quais lições foram aprendidas no processo. **TODOS DEVEM PARTICIPAR.**

## Metodologia

A coleta dos pontos de vista foi individual e assíncrona. Cada integrante escreveu a própria linha na tabela da seção Conteúdo, com as lições aprendidas e a avaliação crítica do próprio uso de IA Generativa, tomando como base os históricos de versão e os commits dos relatórios de [Rich Picture](RichPicture.md), [NFR Framework](NFRFramework.md), [BPMN](BPMN.md) e [Questionário](Questionario.md). Cada inclusão está registrada no histórico de versão desta página (versões 1.1 a 1.4), o que preserva a autoria de cada depoimento.

A IA Generativa foi empregada em três frentes ao longo da entrega. Na redação das atas, um modelo transcreveu e resumiu as reuniões a partir da gravação e preencheu as tabelas de pauta, assuntos tratados e compromissos, com revisão humana posterior. No levantamento inicial de requisitos do Subgrupo 02, um modelo respondeu a consultas sobre os elementos essenciais de um RPG, e as respostas serviram de insumo para o [Rich Picture](RichPicture.md) e para a definição de escopo da [Ata 01 do Subgrupo 02](/Atas/AtaSub02_01.md); as hipóteses daí resultantes foram depois checadas pelo [Questionário](Questionario.md), com 14 respostas de jogadores. No apoio ao estudo e à organização, os integrantes usaram a IA para explicar conceitos do NFR Framework e do BPMN, localizar material de origem e padronizar a documentação no GitHub Pages. Em nenhum caso a saída foi adotada sem conferência com a literatura ou com o comportamento real do sistema.

A Tabela 1 cataloga os usos rastreáveis de IA Generativa, separando os de âmbito geral do projeto dos específicos do Subgrupo 02.

<a id="tabela-1"></a>

| Referência | Uso | Modelo | Finalidade |
|---|---|---|---|
| *Âmbito geral do projeto* | | | |
| [Ata 01](/Atas/AtaGeral01.md) e [Ata 02](/Atas/AtaGeral02.md) das reuniões gerais | Transcrição e resumo da reunião a partir da gravação e preenchimento das tabelas de pauta, pendências, assuntos tratados e compromissos | Gemini 3.1 Pro Estendido | Registrar as atas gerais com rastreabilidade ao vídeo publicado no YouTube |
| [Ata 01 do Subgrupo 01](/Atas/AtaSub01_01.md) | Redação da ata a partir da transcrição automática, na ausência de gravação | GPT-5.6-Sol | Preservar o registro da reunião de planejamento do Subgrupo 01 |
| [Experimento de recriação de Rich Pictures com IA](/Base/Relatórios/SubEquipe_01/RichPictureIA.md) | Geração de imagens de Rich Picture a partir de prompts textuais, após tentativa sem resultado na plataforma Cloudairy | ChatGPT, modelo GPT-5.6 Sol Alto | Avaliar de forma qualitativa se a IA reconstrói o conteúdo conceitual de um Rich Picture a partir de descrição textual |
| *Âmbito do Subgrupo 02* | | | |
| [Ata 01 do Subgrupo 02](/Atas/AtaSub02_01.md) | Transcrição e resumo da reunião a partir da gravação e preenchimento das tabelas da ata | Gemini 3.1 Pro Estendido | Registrar a ata do Subgrupo 02 com rastreabilidade ao vídeo |
| [Rich Picture](RichPicture.md) | Resposta à consulta "Quais elementos principais um jogo RPG deve ter? Seja conciso e preciso", usada no levantamento de requisitos não funcionais e na definição de escopo do jogo | Gemini, versão Flash 3.7 Estendido | Apoiar o entendimento inicial do domínio e a lista de elementos do artefato generalista |
| [Questionário](Questionario.md) | Hipóteses da IA sobre experiência do usuário, como mecânicas pay-to-win e influência de criadores de conteúdo, tomadas como objeto de validação | Gemini, versão Flash 3.7 Estendido | Confrontar as hipóteses da IA com dados de 14 jogadores |
| [NFR Framework](NFRFramework.md) e [BPMN](BPMN.md) | Explicação de conceitos das notações e apontamento de erros conceituais nos rascunhos dos modelos | Não especificado pelos autores | Apoiar o estudo das notações; a modelagem final foi feita e revisada pelos integrantes |

<p align="center">Tabela 1: Registro dos usos rastreáveis de IA Generativa no projeto e no Subgrupo 02. Fonte: Autores, 2026.</p>

## Conteúdo

| Nome do Membro | Lições Aprendidas | Uso da IA Generativa (senso crítico) |
|----------------|-------------------|--------------------------------------|
| João Igor Pereira da Costa | Aprofundei meus conhecimentos em **Engenharia Reversa**, recuperando fluxos da aplicação e representando-os em **BPMN**, além de modelar o **SIG de Segurança** utilizando a notação do **NFR Framework**.|A Inteligência Artificial (IA) mostrou-se uma ferramenta útil para **organizar e aprimorar ideias, revisar textos, identificar inconsistências e explorar alternativas** durante o desenvolvimento do projeto. Seu uso contribuiu para a análise e o refinamento das soluções, atuando como **apoio à equipe sem substituir a tomada de decisões**.|
| João Victor da Silva Batista de Farias |  Aprendi como funciona o processo de **Engenharia Reversa**, conseguindo recuperar fluxos da aplicação e representá-los em **BPMN**. Eu entendi melhor os conceitos de **NFR Framework** e como aplicá-lo na modelagem do **SIG**. | A IA foi utilizada como uma ferramenta de apoio para **identificar inconsistências e explorar alternativas** na lógica dos meus textos. Ela auxiliou nesta minha análise, mas não substituiu a tomada de decisões que eu fiz para concluir o trabaho. |
| Marcelo de Araújo Lopes | Compreendi a fundo o **NFR Framework**: a diferença entre goal e softgoal, a distinção entre NFR softgoal, operacionalização e claim, os tipos de contribuição (make, help, hurt, break, AND/OR) e o procedimento de avaliação por propagação de rótulos. Esse entendimento veio da leitura da literatura (CHUNG et al., 1999) com a IA atuando como apoio na explicação dos conceitos, e foi o que permitiu modelar o **SIG** da subequipe e o **BPMN do Motor de Batalha (ATB)** com a notação correta. Também aprendi a organizar a documentação do projeto no **GitHub Pages**, padronizando páginas de artefato, atas e navegação. | Usei a IA em duas frentes: **estudo** (explicar conceitos do NFR Framework e localizar material de origem, como os capítulos do livro do Chung) e **organização** (reestruturar o GitHub Pages, padronizar artefatos e revisar a documentação). Nesses usos ela **alucinou poucas vezes** e **acelerou bastante o trabalho**, transformando tarefas repetitivas de padronização em minutos. Ainda assim, os erros que apareceram mostraram que a revisão é obrigatória: em um dos casos a IA diagnosticou incorretamente a causa de uma imagem quebrada no site e a "correção" quebrou uma imagem que funcionava — só o teste no servidor local revelou o problema. A conclusão é que a IA é confiável como apoio ao estudo e à organização, mas **toda saída precisa ser verificada contra a literatura ou contra o comportamento real do sistema**, e a decisão de modelagem continua sendo do autor. |
| Marcos Vinícius Gündel da Silva | Eu consegui uma compreensão maior plano de ensino da disciplina. Ela me ajudou a aprender como separar tarefas efetivamente dentro do grupo. Deu sugestões sobre quais tarefas deviam estar contidas no BPMN, o que me ajudou a compreender melhor os objetos disponíveis para modelar o sistema de interesse. Também ajudou na modelagem do SIG apontando erros conceituais, aprofundando meu conhecimento sobre a notação NFR e objetivo dela. | A IA ajudou na divisão de tarefas dentro do grupo em um produto desconhecido, nesse caso o *Final Fantasy VI*. Ela também é útil para gerar novas ideias e oferecer pontos de vista alternativos. No entanto, é necessário ser bem específico no *prompt* e ter um conhecimento mínimo sobre o conteúdo gerado por ela, pois frequentemente ela toma decisões implícitas (principalmente quando o *prompt* é muito vago). Em conversas muito longas, ela se esquece de instruções passadas e até o contexto inteiro, aumentando a chance de alucinações. Além disso, sempre há uma desconfiança por minha parte de que a IA alucinou ou não fez aquilo que eu pedi; isso gera uma necessidade de revisão constante por minha parte. Eu não consegui obter bons diagramas gerados por IA, mas ela consegue sugerir bons elementos do diagrama textualmente.<br><br> Em conclusão, a IA é excelente em tarefas pontuais e de curta duração onde o usuário tem algum nível de domínio sobre o assunto tratado, mas falha quando se trata de grandes projetos e com *prompts* ambíguos. No meu caso, onde eu tinha conhecimento prévio sobre todos os pedidos de ajuda para a IA, ela serviu como uma excelente assistente que torna horas de trabalho em minutos. Porém sempre é preciso revisar e, no caso de código testar exaustivamente. |

<p align="center">Tabela 2: Pontos de vista dos integrantes sobre o uso de IA Generativa. Fonte: Autores, 2026.</p>

## Referências

GOOGLE. **Gemini** [software]. Versões Flash 3.7 Estendido e 3.1 Pro Estendido. [S. l.]: Google LLC, 2026. Disponível em: https://gemini.google.com. Acesso em: 28 ago. 2026.

OPENAI. **ChatGPT** [software]. Modelos GPT-5.6-Sol e GPT-5.6 Sol Alto. [S. l.]: OpenAI, 2026. Disponível em: https://chat.openai.com. Acesso em: 28 ago. 2026.

## Nível de Contribuição dos Integrantes

| Nome | % de Contribuição |
|------|-------------------|
| João Igor Pereira da Costa | 25% |
| João Victor da Silva Batista de Farias | 25% |
| Marcelo de Araújo Lopes | 25% |
| Marcos Vinícius Gündel da Silva | 25% |

<p align="center">Tabela 3: Contribuição dos integrantes. Fonte: Autores, 2026.</p>

## Histórico de Versão

| Versão | Data | Descrição | Autor(es) | Revisor |
|:------:|------|:----------|:----------|:--------|
| 1.0 | 22/08/2026 | Criação da página no modelo do artefato padrão | Marcelo de Araújo Lopes | Marcos Vinícius Gündel da Silva |
| 1.1 | 27/08/2026 | Adição da contribuição da IA, pela visão do João Igor | João Igor Pereira da Costa | Marcos Vinícius Gündel da Silva |
| 1.2 | 27/08/2026 | Adição da contribuição da IA, pela visão do Marcos Vinícius | Marcos Vinícius Gündel da Silva |  |
| 1.3 | 27/08/2026 | Adição da contribuição da IA, pela visão do Marcelo de Araújo Lopes | Marcelo de Araújo Lopes | |
| 1.4 | 28/08/2026 | Adição da contribuição da IA, pela visão do João Victor | João Victor da Silva Batista de Farias | |
| 1.5 | 28/08/2026 | Preenchimento das seções Metodologia e Referências e registro dos usos rastreáveis de IA Generativa no projeto e no Subgrupo 2 | Marcos Vinícius Gündel da Silva | |

<p align="center">Tabela 4: Histórico de versão. Fonte: Autores, 2026.</p>

Ver também: [Artefato Generalista](ArtefatoGeneralista.md) · [Léxico](Lexico.md) · [Rich Picture](RichPicture.md) · [Questionário](Questionario.md) · [NFR Framework](NFRFramework.md) · [BPMN](BPMN.md)
