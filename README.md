# ECSS
Ben Frain's [ECSS](http://ecss.io/) naming conventions. All components are self-contained, grouped with their `html`/`js`/`...` files. Roll your [own classes and components](http://ecss.io/chapter5.html)!

> Be pragmatic, use as much as is appropriate

#### Example

```text
shopping-cart-template/
- shopping-cart.html
- shopping-cart.css
- shopping-cart.js
```

```stylus
// .[namespace][-ModuleOrComponent][_ChildNode][-variant]
.namespace-ModuleOrComponent_ChildNode-variant {}

// A standalone component
.sc-Title {}
.sc-RemoveBtn {}

// A component with multiple views
.mc-ShoppingCart_Title {}
.mc-ShoppingCart_RemoveBtn {}
```

### CSS declaration order
Use [css declaration order](http://codeguide.co/#css-declaration-order) by @mdo,
but mixins come first.

1. Mixins
2. Positioning
3. Box model
4. Typographic
5. Visual

```stylus
.declaration-order
  // Mixins
  baseline-grid()

  // Positioning
  position: absolute
  top: 0
  right: 0
  bottom: 0
  left: 0
  z-index: 100

  // Box-model
  display: block
  float: right
  width: 100px
  height: 100px

  // Typography
  font: normal 13px "Helvetica Neue", sans-serif
  line-height: 1.5
  color: #333
  text-align: center

  // Visual
  background-color: #f5f5f5
  border: 1px solid #e5e5e5
  border-radius: 3px

  // Misc
  opacity: 1
```
