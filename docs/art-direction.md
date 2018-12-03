[< Back home](/responsive-image-widths/)

# Use case: Art Direction

How to deal with multiple `<source>` with `mix/max-width` media queries (Art Direction)?

If you have some code like this:

```html
<picture>
  <source media="(min-width: 800px)" srcset="…" sizes="…">
  <img srcset="…" sizes="…" alt="…">
</picture>
```

You will have to run the script twice, with (at least) these parameters, to get widths for both `srcset`s:

```shell
npx responsive-image-widths --max-viewport 799 --verbose
npx responsive-image-widths --min-viewport 800 --verbose
```