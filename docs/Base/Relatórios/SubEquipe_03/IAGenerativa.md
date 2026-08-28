# SubEquipe_03 — IA Generativa

## Descrição

Registro do **FOCO_03 — IA Generativa** da SubEquipe_03. Reúne os pontos de vista de cada integrante sobre as lições aprendidas e o uso de IA Generativa na entrega.

## Objetivo

Registrar, com senso crítico, como cada membro utilizou IA Generativa no trabalho e quais lições foram aprendidas no processo. **TODOS DEVEM PARTICIPAR.**

## Metodologia

A coleta dos pontos de vista partiu de um artefato visual inicial: um **mapa mental esqueleto**, produzido previamente pela subequipe, contendo apenas os tópicos-chave do conceito de jogo organizados por categoria (estilo, mecânicas, personagens, funcionalidades). A subequipe consolidou o entendimento coletivo diretamente na estrutura do mapa e, a partir dele, conduziu um brainstorming, detalhando verbalmente as regras de jogo (sistema de magia baseado em química, combate por turnos, criação de itens, tipos de área, regras de save) à medida que cada lacuna do mapa era identificada. Os pontos de vista individuais foram registrados por meio de um formulário elaborado pela SubEquipe_02.

A ferramenta utilizada em todos os usos relatados a seguir foi o **Claude**, da Anthropic, tanto pela interface do claude.ai quanto pelo Claude Code no terminal. A IA Generativa foi empregada em cinco momentos distintos ao longo da entrega, apresentados em ordem cronológica:

1. **Validação do planejamento contra os documentos da disciplina**: antes da abertura das issues, a subequipe submeteu o próprio planejamento de sprints e de organização do repositório junto com as Diretrizes de Entrega e o Plano de Ensino, pedindo uma avaliação de aderência. O objetivo era confrontar o que havia sido planejado com o que a disciplina de fato exigia, e não pedir que a IA elaborasse o planejamento.

2. **Estruturação e estilização do mapa mental**: a partir do esqueleto e da descrição textual da mecânica central do jogo, a IA propôs uma reorganização dos ramos (incluindo a criação de um ramo novo, "Sistema de magia", ausente no esqueleto original) e justificou o que poderia ser ideal com as ideias que estavam sendo empregadas durante a reunião antes de gerar a versão final.

3. **Modelagem BPMN**: cada subprocesso do jogo (loop principal, combate, criação de itens, exploração, livros colecionáveis, savepoint) foi modelado separadamente, com a IA decompondo o mapa mental em fluxos com eventos, gateways e raias de responsabilidade, além de indicar se as notações propostas pelos integrantes eram ou não aceitas na especificação. A revisão da documentação foi sempre necessária, pois a IA errava com frequência sobre o que podia ser representado no diagrama.

4. **Refinamento orientado por regras de negócio**: à medida que a equipe fornecia regras mais específicas e novas (ex.: diferenciação entre área segura/não segura, mundo aberto/não aberto, regras de save state), a IA revisou os diagramas já existentes em vez de recomeçá-los do zero, mantendo rastreabilidade entre versões.

5. **Revisão do SIG antes da publicação**: com o SIG na notação do NFR Framework e o Mapa Mental já finalizados como imagem, fora do repositório, a subequipe submeteu os dois artefatos junto com o rascunho feito no Excalidraw durante a reunião e o texto que descrevia o SIG, pedindo uma avaliação crítica antes da publicação no GitPages. O uso foi de revisão do conteúdo já produzido, não de geração do artefato.

Esse último uso foi o que produziu os achados mais relevantes para a qualidade da entrega, e por isso é detalhado aqui. A revisão apontou duas fragilidades no texto que acompanhava o SIG:

