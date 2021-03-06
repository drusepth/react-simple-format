# react-simple-format
[![](https://img.shields.io/travis/rilkevb/react-simple-format.svg)](https://travis-ci.org/rilkevb/react-simple-format) [![](https://img.shields.io/npm/v/react-simple-format.svg)](https://www.npmjs.com/package/react-simple-format)

The port of Rails's [simple_format](http://api.rubyonrails.org/classes/ActionView/Helpers/TextHelper.html#method-i-simple_format) to React.

## Usage

Turns double newlines into different paragraphs. See [examples](examples) for live examples.

```js
const forwardText = "You can't connect the dots looking forward;\n\nYou can only connect them looking backward."

<SimpleFormat text={ forwardText } />
```

This will render:

```html
<div>
  <p>You can't connect the dots looking forward;</p>
  <p>You can only connect them looking backward.</p>
</div>
```

## Props

### `wrapperTag` (string/react class)

Default is `'div'`, but you can change it to something else:

```js
<SimpleFormat text={ ... } wrapperTag='article' />

↓

<article>
  ...
</article>

---

<SimpleFormat text={ ... } wrapperTag={ SomeComponent } />

↓

<SomeComponent>
  ...
</SomeComponent>
```

### `wrapperTagProps` (object)

`props` for the wrapper tag.

### `postfix` (node)

Allows you to add a node at the end of the last `p` tag.


```js
<SimpleFormat text={ ... } postfix='foo' />

↓

<div>
  <p>...</p>
  <p>...foo</p>
</div>
```

## Credits

- [rilkevb](http://github.com/rilkevb)
- [chibicode](http://github.com/chibicode)

## License

MIT
