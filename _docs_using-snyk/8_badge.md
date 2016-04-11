---
title: Badge
---

Once you’re vulnerability free, you can put a badge on your README showing your package has no known security holes. This will show your users you care about security, and tell them that they should care too.

If there are no vulnerabilities, this is indicated by a green badge.

<a class="link--unstyled" href="https://snyk.io/test/npm/name"><img src="https://snyk.io/test/npm/name/badge.svg" alt="Known Vulnerabilities" data-canonical-src="https://snyk.io/test/npm/name/" style="max-width:100%;"></a>

If vulnerabilities have been found, the red badge will show the number of vulnerabilities.

<a class="link--unstyled" href="https://snyk.io/test/npm/jsbin"><img src="https://snyk.io/test/npm/jsbin/badge.svg" alt="Known Vulnerabilities" data-canonical-src="https://snyk.io/test/npm/jsbin/" style="max-width:100%;"></a>

_Note:_ The badge works off the npm package, and does not factor in .snyk files yet. (This means that ignored vulnerabilities will not be taken into account).

Get the badge by copying the relevant snippet below and replacing "name" with the name of your package.

### HTML:

```html
<img src="https://snyk.io/test/npm/name/badge.svg" alt="Known Vulnerabilities" data-canonical-src="https://snyk.io/test/npm/name" style="max-width:100%;"/>
```

### Markdown:

```md
[![Known Vulnerabilities](https://snyk.io/test/npm/name/badge.svg)](https://snyk.io/test/npm/name)
```
