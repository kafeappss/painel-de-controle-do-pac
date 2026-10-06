# Painel de Controle do PAC

Cronograma (gráfico de Gantt) do **Projeto do PAC** — objetivo final: *montar e executar uma oficina que ensine lógica de programação*.

- Cada semana e cada aula é um cartão com **pills das equipes** que trabalham nela
- No computador, as semanas ficam lado a lado e cada equipe sempre na mesma linha (como um Gantt); no celular, os cartões ficam empilhados
- **Toque em uma equipe** (no filtro do topo ou em qualquer pill) para destacar o caminho dela em todas as semanas
- 5 semanas de preparação (06/10 → prazo final 14/11), com os handoffs da semana 3 marcados com ⇄
- **Aula 1 (14/11)**, **Aula 2 (21/11)** e **Aula 3 (28/11)**, das 08:30 às 12:00, até 21 alunos, com as equipes que acompanham
- Contagem regressiva, semana atual destacada e feriados do período

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

- **Link direto para uma equipe:** ao destacar uma equipe, o endereço ganha `#nome-da-equipe` (ex.: `/#mentores`). Mande esse link para o grupo da equipe e a página já abre com ela destacada.
- **Simular outra data:** abra com `?hoje=AAAA-MM-DD` na URL (ex.: `?hoje=2026-10-25`).
