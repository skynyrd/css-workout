## Main SASS Features

1. __Variables__
2. __Nesting__
3. __Operators__: Basic math operations
4. __Partials and Imports__
5. __Mixins__: Reusable CSS code blocks
6. __Functions__: Mixins that returns something.
7. __Extends__: To make different selectors inherit declarations that are common to all of them.
8. __Conditions and Loops__: Not really necessary unless you are writing a css framework.

SASS: Indentation based - Python like syntax.
SCSS: CSS like syntax.

## &

```scss
.someclass {
    li {
        margin: 10px;

        &:first-child {
            margin: 20px;
        }
    }
}

// and

.someclass {
    li {
        margin: 10px;
    }

    li:first-child {
        margin: 20px;
    }
}

// are same!
```

## Extends

```scss
%btn-placeholder {
    padding: 10px;
    display: inline-block;
    ...
}

.btn-main {
    &:link {
        @extend %btn-placeholder;
        background-color: $color-secondary;
    }
}

// Use extends if selectors/elements are related to each other.
```

## Mixins

```scss
@mixin clearfix {
    &::after {
        content: "";
        clear: both;
        display: table;
    }
}

nav {
    margin: 30px;
    
    @include clearfix;
}
```

```scss
@mixin style-link-test($color) {
    text-decoration: none;
    color: $color;
}

li {
    a:link {
        @include style-link-test($color-text-dark);
    }
}
```

## Functions

```scss
@function divide($a, $b) {
    @return $a / $b;
}

nav {
    margin: divide(60, 2) * 1px;
}
```