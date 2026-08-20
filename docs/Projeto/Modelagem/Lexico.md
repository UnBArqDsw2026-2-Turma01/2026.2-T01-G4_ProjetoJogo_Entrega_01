# Léxicos

## Descrição

Os léxicos são termos específicos do domínio da aplicação **G4_ProjetoJogo** que possuem significado particular no contexto do sistema: um RPG de turno 2D (referências: Final Fantasy clássicos, Undertale), com pegada didática — cada ataque do jogador só é executado se ele resolver corretamente uma operação matemática exibida na tela. O documento apresenta a Noção e o Impacto de cada termo identificado, categorizado como sujeito, verbo, objeto ou estado.

## Objetivo

Definir e padronizar o vocabulário utilizado no projeto **G4_ProjetoJogo**, garantindo que todos os envolvidos no desenvolvimento tenham uma compreensão uniforme dos termos específicos do domínio.

## Metodologia

Os léxicos foram identificados através da análise do domínio do jogo e organizados segundo a classificação do LAL (Léxico Ampliado da Linguagem):

- **Sujeito:** entidades que realizam ações (ex.: Jogador, Inimigo).
- **Verbo:** ações executáveis dentro do domínio (ex.: Atacar, Upar).
- **Objeto:** entidades passivas manipuladas pelo sistema (ex.: HP, Item).
- **Estado:** situações específicas em que o sistema ou uma entidade pode se encontrar (ex.: Batalha, Game Over).

Cada termo inclui **Noção**, **Impacto** e, quando aplicável, **Sinônimos**.

## Léxicos Identificados

### SUJEITO

#### L01 - Jogador (Player)

