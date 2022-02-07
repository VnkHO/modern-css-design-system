# Modern CSS Design System

CSS Design System with HTML5 Boilerplate

## More about reset and normalize

More about
[reset.css and normalize.css](https://www.css-tricks.com/reboot-resets-reasoning/)

**normalize.css:** Standardize for every browser. It didn’t remove any styling
from elements that were already consistent across browsers (for the most part).

## Classless CSS

[More about classless css](https://github.com/troxler/awesome-css-frameworks)

## CSS Variable

For example, we can structure it in separate file like:

```
    varaible.css
```

### How to use it ?

We can define with the root element and then use the variable inside the var()
function.

```
    :root {
        --black: #222;
    }

    body {
        background-color: var(--black);
    }
```

We can also scope the css variable inside the element that we want.

```
    :root {
        --black: red;
    }

    body {
        background-color: var(--black);
    }
```

It can be useful for larger design system, themes, different screen sizes,
etc...
