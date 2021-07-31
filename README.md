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

### Using `clamp()` to achieve fluid typography

`clamp(min, prefer value, max)`

prefer value can be set to change with the viewport. The minumum and the maximum can prevent the font size to be too small or too huge.