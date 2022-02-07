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

### CSS Specificity

There is the Cascade Specificity and also with attribute like **ID**, **class**,
etc.. You can use this table to know calculate the specificity:

| Style attribute | ID  | Class, Pseudo-class, attribute | Elements |
| --------------- | --- | ------------------------------ | -------- |

Example:

```

    <!-- HTML -->
    <nav id="nav">
      <li class="active">ah</li>
    </nav>

    /* CSS */
    #nav li {
        color: red;
    }
    /* Got a score of 0 1 0 1 */

    li.active {
        color: blue;
    }

    /* Got a score of  0 0 1 1 */
    /* The color is red */

```

We are an exception which is:

```
    !important
```

That can override everything. Don't use it, it's not a good practice.

### Colors and intentions

It's easier to declare the colors then to define the colors intentions

```
    :root {
    /* Define Colors as colors */
    --green: #00ebc7;
    --red: #ff5470;
    --yellow: #fde24f;
    --black: #1b2d45;
    --darkBlue: #00214d;
    --grey: #bfbfbf;
    --lightGrey: #f2f4f6;

    /* Define Colors intentions */
    --background: var(--lightGrey);
    --textColor: var(--black);
    }

    body {
    background: var(--background);
    color: var(--textColor);
    }

    .dark {
    --background: var(--black);
    --textColor: var(--lightGrey);
    }
```

## Typography

Useful links:

- [typewolf](https://www.typewolf.com/)
- [type-scale](https://www.type-scale.com)
- [v-fonts](https://v-fonts.com/)
- [fontpair](https://www.fontpair.co)
- [Google fonts](https://fonts.google.com/)
- [dafont](https://www.dafont.com/)
- [pangram pangram](https://pangrampangram.com/)
- [loremipsum](https://www.loremipsum.io)

We can use Type Scale to define the scale of our typographies inside our design
system

```
    /* Type */
    --headingFont: 'Space Mono', monospace;
    --bodyFont: 'Work Sans', sans-serif;
    --h1: 3.052em; /* or --fs1 // --fsh1 */
    --h2: 2.441em; /* or --fs2 // --fsh2 */
    --h3: 1.953em; /* or --fs3 // --fsh3 */
    --h4: 1.563em; /* or --fs4 // --fsh4 */
    --h5: 1.25em; /* or --fs5 // --fsh5 */
    --smallText: 0.8em;
```
