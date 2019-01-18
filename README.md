# rollup-plugin-css

![](https://img.shields.io/npm/dm/@henrikjoreteg/rollup-plugin-css.svg)![](https://img.shields.io/npm/v/@henrikjoreteg/rollup-plugin-css.svg)![](https://img.shields.io/npm/l/@henrikjoreteg/rollup-plugin-css.svg)

Rollup plugin for aggregating and outputting CSS. I'm extracting this into it's own repo because I keep finding myself wanting it.

## install

```
npm install @henrikjoreteg/rollup-plugin-css
```

## example

```javascript
import css from '@henrikjoreteg/rollup-plugin-css'

const IS_PROD = process.env.NODE_ENV === 'production'

export default {
  input: 'src/worker',
  output: {
    format: 'umd',
    file: 'public/build/worker.js'
  },
  plugins: [
    css({
      output: './public/build/s.css',
      minify: IS_PROD
    })
  ]
}
```

## changelog

2.0.0 - Renamed `ongenerate`to `generateBundle` per updates to Rollup. Thanks @ryan-codingintrigue

## credits

If you like this follow [@HenrikJoreteg](http://twitter.com/henrikjoreteg) on twitter.

## license

[MIT](http://mit.joreteg.com/)
