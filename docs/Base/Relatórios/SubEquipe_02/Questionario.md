# SubEquipe_02 — Questionário

## Descrição

Registro da iniciativa extra da SubEquipe_02, no escopo do **FOCO_01**. Trata-se de um **questionário estruturado**, aplicado de forma digital via *Google Forms*, cujo propósito foi **levantar a importância atribuída pelos jogadores aos diferentes tipos de requisitos não-funcionais**, com foco em usabilidade e experiência do usuário, de um jogo RPG como o **G4_ProjetoJogo**.

Intitulado *"Avaliação de Usabilidade e Experiência de Usuário de jogos RPG (Heurísticas de Nielsen)"*, o instrumento traduz cada critério de qualidade candidato em uma afirmação avaliada por escala de concordância, tomando como referência as dez heurísticas de usabilidade de *Nielsen (1994)* adaptadas ao contexto de RPG, e complementa a coleta com fatores de experiência do usuário identificados durante a modelagem do [Rich Picture](RichPicture.md).

A iniciativa deriva da [Ata 01 — Reunião Subgrupo 02](/Atas/AtaSub02_01.md) e está registrada na fase [1. Understand](/Base/1.1.1.Understand.md) do Design Sprint. Este documento consolida **o instrumento aplicado e as respostas coletadas**.

## Objetivo

- **Levantar a importância dos tipos de requisitos não-funcionais:** medir, junto a jogadores, o grau de importância atribuído a cada critério de usabilidade e experiência do usuário aplicável a um jogo RPG.
- **Validar hipóteses da equipe:** confrontar com dados concretos as hipóteses levantadas com apoio da IA generativa *Gemini* (GOOGLE, 2026) e representadas no [Rich Picture](RichPicture.md) sobre os fatores que impactam a jogabilidade e a experiência do usuário — em especial os ciclos de *feedback* de percepção negativa (mecânicas *pay-to-win*) e a influência de criadores de conteúdo, discutidos nos itens 6, 7 e 8 dos assuntos tratados da [Ata 01 — Reunião Subgrupo 02](/Atas/AtaSub02_01.md).

## Metodologia

A técnica adotada foi o **questionário**, empregado como instrumento de elicitação e validação de requisitos junto a *stakeholders*, conforme *Barbosa et al. (2021)*. O processo seguiu as etapas descritas a seguir.

Na primeira reunião do Subgrupo 02, realizada em 19/08/2026 (ver [Ata 01 — Reunião Subgrupo 02](/Atas/AtaSub02_01.md)), João Igor propôs a criação de um questionário via *Google Forms* para **validar as hipóteses geradas pelo Gemini sobre a experiência do usuário**, com meta de **10 a 15 respostas** para embasar o relatório final. A elaboração e a gestão do formulário ficaram sob responsabilidade de João Victor da Silva Batista de Farias.

