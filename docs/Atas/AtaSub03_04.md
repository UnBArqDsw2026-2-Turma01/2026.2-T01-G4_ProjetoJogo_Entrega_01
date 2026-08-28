# Ata — Reunião de Engenharia Reversa e Fluxos

## Identificação

| Data | Horário de Início | Horário de Término | Local | Projeto | Redator |
| :--: | :---------------: | :----------------: | :---: | :-----: | :-----: |
| 25/08/2026 | 19:31 | 21:20 | Google Meet | RPG Didático | Gemini PRO 3.1 |

<p align="center">Tabela 1: Identificação da reunião. Fonte: transcrição automática da reunião, 2026.</p>

## Participantes da Reunião

| Convocados | Presente (Sim/Não) |
| :--------- | :----------------: |
| Carlos Henrique Brasil de Souza | Sim |
| Pedro Teixeira | Sim |
| Renan Pereira Reis | Não |

<p align="center">Tabela 2: Participantes da reunião. Fonte: transcrição automática da reunião, 2026.</p>

## Pauta

| Nº | Descrição |
| :-: | :-------- |
| 1 | Metodologia e escolha de jogo para engenharia reversa |
| 2 | Refinamento e montagem dos fluxos e subfluxos do diagrama BPMN |
| 3 | Definição do sistema de salvamento e integração com criação de itens |
| 4 | Lógica do sistema de combate (verificações de vida, morte e dano) |

<p align="center">Tabela 3: Pauta reconstruída a partir dos assuntos discutidos. Fonte: transcrição automática da reunião, 2026.</p>

## Pendências Anteriores

| Nº | Pendência | Responsável | Data |
| :-: | :-------- | :---------- | :--: |
| 1 | Concluir e revisar o diagrama BPMN modelado na ferramenta Miro. | Pedro Teixeira e O Grupo | Reunião anterior (24/08) |

<p align="center">Tabela 4: Pendências anteriores. Fonte: transcrição automática da reunião, 2026.</p>

## Assuntos Tratados

| Nº | Descrição | Tipo |
| :-: | :-------- | :--: |
| 1 | O jogo *Final Fantasy 6* foi selecionado como alvo oficial para a aplicação da engenharia reversa, utilizando pequenos vídeos de gameplay focados em mecânicas pontuais, sem narrações complexas. | 2 |
| 2 | O grupo estabeleceu que ambos os métodos de salvamento ('Save State' e 'Save Point') fariam parte do fluxograma, a fim de espelhar com exatidão a natureza dos salvamentos de áreas diferentes do jogo de inspiração. | 2 |
| 3 | As mecânicas de "livros" e "criação de itens" foram unificadas e incorporadas ao processo de exploração do mundo, ao invés de mantê-las em fluxos separados, visando reduzir a complexidade. | 3 |
| 4 | Para simplificar o sistema e o diagrama BPMN, decidiu-se que o fluxo de batalha será construído de modo que o jogador sempre encare apenas um inimigo por vez. | 2 |
| 5 | O fluxo do combate em si teve suas etapas de lógica aprofundadas. Foi adicionada uma transição de retorno de ação rotulada como "Receber dano do inimigo" e também uma condicional no fluxograma gerando "Zero dano", para o caso de o inimigo ser imune aos efeitos aplicados pelo jogador. | 3 |

<p align="center">Tabela 5: Assuntos tratados. Fonte: transcrição automática da reunião, 2026.</p>

> **Tipos:** 1. Apresentação · 2. Decisão · 3. Definição · 4. Solicitação · 5. Pendência.

## Próxima Reunião

Não agendada explicitamente no registro desta chamada.

## Compromissos

| Nº | Compromisso | Responsável | Data |
| :-: | :---------- | :---------- | :--: |
| 1 | Gravar vídeos do Final Fantasy mostrando salvamento, NPCs, combates, entre outros, para compor as evidências da GD reversa. | Pedro Teixeira | Não especificado |
| 2 | Rotular, analisar os vídeos e realizar o envio (upload) para o GitHub. | Pedro Teixeira e Carlos Henrique Brasil de Souza | Não especificado |
| 3 | Pesquisar se o jogo que possui mecânicas de misturas químicas/alquimia ainda está disponível para integrar as evidências. | Pedro Teixeira | Não especificado |
| 4 | Criar uma nova "branch" no repositório focada na inclusão de conteúdos de SIG, Engenharia Reversa e BPMN. | O grupo | Não especificado |
| 5 | Subir o registro em vídeo referente à primeira reunião no GitHub. | Renan Pereira Reis | Não especificado |

<p align="center">Tabela 6: Compromissos acordados. Fonte: transcrição automática da reunião, 2026.</p>

## Gravação da Reunião

- **[Gravação em Vídeo](https://drive.google.com/file/d/1KSsYQcXpdarHbqYHONZTvyz980tWq1vh/view?usp=drive_web)**
- **[Transcrição Automática](https://docs.google.com/document/d/1Mq_PcWWaM1ecLhRE9nlffmOxu33VCC_QqF1Sob47AUM/edit?usp=drive_web&tab=t.9mivrett4n9w)**

## Histórico de Versão

| Versão | Data | Descrição | Autor(es) | Revisor |
|:------:|------|:----------|:----------|:--------|
| 1.0 | 27/08/2026 | Criação da ata com base na transcrição automática da reunião | Gemini PRO 3.1 | Pedro Teixeira Moriel Sanchez |

<p align="center">Tabela 7: Histórico de versão.</p>
