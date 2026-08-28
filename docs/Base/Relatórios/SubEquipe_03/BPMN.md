# SubEquipe_03 — BPMN

## Descrição

Modelagem de processo de negócio da SubEquipe_03, no escopo do **FOCO_02 — Engenharia Reversa & Modelagem BPMN**. Representa, na notação BPMN, os fluxos sistêmicos levantados por Engenharia Reversa do software escolhido pela subequipe.

## Objetivo

Modelar em BPMN os fluxos identificados durante o processo de Engenharia Reversa, evidenciando as atividades, os eventos, os subprocessos e os pontos de decisão (como exploração, combate e gerenciamento de itens).

## Metodologia

A Engenharia Reversa foi conduzida com base na literatura *(BRAGA; PENTEADO, [s. d.])* que a define como o "processo de exame e compreensão do software existente, para recapturar ou recriar o projeto e decifrar os requisitos atualmente implementados pelo sistema, apresentando-os em um nível ou grau mais alto de abstração".

Foi adotada uma abordagem de Engenharia Reversa por observação da caixa-preta (*black-box*): assistir ao software em execução por meio de capturas em vídeo, catalogar sistematicamente as interações, elementos de interface e transições, e inferir as regras de negócio a partir do comportamento observado. As etapas detalhadas encontram-se na seção [Processo de Engenharia Reversa Aplicado](#processo-de-engenharia-reversa-aplicado).

## Conteúdo

### Processo de Engenharia Reversa Aplicado

A partir dos registros audiovisuais analisados (vídeos em anexo), foi possível inferir as seguintes regras e transições de estado para compor a modelagem:

#### 1. Exploração, Interação e Lojas (Vídeos 1 e 2)
* **Transição de Estado:** A navegação pelo mapa-múndi pode ser interrompida por encontros aleatórios (ativando a tela de combate) ou pela transição para áreas seguras (como a entrada na cidade de Nikeah, visualizada no segundo vídeo).
* **Interface e Regras de Negócio (Lojas):** Ao interagir com NPCs lojistas, abre-se a interface de Compra/Venda. O sistema lê o banco de dados do inventário (Gil disponível, itens em posse) e exibe as armas/itens disponíveis para aquisição. Ao confirmar uma compra, o valor em Gil é deduzido e o item é adicionado ao inventário.
* **Comprovação em Vídeo (Clique nas fotos abaixo):**

<p align="center">
  <a href="https://drive.google.com/file/d/1S7D2vVTuFscxlDViPK-8rxpy7ZNnYfrF/view?usp=sharing" target="_blank">
    <img src="Base/Relatórios/SubEquipe_03/assets/bpmn_thumb1.png" width="80%" alt="Vídeo 1: Exploração e Save State.">
  </a>
</p>

<p align="center">
  <a href="https://drive.google.com/file/d/1rGfz4kKYHT3Xq-1DLQrf7rYgwvI1inAv/view?usp=sharing" target="_blank">
    <img src="Base/Relatórios/SubEquipe_03/assets/bpmn_thumb2.png" width="80%" alt="Vídeo 2: Entrada em Nikeah e interação com Loja.">
  </a>
</p>

#### 2. Transição e Combate em Turnos (Vídeos 3 e 4)
* **Transição de Estado:** Durante a exploração de dungeons como a "Caverna em Veldt", ocorre um encontro aleatório. A interface de exploração sofre um efeito de transição de tela e é substituída instantaneamente pela arena de combate.
* **Interface e Regras de Negócio (Combate):** O combate segue um sistema de turnos. A personagem seleciona um comando no menu de batalha inferior (ex: Ataque, Magia, Itens). O vídeo demonstra o uso da magia *Fogo++* contra o inimigo *Louva-morte*. O sistema calcula o dano (9999), subtrai os PVs do inimigo e, ao derrotá-lo, encerra a batalha exibindo a tela de vitória com as recompensas adquiridas (Gil, EXP e PH de Magia).
* **Comprovação em Vídeo:**

<p align="center">
  <a href="https://drive.google.com/file/d/1RB1NG5I8wCQHz4K2aglmyf6u9GBw-2ru/view?usp=sharing" target="_blank">
    <img src="Base/Relatórios/SubEquipe_03/assets/bpmn_thumb3.png" width="80%" alt="Vídeo 3: Encontro aleatório.">
  </a>
</p>

<p align="center">
  <a href="https://drive.google.com/file/d/1wlHRqZsNUE9HpkJSP2cN5xWH5dCBUvgQ/view?usp=sharing" target="_blank">
    <img src="Base/Relatórios/SubEquipe_03/assets/bpmn_thumb4.png" width="80%" alt="Vídeo 4: Sistema de Combate.">
  </a>
</p>

#### 3. Menu de Status e Ponto de Salvamento (Vídeo 5)
* **Transição de Estado e Interface:** Em áreas hostis como o "Continente Flutuante", o jogador pode acessar o Menu Principal para verificar as condições da equipe (PV, PM, Nível) e as invocações/Magicites equipadas (Maduin, Ramuh, Ifrit, Shiva). Ao entrar em uma área de salvamento específica (indicada por um feixe de luz), o jogador pode salvar o progresso, gravando os dados atuais e a localização no slot escolhido do banco de dados (Arquivo 19).
* **Comprovação em Vídeo:**

<p align="center">
  <a href="https://drive.google.com/file/d/1MYkOsRGcDop79fzm7XLOVNWIpDEQt5kO/view?usp=sharing" target="_blank">
    <img src="Base/Relatórios/SubEquipe_03/assets/bpmn_thumb5.png" width="80%" alt="Vídeo 5: Exploração de masmorra, menu de status e ponto de salvamento.">
  </a>
</p>

### Modelagem BPMN

Abaixo estão apresentados os modelos BPMN dos fluxos levantados pela subequipe, divididos em visões gerais e subprocessos para facilitar a leitura das mecânicas do sistema.

#### 1. Visão Geral: Exploração e Combate
O fluxo principal dita a navegação entre a exploração do mundo e as instâncias de salvamento ou combate.

<img src="Base/Relatórios/SubEquipe_03/assets/Captura de tela 2026-08-27 211134.png" width="100%" alt="Modelo BPMN - Exploração">
<p align="center">Figura 1: Modelo BPMN do fluxo principal de Exploração e transição para Combate. Fonte: Carlos Henrique Brasil de Souza, Pedro Teixeira Moriel Sanchez e Renan Pereira Reis, 2026.</p>

#### 2. Subprocesso: Exploração do Mundo
Detalha as ações possíveis durante a exploração ativa, como a movimentação livre, detecção de encontros, interação com NPCs e o acesso aos registros (Livro).

<img src="Base/Relatórios/SubEquipe_03/assets/Captura de tela 2026-08-27 211214.png" width="100%" alt="Modelo BPMN - Exploração do Mundo">
<p align="center">Figura 2: Modelo BPMN detalhando as atividades na Exploração do Mundo. Fonte: Carlos Henrique Brasil de Souza, Pedro Teixeira Moriel Sanchez e Renan Pereira Reis, 2026.</p>

#### 3. Subprocesso: Combate em Turnos
Mapeamento do motor de batalha em turnos, com destaque para a mecânica de misturar elementos, gerar efeitos elementais, calcular fraquezas, imunidades e a recepção de dano ou estados.

<img src="Base/Relatórios/SubEquipe_03/assets/Captura de tela 2026-08-27 211242.png" width="100%" alt="Modelo BPMN - Combate em Turnos">
<p align="center">Figura 3: Modelo BPMN do fluxo de Combate em turnos e mecânica de efeitos. Fonte: Carlos Henrique Brasil de Souza, Pedro Teixeira Moriel Sanchez e Renan Pereira Reis, 2026.</p>

#### 4. Subprocesso: Livro (Registro)
O processo de validação, registro de livros coletados no inventário/banco de dados e o aprendizado contínuo (combinações e histórias).

<img src="Base/Relatórios/SubEquipe_03/assets/Captura de tela 2026-08-27 211256.png" width="100%" alt="Modelo BPMN - Livro">
<p align="center">Figura 4: Modelo BPMN do fluxo de coleta e registro no Livro. Fonte: Carlos Henrique Brasil de Souza, Pedro Teixeira Moriel Sanchez e Renan Pereira Reis, 2026.</p>

## Referências

BRAGA, Rosana T. Vaccare; PENTEADO, Rosângela. **Engenharia Reversa e Reengenharia**. Material da disciplina SCE 186 – Engenharia de Software. [S. l.: s. n.], [s. d.].

SQUARE ENIX. **Final Fantasy VI Pixel Remaster**. [Vídeos de gameplay capturados pelos autores]. 2026.

## Nível de Contribuição dos Integrantes

| Nome | % de Contribuição |
|------|-------------------|
| Carlos Henrique Brasil de Souza | 33,3% |
| Pedro Teixeira Moriel Sanchez | 33,3% |
| Renan Pereira Reis | 33,3% |

<p align="center">Tabela 1: Contribuição dos integrantes. Fonte: Carlos Henrique Brasil de Souza, Pedro Teixeira Moriel Sanchez e Renan Pereira Reis, 2026.</p>

## Histórico de Versão

| Versão | Data | Descrição | Autor(es) | Revisor |
|:------:|------|:----------|:----------|:--------|
| 1.0 | 27/08/2026 | Criação da página base, adaptação da metodologia e adição dos modelos BPMN (Exploração, Combate, Mundo e Livro) | Carlos Henrique Brasil de Souza, Pedro Teixeira Moriel Sanchez e Renan Pereira Reis | |
| 1.1 | 27/08/2026 | Adição dos achados da engenharia reversa com as análises dos vídeos (Exploração, Combate, Menus) | Carlos Henrique Brasil de Souza, Pedro Teixeira Moriel Sanchez e Renan Pereira Reis | |
| 1.2 | 27/08/2026 | Correção dos caminhos das imagens e vídeos para o diretório `assets/` | Carlos Henrique Brasil de Souza, Pedro Teixeira Moriel Sanchez e Renan Pereira Reis | |
| 1.3 | 27/08/2026 | Alteração da forma de fazer o display dos vídeos | Carlos Henrique Brasil de Souza, Pedro Teixeira Moriel Sanchez e Renan Pereira Reis | |
| 1.4 | 27/08/2026 | Centralização e redimensionamento das miniaturas de vídeo | Carlos Henrique Brasil de Souza, Pedro Teixeira Moriel Sanchez e Renan Pereira Reis | |
| 1.5 | 28/08/2026 | Correção do caminho das imagens nas tags `<img>` (raiz do site) para renderizarem no Docsify local e no GitHub Pages | Marcos Vinícius Gündel da Silva | |
| 1.6 | 28/08/2026 | Registro da autoria conjunta da subequipe nas fontes das figuras e tabelas e no histórico de versão | Carlos Henrique Brasil de Souza, Pedro Teixeira Moriel Sanchez e Renan Pereira Reis | |

<p align="center">Tabela 2: Histórico de versão. Fonte: Carlos Henrique Brasil de Souza, Pedro Teixeira Moriel Sanchez e Renan Pereira Reis, 2026.</p>

Ver também: [Artefato Generalista](ArtefatoGeneralista.md) · [Mapa Mental](MapaMental.md) · [NFR Framework](NFRFramework.md) · [IA Generativa](IAGenerativa.md)