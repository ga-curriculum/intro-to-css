# Intro to CSS - Common Properties

![Hero image](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will learn how to use CSS font, color, and background properties.

CSS properties are used to control the appearance and behavior of HTML elements. There are many different CSS properties, but some of the most common ones are font properties, color, and background.

## Font properties

[Font](https://developer.mozilla.org/en-US/docs/Web/CSS/font) properties let us control the appearance of text on a web page. Some of the most common are:

- `font-family`: Specifies the font family of the text. 
- `font-size`: Specifies size of the text.
- `font-weight`: Specifies the weight of the text (normal, bold, light).
- `font-style`: Specifies the style of text (italic, [oblique](https://css-tricks.com/almanac/properties/f/font-style/), or normal).
- `text-align`: Specifies the alignment of the text (left, center, right)

Let's try styling our `<h3>` elements:

```css
h3 {
  font-family: Arial, sans-serif;
  font-size: 28px;
  font-weight: bold;
  font-style: italic;
  text-align: center;
}
```


## `color`

The [`color`](https://developer.mozilla.org/en-US/docs/Web/CSS/color_value) property allows us to specify the color of various elements in our HTML. 

There are three common ways to specify color values in CSS: 

- [hexadecimal](https://www.freecodecamp.org/news/how-hex-code-colors-work-how-to-choose-colors-without-a-color-picker/) values: `#FF0000 `
- RGB values: `rgb(255, 0, 0)`
- Color name: `red`

All three of the example values above will give us the same color! 

Any of the three methods is acceptable for declaring a color value, but there are some advantages to using RGB or hex codes, namely precision and range.

Hex codes and RGB values afford us a certain degree of precision that color names simply cannot. One of the reasons for this is that once you deviate from basic colors like red, green, blue, and so on, color names can be subjective, meaning they have a tendency to vary depending on the browser or device you're using. 

Another advantage is that hex codes and RGB values give us a lot more range when selecting colors. There are only [140 predefined color keywords](http://web.simmons.edu/~grovesd/comm244/notes/week3/css3-color-names) in CSS, but there are roughly 16 million possible hex code color combinations, and the same is true for RGB values.



## `background`

The [`background`](https://developer.mozilla.org/en-US/docs/Web/CSS/background) property allows us to specify an element's background color, image, or gradient using a color value, image URL, or combination of the two. 

`background` is a **shorthand property**, meaning it can be used to set multiple background properties on one line. We can set the following properties using the `background` shorthand property (or we can use the following as standalone properties):

- `background-color`
- `background-image`: Allows us to set an image as the background of an element. We can either use a hosted image URL from the web, or we can import a file into our project and use a local URL. We can also create a [linear gradient](https://developer.mozilla.org/en-US/docs/Web/CSS/gradient/linear-gradient) instead of using an image.
- `background-repeat`
- `background-position`
- `background-size`
- `background-attachment`
- `background-clip`
- `background-origin`

Let's change the background of our `<div>` elements:

```css
div {
  background: linear-gradient(to top, #fff1eb 0%, #ace0f9 100%);
}
```
