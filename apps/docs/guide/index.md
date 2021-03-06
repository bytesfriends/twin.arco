[tailwind css]: https://tailwindcss.com
[windi css]: https://windicss.org
[arco design]: https://arco.design

# Getting Started

**Twin.Arco** is a color preset depend on [Arco Design].

If your project depend on both [Arco Design] and [Tailwind CSS] or [Windi CSS], this **color preset** give you utilities experience using arco theme color.

## Motivation

AKA, [Arco Design] provides a set of CSS Variables, both color palette and theme.

Without this preset, how to apply arco theme working with **utility-first CSS framework**?

```css style.css
.container {
  color: rgb(var(--red-1));
  background-color: rgb(var(--arcoblue-6));
  border: 1px solid var(--color-border-1);
}
```

Yes, there is no benefit using **utility-first CSS framework** and [Arco Design]

But, now we have this color preset, just coding as using [Windi CSS] or [Tailwind CSS]

```html page.html
<div class="text-red-1 bg-arcoblue-6 border-arco-border-1 border-solid">
  Should Fill Something Here
</div>
```

## Installation

First of all, please install [Windi CSS] or [Tailwind CSS]

Then install this color preset

```sh
pnpm install twin.arco -D
```

## Configuration

:::warning
`extend` is deprecated, please follow above with `preset`
:::

```ts windi.config.ts
import { defineConfig } from 'vite-plugin-windicss'
import { preset } from 'twin.arco'

export default defineConfig({
  presets: [preset()],
})
```

```js tailwind.config.js
const { preset } = require('twin.arco')

module.exports = {
  presets: [preset()],
}
```
