# Sneaker Sales - Landing Page

[![Netlify Status](https://api.netlify.com/api/v1/badges/8dd3688a-8f84-4c53-8702-a2cd7fcbe574/deploy-status)](https://sneaker-sales.netlify.app)

👆🏽 click to check the live page

This is a 1 page landing page.

## Demo
https://user-images.githubusercontent.com/51871665/128419806-927d93b9-7000-4141-b6cc-8b6824fdfb17.mov

## How it's built

**Tech used**: HTML, CSS

## Lesson Learnt

### How to start styling with CSS

1. Set basic css first

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

2. Style the reusable class first

### Use `clamp()` to make fluid typography

`clamp(min, prefer value, max)`

Prefer value can be set to change with the viewport. The minumum and the maximum can prevent the font size to be too small or too huge.

### Use `@supports` to specify specific style if the browser can support 

In scss, we can nest the support

```scss
.hero {

    @supports(property: value){
        property: value;
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

### How to make text wrap around a floated element

`shape-outside` property can achieve that. The shape can be the box sizing value, basic shapes like circle, ellipse, polygon, path or image. `shape-margin` can create margin based on that shape. The effect stops at the image's bound.

### Trick to make a real square

We can use `padding: 100% 100% 0 0` to create a real square in case the element is not a real square. Note that the percentage value in padding and margin percentage is with respect to the width.

### Stacking context

Some special properties will cause elements to form a stacking context. The `z-index` values were only compared among children elements. 

Properties like below will form a stcking context:

1. `position` with `fixed` or `sticky` value

2. `position` with `relative` or `absolute` value and `z-index` is not 0

3. Children of a `flex` or `grid` container and `z-index` is not `auto`

4. `opacity` is less than 1

5. `mix-blend-mode` is not `normal`

6. Element with `transform`, `filter`, `perspective`, `clip-path`, `mask`/`mask-image`/`mask-border` and its value is not `none`


### Custom property

The custom property is inherited so we should provide the value at the class or before.


### How to blend element's background images and background color

Use `background-blend-mode`. The common `multiply` value can achieve the effect like printed two images on transparent film overlapping. 
