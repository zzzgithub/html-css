# Grids

Making flexible and responsive grids using HTML & CSS.

### [▶ Video playlist for grids](https://www.youtube.com/playlist?list=PLWjCJDeWfDdeUChfM6TV2U7jzQVRjsu60)

---

## Flexible grids

Flexible grids in CSS are composed of nested `<div>` elements within a row.

```html
<div class="grid">
	<div class="unit">Grid Unit 1</div>
	<div class="unit">Grid Unit 2</div>
	<div class="unit">Grid Unit 3</div>
</div>
```

Within CSS, we can then float of each of the units to fit beside each other.

```css
.grid {
	overflow: hidden;
}

.unit {
	float: left;
	/* The width is set to 33% because we want to fit three columns in our row. */
	width: 33.3333%;
}
```

This will create a grid row with three columns inside that flex with the width of the browser.
The major problem is that there is no space, or gutter, between each column.
To solve the problem in the most flexible manner, we can put another class on the unit to add the gutter’s padding.

```html
⋮
<div class="unit gutter">
	Grid 1
</div>
⋮
```

```css
.gutter {
	padding-left: 1em;
	padding-right: 1em;
}
```

Using a `.gutter` gives us the flexibility to choose whether we want padding or not.
So we could create grid units with full bleed images.

```html
⋮
<div class="unit">
	<img src="http://placehold.it/500x500" alt="">
</div>
⋮
```

*If you combine the grid system with the modular typography system you’ll see that the type system comes with a series of gutter classes relative to your type size.*

We can also create a column in our grid that takes up ⅔ of the available space—a column that is double width.

```html
⋮
<div class="unit unit-2-3">
	Double Width 1
</div>
⋮
```

```css
.unit-2-3 {
	width: 66.6667%;
}
```

**Videos**

1. [Grids: flexible grids](https://www.youtube.com/watch?v=KN-KIG3mcxE&list=PLWjCJDeWfDdeUChfM6TV2U7jzQVRjsu60&index=1)

---

## Responsive grids

We can extend our flexible grids to be responsive using a technique with multiple classes on our `<div>` elements.

```html
<div class="grid">
	<div class="unit unit-s-1 unit-m-1 unit-l-1-3">Grid Unit 1</div>
	<div class="unit unit-s-1 unit-m-1-2 unit-l-1-3">Grid Unit 2</div>
	<div class="unit unit-s-1 unit-m-1-2 unit-l-1-3">Grid Unit 3</div>
</div>
```

You’ll notice multiple classes on each of the `.unit` `<div>` elements.
Each class represents the position the `<div>` will be in at each different screen size.

- `unit-s-1`—means the unit takes up 100% of the space on small screens
- `unit-m-1-2`—means the unit takes up ½ the available space on medium screens
- `unit-l-1-3`—means the unit takes up ⅓ the available space on large screens

In our CSS we would then create these classes and style them within different media queries.

```css
.unit {
	float: left;
}

.unit-s-1 {
	width: 100%;
}

@media only screen and (min-width: 38em) {

	.unit-m-1 {
		width: 100%;
	}

	.unit-m-1-2 {
		width: 50%;
	}

}

@media only screen and (min-width: 60em) {

	.unit-l-1-3 {
		width: 33.3333%;
	}

}

```

**Videos**

1. [Grids: responsive grids](https://www.youtube.com/watch?v=3Gm785OgJ4E&list=PLWjCJDeWfDdeUChfM6TV2U7jzQVRjsu60&index=2)

---

## Complete grid system

A complete grid system would be composed of rows that can have thirds, quarters, fifths, etc. As many columns as you’d like.

Grid systems also have a series of other capabilities:

1. `hidden` classes provide the ability to hide & show units in specific screen sizes
2. `offset` classes provide the ability to push units way from the edge of the screen and other units

**Videos**

1. [Grids: hiding units on different screen sizes](https://www.youtube.com/watch?v=9Y8IyXFqbNU&list=PLWjCJDeWfDdeUChfM6TV2U7jzQVRjsu60&index=3)
2. [Grids: simplifying fractions for unit sizes](https://www.youtube.com/watch?v=BNFKLqYl8rU&list=PLWjCJDeWfDdeUChfM6TV2U7jzQVRjsu60&index=4)
3. [Grids: pushing units aside using offsets](https://www.youtube.com/watch?v=kVMdNbrHgbQ&list=PLWjCJDeWfDdeUChfM6TV2U7jzQVRjsu60&index=5)
4. [Grids: grids inside grids](https://www.youtube.com/watch?v=hpwjNC4Eo-U&list=PLWjCJDeWfDdeUChfM6TV2U7jzQVRjsu60&index=6)

**Tools**

- **[☛ Gridifier](http://tjb.io/grids)** — A tool I created for myself to generate the default CSS code
- [Grid Builder for Stylus](https://gist.github.com/thomasjbradley/7186573)

---

## Grid frameworks

Bootstrap is a prototyping CSS framework that comes setup with a theme, grids, and components to help you create a quick prototype for any website.

- **<http://getbootstrap.com/>**

*Helpful links*

- [Net.Tuts+: Mobile First with Bootstrap 3](http://net.tutsplus.com/tutorials/html-css-techniques/mobile-first-with-bootstrap-3/)
- [SitePoint: Understanding Twitter Bootstrap 3](http://www.sitepoint.com/understanding-twitter-bootstrap-3/)

*Other frontend grid systems & libraries*

- [Foundation by Zurb](http://foundation.zurb.com/)
- [Pure by Yahoo](http://purecss.io/)
- [Gridset](https://gridsetapp.com/)
- **[☛ Gridifier](http://tjb.io/grids)** — A tool I created for myself to generate the default CSS code

---

## Videos

1. [Grids: flexible grids](https://www.youtube.com/watch?v=KN-KIG3mcxE&list=PLWjCJDeWfDdeUChfM6TV2U7jzQVRjsu60&index=1)
2. [Grids: responsive grids](https://www.youtube.com/watch?v=3Gm785OgJ4E&list=PLWjCJDeWfDdeUChfM6TV2U7jzQVRjsu60&index=2)
3. [Grids: hiding units on different screen sizes](https://www.youtube.com/watch?v=9Y8IyXFqbNU&list=PLWjCJDeWfDdeUChfM6TV2U7jzQVRjsu60&index=3)
4. [Grids: simplifying fractions for unit sizes](https://www.youtube.com/watch?v=BNFKLqYl8rU&list=PLWjCJDeWfDdeUChfM6TV2U7jzQVRjsu60&index=4)
5. [Grids: pushing units aside using offsets](https://www.youtube.com/watch?v=kVMdNbrHgbQ&list=PLWjCJDeWfDdeUChfM6TV2U7jzQVRjsu60&index=5)
6. [Grids: grids inside grids](https://www.youtube.com/watch?v=hpwjNC4Eo-U&list=PLWjCJDeWfDdeUChfM6TV2U7jzQVRjsu60&index=6)

## Links

1. [A List Apart: Content-out Layout](http://alistapart.com/article/content-out-layout)
