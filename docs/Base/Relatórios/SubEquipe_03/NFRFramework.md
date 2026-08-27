# SubEquipe_03 — NFR Framework

## Descrição

Softgoal Interdependency Graph (SIG) da SubEquipe_03, no escopo do **FOCO_01 — Artefatos Generalistas & NFR Framework**. O grafo modela o requisito não funcional **Usabilidade & UX** do **G4_ProjetoJogo** na notação do NFR Framework, decompondo-o em cinco sub-NFRs, associando operacionalizações concretas do jogo a cada um deles e explicitando um conflito entre dois desses sub-NFRs.

## Objetivo

Modelar de forma rastreável como a qualidade *Usabilidade & UX* se realiza no projeto, evidenciando quais funcionalidades contribuem para quais aspectos dessa qualidade, com que intensidade, e onde há tensão entre eles — de modo que as decisões de projeto fiquem justificadas e não arbitrárias.

## Metodologia

### Escolha do softgoal

O softgoal **Usabilidade & UX [RPG Didático]** foi escolhido por ser a ênfase central atribuída ao projeto: *Jogabilidade e Usabilidade/Experiência de Usuário*. A escolha não foi arbitrária — partiu do [Mapa Mental](MapaMental.md), artefato generalista desta mesma entrega, de onde foram extraídas as funcionalidades que se tornaram operacionalizações no grafo: HUD e Livro do Aventureiro, Inventário e atalhos, Combate em turnos, Mistura de Elementos Químicos, NPCs e narrativa.

### Decomposição

A decomposição em cinco sub-NFRs teve duas origens distintas, e vale distingui-las:

- **Quatro derivam das heurísticas de usabilidade de Nielsen:** Estética Minimalista (heurística de *design estético e minimalista*), Correspondência (*correspondência entre o sistema e o mundo real*), Flexibilidade (*flexibilidade e eficiência de uso*) e Recuperação de Erros (*ajudar os usuários a reconhecer, diagnosticar e recuperar-se de erros*).
- **Um não deriva de Nielsen:** *Imersão [Narrativa e Personagens]* foi incorporado por ser específico do domínio de jogos — as heurísticas de Nielsen tratam de interfaces de uso geral e não capturam o envolvimento narrativo, que é determinante para a experiência em um RPG. Sua inclusão foi sustentada pelo dado empírico descrito a seguir.

### Priorização por questionário

Para não priorizar os sub-NFRs por intuição, foi aplicado um questionário sobre usabilidade e experiência de usuário em jogos RPG, estruturado a partir das heurísticas de Nielsen, com escala de 1 a 5 e **14 respondentes**, dos quais 11 declararam já ter jogado 5 ou mais RPGs. A coleta foi precedida de termo de consentimento em conformidade com a LGPD, e os dados são aqui apresentados de forma agregada.

As médias obtidas foram usadas para dois fins: selecionar quais aspectos entrariam no grafo e justificar os rótulos de contribuição. Os quatro sub-NFRs derivados de Nielsen correspondem exatamente aos quatro itens de interface mais bem avaliados pela amostra; os itens com médias menores — consistência de padrões (3,57), visibilidade do estado do sistema (3,50), prevenção de erros (3,50) e reconhecimento em vez de memorização (3,21) — foram deixados fora do escopo deste SIG.

### Modelagem

