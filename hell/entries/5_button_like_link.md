---
title: "#5 button-like-link"
date: 2019-10-22
author: pepelsbey
permalink: /{{ title | slug }}/index.html

badcode: '<a href="#form" role="button" aria-haspopup="true">
    &nbsp;&nbsp;Register&nbsp;&nbsp;
</a>'


goodcodeCSS: '.button {
    /* Use CSS to apply padding */
    padding: 0 0.5em;
}'

goodcode: '<a class="button" href="#form">
    Register
</a>'
---

<div class="section">

## Bad code

```html
{{ badcode | pretty }}
```

</div>

<div class="section">

## What’s bad about it

It’s a link to a form at the same page that looks like a button.

1. By adding `role="button"` to a link, you’re telling that it’s a button, though it acts like a link.
2. `aria-haspopup="true"` suggests that there’s a popup, but it doesn’t exist.
3. Padding should be added via CSS, not `&nbsp;`.

</div>

<div class="section">

## Good code

```css
{{ goodcodeCSS | prettyCSS }}
```

```html
{{ goodcode | pretty }}
```

</div>
