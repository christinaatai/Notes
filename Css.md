# SCSS

## Mixins

#### Optimizing cascading attributes
In this example, border can be either light or dark and with or without opacity; therefore, there are four combinations of color and opacity. You can use `@if` statements inside a mixin to optimize the combinations.

Also note, instead of having an `@if` statement inside of an `@if` statement, you can follow the format in the example.

```
@mixin horizontal_border($opacity: false, $dark: false) {
  $border_color: $white;
  @if $dark == true {
    $border_color: $bg_dark;
  }
  @if $opacity == true {
    background-color:rgba($border_color, $opacity_1);
  } @else {
    background-color: $border_color;
  }
  content: '';
  position: relative;
  width: calc(100% + 24px + 24px);
  height: 2px;
  top: 9px;
  bottom: 0;
  left: -24px;
  display: block;
}
```



## Child divs

```
.myTestClass > * {
    color:red;
    margin: 0 20px;
}
```

Meaning: All children in myTestClass will have red text. Grandchildren will not be affected.

```
div > p {
  background-color: yellow;
}
```

Meaning: All p in parent div will have a yellow background.

## Classes

If you want to style a block with two classnames, append the second classname onto the first classname.

```
[class^=pb_button_toolbar]{
  &[class*=_primary].dark {
    & > [class^=pb_button]::after {
      @include horizontal_border($opacity: true, $dark: true)
    }
  }
}
```

In the example above, `.dark` is appended onto the class `pb_button_toolbar_primary`

## Pseudo elements

If a pseudo element isn't showing, try adding `display: block` as explained [here](https://stackoverflow.com/questions/30526801/absolute-after-pseudo-element-not-displaying-under-relative-parent).

## CSS Selectors
| Example      | Description |
| ----------- | ----------- |
| `.name1.name2`      | All elements with `name1` AND `name 2`       |
| `.name1 .name2`   | All elements with `name2` that has a parent with `name1`        |
| `*`   | All elements        |
| `div > p`   | Selects all p elements that has a `div` parent        |
| `div + p`  | All `p` elements right after `div` element        |
| `p ~ div`   | All `div` emements that come before any `p` element        |



