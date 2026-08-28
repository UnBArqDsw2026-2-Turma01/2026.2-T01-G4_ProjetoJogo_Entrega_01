# SubEquipe_03 — IA Generativa

## Descrição

Registro do **FOCO_03 — IA Generativa** da SubEquipe_03. Reúne os pontos de vista de cada integrante sobre as lições aprendidas e o uso de IA Generativa na entrega.

## Objetivo

Registrar, com senso crítico, como cada membro utilizou IA Generativa no trabalho e quais lições foram aprendidas no processo. **TODOS DEVEM PARTICIPAR.**

## Metodologia

A entrega mínima deste foco são os pontos de vista de cada integrante sobre as lições aprendidas e o uso de IA Generativa. Para produzi-la, a subequipe separou dois procedimentos que respondem a perguntas diferentes: **como cada integrante avalia** a ferramenta, e **onde a ferramenta de fato entrou** na elaboração dos artefatos. O primeiro depende de relato individual; o segundo, de evidência verificável.

Os pontos de vista foram coletados por meio de um formulário elaborado pela SubEquipe_02 e respondido individualmente por cada integrante, preservando a avaliação de cada um em vez de convergir para um texto único da subequipe. As respostas estão transcritas na Tabela 1, e a inclusão de cada uma consta no histórico de versão desta página, o que mantém o elo entre o ponto de vista e seu autor.

O levantamento dos usos foi retrospectivo, a partir da revisão das conversas mantidas com a ferramenta durante a entrega e dos artefatos produzidos em cada etapa. Cada uso foi classificado pelo papel que a IA desempenhou, separando os casos em que ela apoiou apenas a **forma** (legibilidade e redação) daqueles em que interferiu no **conteúdo** (proposta de estrutura e revisão crítica de artefato pronto). Essa separação é o que permite afirmar, artefato por artefato, o que foi decidido pela subequipe e o que veio da ferramenta.

A ferramenta utilizada em todos os usos relatados a seguir foi o **Claude**, da Anthropic, tanto pela interface do claude.ai quanto pelo Claude Code no terminal. A IA Generativa foi empregada em cinco momentos distintos ao longo da entrega, apresentados em ordem cronológica:

1. **Validação do planejamento contra os documentos da disciplina**: antes da abertura das issues, a subequipe submeteu o próprio planejamento de sprints e de organização do repositório junto com as Diretrizes de Entrega e o Plano de Ensino, pedindo uma avaliação de aderência. O objetivo era confrontar o que havia sido planejado com o que a disciplina de fato exigia, e não pedir que a IA elaborasse o planejamento.

2. **Refinamento visual do mapa mental**: a IA foi utilizada para reproduzir o rascunho construído pela subequipe no Excalidraw em uma diagramação mais legível. A estrutura e os nós definidos na reunião foram preservados integralmente, sem acréscimo, remoção ou renomeação de conceitos, conforme registrado na metodologia do [Mapa Mental](MapaMental.md). Nessa mesma interação a ferramenta propôs, por conta própria, uma reestruturação dos ramos, que não foi acatada e é analisada adiante.

3. **Modelagem BPMN**: cada subprocesso do jogo (loop principal, combate, criação de itens, exploração, livros colecionáveis, savepoint) foi modelado separadamente, com a IA decompondo o mapa mental em fluxos com eventos, gateways e raias de responsabilidade, além de indicar se as notações propostas pelos integrantes eram ou não aceitas na especificação. A revisão da documentação foi sempre necessária, pois a IA errava com frequência sobre o que podia ser representado no diagrama.

4. **Refinamento orientado por regras de negócio**: à medida que a equipe fornecia regras mais específicas e novas (ex.: diferenciação entre área segura/não segura, mundo aberto/não aberto, regras de save state), a IA revisou os diagramas já existentes em vez de recomeçá-los do zero, mantendo rastreabilidade entre versões.

5. **Revisão do SIG antes da publicação**: com o SIG na notação do NFR Framework e o Mapa Mental já finalizados como imagem, fora do repositório, a subequipe submeteu os dois artefatos junto com o rascunho feito no Excalidraw durante a reunião e o texto que descrevia o SIG, pedindo uma avaliação crítica antes da publicação no GitPages. O uso foi de revisão do conteúdo já produzido, não de geração do artefato.

Dois episódios do processo ilustram o julgamento que a subequipe precisou exercer sobre o que a ferramenta devolvia.

**A reestruturação do mapa mental que não foi acatada.** Solicitado apenas o refinamento visual do rascunho, a IA foi além do pedido e devolveu um reagrupamento do conceito do jogo em seis blocos, criando agrupamentos como "Sistema de magia" e "Progressão" e propondo uma lógica própria de encadeamento entre eles (Figura 1). A subequipe avaliou a proposta e não a incorporou: o artefato generalista preservou os quatro ramos definidos coletivamente em reunião, como registra a metodologia do [Mapa Mental](MapaMental.md) e mostra a versão ali publicada. O episódio expõe um risco concreto do uso da ferramenta em modelagem, que é reestruturar um artefato já estabilizado quando o pedido era apenas de apoio à forma.

