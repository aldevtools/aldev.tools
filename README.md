# aldev.tools

Source for [aldev.tools](https://aldev.tools) — the landing page for the
`aldevtools` organization.

Built with [Hugo](https://gohugo.io) (extended, 0.165+). No external theme: the
layouts in `layouts/` are the whole design.

## Local preview

```bash
hugo server
```

## Adding or moving a tool

Everything on the page comes from `data/tools.yaml`. `repo` is the full
`owner/name` path, so when a tool migrates into the organization it is a
one-line change:

```yaml
- name: AL Runner
  repo: StefanMaron/BusinessCentral.AL.Runner   # -> aldevtools/BusinessCentral.AL.Runner
  text: Run Business Central AL unit tests in milliseconds.
```

No template edit is needed to add, remove or regroup tools.

## Deployment

`.github/workflows/pages.yml` builds on every push to `main` and publishes to
GitHub Pages. `static/CNAME` holds the custom domain.
