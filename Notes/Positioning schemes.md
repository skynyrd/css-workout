## Normal Flow

* Default positioning scheme
* NOT floated
* NOT absolutely positioned
* Elements laid out according to their source order

```
Default

position: relative
```

## Floats

* Element is removed from the normal flow
* Text and inline elements wrap around the floated element
* Container won't adjust it's height to the element.

```
float: left
float: right
```

## Absolute Positioning

* Element is removed from the normal flow
* No impact on surrounding elements

```
position: fixed
position: absolute
```

## Stacking Contexts

* Layered model
* z-index
* Sometimes other properties like transform can also create a new layer.