- A descrição afirmava que os cinco sub-NFRs derivavam das heurísticas de Nielsen, mas **Imersão** não é uma delas: vem da literatura específica de jogos. A subequipe reescreveu o trecho distinguindo as duas origens, o que transformou uma imprecisão conceitual em uma decisão justificada e rastreável.
- O trade-off entre **Flexibilidade** e **Estética Minimalista** estava desenhado no SIG, mas não era discutido em texto, que é justamente onde a diretriz da disciplina espera encontrar o senso crítico. A discussão foi então escrita e incorporada ao artefato.

Um padrão recorrente em todo o processo foi que, a cada entrega de diagrama, a IA sinalizava explicitamente pontos em aberto ou ambiguidades de modelagem (ex.: frequência do combate aleatório, se "sair do jogo" preserva progresso fora de savepoints), que serviam de gatilho para a próxima rodada de refinamento pela equipe, e não uma geração única e definitiva. Em nenhum dos cinco momentos o resultado da IA foi incorporado sem revisão humana, e os dois achados sobre o SIG mostram que o valor da ferramenta esteve mais em expor lacunas do que em produzir o artefato final.

<p align="center">
  <img src="Base/Relatórios/SubEquipe_03/assets/ia2.jpeg" alt="Estruturação do mapa mental pela IA" width="400">
</p>

<p align="center">Figura 1: Reorganização dos ramos do mapa mental proposta pela IA, com a criação do ramo <em>Sistema de magia</em>, ausente no esqueleto original. Fonte: Carlos Henrique Brasil de Souza, Pedro Teixeira Moriel Sanchez e Renan Pereira Reis, 2026 (captura de tela da conversa da subequipe com o Claude, da Anthropic, em claude.ai).</p>

<p align="center">
  <img src="Base/Relatórios/SubEquipe_03/assets/ia1.jpeg" alt="Modelagem BPMN pela IA" width="400">
</p>

<p align="center">Figura 2: Modelagem do fluxo de exploração do mundo em notação BPMN, gerada a partir do detalhamento das regras pela subequipe. Fonte: Carlos Henrique Brasil de Souza, Pedro Teixeira Moriel Sanchez e Renan Pereira Reis, 2026 (captura de tela da conversa da subequipe com o Claude, da Anthropic, modelo Sonnet 5, em claude.ai).</p>

## Conteúdo

| Nome do Membro | Lições Aprendidas | Uso da IA Generativa (senso crítico) |
|----------------|-------------------|--------------------------------------|
| Carlos Henrique Brasil de Souza | Compreendi melhor os conceitos de Arquitetura de Software e como os componentes do sistema se comunicam. A prática da Engenharia Reversa foi essencial para mapear a estrutura da aplicação e representar esses processos de forma clara usando diagramas BPMN. | Usei a IA para esclarecer dúvidas sobre padrões arquiteturais e para revisar a documentação. Notei que a IA ajuda muito com a teoria, mas frequentemente sugere soluções arquiteturais muito genéricas. Foi preciso adaptar e validar todas as sugestões para o contexto real do nosso projeto. |
| Pedro Teixeira Moriel Sanchez | Aprendi como as decisões de Arquitetura de Software impactam diretamente os requisitos não-funcionais da aplicação. O uso do NFR Framework e a modelagem em BPMN me ajudaram a visualizar a estrutura do sistema e como os diferentes módulos interagem entre si. | A IA serviu como apoio para formatar textos e explicar como estruturar nossos artefatos. No entanto, percebi que ela tem dificuldade em gerar a lógica estrutural e arquitetural correta. Ela é boa para apoiar a escrita, mas a modelagem da arquitetura precisa ser feita inteiramente por nós. |
| Renan Pereira Reis | Entendi a importância de documentar bem a Arquitetura de Software para manter a organização do projeto. A modelagem do SIG no NFR Framework deixou mais claro como as restrições e escolhas arquiteturais moldam o desenvolvimento e o comportamento do sistema. | Utilizei a IA para gerar propostas de templates de documentação e resumir conceitos. O senso crítico foi fundamental ao notar que a IA, às vezes, inventa ou mistura padrões arquiteturais que não faziam sentido para o nosso escopo. A revisão humana do que foi gerado foi indispensável. |

