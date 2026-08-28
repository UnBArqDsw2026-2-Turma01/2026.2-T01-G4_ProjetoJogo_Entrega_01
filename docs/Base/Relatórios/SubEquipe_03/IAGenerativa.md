# SubEquipe_03 — IA Generativa

## Descrição

Registro do **FOCO_03 — IA Generativa** da SubEquipe_03. Reúne os pontos de vista de cada integrante sobre as lições aprendidas e o uso de IA Generativa na entrega.

## Objetivo

Registrar, com senso crítico, como cada membro utilizou IA Generativa no trabalho e quais lições foram aprendidas no processo. **TODOS DEVEM PARTICIPAR.**

## Metodologia

A entrega mínima deste foco são os pontos de vista de cada integrante sobre as lições aprendidas e o uso de IA Generativa. A seção reúne duas coisas distintas: o que cada um pensa sobre a ferramenta, na Tabela 1, e onde a ferramenta efetivamente entrou na produção dos artefatos, relatado a seguir com as evidências correspondentes.

Os pontos de vista da Tabela 1 foram redigidos individualmente, cada integrante respondendo apenas pela própria experiência, sem convergir para um texto único da subequipe. A inclusão de cada um está registrada no histórico de versão desta página, o que preserva o elo entre o ponto de vista e seu autor.

O relato dos usos segue um critério único: separar aquilo em que a ferramenta apoiou apenas a **forma** de um artefato, como legibilidade e redação, daquilo em que ela tocou o **conteúdo**, propondo estrutura ou revisando criticamente um artefato pronto. Só a segunda categoria interfere no que a subequipe afirma nos artefatos, e é sobre ela que a análise se concentra. A ferramenta utilizada em todos os casos foi o **Claude**, da Anthropic, pela interface do claude.ai e pelo Claude Code no terminal.

### Uso no Mapa Mental

Antes de construir o artefato, a subequipe pediu à ferramenta uma organização de partida para o conceito do jogo. A IA devolveu uma estrutura em seis blocos, ancorada em um ramo próprio de *Sistema de magia* (Figura 1). A proposta não foi seguida: a subequipe construiu o mapa em reunião, no Excalidraw, consolidando a mistura de elementos químicos entre as Mecânicas de Jogo, e chegou aos quatro ramos publicados no [Mapa Mental](MapaMental.md).

<p align="center">
  <img src="Base/Relatórios/SubEquipe_03/assets/ia2.jpeg" alt="Organização inicial proposta pela IA e não seguida pela subequipe" width="400">
</p>

<p align="center">Figura 1: Organização inicial para o conceito do jogo proposta pela IA, em seis blocos e ancorada em um ramo próprio de <em>Sistema de magia</em>. A proposta antecedeu a construção do mapa mental e não foi seguida pela subequipe. Fonte: Carlos Henrique Brasil de Souza, Pedro Teixeira Moriel Sanchez e Renan Pereira Reis, 2026 (captura de tela de conversa da subequipe com o Claude, da Anthropic, em claude.ai).</p>

A ferramenta foi usada uma segunda vez nesse artefato, já com o rascunho pronto, apenas para reproduzi-lo em uma diagramação mais legível. Nessa etapa nenhum conceito foi acrescentado, removido ou renomeado, conforme registra a metodologia do [Mapa Mental](MapaMental.md). O alcance da IA no artefato generalista, portanto, ficou restrito à forma: a estrutura que ela propôs foi recusada, e a que ela reproduziu já era da subequipe.

### Uso no SIG

Com o SIG na notação do NFR Framework e o Mapa Mental já finalizados como imagem, fora do repositório, a subequipe submeteu os dois artefatos junto com o rascunho do Excalidraw e o texto que descrevia o SIG, pedindo uma avaliação crítica antes da publicação. O uso foi de revisão do conteúdo já produzido, não de geração do artefato, e apontou duas fragilidades:

- A descrição afirmava que os cinco sub-NFRs derivavam das heurísticas de Nielsen, mas **Imersão** não é uma delas: vem da literatura específica de jogos. A subequipe reescreveu o trecho distinguindo as duas origens, o que transformou uma imprecisão conceitual em uma decisão justificada e rastreável.
- O trade-off entre **Flexibilidade** e **Estética Minimalista** estava desenhado no SIG, mas não era discutido em texto, que é justamente onde a diretriz da disciplina espera encontrar o senso crítico. A discussão foi então escrita e incorporada ao [artefato](NFRFramework.md).

### Uso na Modelagem BPMN

Cada subprocesso do jogo (loop principal, combate, criação de itens, exploração, livros colecionáveis, savepoint) foi modelado separadamente, com a IA decompondo o mapa mental em fluxos com eventos, gateways e raias de responsabilidade, além de indicar se as notações propostas pelos integrantes eram ou não aceitas na especificação. A revisão da documentação foi sempre necessária, pois a IA errava com frequência sobre o que podia ser representado no diagrama.

<p align="center">
  <img src="Base/Relatórios/SubEquipe_03/assets/ia1.jpeg" alt="Modelagem BPMN pela IA" width="400">
</p>

