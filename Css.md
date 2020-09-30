# CSS

## Mixins

#### Optimizing cascading attributes
In this example, border can be either light or dark and with or without opacity; therefore, there are four combinations of color and opacity. You can use `@if` statements inside a mixin to optimize the combinations.

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

## Pseudo elements

If a pseudo element isn't showing, try adding `display: block` as explained [here](https://stackoverflow.com/questions/30526801/absolute-after-pseudo-element-not-displaying-under-relative-parent).

