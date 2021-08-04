# Sneaker Sales Landing Page

## Lesson Learnt

### Style from the reusable class first

### Set basic css

```css
*, *::before, *::after {
    box-sizing: border-box;
}

body {
    margin: 0;
    font-family: 'Noto Sans JP', sans-serif;
    line-height: 1.6;
}
```

### Use `clamp()` to achieve fluid typography

`clamp(min, prefer value, max)`

prefer value can be set to change with the viewport. The minumum and the maximum can prevent the font size to be too small or too huge.

### Use `@supports` to specify the style if the browser can support specific property

In scss, we can nest the support
```scss
.hero {
    color: white;
    text-align:center;
    padding: 15em 0;
    background: #222;

    @supports(background-blend-mode:multiply){
        background:url(../img/shoe-3.png),
        radial-gradient(#444, #111);
        background-blend-mode: multiply;
    }
}
```

In css, use it like this: 
```css
@support (property: value){
    .class{

    }
    element{

    }
}
```


### padding and margin percentage is based on the width

### Trick to make a real square
Using padding:100%;

### Transform createa stacking within the element block

### Stacking context

### Custom property

The custom property is inherited so we should provide the value at the class or before.

### How to make text wrap around a defined shape

`shape-outside` property can achieve that. The shape can be the box sizing value, basic shapes like circle, ellipse, polygon, path or image. 