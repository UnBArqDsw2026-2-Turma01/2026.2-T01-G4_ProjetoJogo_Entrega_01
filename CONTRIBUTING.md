# Guia de Contribuição

## Contexto

Este repositório reúne a documentação e os artefatos do Grupo 04 da disciplina FGA0208, Arquitetura e Desenho de Software, da Universidade de Brasília. O trabalho é desenvolvido por subequipes e depende de rastreabilidade entre reuniões, decisões, issues, commits, pull requests e artefatos publicados.

Contribuições de integrantes do grupo e de colaboradores externos devem seguir este guia, o [Código de Conduta](CODE_OF_CONDUCT.md) e as orientações acadêmicas da disciplina.

## Antes de começar

1. Consulte as issues e o quadro do projeto para verificar se a tarefa já está registrada.
2. Leia os guias e os documentos relacionados ao artefato que será alterado.
3. Confirme o escopo, os responsáveis e os critérios de aceitação da tarefa.
4. Comente na issue ou atribua a tarefa a si antes de iniciar, evitando trabalho duplicado.
5. Para mudanças relevantes ainda não discutidas, abra uma solicitação ou alinhe a proposta com o grupo antes da implementação.

Use, quando aplicável, os formulários disponíveis em `.github/ISSUE_TEMPLATE/`:

- `artefato_subgrupo_form.yml` para artefatos, relatórios e iniciativas das subequipes;
- `ata_reuniao_form.yml` para reuniões gerais ou de subequipe;
- `atividade_geral_form.yml` para tarefas transversais do grupo;
- `bug_report_form.yml` para problemas reproduzíveis;
- `feature_request_form.yml` para melhorias e iniciativas extras.

Prefira uma issue por unidade de trabalho. As labels devem indicar, quando pertinente, a entrega, o foco, a subequipe e o tipo de contribuição, seguindo exemplos como `entrega-01`, `foco-1`, `subequipe-01` e `documentacao`.

## Escopo e propriedade dos arquivos

- Altere somente os arquivos necessários para a issue.
- Não modifique páginas de outra subequipe para padronizá-las sem acordo com seus responsáveis.
- Preserve alterações preexistentes e não remova contribuições ou evidências de autoria.
- Separe correções não relacionadas em outra issue e outro pull request.
- Antes de concluir, confira `git status` e `git diff` para identificar alterações acidentais.

## Branches

A branch `main` é utilizada para integração e está protegida por um ruleset ativo. O trabalho deve ocorrer em uma branch temática criada diretamente a partir da versão mais recente de `origin/main`.

```bash
git fetch origin
git switch -c docs/subgrupo01-nome-do-artefato origin/main
```

Use nomes curtos e descritivos:

- `docs/<escopo>-<assunto>` para documentação;
- `feat/<assunto>` para nova funcionalidade;
- `fix/<assunto>` para correção;
- `chore/<assunto>` para manutenção sem alteração funcional.

Exemplos já compatíveis com o fluxo do projeto incluem `docs/reunioes-gerais`, `docs/subgrupo01-rich-picture` e `docs/subgrupo02-bpmn`.

Para incorporar mudanças recentes de `main` em uma branch já existente, utilize:

```bash
git fetch origin
git merge origin/main
```

Resolva eventuais conflitos na branch temática, valide novamente os arquivos e envie a atualização para o repositório remoto.

### Ruleset da branch principal

O ruleset `Main ruleset`, consultado em 27/08/2026, aplica as seguintes regras à branch padrão:

- toda alteração em `main` deve passar por pull request;
- o pull request precisa de pelo menos uma aprovação de uma pessoa com permissão de escrita;
- pull requests abertos pelo GitHub Copilot sem atribuição a uma pessoa exigem uma aprovação adicional;
- a branch `main` não pode ser excluída;
- *force pushes* e outras atualizações que não sejam *fast-forward* são bloqueados;
- `merge`, `squash` e `rebase` são métodos de integração permitidos.

O ruleset não possui pessoas ou equipes autorizadas a ignorar essas regras. Portanto, não tente enviar commits diretamente para `main`.

## Padrões para documentação

A documentação publicada utiliza Docsify e está localizada em `docs/`.

- Escreva em português do Brasil, com linguagem objetiva e revisão ortográfica.
- Evite travessões. Prefira vírgulas, dois-pontos, parênteses ou frases separadas.
- Não deixe textos de exemplo, campos vazios ou placeholders na versão final.
- Use links relativos ou iniciados em `/` que funcionem no site publicado. Não use caminhos locais `file://`.
- Armazene imagens, vídeos e arquivos-fonte na pasta do artefato ou em sua pasta `assets`, usando caminhos relativos.
- Inclua legenda e fonte em figuras e tabelas que apresentem conteúdo ou evidências.
- Em tabelas meramente organizacionais, não use uma fonte genérica como “Autores”.
- Cite a origem específica quando os dados vierem de gravações, transcrições, jogos, artigos ou outras evidências.
- Atualize o histórico de versão de todo documento alterado, registrando apenas responsáveis humanos.
- Registre a contribuição individual e seus comprobatórios em `docs/Base/1.2.ParticipacoesBase.md` quando pertinente.
- Adicione páginas novas ao `docs/_sidebar.md` e ao índice correspondente.
- Preserve também o arquivo-fonte editável de diagramas quando houver, como `.bpmn`, `.drawio` ou `.tldr`.

