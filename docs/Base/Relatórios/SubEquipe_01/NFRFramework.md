# SubEquipe_01 — NFR Framework

## Descrição

Softgoal Interdependency Graph (SIG) da SubEquipe_01, no escopo do **FOCO_01**. Modela os critérios de qualidade **Jogabilidade** e **Usabilidade/UX** do sistema **G4_ProjetoJogo** na notação do NFR Framework.

## Objetivo

Modelar um requisito não funcional do projeto por meio de um SIG, decompondo o softgoal em subobjetivos e operacionalizações, com as respectivas contribuições.

## Metodologia

A modelagem seguiu o NFR Framework de Chung et al. (2000), que trata requisitos não funcionais como *softgoals* — objetivos sem critério binário de satisfação, refinados por decomposição até operacionalizações concretas e avaliados por rótulos de contribuição (MAKE, HELP, HURT, BREAK).

Foram escolhidos, com igual peso, os critérios **Jogabilidade** e **Usabilidade/UX**. A escolha partiu das reuniões de definição de escopo do subgrupo e do [Rich Picture](RichPicture.md) produzido a partir da engenharia reversa do jogo *Final Fantasy VI*, cujo ciclo central de observação foi o combate — ataque, uso de itens, gerenciamento de recursos e equipamentos — e a interação do jogador com a interface (HUD, menus e feedback de ações).

O softgoal raiz **Usabilidade/UX e Jogabilidade** foi decomposto por refinamento AND nos dois softgoals de mesmo nível:

- **Jogabilidade**, refinada (contribuição `+`) em três sub-softgoals: *Gerenciamento de Recursos*, *Progressão Estratégica* e *Feedback de Ações* — refletindo, respectivamente, a observação de como o jogador administra itens e recursos durante a batalha, como o personagem evolui (equipamentos, atributos) ao longo do jogo, e como o sistema comunica o resultado das ações do jogador.
- **Usabilidade/UX**, refinada (contribuição `+`) em *Clareza da Interface*, *Eficiência da Interação* e *Aprendizado* — alinhados, respectivamente, às heurísticas de Nielsen (1994) de correspondência/estética minimalista, flexibilidade e eficiência de uso, e reconhecimento em vez de memorização.

Os seis sub-softgoals convergem, todos com contribuição `+`, para uma operacionalização central — **Operacionalizações** —, que por sua vez se desdobra em dois mecanismos concretos identificados na engenharia reversa do jogo: **Sistema de Equipamentos**, sustentado pelas ações *Visualizar Mudanças*, *Equipar Personagem* e *Alterar Atributos*; e **Uso de Itens**, sustentado por *Consultar Itens*, *Escolher Alvo* e *Mostrar Efeitos*. Essa convergência representa que a satisfação conjunta dos seis softgoals de qualidade depende do mesmo par de mecanismos observados no jogo, evitando duplicar operacionalizações equivalentes para cada ramo.

O SIG foi construído na ferramenta web **DSM3Goals**, do Centro de Informática da UFPE (DSM3, 2026), a mesma adotada pelos demais subgrupos, por implementar diretamente a notação de Chung et al. (softgoals, decomposições e rótulos de contribuição).

A rastreabilidade com o [Rich Picture](RichPicture.md) foi mantida: os elementos Combate, Itens, Equipamentos e HUD que aparecem no artefato generalista são os mesmos reposicionados no SIG como meios de satisfazer Jogabilidade e Usabilidade/UX.

## Conteúdo

<p align="center">
  <img src="Base/Relatórios/SubEquipe_01/assets/subequipe01_sig_nfr_v1.png" alt="SIG na notação NFR Framework do G4_ProjetoJogo - Jogabilidade e Usabilidade/UX" width="100%">
</p>

<p align="center">Figura 1: SIG de Jogabilidade e Usabilidade/UX na notação do NFR Framework. Fonte: Yogi Nam de Souza Barbosa, 2026.</p>

## Referências

CHUNG, L.; NIXON, B. A.; YU, E.; MYLOPOULOS, J. **Non-Functional Requirements in Software Engineering**. Boston: Kluwer Academic Publishers, 2000. (The Kluwer International Series in Software Engineering, v. 5).

DSM3. **DSM3 Goal Modeling Tools: NFR Framework** [software]. Recife: Centro de Informática, Universidade Federal de Pernambuco, 2026. Disponível em: https://www.cin.ufpe.br/~jhcp/dsm3goals/nfr.html. Acesso em: 28 ago. 2026.

NIELSEN, Jakob. **10 Usability Heuristics for User Interface Design**. Nielsen Norman Group, 1994. Disponível em: https://www.nngroup.com/articles/ten-usability-heuristics/. Acesso em: 28 ago. 2026.

## Nível de Contribuição dos Integrantes

| Nome | % de Contribuição |
|------|-------------------|
| Cibelly Lourenço | 33,3% |
| Yogi Nam de Souza Barbosa | 33,3% |
| Gabriel Andrade Magioli | 33,3% |

<p align="center">Tabela 1: Contribuição dos integrantes. Fonte: Autores, 2026.</p>

## Histórico de Versão

| Versão | Data | Descrição | Autor(es) | Revisor |
|:------:|------|:----------|:----------|:--------|
| 1.0 | 22/08/2026 | Criação da página no modelo do artefato padrão | Marcelo de Araújo Lopes | |
| 1.1 | 28/08/2026 | Elaboração do SIG na notação do NFR Framework | Yogi Nam de Souza Barbosa, Cibelly Lourenço Ferreira | |
| 1.2 | 28/08/2026 | Preenchimento das seções Metodologia, Conteúdo, Referências e Contribuição dos integrantes | Cibelly Lourenço, Yogi Nam de Souza Barbosa, Gabriel Andrade Magioli | |

<p align="center">Tabela 2: Histórico de versão. Fonte: Autores, 2026.</p>

Ver também: [Artefato Generalista](ArtefatoGeneralista.md) · [Rich Picture](RichPicture.md) · [BPMN](BPMN.md) · [IA Generativa](IAGenerativa.md)