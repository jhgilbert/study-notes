# Layout algorithms

CSS is a collection of layout algorithms such as Flexbox, Grid, Positioned Layout (achieved by setting the `position` property to values like `relative` or `absolute`), and Flow (default). Each algorithm implements each CSS property however it wants.

For example, `z-index` doesn't have an effect in Flow layout. But if you use `position` to switch to Positioned Layout, it takes effect. But you don't have to use Positioned Layout for `z-index` to take effect -- you could use Flexbox or Grid as well.

## Flexbox

Use Flexbox when you want to control the distribution of elements across either the horizontal or vertical axis.

## Grid

Use Grid when you want to achieve a two-dimensional layout (you want to arrange elements across both a horizontal and a vertical axis).
