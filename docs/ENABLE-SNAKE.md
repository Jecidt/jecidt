# Activar la serpiente de contribuciones

1. En tu repositorio de perfil, crea `.github/workflows/snake.yml`.
2. Sustituye `Jecidt` por tu usuario.
3. Guarda el archivo y abre la pestaña **Actions** para ejecutar el workflow.

```yaml
name: Generate contribution snake
on:
  schedule:
    - cron: "17 2 * * *"
  workflow_dispatch:
permissions:
  contents: write
jobs:
  generate:
    runs-on: ubuntu-latest
    steps:
      - uses: Platane/snk@v3
        with:
          github_user_name: Jecidt
          outputs: |
            dist/github-contribution-grid-snake.svg
      - uses: crazy-max/ghaction-github-pages@v4
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```

Cuando termine, la imagen del README debe apuntar a:
`https://raw.githubusercontent.com/Jecidt/Jecidt/output/github-contribution-grid-snake.svg`

Si no quieres usar GitHub Actions, elimina la sección de la serpiente del README.