A modelagem seguiu o método do NFR Framework (CHUNG et al., 2000), empregando decomposição, operacionalizações, rótulos de contribuição e *claims* como justificativas explícitas. A ferramenta utilizada foi a **DSM3Goals** (https://www.cin.ufpe.br/~jhcp/dsm3goals/nfr.html).

### Limitações

Três limitações devem ser consideradas na leitura dos resultados: a amostra é pequena (n=14) e obtida por conveniência, não sendo estatisticamente representativa; as respostas medem **importância autodeclarada**, não comportamento observado em uso real; e a amostra é enviesada para jogadores experientes, o que pode superestimar a importância de recursos de eficiência como atalhos. Um dos itens apresentou dispersão alta (desvio-padrão de 1,55 na confirmação antes de ações irreversíveis), indicando que essa preferência divide a amostra.

## Conteúdo

![SIG de Usabilidade e UX na notação do NFR Framework](SIG.png ':size=100%')

<p align="center">Figura 1: SIG de Usabilidade &amp; UX [RPG Didático] na notação do NFR Framework. Fonte: Renan Pereira Reis, 2026.</p>

### Sub-NFRs e sustentação empírica

| Sub-NFR no SIG | Item avaliado no questionário | Média (1–5) |
|----------------|-------------------------------|:-----------:|
| Correspondência [Ícones e Metáforas] | Ícones, termos e metáforas intuitivos e condizentes com o universo do jogo | **4,43** |
| Estética Minimalista [HUD] | Interface limpa, exibindo apenas dados contextualmente relevantes | **4,43** |
| Imersão [Narrativa e Personagens] | História rica e personagens bem desenvolvidos | **4,36** |
| Flexibilidade [Combate e Inventário] | Atalhos rápidos e personalização para tarefas repetitivas | **4,14** |
| Recuperação de Erros [Combate/Mistura] | Explicações claras sobre o motivo de uma ação ter falhado | **4,07** |

<p align="center">Tabela 1: Sub-NFRs do SIG e médias do questionário aplicado (n=14). Fonte: Renan Pereira Reis, 2026, com base no questionário aplicado pela equipe.</p>

### Operacionalizações

Cada sub-NFR é satisfeito por uma operacionalização extraída do Mapa Mental:

| Sub-NFR | Operacionalização | Contribuição |
|---------|-------------------|:------------:|
| Estética Minimalista | HUD contextual e enxuto | `++` |
| Correspondência | Ícones temáticos consistentes | `++` |
| Imersão | Narrativa + sidequests + NPCs | `++` |
| Flexibilidade | Atalhos/slots configuráveis | `++` |
| Recuperação de Erros | Mensagens de erro explicativas | `++` |

<p align="center">Tabela 2: Operacionalizações e contribuições. Fonte: Renan Pereira Reis, 2026.</p>

### Claims

O grafo emprega dois *claims* — as nuvens tracejadas — para justificar contribuições que, de outro modo, seriam afirmações sem lastro:

- **"Tela limpa é preferência forte da amostra"** sustenta a contribuição `++` para Estética Minimalista. O item correspondente obteve a maior média do questionário (4,43), o que torna o claim verificável e não retórico.
- **"Ocupa área permanente no HUD"** sustenta a contribuição negativa descrita a seguir.

### O trade-off entre Flexibilidade e Estética Minimalista

O ponto mais relevante do grafo é que a operacionalização **Atalhos/slots configuráveis** não é neutra: ela contribui `++` para *Flexibilidade [Combate e Inventário]*, mas `−` para *Estética Minimalista [HUD]*, porque ocupa área permanente na tela. Os dois sub-NFRs afetados são desejáveis, e satisfazer plenamente um implica sacrificar parte do outro.

O questionário permite resolver o conflito com base em evidência em vez de preferência dos autores. A tela limpa obteve média 4,43 e os atalhos, 4,14: ambos são valorizados, com leve vantagem para a interface enxuta. A decisão de projeto adotada, portanto, é **manter os atalhos como configuráveis e opcionais**, e não como elementos fixos do HUD — o jogador que valoriza eficiência pode ativá-los, sem que isso seja imposto a quem prefere a tela limpa. O `−` permanece registrado no grafo por ser um efeito real da operacionalização, ainda que mitigado pela decisão.

### Rastreabilidade e elos com outros artefatos

- **[Mapa Mental](MapaMental.md)** — origem das operacionalizações e do próprio recorte de qualidade adotado.
- **[Léxico](/Base/Relatórios/SubEquipe_02/Lexico.md)** — os termos usados no grafo (*HUD*, *Inventário*, *Sidequest*, *NPC*, *Mistura de Elementos*) seguem o vocabulário definido para o domínio.
- **[BPMN](BPMN.md)** — os fluxos modelados por engenharia reversa permitem observar, em um jogo real, como as operacionalizações aqui propostas se manifestam em uso.

## Referências

> CHUNG, Lawrence; NIXON, Brian A.; YU, Eric; MYLOPOULOS, John. **Non-Functional Requirements in Software Engineering**. Boston: Kluwer Academic Publishers, 2000.

> NIELSEN, Jakob. **Usability Engineering**. Boston: Academic Press, 1993.

> NIELSEN, Jakob. **10 Usability Heuristics for User Interface Design**. Nielsen Norman Group, 1994. Disponível em: https://www.nngroup.com/articles/ten-usability-heuristics/. Acesso em: 26 ago. 2026.

## Nível de Contribuição dos Integrantes

| Nome | % de Contribuição |
|------|-------------------|
|  |  |

<p align="center">Tabela 3: Contribuição dos integrantes. Fonte: Renan Pereira Reis, 2026.</p>

## Histórico de Versão

| Versão | Data | Descrição | Autor(es) | Revisor |
|:------:|------|:----------|:----------|:--------|
| 1.0 | 22/08/2026 | Criação da página no modelo do artefato padrão | Marcelo de Araújo Lopes | |
| 2.0 | 27/08/2026 | Publicação do SIG, metodologia, sustentação empírica, análise do trade-off e rastreabilidade | Renan Pereira Reis | |

<p align="center">Tabela 4: Histórico de versão. Fonte: Renan Pereira Reis, 2026.</p>

Ver também: [Artefato Generalista](ArtefatoGeneralista.md) · [Mapa Mental](MapaMental.md) · [BPMN](BPMN.md) · [IA Generativa](IAGenerativa.md)
