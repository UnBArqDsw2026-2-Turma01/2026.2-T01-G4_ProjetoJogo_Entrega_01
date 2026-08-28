# Léxicos

## Descrição

Os léxicos são termos específicos do domínio da aplicação **G4_ProjetoJogo** que possuem significado particular no contexto do sistema: um **RPG medieval 2D de mundo semiaberto** com história linear e combate por turnos (referências: Final Fantasy clássicos, Undertale). Sua mecânica distintiva é a **mistura de elementos químicos** da tabela periódica para a criação de itens, realizada fora do combate. O documento apresenta a Noção e o Impacto de cada termo identificado, categorizado como sujeito, verbo, objeto ou estado.

## Objetivo

Definir e padronizar o vocabulário utilizado no projeto **G4_ProjetoJogo**, garantindo que todos os envolvidos no desenvolvimento tenham uma compreensão uniforme dos termos específicos do domínio.

## Metodologia

Os léxicos foram identificados através da análise do domínio do jogo, tendo como base o Mapa Mental elaborado pela equipe, e organizados segundo a classificação do LAL (Léxico Ampliado da Linguagem):

- **Sujeito:** entidades que realizam ações (ex.: Jogador, Inimigo).
- **Verbo:** ações executáveis dentro do domínio (ex.: Atacar, Upar).
- **Objeto:** entidades passivas manipuladas pelo sistema (ex.: HP, Item).
- **Estado:** situações específicas em que o sistema ou uma entidade pode se encontrar (ex.: Batalha, Game Over).

Cada termo inclui **Noção**, **Impacto** e, quando aplicável, **Sinônimos**.

## Léxicos Identificados

### SUJEITO

#### L01 - Jogador (Player)

