# SubEquipe_02 — NFR Framework

## Descrição

Softgoal Interdependency Graph (SIG) da SubEquipe_02, no escopo do **FOCO_01**. Modela um critério de qualidade do sistema **G4_ProjetoJogo** na notação do NFR Framework.

## Objetivo

Modelar um requisito não funcional do projeto por meio de um SIG, decompondo o softgoal em subobjetivos e operacionalizações, com as respectivas contribuições.

## Metodologia

A modelagem seguiu o NFR Framework de Chung et al. (2000), abordagem orientada a processo que trata requisitos não funcionais como *softgoals*, objetivos sem critério binário de satisfação que são refinados até operacionalizações e avaliados por propagação de rótulos. O grafo resultante, o *Softgoal Interdependency Graph* (SIG), reúne *NFR softgoals*, *operationalizing softgoals* e *claim softgoals*, ligados por decomposições AND e OR e por contribuições dos tipos MAKE (++), HELP (+), HURT (-) e BREAK (--).

Foram escolhidos dois critérios de qualidade com igual peso: Jogabilidade e Usabilidade/UX. A escolha decorre do escopo fixado na [Ata 01 — Reunião Subgrupo 02](/Atas/AtaSub02_01.md), que delimitou o G4_ProjetoJogo com foco em usabilidade e experiência do usuário, e do [Rich Picture](RichPicture.md), organizado em torno do Jogador e do ciclo central de Combate e Exploração. São também os dois critérios investigados pelo [Questionário](Questionario.md) da subequipe.

Jogabilidade foi decomposta (AND) em Fluida e Divertida. Divertida recebe contribuição de Exploração e de Combate, e Fluida recebe contribuição de Geração procedural de mapas e encontros e de Viagem Rápida. Exploração refina-se em Achar tesouros, Encontrar outros NPC e encontrar novas áreas, esta última desdobrada em Encontrar novos recursos, criar novos itens e Novos Monstros. Combate refina-se em Encontrar inimigos, Gastar recursos durante a luta, Vida, Controles e Árvore de Habilidades, e Controles abrange Atacar, Fugir, Usar algum item e Mapeamento de Botões. Usabilidade/UX foi decomposta (AND) em HUD com todas as informações e Tutorial: o HUD recebe contribuição de Minimapa Dinâmico, Feedback Visual de Dano, Combate e Controles, e o Tutorial recebe contribuição de Dicas Contextuais e do Livro do aventureiro. Dois *claim softgoals* registram a justificativa das contribuições negativas: o jogador precisa de itens coletados para sustentar o combate, e fugir de uma luta pode fazer o jogador perder vida.

O SIG foi construído na ferramenta web DSM3, módulo NFR Framework (DSM3, 2026), aplicação do Centro de Informática da UFPE que implementa a notação de Chung et al. (softgoals, contribuições e *claims*) e exporta em PNG e SVG. Optou-se por ela, e não pelo Miro adotado no Rich Picture, pelo suporte direto aos elementos do NFR Framework.

A rastreabilidade com o [Rich Picture](RichPicture.md) versão 2 foi mantida item a item: Combate, Exploração, Mapa, Vila, NPC, Ferreiro, Monstro, Boss, XP, Itens, Tesouros e o Livro do jogador, aqui chamado Livro do aventureiro, já constavam do artefato generalista. O SIG parte desses elementos e os reposiciona como meios de satisfazer Jogabilidade e Usabilidade/UX, sem introduzir conceitos fora do domínio validado.

O sinal e a força das contribuições para Usabilidade/UX foram calibrados pelos resultados do [Questionário](Questionario.md), com 14 respostas válidas em escala de 1 a 5 e afirmações derivadas das heurísticas de Nielsen (1994). A concordância alta com estética e design minimalista (Q7) e com correspondência com o mundo real (Q2) sustenta as contribuições MAKE das operacionalizações de HUD e de interface, enquanto a baixa importância atribuída à influência de criadores de conteúdo (Q13) manteve esse fator fora do SIG, e a rejeição a mecânicas *pay-to-win* (Q10) embasou a decisão de não operacionalizar compras dentro de Jogabilidade.

A versão 1 fixou os softgoals raiz e a primeira decomposição. A versão 2 reorganizou o grafo em torno do Jogador, acrescentou as operacionalizações Minimapa Dinâmico, Dicas Contextuais, Feedback Visual de Dano, Árvore de Habilidades e Mapeamento de Botões, e explicitou os *claim softgoals*.

## Conteúdo

### Versão 1

<p align="center">
  <img src="Base/Relatórios/SubEquipe_02/assets/subequipe02_sig_nfr_v1.png" alt="SIG na notação NFR Framework do G4_ProjetoJogo - Versão 1" width="100%">
</p>

<p align="center">Figura 1: Versão 1 SIG na notação NFR Framework. Fonte: LOPES, Marcelo (2026).</p>

### Versão 2

<p align="center">
  <img src="Base/Relatórios/SubEquipe_02/assets/subequipe02_sig_nfr_v2.png" alt="SIG na notação NFR Framework do G4_ProjetoJogo - Versão 2" width="100%">
</p>

<p align="center">Figura 2: Versão 2 SIG na notação NFR Framework. Fonte: SILVA, Marcos; FARIAS, João; COSTA, João (2026).</p>

## Referências

CHUNG, L.; NIXON, B. A.; YU, E.; MYLOPOULOS, J. **Non-Functional Requirements in Software Engineering**. Boston: Kluwer Academic Publishers, 2000. (The Kluwer International Series in Software Engineering, v. 5).

DSM3. **DSM3 Goal Modeling Tools: NFR Framework** [software]. Recife: Centro de Informática, Universidade Federal de Pernambuco, 2026. Disponível em: https://www.cin.ufpe.br/~jhcp/dsm3goals/nfr.html. Acesso em: 28 ago. 2026.

NIELSEN, Jakob. **10 Usability Heuristics for User Interface Design**. Nielsen Norman Group, 1994. Disponível em: https://www.nngroup.com/articles/ten-usability-heuristics/. Acesso em: 28 ago. 2026.

## Nível de Contribuição dos Integrantes

| Nome | % de Contribuição |
|------|-------------------|
| João Igor Pereira da Costa | 25% |
| João Victor da Silva Batista de Farias | 25% |
| Marcelo de Araújo Lopes | 25% |
| Marcos Vinícius Gündel da Silva | 25% |

<p align="center">Tabela 1: Contribuição dos integrantes.</p>

## Histórico de Versão

| Versão | Data | Descrição | Autor(es) | Revisor |
|:------:|------|:----------|:----------|:--------|
| 1.0 | 22/08/2026 | Criação da página no modelo do artefato padrão | Marcelo de Araújo Lopes | Marcos Vinícius Gündel da Silva |
| 1.1 | 23/08/2026 | Elaboração da versão 1 do SIG na notação do NFR Framework | Marcelo de Araújo Lopes | |
| 1.2 | 28/08/2026 | Elaboração da versão 2 do SIG na notação do NFR Framework | Marcos Vinícius Gündel da Silva | |
| 1.3 | 28/08/2026 | Preenchimento das seções Metodologia e Referências | Marcos Vinícius Gündel da Silva | |

<p align="center">Tabela 2: Histórico de versão.</p>

Ver também: [Artefato Generalista](ArtefatoGeneralista.md) · [Léxico](Lexico.md) · [Rich Picture](RichPicture.md) · [Questionário](Questionario.md) · [BPMN](BPMN.md) · [IA Generativa](IAGenerativa.md)