### Atas de reunião

As atas devem seguir [docs/Guias/AtaPadrao.md](docs/Guias/AtaPadrao.md) e o índice da reunião correspondente.

- Use uma issue por reunião geral ou de subequipe.
- Nomeie atas internas como `docs/Atas/AtaSubNN_XX.md`.
- Mantenha apenas os integrantes convocados na tabela de participantes.
- Use gravações ou transcrições como fontes primárias e preserve a evidência disponível.
- Não invente horário, decisão, responsável ou prazo. Identifique explicitamente as informações ausentes.
- Diferencie propostas, decisões e pendências.
- Relacione decisões aos artefatos produzidos e atualize o índice da subequipe.

## Commits

Faça commits pequenos, coesos e fáceis de revisar. A mensagem deve descrever a alteração realizada, preferencialmente no formato:

```text
docs: adiciona modelo BPMN do fluxo de batalha
feat: implementa seleção de personagem
fix: corrige link da ata do subgrupo 01
chore: atualiza configuração do Docsify
```

Evite mensagens genéricas como `ajustes`, `mudanças` ou `final`. Não reescreva a autoria de commits de outras pessoas e não inclua ferramentas de inteligência artificial como autoras dos commits ou dos históricos de versão.

Antes de enviar uma contribuição, uma sequência recomendada é:

```bash
git status --short
git diff --check
git add caminho/do/arquivo
git diff --cached --check
git commit -m "docs: descreve a alteração realizada"
git push -u origin docs/subgrupo01-nome-do-artefato
```

Substitua o caminho, a mensagem e o nome da branch pelos valores correspondentes à tarefa. Não use `git add .` sem antes conferir o estado do repositório.

## Pull requests

Todo pull request deve:

1. ter `main` como branch de destino;
2. possuir título que identifique claramente o escopo;
3. preencher o modelo disponível em `.github/pull_request_template.md`;
4. explicar o contexto, as principais mudanças e como elas foram verificadas;
5. relacionar a issue correspondente;
6. limitar-se ao escopo combinado;
7. solicitar revisão de uma pessoa diferente da autora principal;
8. resolver comentários e conflitos antes da integração.

Use `Closes #N` quando o pull request atender integralmente aos critérios da issue. Se ele representar apenas parte do trabalho, use `Relaciona #N` e mantenha a issue aberta.

Para alterações visuais, inclua capturas ou indique como visualizar o resultado. Não faça a integração enquanto os critérios de aceitação, a definição de pronto e a revisão aplicável não estiverem concluídos.

## Validação local

Para visualizar a documentação:

```bash
npx docsify-cli serve docs
```

Antes de solicitar revisão, verifique:

- carregamento das páginas pelo Docsify;
- funcionamento dos links e da navegação lateral;
- exibição de imagens, diagramas e vídeos;
- ausência de placeholders e caminhos locais;
- legendas, fontes, referências e históricos de versão;
- consistência entre issue, artefato, ata e quadro de participações;
- ausência de alterações fora do escopo.

## Integridade acadêmica e uso de IA

- Todo conteúdo externo deve ser citado e utilizado de acordo com sua licença ou com os limites legais aplicáveis.
- Cada integrante deve declarar apenas contribuições que efetivamente realizou.
- Ferramentas de inteligência artificial podem auxiliar o trabalho quando permitido pela disciplina, mas o conteúdo deve ser verificado por uma pessoa responsável.
- O uso de IA deve ser informado na metodologia ou no campo apropriado quando for relevante para compreender a produção do artefato.
- Modelos de IA não devem aparecer como autores nos históricos de versão.
- Dados pessoais, informações privadas ou materiais sem autorização não devem ser enviados a ferramentas externas.

## Licença

Ao contribuir, você concorda que sua contribuição será disponibilizada sob a [Licença MIT](LICENSE), respeitados os direitos aplicáveis aos materiais de terceiros.

A licença aplica-se somente ao conteúdo sobre o qual os integrantes do projeto possuam os direitos necessários. Capturas e gravações de jogos, marcas, logotipos, publicações, trechos e outros materiais de terceiros permanecem sujeitos aos direitos e termos de seus respectivos titulares.

## Histórico de versão

| Versão | Data | Descrição | Autor(es) | Revisor |
|:------:|:----:|-----------|------------|---------|
| 1.0 | 27/08/2026 | Criação do guia de contribuição com formulários, ruleset, branches, commits e pull requests | Yogi Nam de Souza Barbosa | |

<p align="center">Tabela 1: Histórico de versão.</p>
