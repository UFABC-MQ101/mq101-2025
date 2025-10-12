# Contribuindo

## Padrões de *branch* e commits
- Crie *branches* por tópico: `nome-topico-descritivo`.
- Use mensagens de commit descritivas; recomenda-se *Conventional Commits*.

## Pull Requests
- Use o *template* padrão.
- Inclua reprodução mínima (scripts e `sessionInfo()`).
- PRs devem passar pela checagem automática (`lintr`, renderização Quarto).

## Estilo de código
- Siga `styler` e `lintr` no R. Execute:
  ```r
  styler::style_dir()
  lintr::lint_dir(exclusions = list("data"))
  ```
