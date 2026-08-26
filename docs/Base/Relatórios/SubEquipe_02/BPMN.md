# SubEquipe_02 — BPMN

## Descrição

Modelagem de processo de negócio da SubEquipe_02, no escopo do **FOCO_02 — Engenharia Reversa & Modelagem BPMN**. Representa, na notação BPMN, fluxos de sistemas do jogo **Final Fantasy VI**, escolhido pela subequipe como objeto de Engenharia Reversa. Cada integrante ficou responsável por um sistema do jogo.

## Objetivo

Modelar em BPMN um fluxo identificado durante o processo de Engenharia Reversa, evidenciando as atividades, os eventos e os pontos de decisão do processo.

## Metodologia

A Engenharia Reversa foi conduzida com base na literatura (BRAGA; PENTEADO, [s. d.]), que a define como o "processo de exame e compreensão do software existente, para recapturar ou recriar o projeto e decifrar os requisitos atualmente implementados pelo sistema, apresentando-os em um nível ou grau mais alto de abstração". Como a subequipe não possui acesso ao código-fonte do jogo, foi adotada uma abordagem de Engenharia Reversa por observação da caixa-preta (*black-box*): assistir ao software em execução, catalogar sistematicamente os elementos de interface e as transições de tela, e inferir as regras de negócio a partir do comportamento observado, etapas detalhadas na seção [Processo de Engenharia Reversa Aplicado](#processo-de-engenharia-reversa-aplicado).

O jogo escolhido pela subequipe foi **Final Fantasy VI**. Os sistemas do jogo a serem modelados em BPMN foram divididos entre os quatro integrantes conforme definido em conversa da equipe (Figura 1):

![Print da conversa de WhatsApp definindo a divisão dos sistemas de FF6 para o BPMN](assets/bpmn_divisao.png)

<p align="center">Figura 1: Divisão dos sistemas de FF6 entre os integrantes da SubEquipe_02. Fonte: Conversa da equipe (WhatsApp), 2026.</p>

- Marcelo Araújo: Motor de Batalha (ATB)
- Marcos Vinícius: O Coliseu (nossa "Alquimia" de itens)
- João Igor: Sistema de Magicites (progressão e magias)
- João Victor: Habilidades Exclusivas (como o Blitz)

Cada integrante aplica individualmente o processo de Engenharia Reversa descrito acima ao seu sistema. A seguir, a metodologia específica de cada um.

### Motor de Batalha (ATB)

*A ser preenchido.*

### O Coliseu

Para o levantamento do fluxo do Coliseu, foi assistido o vídeo *"Final Fantasy 6 Pixel Remaster #41 - Coliseum"* (CARNAGE PANDA, 2022), do canal **carnage panda**, no YouTube. A partir do vídeo, foram extraídas capturas de tela de cada decisão e transição do fluxo de aposta do Coliseu, reunidas na pasta `assets` deste documento e utilizadas como evidência para a listagem dos elementos de interface, o registro das transições de estado e a inferência das regras de negócio apresentadas na próxima seção.

### Sistema de Magicites

*A ser preenchido.*

### Habilidades Exclusivas

*A ser preenchido.*

## Conteúdo

### Processo de Engenharia Reversa Aplicado

#### Coliseu

As capturas de tela a seguir, extraídas do vídeo do canal carnage panda (CARNAGE PANDA, 2022), documentam a sequência completa do fluxo de aposta do Coliseu. Para cada uma, são listados os elementos de interface, as transições de estado e as regras de negócio identificados naquela etapa específica.

![Diálogo inicial do guarda do Coliseu](assets/coliseu_1_inicio.png)

<p align="center">Figura 2: Diálogo inicial do guarda da entrada do Coliseu. Fonte: CARNAGE PANDA, 2022.</p>

**Elementos de Interface**

- Caixa de diálogo do guarda, exibindo a pergunta "Care to fight in the coliseum?".
- Menu textual de resposta com três opções: "With pleasure!", "No thanks." e "Could you explain?", exibido como uma segunda caixa sobreposta à caixa de diálogo, sem ocultá-la.

**Transições de Estado**

- A caixa de pergunta do guarda **não é ocultada** quando o menu de respostas surge: as duas caixas ficam visíveis simultaneamente, caracterizando uma sobreposição (*overlay*) e não uma substituição de tela.
- Ao clicar em "Could you explain?", o software exibe uma explicação textual das mecânicas do Coliseu e, em seguida, **retorna** à mesma pergunta inicial do guarda, configurando um laço (*loop*) no fluxo.
- Ao clicar em "No thanks.", o fluxo é encerrado e a tela retorna ao jogo normal, fora do Coliseu.
- Ao clicar em "With pleasure!", a tela do guarda é substituída integralmente pela tela de seleção de item para aposta (Figura 3).

![Tela de seleção do item a ser apostado](assets/coliseu_2_aposta.png)

<p align="center">Figura 3: Lista de itens do inventário disponíveis para aposta. Fonte: CARNAGE PANDA, 2022.</p>

**Elementos de Interface**

- Lista/aba de itens do inventário do jogador disponíveis para aposta, rolada verticalmente.

**Transições de Estado**

- Ao clicar em um item da lista, o software **não remove** o item nem avança diretamente, em vez disso, sobrepõe o modal de confirmação "Bet this item?" (Figura 4).

**Regras de Negócio**

- A lista de itens apostáveis é composta exclusivamente pelos itens presentes no inventário atual do jogador, não há itens exclusivos do Coliseu na lista.

![Modal de confirmação da aposta](assets/coliseu_3_aposta_confirmacao.png)

<p align="center">Figura 4: Modal de confirmação do item apostado. Fonte: CARNAGE PANDA, 2022.</p>

**Elementos de Interface**

- Modal de confirmação da aposta, com a pergunta "Bet this item?" e as opções "Yes" / "No".

**Transições de Estado**

- Clicar em "No" fecha o modal e retorna à tela de seleção de item (Figura 3).
- Clicar em "Yes" avança para a tela de seleção de personagem (Figura 5).

**Regras de Negócio**

- O item apostado só é efetivamente removido do inventário no momento em que um personagem é selecionado para o combate (Figura 5), e não neste momento de confirmação, ou seja, a aposta só se torna irreversível quando o combate está prestes a começar.

![Tela de seleção do personagem combatente](assets/coliseu_4_selecao.png)

<p align="center">Figura 5: Seleção do personagem combatente, com item apostado, item de recompensa e adversário exibidos. Fonte: CARNAGE PANDA, 2022.</p>

**Elementos de Interface**

- Painéis superiores fixos com o item apostado (ex.: "Flametongue") e o item prometido como recompensa (ex.: "Organyx").
- Rótulo central "VS." com o nome do adversário (ex.: "Great Malboro") e o nome do personagem em destaque (ex.: "Shadow").
- Lista de seleção com cursor, exibindo todos os personagens da party atual disponíveis para o combate, e botão de confirmação "Confirm".

**Transições de Estado**

- Qualquer escolha de personagem da party avança para a tela de combate automático (Figura 6), não há opção de retorno a essa altura do fluxo.

**Regras de Negócio**

- Apenas um personagem da party atual participa do combate por vez: o Coliseu isola o combatente selecionado, mesmo que a party tenha múltiplos membros disponíveis.

![Tela de combate automático no Coliseu](assets/coliseu_5_combate.png)

<p align="center">Figura 6: Combate automático entre o personagem escolhido e o adversário. Fonte: CARNAGE PANDA, 2022.</p>

**Elementos de Interface**

- Arena de combate automático, sem menu de comandos do jogador.

**Transições de Estado**

- Ao final do combate, a tela é substituída pela tela de vitória (Figura 7) ou de derrota (Figura 8), dependendo do resultado, sem intervenção do jogador durante a transição.

**Regras de Negócio**

- O jogador **não tem controle** sobre as ações do personagem durante o combate: a batalha do Coliseu é inteiramente automática/simulada pelo sistema, ao contrário do combate ATB padrão do modo aventura.

![Tela de vitória do Coliseu](assets/coliseu_6a_vitoria.png)

<p align="center">Figura 7: Tela de vitória, com a entrega do item de recompensa. Fonte: CARNAGE PANDA, 2022.</p>

**Elementos de Interface**

- Tela de resultado de vitória, com animação do personagem e contadores de Gil, EXP e Magic AP ganhos.

**Regras de Negócio**

- Em caso de vitória, os ganhos usuais de batalha são zerados (0 de Gil, 0 de EXP e 0 de Magic AP) e, em seu lugar, o jogador recebe o item prometido como recompensa: o Coliseu segue, portanto, uma lógica de recompensa própria, distinta do combate convencional.

![Tela de derrota do Coliseu](assets/coliseu_6b_derrota.png)

<p align="center">Figura 8: Tela de derrota, sem concessão de recompensa. Fonte: CARNAGE PANDA, 2022.</p>

**Elementos de Interface**

- Transição "Fade to black" ao final da animação de derrota do personagem.

**Regras de Negócio**

- Em caso de derrota, o item apostado é **permanentemente perdido** (não retorna ao inventário) e nenhuma recompensa é concedida, caracterizando uma mecânica de risco: o jogador aposta um item na expectativa de ganhar outro, podendo perder o que apostou.

### Modelagem BPMN

*Inserir aqui o modelo BPMN do fluxo levantado, com legenda e fonte.*

<p align="center">Figura 9: Modelo BPMN do fluxo de &lt;&lt;nome do fluxo&gt;&gt;. Fonte: Autores, 2026.</p>

## Referências

BRAGA, Rosana T. Vaccare; PENTEADO, Rosângela. **Engenharia Reversa e Reengenharia**. Material da disciplina SCE 186 – Engenharia de Software. [S. l.: s. n.], [s. d.].

CARNAGE PANDA. **Final Fantasy 6 Pixel Remaster #41 - Coliseum**. YouTube, 5 abr. 2022. Disponível em: https://www.youtube.com/watch?v=vAIxn-R0GFM. Acesso em: 25 ago. 2026.

## Nível de Contribuição dos Integrantes

| Nome | % de Contribuição |
|------|-------------------|
| Marcos Vinícius Gündel da Silva | |

<p align="center">Tabela 1: Contribuição dos integrantes. Fonte: Autores, 2026.</p>

## Histórico de Versão

| Versão | Data | Descrição | Autor(es) | Revisor |
|:------:|------|:----------|:----------|:--------|
| 1.0 | 22/08/2026 | Criação da página no modelo do artefato padrão | Marcelo de Araújo Lopes | |
| 1.1 | 25/08/2026 | Preenchimento do processo de Engenharia Reversa aplicado ao Coliseu (FF6): metodologia e, para cada tela do fluxo, os elementos de interface, as transições de estado e as regras de negócio identificados | Marcos Vinícius Gündel da Silva | |

<p align="center">Tabela 2: Histórico de versão. Fonte: Autores, 2026.</p>

Ver também: [Artefato Generalista](ArtefatoGeneralista.md) · [Léxico](Lexico.md) · [Rich Picture](RichPicture.md) · [NFR Framework](NFRFramework.md) · [IA Generativa](IAGenerativa.md)