O formulário foi estruturado com base nas **dez heurísticas de usabilidade de Nielsen (1994)**, traduzidas em afirmações contextualizadas para um jogo RPG, e acrescido de **quatro fatores de experiência do usuário** decorrentes das hipóteses do [Rich Picture](RichPicture.md) (monetização/*pay-to-win*, conquistas externas, narrativa e imersão, e influência de criadores de conteúdo). A composição foi a seguinte:

- **Termo de Consentimento (LGPD):** abertura do formulário com termo informando que os dados seriam usados apenas para fins de pesquisa e tratados de forma anônima e agregada, com canal para solicitação de retirada de dados (*fariassilva.jb@gmail.com*). Todas as respostas registradas contêm o aceite explícito do termo.
- **Pergunta de perfil:** *"Quantos RPGs você já jogou?"*, com as opções `1`, `2-5`, `5-10` e `10 ou mais`, para segmentação dos respondentes por experiência prévia.
- **Afirmações fechadas:** 13 afirmações no formato *"É importante para mim que..."*, avaliadas em **escala linear de 1 a 5**, na qual valores mais altos indicam maior concordância com a importância do atributo descrito.
- **Campos de *feedback* opcionais:** espaço livre associado a cada questão; não foi preenchido por nenhum respondente.

O mapeamento entre cada afirmação e o requisito não-funcional investigado é apresentado na [Tabela 1](#tabela-1).

### Aplicação e coleta

O questionário foi distribuído digitalmente pelo *Google Forms* a uma **amostra por conveniência** (grupo de amigos e conhecidos do subgrupo). A coleta ocorreu **entre 20 e 27 de agosto de 2026**, resultando em **14 respostas válidas**, dentro da meta de 10 a 15 estabelecida na reunião. O formulário também está registrado na seção *Questionário* da fase [1. Understand](/Base/1.1.1.Understand.md).

## Conteúdo

### Instrumento

<a id="tabela-1"></a>

| # | Afirmação (resumo) | Requisito não-funcional / heurística de Nielsen investigada |
|:--:|--------------------|-----------------------------------------------------------|
| Q1 | Acesso visual imediato e claro a atributos vitais, efeitos de status e progresso de missões em tempo real | Visibilidade do status do sistema (H1) |
| Q2 | Ícones, termos e metáforas visuais condizentes com a lógica do universo do jogo | Correspondência entre o sistema e o mundo real (H2) |
| Q3 | Comandos, atalhos e comportamentos de interface consistentes em todas as telas | Consistência e padrões (H4) |
| Q4 | Confirmação ou aviso antes de ações irreversíveis (vender itens raros, gastar recursos escassos) | Prevenção de erros e controle/liberdade do usuário (H5/H3) |
| Q5 | Visualizar requisitos de combate e detalhes de missões na tela atual, sem memorizar menus anteriores | Reconhecimento em vez de memorização (H6) |
| Q6 | Atalhos rápidos e personalização para agilizar tarefas repetitivas de inventário e combate | Flexibilidade e eficiência de uso (H7) |
| Q7 | Interface limpa, exibindo apenas dados contextualmente relevantes, sem poluição visual | Estética e design minimalista (H8) |
| Q8 | Explicações claras sobre o motivo de uma ação ter falhado (falta de mana, alcance) e como corrigi-la | Ajudar a reconhecer, diagnosticar e recuperar-se de erros (H9) |
| Q9 | Orientações claras sobre objetivos, controles e mecânicas de habilidades | Ajuda e documentação (H10) |
| Q10 | Vantagens pagas com dinheiro real (*pay-to-win*) reduzem a motivação e comprometem a diversão | Fator de UX: monetização (*pay-to-win*); hipótese do Rich Picture |
| Q11 | Conquistas externas (Steam, consoles) como incentivo para continuar jogando e explorar conteúdo opcional | Fator de UX: engajamento e retenção |
| Q12 | História rica e personagens bem desenvolvidos que sustentem o interesse pelo universo ficcional | Fator de UX: narrativa e imersão |
| Q13 | Opiniões e transmissões de influenciadores moldam expectativas e a forma de avaliar a experiência | Fator de UX: influência de criadores de conteúdo; hipótese do Rich Picture |

<p align="center">Tabela 1: Instrumento do questionário — afirmações e requisitos não-funcionais investigados. Fonte: SILVA, Marcos; FARIAS, João; COSTA, João (2026), com base em Nielsen (1994) e no formulário de pesquisa aplicado pela subequipe.</p>

### Perfil dos respondentes

| Quantos RPGs já jogou? | Respondentes |
|------------------------|:------------:|
| 1 | 1 |
| 2 a 5 | 2 |
| 5 a 10 | 6 |
| 10 ou mais | 5 |
| **Total** | **14** |

<p align="center">Tabela 2: Perfil dos respondentes quanto à experiência prévia com RPGs. Fonte: SILVA, Marcos; FARIAS, João; COSTA, João (2026).</p>

### Respostas individuais

| Respondente | RPGs jogados | Q1 | Q2 | Q3 | Q4 | Q5 | Q6 | Q7 | Q8 | Q9 | Q10 | Q11 | Q12 | Q13 |
|:-----------:|:------------:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:---:|:---:|:---:|:---:|
| R01 | 2–5 | 5 | 5 | 5 | 4 | 4 | 5 | 5 | 4 | 5 | 5 | 2 | 5 | 5 |
| R02 | 5–10 | 5 | 5 | 2 | 5 | 3 | 5 | 4 | 5 | 4 | 4 | 4 | 4 | 1 |
| R03 | 10 ou mais | 3 | 5 | 4 | 4 | 4 | 4 | 5 | 4 | 4 | 5 | 3 | 5 | 2 |
| R04 | 10 ou mais | 3 | 4 | 3 | 4 | 5 | 5 | 5 | 4 | 4 | 5 | 5 | 5 | 1 |
| R05 | 10 ou mais | 3 | 5 | 5 | 1 | 2 | 4 | 5 | 3 | 4 | 5 | 5 | 5 | 2 |
| R06 | 5–10 | 1 | 5 | 5 | 5 | 1 | 4 | 3 | 4 | 4 | 3 | 4 | 4 | 1 |
| R07 | 10 ou mais | 3 | 3 | 3 | 3 | 3 | 3 | 3 | 3 | 3 | 3 | 3 | 3 | 3 |
| R08 | 5–10 | 3 | 4 | 2 | 4 | 2 | 5 | 4 | 5 | 2 | 5 | 5 | 5 | 4 |
| R09 | 2–5 | 4 | 5 | 4 | 5 | 5 | 5 | 5 | 3 | 4 | 4 | 2 | 4 | 2 |
| R10 | 5–10 | 3 | 4 | 2 | 1 | 4 | 3 | 5 | 5 | 3 | 3 | 4 | 5 | 4 |
| R11 | 10 ou mais | 5 | 4 | 5 | 5 | 5 | 5 | 5 | 5 | 5 | 3 | 3 | 3 | 3 |
| R12 | 5–10 | 3 | 5 | 2 | 1 | 2 | 4 | 5 | 5 | 4 | 5 | 4 | 5 | 2 |
| R13 | 1 | 3 | 3 | 3 | 2 | 2 | 3 | 3 | 2 | 3 | 3 | 3 | 3 | 2 |
| R14 | 5–10 | 5 | 5 | 5 | 5 | 3 | 3 | 5 | 5 | 5 | 5 | 5 | 5 | 3 |

<p align="center">Tabela 3: Respostas individuais ao questionário, em escala de 1 a 5. Coleta entre 20 e 24 de agosto de 2026. Fonte: SILVA, Marcos; FARIAS, João; COSTA, João (2026).</p>

### Distribuição das respostas por afirmação

| Afirmação | 1 | 2 | 3 | 4 | 5 | n |
|-----------|:-:|:-:|:-:|:-:|:-:|:-:|
| Q1: Visibilidade do status do sistema | 1 | 0 | 8 | 1 | 4 | 14 |
| Q2: Correspondência com o mundo real | 0 | 0 | 2 | 4 | 8 | 14 |
| Q3: Consistência e padrões | 0 | 4 | 3 | 2 | 5 | 14 |
| Q4: Prevenção de erros / ações irreversíveis | 3 | 1 | 1 | 4 | 5 | 14 |
| Q5: Reconhecimento em vez de memorização | 1 | 4 | 3 | 3 | 3 | 14 |
| Q6: Flexibilidade e eficiência de uso | 0 | 0 | 4 | 4 | 6 | 14 |
| Q7: Estética e design minimalista | 0 | 0 | 3 | 2 | 9 | 14 |
| Q8: Recuperação de erros (mensagens de falha) | 0 | 1 | 3 | 4 | 6 | 14 |
| Q9: Ajuda e documentação | 0 | 1 | 3 | 7 | 3 | 14 |
| Q10: *Pay-to-win* compromete a experiência | 0 | 0 | 5 | 2 | 7 | 14 |
| Q11: Conquistas externas como incentivo | 0 | 2 | 4 | 4 | 4 | 14 |
| Q12: Narrativa e personagens | 0 | 0 | 3 | 3 | 8 | 14 |
| Q13: Influência de criadores de conteúdo | 3 | 5 | 3 | 2 | 1 | 14 |

<p align="center">Tabela 4: Distribuição de frequência das respostas por afirmação (contagem de respostas em cada ponto da escala). Fonte: SILVA, Marcos; FARIAS, João; COSTA, João (2026).</p>

## Referências

BARBOSA, S. D. J.; SILVA, B. S. da; SILVEIRA, M. S.; GASPARINI, I.; DARIN, T.; BARBOSA, G. D. J. **Interação Humano-Computador e Experiência do Usuário**. Autopublicação, 2021. ISBN 978-65-00-19677-1.

GOOGLE. **Gemini** [software]. Versão Flash 3.7 Estendido. Resposta à consulta sobre os elementos principais de um jogo RPG. [S.l.]: Google LLC, 2026. Disponível em: https://gemini.google.com. Acesso em: 19 ago. 2026.

GOOGLE. **Google Forms** [software]. Disponível em: https://forms.google.com. Acesso em: 27 ago. 2026.

NIELSEN, Jakob. **10 Usability Heuristics for User Interface Design**. Nielsen Norman Group, 1994. Disponível em: https://www.nngroup.com/articles/ten-usability-heuristics/. Acesso em: 27 ago. 2026.

## Nível de Contribuição dos Integrantes

| Nome | % de Contribuição |
|------|-------------------|
| João Igor Pereira da Costa | 30,0% |
| João Victor da Silva Batista de Farias | 50,0% |
| Marcelo de Araújo Lopes | 0,0% |
| Marcos Vinícius Gündel da Silva | 20,0% |

<p align="center">Tabela 5: Contribuição dos integrantes.</p>

## Histórico de Versão

| Versão | Data | Descrição | Autor(es) | Revisor |
|:------:|------|:----------|:----------|:--------|
| 1.0 | 19/08/2026 | Ideação do Questionário | João Igor Pereira da Costa | |
| 1.1 | 20/08/2026 | Criação do Questionário | João Victor da Silva Batista de Farias | |
| 1.2 | 27/08/2026 | Limpeza dos dados do questionário; Relação com as Heurísticas de Nielsen e preenchimento da seção de metodologia | Marcos Vinícius Gündel da Silva | |

<p align="center">Tabela 6: Histórico de versão.</p>

Ver também: [Rich Picture](RichPicture.md) · [Léxico](Lexico.md) · [NFR Framework](NFRFramework.md) · [BPMN](BPMN.md) · [IA Generativa](IAGenerativa.md) · [Artefato Generalista](ArtefatoGeneralista.md) · [Ata 01 — Reunião Subgrupo 02](/Atas/AtaSub02_01.md) · [1. Understand](/Base/1.1.1.Understand.md)
