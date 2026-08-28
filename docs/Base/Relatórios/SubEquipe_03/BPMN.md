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

*(Os vídeos de comprovação, as capturas de tela das interfaces, transições de estado e as regras de negócio identificadas serão documentados aqui nas próximas etapas).*

### Modelagem BPMN

Abaixo estão apresentados os modelos BPMN dos fluxos levantados pela subequipe, divididos em visões gerais e subprocessos para facilitar a leitura das mecânicas do sistema.

#### 1. Visão Geral: Exploração e Combate
O fluxo principal dita a navegação entre a exploração do mundo e as instâncias de salvamento ou combate.

<p align="center">Figura 1: Modelo BPMN do fluxo principal de Exploração e transição para Combate. Fonte: Autores, 2026.</p>

#### 2. Subprocesso: Exploração do Mundo
Detalha as ações possíveis durante a exploração ativa, como a movimentação livre, detecção de encontros, interação com NPCs e o acesso aos registros (Livro).

<p align="center">Figura 2: Modelo BPMN detalhando as atividades na Exploração do Mundo. Fonte: Autores, 2026.</p>

#### 3. Subprocesso: Combate em Turnos
Mapeamento do motor de batalha em turnos, com destaque para a mecânica de misturar elementos, gerar efeitos elementais, calcular fraquezas, imunidades e a recepção de dano ou estados.

<p align="center">Figura 3: Modelo BPMN do fluxo de Combate em turnos e mecânica de efeitos. Fonte: Autores, 2026.</p>

#### 4. Subprocesso: Livro (Registro)
O processo de validação, registro de livros coletados no inventário/banco de dados e o aprendizado contínuo (combinações e histórias).

<p align="center">Figura 4: Modelo BPMN do fluxo de coleta e registro no Livro. Fonte: Autores, 2026.</p>

## Referências

BRAGA, Rosana T. Vaccare; PENTEADO, Rosângela. **Engenharia Reversa e Reengenharia**. Material da disciplina SCE 186 – Engenharia de Software. [S. l.: s. n.], [s. d.].

*(As referências audiovisuais para as comprovações de engenharia reversa serão inseridas aqui).*

## Nível de Contribuição dos Integrantes

| Nome | % de Contribuição |
|------|-------------------|
| Carlos Henrique Brasil de Souza | 33,3% |
| Pedro Teixeira Moriel Sanchez | 33,3% |
| Renan Pereira Reis | 33,3% |

<p align="center">Tabela 1: Contribuição dos integrantes. Fonte: Autores, 2026.</p>

## Histórico de Versão

| Versão | Data | Descrição | Autor(es) | Revisor |
|:------:|------|:----------|:----------|:--------|
| 1.0 | 27/08/2026 | Criação da página base, adaptação da metodologia e adição dos modelos BPMN (Exploração, Combate, Mundo e Livro) | Pedro Teixeira Moriel Sanchez | |

<p align="center">Tabela 2: Histórico de versão. Fonte: Autores, 2026.</p>

Ver também: [Artefato Generalista](ArtefatoGeneralista.md) · [Mapa Mental](MapaMental.md) · [NFR Framework](NFRFramework.md) · [IA Generativa](IAGenerativa.md)
