# alpinejs-swipe

AlpineJS custom directive to detect swipe gestures on an element.

[![npm](https://img.shields.io/npm/v/alpinejs-swipe)](https://www.npmjs.com/package/alpinejs-swipe)
![npm bundle size](https://img.shields.io/bundlephobia/minzip/alpinejs-swipe)
![Module system](https://img.shields.io/badge/module%20system-ESM%2C%20CJS%2C%20UMD-brightgreen)

## Installation

### CDN

Include the following `<script>` tag in the `<head>` of your document:

``` html
<script src="https://unpkg.com/alpinejs-swipe"></script>
```

> **Important**: This must be added **before** loading Alpine.js when using CDN links.

### NPM

You can also install using a package manager.

```
npm install alpinejs-swipe
yarn add alpinejs-swipe
```

And then register the plugin **before** `Alpine.start()`:

```js
import swipePlugin from "alpinejs-swipe";
Alpine.plugin(swipePlugin);
Alpine.start();
```


## Usage

Just use the "x-swipe" directive with an expression and you'll be called back when the user swipes in the direction you want.

```html
<div x-swipe:down="console.log('SWIPED DOWN!')"></div>
<div x-swipe:right="console.log('SWIPED RIGHT!')"></div>
```

You can also define a threshold with modifiers:

```html
<div x-swipe:down.threshold.200px="console.log('SWIPED DOWN!')"></div>
```

> _The default threshold is 50._

If you want, it's also possible to be called back when the user swipes to any side, just omit the direction:

```html
<div x-swipe="console.log('SWIPED!')"></div>
```

> _In this case the direction will be passed to the function in the expression through the first argument._

## Future ideas

- Allow other gestures detection (like pan, doubletap and longpress) with https://github.com/sciactive/tinygesture.

## License

Licensed under the MIT license, see [LICENSE.md](LICENSE.md) for details.
