# ECSS

> ⚠️ For small things, such as Anki Programming Themes, this is overkill.
> It's proven effective for large-scale projects with large teams.
> The alternative that I'm now working with is [GPS](https://archive.ph/gXCRi) (`global`, `page`, `section`).
> I couple that with a couple of cherry picked features from ECSS.

Ben Frain's [ECSS](https://ecss.benfrain.com) naming conventions. All components are self-contained, grouped with their `html`/`js`/`...` files. Roll your [own classes and components](https://ecss.benfrain.com/chapter4.html)!

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
Use [css declaration order](https://codeguide.co/#declaration-order) by @mdo. Mixins (if any) also come first.

1. Positioning
2. Box model
3. Typography
4. Visual
5. Miscellaneous


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

  // Box model
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
