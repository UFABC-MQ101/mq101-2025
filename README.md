# MQ101 — Métodos Quantitativos para Políticas Públicas 101

Repositório público da disciplina. Este repositório hospeda o programa, slides, roteiros de laboratório, listas de exercícios, dados e código.

## Objetivos didáticos
- Treinar boas práticas de programação e versionamento.
- Promover reprodutibilidade científica e ciência aberta.
- Padronizar submissões de listas de exercícios via GitHub.

## Como navegar
- Programa: [`syllabus/`](syllabus/)
- Slides: [`slides/`](slides/)
- Laboratório (R/Quarto): [`labs/`](labs/)
- Exercícios e enunciados: [`exercises/`](exercises/)
- Submissões dos(as) alunos(as): [`exercises/submissions/`](exercises/submissions/)
- Dados (raw/processed/dictionary): [`data/`](data/)
- Site do curso (GitHub Pages): pasta `docs/`.

## Ambiente de software
- R (≥ 4.3), RStudio/Posit, Quarto.
- Pacotes R serão gerenciados com `renv`. Após clonar:
  ```r
  install.packages('renv')
  renv::init()        # primeira vez
  renv::restore()     # usuários subsequentes
  ```

## Fluxo de trabalho
1. Faça *fork* ou *clone*.
2. Crie *branch* por tópico (ex.: `lab01-ajuste-modelo`).
3. Commits descritivos (padrão *Conventional Commits* é recomendado).
4. Abra *Pull Request* para `main`.

## Submissões de listas (via Pull Request)
- Estrutura para cada exercício:
  ```
  exercises/submissions/ex01/<RA>-<sobrenome>/
    ├─ README.md
    ├─ script.R
    └─ respostas.pdf
  ```
- PR deve usar o *template* e passar as verificações (lintr/estilo e renderização).

## Licenças
- Código: MIT (arquivo `LICENSE-MIT`).
- Conteúdo didático (textos, slides): CC BY 4.0 (arquivo `LICENSE-CC-BY-4.0`).

## Citação
Consulte `CITATION.cff`.
