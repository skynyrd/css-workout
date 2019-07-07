__Clear fix (float)__

```css
.clearfix::after {
    content: "",
    clear: both,
    display: table
}
```

__Colour darken && lighten (SASS)__

```scss
$light: lighten($color,15%);
$dark: darken($color,15%);
```