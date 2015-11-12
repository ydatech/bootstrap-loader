## Usage

Webpack — simply apply on entry point:

```js
// No Bootstrap
entry: './app'

// Load Bootstrap
entry: 'bootstrap!./app'
```

Config is optional. It can be placed in root dir with name `.bootstraprc`. `YAML` / `JSON` are ok:

```yaml
---
useFlexbox: true

styleLoaders:
  - style
  - css
  - sass

styles:
  normalize: true
  print: true

scripts:
  alert: true
  button: true
```

```json
{
  "useFlexbox": true,

  "styleLoaders": ["style", "css", "sass"],

  "styles": {
    "normalize": true,
    "print": true
  },

  "scripts": {
    "alert": true,
    "button": true
  }
}
```

If there is no config provided — default one will be used:

```yaml
---
verbose: false

useFlexbox: true

styleLoaders:
  - style
  - css
  - sass

extractStyles: false
# env:
#   development:
#     extractText: false
#   production:
#     extractText: true

# bootstrapCustomizations: ./path/to/bootstrapCustomizations.scss

### Bootstrap styles
styles:

  # Core variables and mixins
  variables: true
  mixins: true

  # Reset and dependencies
  normalize: true
  print: true

  # Core CSS
  reboot: true
  type: true
  images: true
  code: true
  grid: true
  tables: true
  forms: true
  buttons: true

  # Components
  animation: true
  dropdown: true
  button-group: true
  input-group: true
  custom-forms: true
  nav: true
  navbar: true
  card: true
  breadcrumb: true
  pagination: true
  pager: true
  labels: true
  jumbotron: true
  alert: true
  progress: true
  media: true
  list-group: true
  responsive-embed: true
  close: true

  # Components w/ JavaScript
  modal: true
  tooltip: true
  popover: true
  carousel: true

  # Utility classes
  utilities: true
  utilities-spacing: true
  utilities-responsive: true

### Bootstrap scripts
scripts:
  alert: true
  button: true
  carousel: true
  collapse: true
  dropdown: true
  modal: true
  popover: true
  scrollspy: true
  tab: true
  tooltip: true
  util: true
```