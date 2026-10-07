# Painel de Controle do PAC

Cronograma (gráfico de Gantt) do **Projeto do PAC** — objetivo final: *montar e executar uma oficina que ensine lógica de programação*.

Visual no estilo de ferramenta de gestão (Jira/ClickUp). No topo ficam os dados do projeto (prazo, aulas, horário, turma e progresso) e o cartão **Esta semana**, com as equipes que estão trabalhando agora e a próxima aula. Abaixo, três abas:

- **Cronograma** — linha do tempo com dias, semanas e meses; barras por equipe, semana de handoff destacada com seta para a equipe que recebe, aulas como marcos (◆), linha de hoje, fins de semana e feriados
- **Quadro** — uma coluna por semana e por aula (Aula 1, 2 e 3), com um cartão para cada equipe
- **Lista** — tabela das equipes agrupada por status

Também tem: status de cada equipe calculado pela data (A fazer, Em andamento, Aguardando, Nas aulas, Concluída), campos do projeto (prazo, aulas, horário, turma, progresso da preparação) e filtro por equipe.

É um único arquivo `index.html` (HTML + CSS + JavaScript puro), sem dependências e sem build.

## Publicar na Vercel

1. Em [vercel.com/new](https://vercel.com/new), importe este repositório.
2. Em **Framework Preset**, escolha **Other**. Deixe *Build Command* e *Output Directory* vazios.
3. Clique em **Deploy**.

Cada push na branch de produção publica a nova versão automaticamente.

## Editar datas, equipes e aulas

Abra `index.html` e altere o bloco `DADOS` no início do `<script>`:

- `semanas`: início e fim de cada semana (`AAAA-MM-DD`)
- `aulas`: datas das aulas
- `equipes`: em quais semanas cada equipe trabalha, handoffs e se acompanha as aulas
- `horario`, `maxAlunos`, `prazoFinal`, `feriados`

## Dicas

- **Link direto para uma equipe:** ao filtrar uma equipe, o endereço ganha `#nome-da-equipe` (ex.: `/#mentores`). Mande esse link para o grupo da equipe e a página já abre filtrada.
- A aba escolhida fica salva no navegador de cada pessoa.
- **Simular outra data:** abra com `?hoje=AAAA-MM-DD` na URL (ex.: `?hoje=2026-10-25`).
