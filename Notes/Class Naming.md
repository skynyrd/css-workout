## Naming Strategy: Block Element Modifier

* __Block__: Standalone component that is meaningful on its own.
* __Element__: Part of a block, no standalone meaning
* __Modifier__: A different version of a block or an element.

```css
.block {}
.block__element {}
.block__element--modifier {}
```

Example:

```html
<figure class="recipe">
    <div class="recipe__hero">...</div>
    <a class="recipe__btn btn btn--round" href="#">Try</a>
</figure>
```