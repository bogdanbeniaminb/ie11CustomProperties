# CSS Variables for IE11
Custom Properties polyfill for IE11


## It can:
- handle dynamic added `<style>`, `<link>`-elements
- handle dynamic added html-content
- cascade works
- inheritance works
- chaining `--bar:var(--foo)`
- fallback `var(--color, blue)`
- :focus, :target, :hover
- js-integration:
    - `style.setProperty('--x','y')`
    - `style.getPropertyValue('--x')`
    - `getComputedStyle(el).getPropertyValue('--inherited')` !!
- style-attriutes `<div ie-style="--foo:bar"`
- under 2k (min+gzip) and Lightweight dependency-free, who would have thought that?

## Demo:
https://rawcdn.githack.com/nuxodin/ie11CustomProperties/16836601aad3e1e4a1f039e12aa48355d0cd08bb/test.html

## Limitations
#### styles in element-attributes
There is no way to get the raw content of style-attributes in IE11.  
Use `<div style="--color:blue" ie-style="--color:blue">` for it

#### specificity for properties containing "var()"
...is always little highter, cause each selector gets an additional class-selector
eg. `#header` results in `#header.iecp_u44`


## Help wanted!
Please test and report bugs.
And add a ⭐️ and tweet about if you like it.
