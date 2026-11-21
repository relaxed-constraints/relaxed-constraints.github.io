# Relaxed Constraints website

This repository publishes the [Relaxed Constraints project directory](https://relaxed-constraints.github.io/).

## Local development

Use uv with Python 3.11 or later.

```sh
uv sync --locked --group docs
uv run --group docs relcon-docs configure --check
uv run --group docs zensical build --strict
uv run --group docs zensical serve
```

Edit `docs/index.md` for homepage content and `mkdocs.yml` for site settings.
After upgrading the locked `relcon-docs` dependency, run
`uv run --group docs relcon-docs configure` to refresh the shared files.

## GitHub Pages

In this repository's **Settings → Pages**, set **Source** to **GitHub Actions**.
The Documentation workflow builds and deploys on pushes to `main` and can also
be run manually from the Actions tab.
