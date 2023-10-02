# Intro to CSS - Selectors

![Hero image](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will be able to target specific elements with CSS id, class, and combinator selectors.

As we learned with the `element selectors`, selectors are used to target specific HTML elements on a web page. This allows us to style those elements in any way you want. `id` and `class` selectors allow us to narrow down the elements we want to select. Rather selecting every `<div>` in our HTML, we can select only the `<div>`s that have a given `id` or `class`. 

## `id` selector

Id selectors are the most specific type of selector. They target elements with a specific `id` attribute which is defined in our HTML. 

To use an `id` selector, simply add the `#` symbol followed by the `id` value.

Let's change our `<p>` tag with the `id` of `about`:

```css
#about {
  font-style: italic;
  color: hotpink;
}
```

> 🚨 `id`'s on elements should always be unique.

## `class` selector

The `class` selector is similar to the `id` selector, but is less specific. We use the `class` selector to grab one of the values within the `class` attribute - yes, the `class` attribute accepts multiple space-separated values!

To use a `class` selector, simply add a `.` period followed by the CSS class name.

### You Do 💪

Target the `<div>`s with the class name `crazy`, and give them a border that is solid, 2px wide, and red in color. 


## Combinators

Combinators provide a powerful way to select elements based upon their relationship to other elements.

The most common combinator is the **descendant selector**.

We use the descendant selector to target elements **nested** within another element, **regardless of the depth of the nesting**.

A *descendant selector* is defined by using a *space* character between two other selectors:

```css
/* This will match all <span> tags nested anywhere within an <h3> tag having a class of "sub-title" */
h3.sub-title span { ... }
```

### You Do 💪
Using a descendant selector, set the text color of the `<p>` tag with the text of “This is a paragraph inside of the third DIV” to `darkgreen` and make it bold.


### There are three additional combinators

These are not quite as common but can come in handy…

- The **child selector** (`>`)
  The child selector is similar to the *descendant selector*, except that it only matches elements that are **direct** children, that is, nested only one-level deep:

  ```css
  /* Selects all <li> tags that are direct children of a <ul.top-level-list> */
  .top-level-list > li {
	  color: orange;
  }
  ```

  After adding this, you’ll notice that our `<li>` elements that are not **direct children** of the `<ul.top-level-list>` are still being colored orange. This is because of *inheritance* which we don't need to worry about right now.

- The **adjacent sibling selector** (`+`)
  ```css
  li + li {
    color: green;
  }
  ```

  Would select `<li>` tags only if they were preceded **immediately** by another `<li>` at the same level (sibling) and give them a color of green.

- The **general sibling selector** (`~`)
  Similar to the *adjacent sibling selector*. Selects all instances of the second element that appear after the first element, at the same level:

  ```css
  img ~ p {
	  border: 1px solid red;
  }
  ```

  Would target all `<p>` tags that are siblings following a `<img>`.

> 🧠 The last component listed in a combination selector determines what is targeted! For example, looking above, only `<p>` elements are selected, not the `<img>`.

### CSS Selectors - Key Takeaways

CSS selectors provide enormous capability and flexibility to target any element(s) for styling!

CSS selectors allow us to target an element, or elements, without assigning a bunch of ids.

As a general note, lean toward using classes instead of ids - remember, ids need to be unique.
