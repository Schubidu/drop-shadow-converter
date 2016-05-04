#drop-shadow-converter
Convert Photoshop Drop Shadows to CSS3 Box & Text Shadows - See more at: http://www.melanieceraso.com/psd-to-css3/
Use original photoshop drop shadow in your less or scss.

##Less

```less
@import "../less/drop-shadow-converter";

/* just color */
div {
  .dropShadowConverter(#123);
  box-shadow: @boxShadow;
  text-shadow: @textShadow;
}

/* opacity */
div {
  .dropShadowConverter(#000, @opacity: 25%);
  box-shadow: @boxShadow;
  text-shadow: @textShadow;
}

/* distance */
div {
  .dropShadowConverter(#000, @distance: 10px);
  box-shadow: @boxShadow;
  text-shadow: @textShadow;
}

/* distance and angle */
div {
  .dropShadowConverter(#000, @angle: 45, @distance: 10px);
  box-shadow: @boxShadow;
  text-shadow: @textShadow;
}

/* spread and size */
div {
  .dropShadowConverter(#000, @spread: 15, @size: 15px);
  box-shadow: @boxShadow;
  text-shadow: @textShadow;
}

/* all together */
div {
  .dropShadowConverter(#123, @angle: 45, @distance: 10px, @spread: 15, @size: 15px, @opacity: 25%);
  box-shadow: @boxShadow;
  text-shadow: @textShadow;
}

```

##SCSS
```scss
// math functions are not included in sass
@import "../scss/mathfunctions";
// import converter
@import "../scss/drop-shadow-converter";

/* just color */
div {
  box-shadow: drop-shadow-converter(#123);
  text-shadow: drop-shadow-converter(#123, $is-text-shadow: true);
}

/* opacity */
div {
  box-shadow: drop-shadow-converter(#000, $opacity: 25%);
  text-shadow: drop-shadow-converter(#000, $opacity: 25%, $is-text-shadow: true);
}

/* distance */
div {
  box-shadow: drop-shadow-converter(#000, $distance: 10px);
  text-shadow: drop-shadow-converter(#000, $distance: 10px, $is-text-shadow: true);
}

/* distance and angle */
div {
  box-shadow: drop-shadow-converter(#000, $angle: 45, $distance: 10px);
  text-shadow: drop-shadow-converter(#000, $angle: 45, $distance: 10px, $is-text-shadow: true);
}

/* spread and size */
div {
  box-shadow: drop-shadow-converter(#000, $spread: 15, $size: 15px);
  text-shadow: drop-shadow-converter(#000, $spread: 15, $size: 15px, $is-text-shadow: true);
}

/* all together */
div {
  box-shadow: drop-shadow-converter(#123, $angle: 45, $distance: 10px, $spread: 15, $size: 15px, $opacity: 25%);
  text-shadow: drop-shadow-converter(#123, $angle: 45, $distance: 10px, $spread: 15, $size: 15px, $opacity: 25%, $is-text-shadow: true);
}
```