- **Noção:** Personagem controlado pelo usuário durante a partida. Possui atributos como [HP](#l15-hp-pontos-de-vida), [MP](#l16-mp-pontos-de-magia) e nível.
- **Impacto:**
  - Escolhe uma ação a cada [Turno](#l13-turno) (ex.: [Atacar](#l04-atacar), [Defender](#l05-defender), [Usar Item](#l07-usar-item), [Fugir](#l08-fugir)).
  - Precisa [Responder Desafio Matemático](#l06-responder-desafio-matemático) para que um ataque seja efetivado.
  - Pode [Upar](#l09-upar) ao acumular experiência suficiente.
  - Leva o sistema a [Game Over](#l24-game-over) quando seu HP chega a 0.

**Fonte:** Marcelo, 2026.

#### L02 - Inimigo

- **Noção:** Entidade controlada pelo jogo que se opõe ao [Jogador](#l01-jogador-player) durante uma [Batalha](#l22-batalha).
- **Impacto:**
  - Ocupa uma posição na fila de [Turnos](#l13-turno).
  - Pode causar [Dano](#l17-dano) ao Jogador através de ataques, sem exigir resolução de [Desafio Matemático](#l14-desafio-matemático).
  - Ao ser derrotado, pode gerar [Loot](#l19-loot) e contribuir para a [Vitória](#l23-vitória) do Jogador.

**Fonte:** Marcelo, 2026.

#### L03 - Chefe (Boss)

- **Noção:** [Inimigo](#l02-inimigo) especial, geralmente mais forte, associado a um marco de progressão do jogo (ex.: final de uma fase).
- **Impacto:**
  - Inicia uma [Batalha](#l22-batalha) com regras ou padrões de ataque diferenciados dos inimigos comuns.
  - Sua derrota pode desbloquear novas áreas, itens ou progressão de história.

**Fonte:** Marcelo, 2026.

### VERBO

#### L04 - Atacar

- **Noção:** Ação escolhida pelo [Jogador](#l01-jogador-player) em seu [Turno](#l13-turno) com a intenção de causar [Dano](#l17-dano) a um [Inimigo](#l02-inimigo).
- **Impacto:**
  - Dispara a exibição de um [Desafio Matemático](#l14-desafio-matemático) na tela.
  - Se o Jogador [Responder Desafio Matemático](#l06-responder-desafio-matemático) corretamente, o ataque é aplicado e o Dano é subtraído do HP do alvo.
  - Se a resposta for incorreta, o ataque falha e nenhum Dano é causado.

**Fonte:** Marcelo, 2026.

#### L05 - Defender

- **Noção:** Ação escolhida pelo [Jogador](#l01-jogador-player) em seu [Turno](#l13-turno) para reduzir o Dano recebido no próximo ataque inimigo.
- **Impacto:**
  - Não exige resolução de [Desafio Matemático](#l14-desafio-matemático).
  - Reduz temporariamente a efetividade do próximo ataque de um [Inimigo](#l02-inimigo) contra o Jogador.

**Fonte:** Marcelo, 2026.

#### L06 - Responder Desafio Matemático

- **Noção:** Ação de o [Jogador](#l01-jogador-player) informar o resultado de uma operação matemática (ex.: "2+2") exibida ao escolher [Atacar](#l04-atacar).
- **Impacto:**
  - Resposta correta: libera a execução do ataque com [Dano](#l17-dano) normal.
  - Resposta incorreta ou fora do tempo: cancela a ação de ataque, sem Dano causado.
  - Sinônimos: **Resolver Conta**.

**Fonte:** Marcelo, 2026.

#### L07 - Usar Item

- **Noção:** Ação escolhida pelo [Jogador](#l01-jogador-player) em seu [Turno](#l13-turno) para consumir um [Item](#l18-item) do inventário.
- **Impacto:**
  - Pode restaurar [HP](#l15-hp-pontos-de-vida) ou [MP](#l16-mp-pontos-de-magia), ou aplicar outros efeitos.
  - Remove uma unidade do Item consumido do inventário do Jogador.

**Fonte:** Marcelo, 2026.

#### L08 - Fugir

- **Noção:** Ação escolhida pelo [Jogador](#l01-jogador-player) em seu [Turno](#l13-turno) para tentar encerrar a [Batalha](#l22-batalha) sem derrotar os inimigos.
- **Impacto:**
  - Se bem-sucedida, encerra a Batalha imediatamente, sem [Vitória](#l23-vitória) nem [Game Over](#l24-game-over).
  - Pode falhar dependendo das regras do encontro, mantendo o Jogador em combate.

**Fonte:** Marcelo, 2026.

#### L09 - Upar

- **Noção:** Subir de nível (do inglês *"level up"*), aumentando os atributos do [Jogador](#l01-jogador-player) ao acumular experiência suficiente.
- **Impacto:**
  - Eleva o nível do Jogador, geralmente aumentando HP, MP e/ou Dano.
  - Pode desbloquear novas habilidades ou dificuldades de [Desafio Matemático](#l14-desafio-matemático).

**Fonte:** Marcelo, 2026.

#### L10 - Tankar

- **Noção:** Ato de um personagem absorver [Dano](#l17-dano) no lugar de outros, mantendo-se como alvo principal dos inimigos (do inglês *"tank"*).
- **Impacto:**
  - Aplicável em contextos com múltiplos personagens jogáveis (ex.: party), reduzindo o Dano recebido pelos demais.

**Fonte:** Marcelo, 2026.

#### L11 - Farmar

- **Noção:** Repetir [Batalhas](#l22-batalha) ou ações para acumular recurso, como experiência, [Loot](#l19-loot) ou moeda.
- **Impacto:**
  - Contribui para o progresso de [Upar](#l09-upar) e para a formação de [Build](#l20-build) do Jogador.
  - Sinônimos: **Grindar**.

**Fonte:** Marcelo, 2026.

#### L12 - Zerar

- **Noção:** Concluir o jogo, completando a campanha ou história principal.
- **Impacto:**
  - Marca o encerramento da progressão principal do Jogador.

**Fonte:** Marcelo, 2026.

### OBJETO

#### L13 - Turno

- **Noção:** Unidade de tempo do combate. A cada Turno, um personagem ([Jogador](#l01-jogador-player) ou [Inimigo](#l02-inimigo)) executa uma ação, seguindo uma ordem/fila.
- **Impacto:**
  - Organiza a sequência de ações dentro de uma [Batalha](#l22-batalha).
  - Determina quando o Jogador pode [Atacar](#l04-atacar), [Defender](#l05-defender), [Usar Item](#l07-usar-item) ou [Fugir](#l08-fugir).

**Fonte:** Marcelo, 2026.

#### L14 - Desafio Matemático

- **Noção:** Operação matemática (ex.: "2+2") exibida ao [Jogador](#l01-jogador-player) ao escolher a ação [Atacar](#l04-atacar). Deve ser resolvida corretamente para o ataque ser efetivado.
- **Impacto:**
  - É a condição de sucesso da ação Atacar.
  - Sua dificuldade pode escalar conforme a progressão do jogo.

**Fonte:** Marcelo, 2026.

#### L15 - HP (Pontos de Vida)

- **Noção:** Recurso que representa a vida de um personagem. Ao chegar a 0, o personagem é derrotado.
- **Impacto:**
  - É reduzido por [Dano](#l17-dano) recebido em combate.
  - Zerar o HP do [Jogador](#l01-jogador-player) leva ao estado de [Game Over](#l24-game-over).
  - Zerar o HP de todos os [Inimigos](#l02-inimigo) leva ao estado de [Vitória](#l23-vitória).

**Fonte:** Marcelo, 2026.

#### L16 - MP (Pontos de Magia)

- **Noção:** Recurso consumido para uso de habilidades especiais ou magias, quando aplicável.
- **Impacto:**
  - Pode ser restaurado através de [Usar Item](#l07-usar-item).

**Fonte:** Marcelo, 2026.

#### L17 - Dano

- **Noção:** Quantidade de [HP](#l15-hp-pontos-de-vida) subtraída de um alvo quando um ataque é bem-sucedido.
- **Impacto:**
  - Resulta da ação [Atacar](#l04-atacar) quando o [Desafio Matemático](#l14-desafio-matemático) é respondido corretamente.
  - Pode levar um personagem ao estado de derrota quando reduz seu HP a 0.

**Fonte:** Marcelo, 2026.

#### L18 - Item

- **Noção:** Objeto do inventário do [Jogador](#l01-jogador-player) que pode ser consumido através da ação [Usar Item](#l07-usar-item).
- **Impacto:**
  - Pode restaurar [HP](#l15-hp-pontos-de-vida) ou [MP](#l16-mp-pontos-de-magia), entre outros efeitos.

**Fonte:** Marcelo, 2026.

#### L19 - Loot

- **Noção:** Itens obtidos como recompensa ao derrotar [Inimigos](#l02-inimigo) ou explorar o mundo do jogo.
- **Impacto:**
  - Alimenta o inventário de [Itens](#l18-item) do Jogador.
  - É um dos objetivos da ação [Farmar](#l11-farmar).

**Fonte:** Marcelo, 2026.

#### L20 - Build

- **Noção:** Combinação de atributos, itens e habilidades escolhida para montar o [Jogador](#l01-jogador-player).
- **Impacto:**
  - É moldada pelo resultado de ações como [Upar](#l09-upar) e [Farmar](#l11-farmar).

**Fonte:** Marcelo, 2026.

#### L21 - HUD de Batalha

- **Noção:** Elementos de interface exibidos durante o combate, incluindo HP, MP, menu de ações e o prompt do [Desafio Matemático](#l14-desafio-matemático).
- **Impacto:**
  - É o principal meio de comunicação do estado da [Batalha](#l22-batalha) ao Jogador.

**Fonte:** Marcelo, 2026.

### ESTADO

#### L22 - Batalha

- **Noção:** Situação de combate por turnos ativa entre [Jogador](#l01-jogador-player) e um ou mais [Inimigos](#l02-inimigo).
- **Impacto:**
  - Habilita a fila de [Turnos](#l13-turno) e as ações do Jogador.
  - É encerrada pelos estados de [Vitória](#l23-vitória), [Game Over](#l24-game-over) ou pela ação [Fugir](#l08-fugir) bem-sucedida.

**Fonte:** Marcelo, 2026.

#### L23 - Vitória

- **Noção:** Estado alcançado quando todos os [Inimigos](#l02-inimigo) de uma [Batalha](#l22-batalha) são derrotados.
- **Impacto:**
  - Encerra a Batalha e pode conceder experiência e [Loot](#l19-loot) ao Jogador.

**Fonte:** Marcelo, 2026.

#### L24 - Game Over

- **Noção:** Estado alcançado quando o [HP](#l15-hp-pontos-de-vida) do [Jogador](#l01-jogador-player) chega a 0.
- **Impacto:**
  - Encerra a partida ou retorna o Jogador a um ponto de save/checkpoint anterior, conforme a regra do jogo.

**Fonte:** Marcelo, 2026.

#### L25 - AFK

- **Noção:** Estado de um jogador ausente/inativo (do inglês *"Away From Keyboard"*), sem interagir com o jogo por um período.
- **Impacto:**
  - Pode causar falha automática em um [Turno](#l13-turno) por ausência de resposta ao [Desafio Matemático](#l14-desafio-matemático).

**Fonte:** Marcelo, 2026.

## Bibliografia

SERRANO, Milene; SERRANO, Maurício. Requisitos – Aula 10.