<p align="center">Figura 2: Modelagem do fluxo de exploração do mundo em notação BPMN, gerada a partir do detalhamento das regras pela subequipe. Fonte: Carlos Henrique Brasil de Souza, Pedro Teixeira Moriel Sanchez e Renan Pereira Reis, 2026 (captura de tela de conversa da subequipe com o Claude, da Anthropic, modelo Sonnet 5, em claude.ai).</p>

À medida que a subequipe fornecia regras mais específicas e novas (ex.: diferenciação entre área segura e não segura, mundo aberto e não aberto, regras de save state), a IA revisou os diagramas já existentes em vez de recomeçá-los do zero, mantendo rastreabilidade entre versões. A cada entrega de diagrama a ferramenta sinalizava pontos em aberto ou ambiguidades de modelagem (ex.: frequência do combate aleatório, se "sair do jogo" preserva progresso fora de savepoints), que serviam de gatilho para a rodada seguinte de refinamento, em vez de uma geração única e definitiva.

### Uso no planejamento da entrega

Antes da abertura das issues, a subequipe submeteu o próprio planejamento de sprints e de organização do repositório junto com as Diretrizes de Entrega e o Plano de Ensino, pedindo uma avaliação de aderência. O objetivo era confrontar o que havia sido planejado com o que a disciplina exigia, e não delegar o planejamento à ferramenta.

### Balanço

Nos quatro usos o resultado passou por revisão da subequipe antes de entrar em qualquer artefato, e em dois deles foi recusado no todo ou em parte. O que a ferramenta ofereceu com mais consistência não foi conteúdo pronto, mas a exposição de lacunas: notações inválidas na modelagem, pontos em aberto nos fluxos, uma imprecisão conceitual no SIG e uma estrutura que a subequipe precisou decidir não usar. O ganho esteve em ter algo concreto contra o que reagir, e o custo foi a revisão obrigatória de tudo o que ela devolveu.

## Conteúdo

| Nome do Membro | Lições Aprendidas | Uso da IA Generativa (senso crítico) |
|----------------|-------------------|--------------------------------------|
| Carlos Henrique Brasil de Souza | Compreendi melhor os conceitos de Arquitetura de Software e como os componentes do sistema se comunicam. A prática da Engenharia Reversa foi essencial para mapear a estrutura da aplicação e representar esses processos de forma clara usando diagramas BPMN. | Usei a IA para esclarecer dúvidas sobre padrões arquiteturais e para revisar a documentação. Notei que a IA ajuda muito com a teoria, mas frequentemente sugere soluções arquiteturais muito genéricas. Foi preciso adaptar e validar todas as sugestões para o contexto real do nosso projeto. |
| Pedro Teixeira Moriel Sanchez | Aprendi como as decisões de Arquitetura de Software impactam diretamente os requisitos não-funcionais da aplicação. O uso do NFR Framework e a modelagem em BPMN me ajudaram a visualizar a estrutura do sistema e como os diferentes módulos interagem entre si. | A IA serviu como apoio para formatar textos e explicar como estruturar nossos artefatos. No entanto, percebi que ela tem dificuldade em gerar a lógica estrutural e arquitetural correta. Ela é boa para apoiar a escrita, mas a modelagem da arquitetura precisa ser feita inteiramente por nós. |
| Renan Pereira Reis | Entendi a importância de documentar bem a Arquitetura de Software para manter a organização do projeto. A modelagem do SIG no NFR Framework deixou mais claro como as restrições e escolhas arquiteturais moldam o desenvolvimento e o comportamento do sistema. | Utilizei a IA para gerar propostas de templates de documentação e resumir conceitos. O senso crítico foi fundamental ao notar que a IA, às vezes, inventa ou mistura padrões arquiteturais que não faziam sentido para o nosso escopo. A revisão humana do que foi gerado foi indispensável. |

<p align="center">Tabela 1: Pontos de vista dos integrantes sobre o uso de IA Generativa. Fonte: Carlos Henrique Brasil de Souza, Pedro Teixeira Moriel Sanchez e Renan Pereira Reis, 2026.</p>

### Rastreabilidade e Elos com Outros Artefatos

Os usos relatados na Metodologia estão ancorados nos três artefatos da subequipe, cada um verificável na página correspondente: o [Mapa Mental](MapaMental.md), cuja estrutura foi definida em reunião e não pela proposta da Figura 1; o [NFR Framework](NFRFramework.md), que incorporou os dois achados da revisão; e o [BPMN](BPMN.md), cujos fluxos foram modelados com o apoio descrito e revisados pela subequipe.

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
| 2.0 | 28/08/2026 | Reescrita da seção: metodologia reorganizada por artefato, com o critério de forma e conteúdo, balanço crítico dos usos, legendas e fontes das figuras, rastreabilidade e elos com outros artefatos, e registro da autoria conjunta da subequipe nas fontes e no histórico | Carlos Henrique Brasil de Souza, Pedro Teixeira Moriel Sanchez e Renan Pereira Reis | |

<p align="center">Tabela 3: Histórico de versão. Fonte: Carlos Henrique Brasil de Souza, Pedro Teixeira Moriel Sanchez e Renan Pereira Reis, 2026.</p>

Ver também: [Artefato Generalista](ArtefatoGeneralista.md) · [Mapa Mental](MapaMental.md) · [NFR Framework](NFRFramework.md) · [BPMN](BPMN.md)