<p align="center">Tabela 1: Pontos de vista dos integrantes sobre o uso de IA Generativa. Fonte: Carlos Henrique Brasil de Souza, Pedro Teixeira Moriel Sanchez e Renan Pereira Reis, 2026.</p>

## Referências

BRAGA, Rosana T. Vaccare. *Engenharia Reversa e Reengenharia*. Material adaptado a partir do concedido pela Profa. Rosângela Penteado, disciplina SCE 186 – Engenharia de Software (DC - UFSCar).

NIELSEN, Jakob. **10 Usability Heuristics for User Interface Design**. Nielsen Norman Group, 1994. Disponível em: https://www.nngroup.com/articles/ten-usability-heuristics/. Acesso em: 26 ago. 2026.

OBJECT MANAGEMENT GROUP. *BPMN Specification - Business Process Model and Notation*. Disponível em: <https://www.bpmn.org/>. Acesso em: 27 ago. 2026.

## Nível de Contribuição dos Integrantes

| Nome | % de Contribuição |
|------|-------------------|
| Carlos Henrique Brasil de Souza | 33,3% |
| Pedro Teixeira Moriel Sanchez | 33,3% |
| Renan Pereira Reis | 33,3% |

<p align="center">Tabela 2: Contribuição dos integrantes. Fonte: Carlos Henrique Brasil de Souza, Pedro Teixeira Moriel Sanchez e Renan Pereira Reis, 2026.</p>

## Histórico de Versão

| Versão | Data | Descrição | Autor(es) | Revisor |
|:------:|------|:----------|:----------|:--------|
| 1.0 | 22/08/2026 | Criação da página no modelo do artefato padrão | Marcelo de Araújo Lopes | Marcos Vinícius Gündel da Silva |
| 1.1 | 27/08/2026 | Adição da contribuição da IA, pela visão do Carlos | Carlos Henrique Brasil de Souza, Pedro Teixeira Moriel Sanchez e Renan Pereira Reis |  |
| 1.2 | 27/08/2026 | Adição da contribuição da IA, pela visão do Pedro | Carlos Henrique Brasil de Souza, Pedro Teixeira Moriel Sanchez e Renan Pereira Reis | |
| 1.3 | 27/08/2026 | Adição da contribuição da IA, pela visão do Renan | Carlos Henrique Brasil de Souza, Pedro Teixeira Moriel Sanchez e Renan Pereira Reis |  |
| 1.4 | 28/08/2026 | Correção do caminho das imagens e do link de download (raiz do site) para renderizarem no Docsify local e no GitHub Pages | Marcos Vinícius Gündel da Silva | |
| 1.5 | 28/08/2026 | Registro da autoria conjunta da subequipe nas fontes das figuras e tabelas e no histórico de versão | Carlos Henrique Brasil de Souza, Pedro Teixeira Moriel Sanchez e Renan Pereira Reis | |
| 1.6 | 28/08/2026 | Adição das legendas e fontes das figuras do registro de uso de IA e correção da subequipe citada na descrição | Carlos Henrique Brasil de Souza, Pedro Teixeira Moriel Sanchez e Renan Pereira Reis | |
| 1.7 | 28/08/2026 | Reescrita da metodologia com os cinco usos de IA Generativa, incluindo a revisão do SIG, e remoção do link do registro externo | Carlos Henrique Brasil de Souza, Pedro Teixeira Moriel Sanchez e Renan Pereira Reis | |

<p align="center">Tabela 3: Histórico de versão. Fonte: Carlos Henrique Brasil de Souza, Pedro Teixeira Moriel Sanchez e Renan Pereira Reis, 2026.</p>

Ver também: [Artefato Generalista](ArtefatoGeneralista.md) · [Mapa Mental](MapaMental.md) · [NFR Framework](NFRFramework.md) · [BPMN](BPMN.md)