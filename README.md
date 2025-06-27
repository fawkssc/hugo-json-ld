# Hugo JSON+LD

Hugo JSON+LD adds some basic templates for [Google Structured Data](https://developers.google.com/search/docs/appearance/structured-data/intro-structured-data).

## Usage

Add the following to the `head` block:

```html
{{ partial "head/json-ld.html" (dict "Page" . [options]) }}
```

Options:

- *Graph* — *optional* The graph to use when building the structured data

## Default Configuration

`config/_default/params.toml`
```toml
[jsonld]
[[jsonld.graph]]
    name = "WebPage"
[[jsonld.graph]]
    name = "WebSite"
```
## Front Matter
```toml
[jsonld]
    inheritGraph = true
[[jsonld.graph]]
    name = [template]
