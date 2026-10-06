# Painel de Controle do PAC

Cronograma (gráfico de Gantt) do **Projeto do PAC** — objetivo final: *montar e executar uma oficina que ensine lógica de programação*.

- 5 semanas de preparação (06/10 → prazo final 14/11), com as equipes de cada semana e os handoffs da semana 3
- 3 aulas separadas: **Aula 1 (14/11)**, **Aula 2 (21/11)** e **Aula 3 (28/11)**, das 08:30 às 12:00, até 21 alunos
- Nas aulas acompanham: Comunicação e Registro, Ambiente e Suporte, Mentores e Professores
- Marca o dia de hoje, a semana atual, a próxima aula e os feriados no período

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

Para ver como o painel fica em outra data, abra com `?hoje=AAAA-MM-DD` na URL (ex.: `?hoje=2026-10-25`).
