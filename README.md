# hugolify-content-uncinqify

Content shared by the Un Cinq product sites: the advantages pages, contact, legal pages, pricing and menus, with the `brand` shortcodes that adapt them to each site through `params.brand`.

## Install

Edit `config/_default/module.yaml` to install the `hugolify-content-uncinqify` module.

### V2

The `v2` branch targets Hugolify v2 with the design system: `_partials` and `_shortcodes`, header and footer menus, `ctas` on the cta blocks, Lucide icon names.

```yml
imports:
  - path: github.com/sebousan/hugolify-content-uncinqify
  - path: github.com/sebousan/hugolify-theme-uncinqify/v2

  # Core theme
  - path: github.com/hugolify/hugolify-theme/v2 # Required
  - path: github.com/hugolify/hugolify-theme-icons
  - path: github.com/hugolify/hugolify-theme-design-system
```

Both branches share one module path, so a v2 site pins a commit of the `v2` branch (`@v2` would be read as a version query, not as the branch):

```bash
hugo mod get github.com/sebousan/hugolify-content-uncinqify@<commit>
```

### V1

```yml
imports:
  - path: github.com/sebousan/hugolify-content-uncinqify
  - path: github.com/sebousan/hugolify-theme-uncinqify
  - path: github.com/hugolify/hugolify-theme # Required
```

## Documentation

https://www.hugolify.io/docs/

## Licensing

Hugolify is free for personal or commercial projects (MIT license)