**Os dois achados sobre o SIG.** A revisão anterior à publicação apontou duas fragilidades no texto que acompanhava o SIG:

- A descrição afirmava que os cinco sub-NFRs derivavam das heurísticas de Nielsen, mas **Imersão** não é uma delas: vem da literatura específica de jogos. A subequipe reescreveu o trecho distinguindo as duas origens, o que transformou uma imprecisão conceitual em uma decisão justificada e rastreável.
- O trade-off entre **Flexibilidade** e **Estética Minimalista** estava desenhado no SIG, mas não era discutido em texto, que é justamente onde a diretriz da disciplina espera encontrar o senso crítico. A discussão foi então escrita e incorporada ao artefato.

Um padrão recorrente em todo o processo foi que, a cada entrega de diagrama, a IA sinalizava explicitamente pontos em aberto ou ambiguidades de modelagem (ex.: frequência do combate aleatório, se "sair do jogo" preserva progresso fora de savepoints), que serviam de gatilho para a próxima rodada de refinamento pela equipe, e não uma geração única e definitiva. Em nenhum dos cinco momentos o resultado da IA foi incorporado sem revisão humana, e os episódios acima mostram que o valor da ferramenta esteve mais em expor lacunas e em provocar decisões explícitas do que em produzir os artefatos finais.

<p align="center">
  <img src="Base/Relatórios/SubEquipe_03/assets/ia2.jpeg" alt="Reagrupamento conceitual proposto pela IA e não acatado pela subequipe" width="400">
</p>

<p align="center">Figura 1: Reagrupamento conceitual do jogo devolvido pela IA, com a criação de agrupamentos como <em>Sistema de magia</em> e <em>Progressão</em>. A proposta não foi acatada: o Mapa Mental preservou os quatro ramos definidos pela subequipe em reunião. Fonte: Carlos Henrique Brasil de Souza, Pedro Teixeira Moriel Sanchez e Renan Pereira Reis, 2026 (captura de tela de conversa da subequipe com o Claude, da Anthropic, em claude.ai).</p>

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

### Rastreabilidade e Elos com Outros Artefatos

Cada uso relatado tem contrapartida verificável em um artefato desta entrega, o que permite aferir o alcance real da ferramenta:

- **[Mapa Mental](MapaMental.md)** — a IA atuou no refinamento visual do rascunho do Excalidraw. A reestruturação que propôs por conta própria (Figura 1) não foi acatada, e o artefato publicado preserva os quatro ramos definidos em reunião.
- **[NFR Framework](NFRFramework.md)** — a revisão anterior à publicação originou a distinção entre as heurísticas de Nielsen e a literatura de jogos na origem dos sub-NFRs, e a discussão textual do trade-off entre Flexibilidade e Estética Minimalista.
- **[BPMN](BPMN.md)** — a decomposição em subprocessos e a verificação da notação apoiaram a modelagem dos fluxos, sempre com revisão da subequipe (Figura 2).

As reuniões que precederam e orientaram esses usos estão registradas nas atas [01](/Atas/AtaSub03_01.md), [02](/Atas/AtaSub03_02.md), [03](/Atas/AtaSub03_03.md), [04](/Atas/AtaSub03_04.md) e [05](/Atas/AtaSub03_05.md) da subequipe.

## Referências

BRAGA, Rosana T. Vaccare. *Engenharia Reversa e Reengenharia*. Material adaptado a partir do concedido pela Profa. Rosângela Penteado, disciplina SCE 186 – Engenharia de Software (DC - UFSCar).

NIELSEN, Jakob. **10 Usability Heuristics for User Interface Design**. Nielsen Norman Group, 1994. Disponível em: https://www.nngroup.com/articles/ten-usability-heuristics/. Acesso em: 26 ago. 2026.

OBJECT MANAGEMENT GROUP. *BPMN Specification - Business Process Model and Notation*. Disponível em: <https://www.bpmn.org/>. Acesso em: 27 ago. 2026.

SERRANO, Milene. **Organização do Projeto & Diretrizes de Entrega**. Universidade de Brasília, FGA, 2026.

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
| 1.8 | 28/08/2026 | Correção do relato sobre o mapa mental, que atribuía à IA uma reorganização de ramos não acatada pela subequipe, em contradição com a metodologia do Mapa Mental | Carlos Henrique Brasil de Souza, Pedro Teixeira Moriel Sanchez e Renan Pereira Reis | |
| 1.9 | 28/08/2026 | Refinamento da metodologia conforme as diretrizes da disciplina e inclusão da seção de rastreabilidade e elos com outros artefatos | Carlos Henrique Brasil de Souza, Pedro Teixeira Moriel Sanchez e Renan Pereira Reis | |

<p align="center">Tabela 3: Histórico de versão. Fonte: Carlos Henrique Brasil de Souza, Pedro Teixeira Moriel Sanchez e Renan Pereira Reis, 2026.</p>

Ver também: [Artefato Generalista](ArtefatoGeneralista.md) · [Mapa Mental](MapaMental.md) · [NFR Framework](NFRFramework.md) · [BPMN](BPMN.md)