# SubEquipe_01 — NFR Framework

## Descrição

Softgoal Interdependency Graph (SIG) da SubEquipe_01, no escopo do **FOCO_01**. Modela os critérios de qualidade **Jogabilidade** e **Usabilidade/UX** do sistema **G4_ProjetoJogo** na notação do NFR Framework.

## Objetivo

Modelar critérios não funcionais do projeto por meio de um SIG, decompondo os *softgoals* em subobjetivos e operacionalizações, com as respectivas contribuições.

## Metodologia

A modelagem seguiu o NFR Framework de Chung et al. (2000), que trata requisitos não funcionais como *softgoals*, objetivos sem critério binário de satisfação, refinados por decomposição até operacionalizações concretas e avaliados por rótulos de contribuição (MAKE, HELP, HURT, BREAK).

Foram escolhidos, com igual peso, os critérios **Jogabilidade** e **Usabilidade/UX**, ênfases definidas para o G4_ProjetoJogo. Os mecanismos usados para operacionalizá-los foram recuperados pela [engenharia reversa de *Final Fantasy VI*](BPMN.md), especialmente nos fluxos de combate, uso de itens, gerenciamento de recursos e equipamentos. O [Rich Picture](RichPicture.md), elaborado anteriormente como artefato exploratório, também registra conceitos relacionados, como combate, itens, equipamentos e HUD.

O *softgoal* raiz **Usabilidade/UX e Jogabilidade** foi decomposto por refinamento AND nos dois *softgoals* de mesmo nível:

- **Jogabilidade**, refinada (contribuição `+`) em três sub-*softgoals*: *Gerenciamento de Recursos*, *Progressão Estratégica* e *Feedback de Ações*, refletindo, respectivamente, a observação de como o jogador administra itens e recursos durante a batalha, como o personagem evolui (equipamentos, atributos) ao longo do jogo e como o sistema comunica o resultado das ações do jogador.
- **Usabilidade/UX**, refinada (contribuição `+`) em *Clareza da Interface*, *Eficiência da Interação* e *Aprendizado*, alinhados, respectivamente, às heurísticas de Nielsen (1994) de correspondência e estética minimalista, flexibilidade e eficiência de uso e reconhecimento em vez de memorização.

Os seis sub-*softgoals* convergem, todos com contribuição `+`, para uma operacionalização central, **Operacionalizações**, que por sua vez se desdobra em dois mecanismos concretos identificados na engenharia reversa do jogo: **Sistema de Equipamentos**, sustentado pelas ações *Visualizar Mudanças*, *Equipar Personagem* e *Alterar Atributos*; e **Uso de Itens**, sustentado por *Consultar Itens*, *Escolher Alvo* e *Mostrar Efeitos*. Essa convergência representa que a satisfação conjunta dos seis *softgoals* de qualidade depende do mesmo par de mecanismos observados no jogo, evitando duplicar operacionalizações equivalentes para cada ramo.

O SIG foi construído na ferramenta web **DSM3Goals**, do Centro de Informática da UFPE (DSM3, 2026), a mesma adotada pelos demais subgrupos, por implementar diretamente a notação de Chung et al. (softgoals, decomposições e rótulos de contribuição).

A rastreabilidade com o [Rich Picture](RichPicture.md) foi mantida: os elementos Combate, Itens, Equipamentos e HUD que aparecem no artefato generalista são os mesmos reposicionados no SIG como meios de satisfazer Jogabilidade e Usabilidade/UX.

## Conteúdo

<p align="center">
  <img src="Base/Relatórios/SubEquipe_01/assets/subequipe01_sig_nfr_v1.png" alt="SIG na notação NFR Framework do G4_ProjetoJogo - Jogabilidade e Usabilidade/UX" width="100%">
</p>

<p align="center">Figura 1: SIG de Jogabilidade e Usabilidade/UX na notação do NFR Framework. Fonte: Cibelly Lourenço Ferreira, Gabriel Andrade Magioli e Yogi Nam de Souza Barbosa, 2026.</p>

O SIG é útil para relacionar as qualidades pretendidas a funcionalidades observáveis e orientar decisões futuras do projeto. Como limitação, o modelo concentra contribuições positivas e ainda não explicita conflitos entre jogabilidade e simplicidade de uso; esses impactos deverão ser reavaliados quando houver requisitos e protótipos mais detalhados.

## Referências

CHUNG, L.; NIXON, B. A.; YU, E.; MYLOPOULOS, J. **Non-Functional Requirements in Software Engineering**. Boston: Kluwer Academic Publishers, 2000. (The Kluwer International Series in Software Engineering, v. 5).

DSM3. **DSM3 Goal Modeling Tools: NFR Framework** [software]. Recife: Centro de Informática, Universidade Federal de Pernambuco, 2026. Disponível em: https://www.cin.ufpe.br/~jhcp/dsm3goals/nfr.html. Acesso em: 28 ago. 2026.

NIELSEN, Jakob. **10 Usability Heuristics for User Interface Design**. Nielsen Norman Group, 1994. Disponível em: https://www.nngroup.com/articles/ten-usability-heuristics/. Acesso em: 28 ago. 2026.

## Nível de Contribuição dos Integrantes

| Nome | % de Contribuição |
|------|-------------------|
| Cibelly Lourenço Ferreira | 33,4% |
| Gabriel Andrade Magioli | 33,3% |
| Yogi Nam de Souza Barbosa | 33,3% |

<p align="center">Tabela 1: Contribuição dos integrantes.</p>

## Histórico de Versão

| Versão | Data | Descrição | Autor(es) | Revisor |
|:------:|------|:----------|:----------|:--------|
| 1.0 | 22/08/2026 | Criação da página no modelo do artefato padrão | Marcelo de Araújo Lopes | Marcos Vinícius Gündel da Silva |
| 1.1 | 28/08/2026 | Elaboração do SIG na notação do NFR Framework | Cibelly Lourenço Ferreira, Gabriel Andrade Magioli e Yogi Nam de Souza Barbosa | Marcos Vinícius Gündel da Silva |
| 1.2 | 28/08/2026 | Preenchimento das seções Metodologia, Conteúdo, Referências e Contribuição dos integrantes | Cibelly Lourenço Ferreira, Gabriel Andrade Magioli e Yogi Nam de Souza Barbosa | Marcos Vinícius Gündel da Silva |
| 1.3 | 28/08/2026 | Correção da rastreabilidade, da autoria e das fontes das tabelas; inclusão da análise crítica do SIG | Yogi Nam de Souza Barbosa | Marcos Vinícius Gündel da Silva |

<p align="center">Tabela 2: Histórico de versão.</p>

Ver também: [Rich Picture](RichPicture.md) · [Engenharia Reversa e BPMN](BPMN.md) · [IA Generativa](IAGenerativa.md)
