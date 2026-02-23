1. @layer - Organize CSS specificity
This helps manage cascade and makes overriding styles more predictable.

``` css
@layer reset, base, components, utilities;

@layer base {
    /* Define font sizes, resets */
}

@layer components {
    /* Buttons, cards, forms */
}
```

2. clamp() - Replace media query font sizing
Current approach uses multiple media queries for --font-size. Could use:

``` css
:root {
    --font-size: clamp(100%, 1vw + 0.5rem, 131.25%);
}
```

3. Logical properties - Already partially used, expand it

``` css
/* Instead of: margin-left, margin-right */
nav ol:first-of-type {
    margin-inline-start: calc(var(--nav-element-spacing-horizontal) * -1);
}

/* For padding on all sides */
details summary {
    padding-inline: var(--nav-link-spacing-horizontal);
}
```

4. color-mix() - Generate hover/active states dynamically

``` css
button {
    --background-color: var(--primary-background);

    &:hover {
        --background-color: color-mix(in srgb, var(--primary-background) 80%, black);
    }
}
```

5. Container Queries instead of page-based @media - enables more responsive Component-based styling

``` css
@container (min-width: 700px) {
    .grid {
        grid-template-columns: repeat(auto-fit, minmax(0%, 1fr));
    }
}
```
6. accent-color - Simplify form element theming
``` css
input:where([type='checkbox'], [type='radio'], [type='range']) {
    accent-color: var(--primary);
}
```
7. text-wrap: balance - Better heading typography
``` css
h1, h2, h3 {
    text-wrap: balance;
}
```
8. scrollbar-gutter - Prevent layout shift
``` css
html {
    scrollbar-gutter: stable;
}
```
9. Modern color spaces - oklch() for better color manipulation

``` css
:root {
    --primary: oklch(55% 0.15 142); /* More perceptually uniform */
}
```
10. :has() - More powerful parent/context selection (already using)
Could replace some .has( with simpler selectors in certain cases.

11. adopt richer table & RTL demos as in https://lissomware.github.io/css/

12. hr styling and vertical hr divider as in classless shadcn

13. add `<aside>` styling similar to mvp.css
