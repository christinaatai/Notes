# CSS

### Child divs

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

### Pseudo elements

If a pseudo element isn't showing, try adding `display: block` as explained [here](https://stackoverflow.com/questions/30526801/absolute-after-pseudo-element-not-displaying-under-relative-parent).
