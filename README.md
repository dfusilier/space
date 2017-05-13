# Space

Comprehensive set of Sass mixins and utility classes for organizing space. Includes breakpoints, grid, and space patterns. Inspired by [Space in Design Systems](https://medium.com/eightshapes-llc/space-in-design-systems-188bcbae0d62) by Nathan Curtis.

Uses a modular scale based on 4px by default.

```
// Unit on which all spacing is based
$SPACING_BASE: 4px !default;

// Modular spacing scale
$SPACING_LEVELS: (0, 0.5, 1, 2, 3, 4, 6, 8, 12, 16) !default;
```


## Insets

Use insets to add space between a parent and its children. Adds padding on all four sides.

#### Mixin
`@include inset($level);`

#### Utility classes
`.inset-[level]` or `.inset-[level]-[breakpoint]`

## Sections

Apply `.section` along with an `.inset` to the major regions of your layout to ensure the horizontal padding aligns with you site's standard page gutters.



## Stack spacing

Use stack spacing to add vertical space between siblings. Adds margin to the bottom of the element.

#### Mixin
`@include stack($level);`

#### Utility classes
`.stack-[level]` or `.stack-[level]-[breakpoint]`



## Inline spacing

Use inline spacing to add horizontal space between siblings. Adds margin to the right of the element.

#### Mixin
`@include inline($level);`

#### Utility classes
`.inline-[level]` or `.inline-[level]-[breakpoint]`



## Gutter spacing

Use gutter spacing to add gutters between columns. When used on rows, adds padding to either side of each col and negative margins to either side of the row.

#### Mixin
`@include gutter($level);`

#### Utility classes
`.gutter-[level]` or `.gutter-[level]-[breakpoint]`



## Bustout spacing

Use bustout spacing to enable children to "bustout" of their parent. Adds negative margin to the left and right of the element.

#### Mixin
`@include bustout($level);`

#### Utility classes
`.bustout-[level]` or `.bustout-[level]-[breakpoint]`



## Breakpoints
Use the default breakpoints included below, or override with your own.

```
$BREAKPOINTS: (
  xs: null,
  sm: 576px,
  md: 768px,
  ld: 992px,
  xl: 1200px
) !default;
```

## Grid
A fairly standard flexbox grid composed of columns, rows, and containers. Use the default 12-column grid by default, or include your own:

```
$GRID_COLUMNS: 12 !default;
```

#### Rows and columns
`.row`
`.col`, `.col-[level]`, or `.col-[level]-[breakpoint]`

#### Containers
Use containers to limit the size of rows. Use the default containers, or override with your own:

```
$GRID_CONTAINERS: (
  xs: 360px,
  sm: 540px,
  md: 720px,
  lg: 960px,
  xl: 1140px
) !default;
```

`.container-max-[breakpoint]`

