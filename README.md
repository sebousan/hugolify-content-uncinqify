# hugolify-content-uncinqify

Content shared by the Un Cinq product sites: the advantages pages, contact, legal pages, pricing and menus, with the `brand` shortcodes that adapt them to each site through `params.brand`.

## Install

Edit `config/_default/module.yaml` to install the `hugolify-content-uncinqify` module.

### V2

The `main` branch targets Hugolify v2 with the design system: `_partials` and `_shortcodes`, header and footer menus, `ctas` on the cta blocks, Lucide icon names. Its module path ends with `/v2`.

```yml
imports:
  - path: github.com/sebousan/hugolify-content-uncinqify/v2
  - path: github.com/sebousan/hugolify-theme-uncinqify/v2

  # Core theme
  - path: github.com/hugolify/hugolify-theme/v2 # Required
  - path: github.com/hugolify/hugolify-theme-icons
  - path: github.com/hugolify/hugolify-theme-design-system
```

The release tags have no `v` prefix, so Go does not read them as versions: `hugo mod get` resolves a tag to a pseudo-version of its commit.

```bash
hugo mod get github.com/sebousan/hugolify-content-uncinqify/v2@<tag>
```

### V1

The `v1` branch keeps the module path without suffix for the sites still on Hugolify v1.

```yml
imports:
  - path: github.com/sebousan/hugolify-content-uncinqify
  - path: github.com/sebousan/hugolify-theme-uncinqify
  - path: github.com/hugolify/hugolify-theme # Required
```

A v1 site pins a 1.x tag or a commit of the `v1` branch (`@v1` would be read as a version query, not as the branch):

```bash
hugo mod get github.com/sebousan/hugolify-content-uncinqify@<tag or commit>
```

## Releases

Publishing a GitHub release runs `release-update.yml`, which updates `main` of the Un Cinq product sites. It reads the module path from `go.mod` at the released tag and skips every site whose `go.mod` does not require that path: a 2.x release only reaches the sites on `/v2`, a 1.x release from the `v1` branch only the sites still on v1.

## Documentation

https://www.hugolify.io/docs/

## Licensing

Hugolify is free for personal or commercial projects (MIT license)
