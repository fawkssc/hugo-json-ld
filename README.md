# Hugo JSON+LD

Hugo JSON+LD adds some basic templates for [Google Structured Data](https://developers.google.com/search/docs/appearance/structured-data/intro-structured-data).

## Usage

Add the following to the `head` block:

```html
{{ partial "head/json-ld.html" (dict "Page" . [options]) }}
```

Options:

- *Partial* — *optional* The partial path to use
- *Template* - *optional* The template name to use

## Default Configuration

`config/_default/params.toml`
```toml
[jsonld]
    template = "website"
```

## Override The Template

1) Home: `partials/ld.json`
2) Templates: `partils/json-ld/[name].json`
3) Page Bundle: `content/[archtype]/[page]/ld.json`