- **Noção:** Personagem controlado pelo usuário durante a partida. Possui atributos como [HP](#l17-hp-pontos-de-vida), [MP](#l18-mp-pontos-de-magia) e nível.
- **Impacto:**
  - Escolhe uma ação a cada [Turno](#l15-turno) (ex.: [Atacar](#l04-atacar), [Defender](#l05-defender), [Usar Item](#l06-usar-item), [Fugir](#l07-fugir)).
  - Pode [Explorar](#l12-explorar) o [Mundo Semiaberto](#l26-mundo-semiaberto) livremente entre os combates.
  - Pode [Misturar Elementos](#l09-misturar-elementos) para [Criar Itens](#l10-criar-item).
  - Pode [Upar](#l08-upar) ao acumular experiência suficiente.
  - Leva o sistema a [Game Over](#l30-game-over) quando seu HP chega a 0.

**Fonte:** Marcelo, 2026.

#### L02 - Inimigo

- **Noção:** Entidade controlada pelo jogo que se opõe ao [Jogador](#l01-jogador-player) durante uma [Batalha](#l28-batalha).
- **Impacto:**
  - Ocupa uma posição na fila de [Turnos](#l15-turno).
  - Pode causar [Dano](#l19-dano) ao Jogador através de ataques.
  - Ao ser derrotado, pode gerar [Loot](#l21-loot) e contribuir para a [Vitória](#l29-vitória) do Jogador.

**Fonte:** Marcelo, 2026.

#### L03 - NPC (Personagem Não Jogável)

- **Noção:** Personagem controlado pelo jogo que não se opõe ao [Jogador](#l01-jogador-player), atuando como vendedor ou fornecedor de missões (*quest-giver*).
- **Impacto:**
  - Como vendedor, permite ao Jogador adquirir [Itens](#l20-item) e [Elementos Químicos](#l22-elemento-químico).
  - Como quest-giver, disponibiliza [Sidequests](#l24-sidequest) ao Jogador.
  - Não participa da fila de [Turnos](#l15-turno) de uma [Batalha](#l28-batalha).

**Fonte:** Marcelo, 2026.

### VERBO

#### L04 - Atacar

- **Noção:** Ação escolhida pelo [Jogador](#l01-jogador-player) em seu [Turno](#l15-turno) com a intenção de causar [Dano](#l19-dano) a um [Inimigo](#l02-inimigo).
- **Impacto:**
  - Aplica o Dano ao alvo, subtraindo-o de seu [HP](#l17-hp-pontos-de-vida).
  - Encerra o Turno do Jogador, passando a vez ao próximo personagem da fila.

**Fonte:** Marcelo, 2026.

#### L05 - Defender

- **Noção:** Ação escolhida pelo [Jogador](#l01-jogador-player) em seu [Turno](#l15-turno) para reduzir o Dano recebido no próximo ataque inimigo.
- **Impacto:**
  - Reduz temporariamente a efetividade do próximo ataque de um [Inimigo](#l02-inimigo) contra o Jogador.

**Fonte:** Marcelo, 2026.

#### L06 - Usar Item

- **Noção:** Ação escolhida pelo [Jogador](#l01-jogador-player) em seu [Turno](#l15-turno) para consumir um [Item](#l20-item) do [Inventário](#l23-inventário).
- **Impacto:**
  - Pode restaurar [HP](#l17-hp-pontos-de-vida) ou [MP](#l18-mp-pontos-de-magia), ou aplicar outros efeitos.
  - Remove uma unidade do Item consumido do Inventário do Jogador.

**Fonte:** Marcelo, 2026.

#### L07 - Fugir

- **Noção:** Ação escolhida pelo [Jogador](#l01-jogador-player) em seu [Turno](#l15-turno) para tentar encerrar a [Batalha](#l28-batalha) sem derrotar os inimigos.
- **Impacto:**
  - Se bem-sucedida, encerra a Batalha imediatamente, sem [Vitória](#l29-vitória) nem [Game Over](#l30-game-over).
  - Pode falhar dependendo das regras do encontro, mantendo o Jogador em combate.

**Fonte:** Marcelo, 2026.

#### L08 - Upar

- **Noção:** Subir de nível (do inglês *"level up"*), aumentando os atributos do [Jogador](#l01-jogador-player) ao acumular experiência suficiente.
- **Impacto:**
  - Eleva o nível do Jogador, geralmente aumentando HP, MP e/ou Dano.
  - Pode desbloquear novas habilidades ou receitas de [Criação de Item](#l10-criar-item).

**Fonte:** Marcelo, 2026.

#### L09 - Misturar Elementos

- **Noção:** Ação de combinar dois ou mais [Elementos Químicos](#l22-elemento-químico) da tabela periódica, realizada fora da [Batalha](#l28-batalha).
- **Impacto:**
  - Combinação válida: resulta na [Criação de um Item](#l10-criar-item), que é adicionado ao [Inventário](#l23-inventário).
  - Combinação inválida: não gera Item e pode consumir os Elementos utilizados.
  - As combinações conhecidas ficam registradas no [Livro do Aventureiro](#l25-livro-do-aventureiro).
  - Sinônimos: **Combinar Elementos**.

**Fonte:** Marcelo, 2026.

#### L10 - Criar Item

- **Noção:** Ação de produzir um novo [Item](#l20-item) a partir da [Mistura de Elementos](#l09-misturar-elementos) químicos.
- **Impacto:**
  - Adiciona o Item resultante ao [Inventário](#l23-inventário) do [Jogador](#l01-jogador-player).
  - Consome os [Elementos Químicos](#l22-elemento-químico) utilizados na receita.
  - Sinônimos: **Craftar**.

**Fonte:** Marcelo, 2026.

#### L11 - Personalizar Personagem

- **Noção:** Ação de o [Jogador](#l01-jogador-player) alterar a aparência ou os atributos visuais de seu personagem.
- **Impacto:**
  - Modifica a representação visual do Jogador no mundo do jogo.
  - Não altera o resultado das [Batalhas](#l28-batalha).

**Fonte:** Marcelo, 2026.

#### L12 - Explorar

- **Noção:** Ação de o [Jogador](#l01-jogador-player) se movimentar livremente pelo [Mundo Semiaberto](#l26-mundo-semiaberto) fora do combate.
- **Impacto:**
  - Permite encontrar [NPCs](#l03-npc-personagem-não-jogável), [Elementos Químicos](#l22-elemento-químico) e [Savepoints](#l27-savepoint).
  - Pode iniciar uma [Batalha](#l28-batalha) ao encontrar um [Inimigo](#l02-inimigo).

**Fonte:** Marcelo, 2026.

#### L13 - Farmar

- **Noção:** Repetir [Batalhas](#l28-batalha) ou ações para acumular recurso, como experiência, [Loot](#l21-loot) ou [Elementos Químicos](#l22-elemento-químico).
- **Impacto:**
  - Contribui para o progresso de [Upar](#l08-upar) e para o acúmulo de insumos para [Criar Itens](#l10-criar-item).
  - Sinônimos: **Grindar**.

**Fonte:** Marcelo, 2026.

#### L14 - Zerar

- **Noção:** Concluir o jogo, completando a [História Linear](#l31-história-linear) principal.
- **Impacto:**
  - Marca o encerramento da progressão principal do Jogador.

**Fonte:** Marcelo, 2026.

### OBJETO

#### L15 - Turno

- **Noção:** Unidade de tempo do combate. A cada Turno, um personagem ([Jogador](#l01-jogador-player) ou [Inimigo](#l02-inimigo)) executa uma ação, seguindo uma ordem/fila.
- **Impacto:**
  - Organiza a sequência de ações dentro de uma [Batalha](#l28-batalha).
  - Determina quando o Jogador pode [Atacar](#l04-atacar), [Defender](#l05-defender), [Usar Item](#l06-usar-item) ou [Fugir](#l07-fugir).

**Fonte:** Marcelo, 2026.

#### L16 - HUD de Batalha

- **Noção:** Elementos de interface exibidos durante o combate, incluindo [HP](#l17-hp-pontos-de-vida), [MP](#l18-mp-pontos-de-magia) e o menu de ações.
- **Impacto:**
  - É o principal meio de comunicação do estado da [Batalha](#l28-batalha) ao Jogador.

**Fonte:** Marcelo, 2026.

#### L17 - HP (Pontos de Vida)

- **Noção:** Recurso que representa a vida de um personagem. Ao chegar a 0, o personagem é derrotado.
- **Impacto:**
  - É reduzido por [Dano](#l19-dano) recebido em combate.
  - Zerar o HP do [Jogador](#l01-jogador-player) leva ao estado de [Game Over](#l30-game-over).
  - Zerar o HP de todos os [Inimigos](#l02-inimigo) leva ao estado de [Vitória](#l29-vitória).

**Fonte:** Marcelo, 2026.

#### L18 - MP (Pontos de Magia)

- **Noção:** Recurso consumido para uso de habilidades especiais ou magias, quando aplicável.
- **Impacto:**
  - Pode ser restaurado através de [Usar Item](#l06-usar-item).

**Fonte:** Marcelo, 2026.

#### L19 - Dano

- **Noção:** Quantidade de [HP](#l17-hp-pontos-de-vida) subtraída de um alvo quando um ataque é bem-sucedido.
- **Impacto:**
  - Resulta da ação [Atacar](#l04-atacar).
  - Pode levar um personagem ao estado de derrota quando reduz seu HP a 0.

**Fonte:** Marcelo, 2026.

#### L20 - Item

- **Noção:** Objeto do [Inventário](#l23-inventário) do [Jogador](#l01-jogador-player) que pode ser consumido através da ação [Usar Item](#l06-usar-item). Pode ser obtido como [Loot](#l21-loot), comprado de um [NPC](#l03-npc-personagem-não-jogável) ou produzido via [Criar Item](#l10-criar-item).
- **Impacto:**
  - Pode restaurar [HP](#l17-hp-pontos-de-vida) ou [MP](#l18-mp-pontos-de-magia), entre outros efeitos.

**Fonte:** Marcelo, 2026.

#### L21 - Loot

- **Noção:** Itens e [Elementos Químicos](#l22-elemento-químico) obtidos como recompensa ao derrotar [Inimigos](#l02-inimigo) ou explorar o mundo do jogo.
- **Impacto:**
  - Alimenta o [Inventário](#l23-inventário) do Jogador.
  - É um dos objetivos da ação [Farmar](#l13-farmar).

**Fonte:** Marcelo, 2026.

#### L22 - Elemento Químico

- **Noção:** Insumo baseado em um elemento da tabela periódica, coletável no mundo do jogo e utilizado como matéria-prima na [Mistura de Elementos](#l09-misturar-elementos).
- **Impacto:**
  - É armazenado no [Inventário](#l23-inventário) do [Jogador](#l01-jogador-player).
  - É consumido ao [Criar Item](#l10-criar-item).
  - Pode ser obtido via [Loot](#l21-loot), [Exploração](#l12-explorar) ou compra com [NPCs](#l03-npc-personagem-não-jogável).

**Fonte:** Marcelo, 2026.

#### L23 - Inventário

- **Noção:** Estrutura que armazena os [Itens](#l20-item) e [Elementos Químicos](#l22-elemento-químico) que o [Jogador](#l01-jogador-player) possui.
- **Impacto:**
  - Fornece os insumos para a [Mistura de Elementos](#l09-misturar-elementos).
  - Determina quais Itens estão disponíveis para a ação [Usar Item](#l06-usar-item) durante a [Batalha](#l28-batalha).

**Fonte:** Marcelo, 2026.

#### L24 - Sidequest

- **Noção:** Missão secundária, opcional, disponibilizada por um [NPC](#l03-npc-personagem-não-jogável), paralela à [História Linear](#l31-história-linear) principal.
- **Impacto:**
  - Ao ser concluída, pode conceder [Loot](#l21-loot), experiência ou [Elementos Químicos](#l22-elemento-químico).
  - Não é obrigatória para [Zerar](#l14-zerar) o jogo.
  - Sinônimos: **Missão Secundária**.

**Fonte:** Marcelo, 2026.

#### L25 - Livro do Aventureiro

- **Noção:** Registro consultável pelo [Jogador](#l01-jogador-player) que reúne as informações descobertas ao longo da partida, como as receitas de [Mistura de Elementos](#l09-misturar-elementos) já conhecidas.
- **Impacto:**
  - Permite ao Jogador reproduzir combinações já descobertas sem depender de tentativa e erro.
  - É atualizado conforme o Jogador descobre novas receitas.

**Fonte:** Marcelo, 2026.

#### L26 - Mundo Semiaberto

- **Noção:** Estrutura do mundo do jogo que permite [Exploração](#l12-explorar) livre dentro de áreas delimitadas, sem a liberdade total de um mundo aberto.
- **Impacto:**
  - Define os limites da movimentação do [Jogador](#l01-jogador-player) entre as etapas da [História Linear](#l31-história-linear).

**Fonte:** Marcelo, 2026.

#### L27 - Savepoint

- **Noção:** Ponto específico do mundo no qual o progresso do [Jogador](#l01-jogador-player) pode ser salvo.
- **Impacto:**
  - Registra o estado atual da partida.
  - Define o ponto de retorno do Jogador após um [Game Over](#l30-game-over).

**Fonte:** Marcelo, 2026.

### ESTADO

#### L28 - Batalha

- **Noção:** Situação de combate por turnos ativa entre [Jogador](#l01-jogador-player) e um ou mais [Inimigos](#l02-inimigo).
- **Impacto:**
  - Habilita a fila de [Turnos](#l15-turno) e as ações do Jogador.
  - Impede as ações de [Exploração](#l12-explorar) e [Mistura de Elementos](#l09-misturar-elementos) enquanto estiver ativa.
  - É encerrada pelos estados de [Vitória](#l29-vitória), [Game Over](#l30-game-over) ou pela ação [Fugir](#l07-fugir) bem-sucedida.

**Fonte:** Marcelo, 2026.

#### L29 - Vitória

- **Noção:** Estado alcançado quando todos os [Inimigos](#l02-inimigo) de uma [Batalha](#l28-batalha) são derrotados.
- **Impacto:**
  - Encerra a Batalha e pode conceder experiência e [Loot](#l21-loot) ao Jogador.

**Fonte:** Marcelo, 2026.

#### L30 - Game Over

- **Noção:** Estado alcançado quando o [HP](#l17-hp-pontos-de-vida) do [Jogador](#l01-jogador-player) chega a 0.
- **Impacto:**
  - Encerra a partida e retorna o Jogador ao último [Savepoint](#l27-savepoint) registrado.

**Fonte:** Marcelo, 2026.

#### L31 - História Linear

- **Noção:** Estrutura narrativa do jogo, na qual os eventos principais ocorrem em uma sequência fixa, sem ramificações.
- **Impacto:**
  - Define a ordem de progressão do [Jogador](#l01-jogador-player) até [Zerar](#l14-zerar) o jogo.
  - Convive com as [Sidequests](#l24-sidequest), que são opcionais e paralelas.

**Fonte:** Marcelo, 2026.

## Bibliografia

SERRANO, Milene; SERRANO, Maurício. Requisitos – Aula 10.

## Nível de Contribuição dos Integrantes

| Nome | % de Contribuição |
|------|-------------------|
| João Igor Pereira da Costa | 0,0% |
| João Victor da Silva Batista de Farias | 0,0% |
| Marcelo de Araújo Lopes | 100,0% |
| Marcos Vinícius Gündel da Silva | 0,0% |

<p align="center">Tabela 1: Contribuição dos integrantes.</p>

## Histórico de Versão

| Versão | Data | Descrição | Autor(es) | Revisor |
|:------:|------|:----------|:----------|:--------|
| 1.0 | 22/08/2026 | Criação do Léxico do domínio (LAL) | Marcelo de Araújo Lopes | |
| 1.1 | 22/08/2026 | Remoção da mecânica de desafio matemático e inclusão dos termos de química e exploração, conforme o Mapa Mental | Marcelo de Araújo Lopes | |

<p align="center">Tabela 2: Histórico de versão.</p>

Ver também: [Artefato Generalista](ArtefatoGeneralista.md) · [Rich Picture](RichPicture.md) · [NFR Framework](NFRFramework.md) · [BPMN](BPMN.md) · [IA Generativa](IAGenerativa.md)
