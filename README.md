# Manual do usuário — GE-Associados

Site Jekyll (tema [just-the-docs](https://just-the-docs.com/)) publicado no GitHub Pages
pelo workflow [`.github/workflows/pages.yml`](.github/workflows/pages.yml) a cada push na `main`.

**Não publique daqui na mão:** use `Projeto/bin/publish-manual.sh` na raiz do container.

## Preview local (opcional)

```bash
bundle install
bundle exec jekyll serve
```

## Onde ficam as coisas

- `index.md`, `*.md` — páginas do manual.
- `assets/img/` — prints das telas (capturados com Playwright pela skill `user-manual`).
- `_manual/` — material de trabalho (roteiro de prints, config), **excluído do build**.
- `_sass/color_schemes/ge-associados.scss` — cores. ⚠️ Placeholder até haver identidade visual definida.
