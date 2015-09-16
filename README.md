# sass-svg
Inline SVG for Sass.

## Quick Start
- `npm install sass-svg --save`

```scss
// Will likely be ../node_modules/sass-svg/index
@import 'path/to/sass-svg';

.arrow {
  @include svg {
    @include svg('polygon', (
      fill: green,
      points: (50,100 0,0 0,100)
    ));
  }
}
```

**Result:**
```css
.arrow {
  background: url("data:image/svg+xml;charset=utf8,%3Csvg%20xmlns
    %3D%22http%3A%2F%2Fwww%2Ew3%2Eorg%2F2000%2Fsvg%22%3E%3Cpolygon
    %20fill%3D%22green%22%20points%3D%2250%2C%20100%200%2C%200%200
    %2C%20100%22%2F%3E%3C%2Fsvg%3E");
}
```
