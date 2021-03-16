# What I Learned in Week 2 at Code Immersives

### Introduction

In this README file I try to simply explain the concepts I learned in week 2 at Code Immersives.

---------------------------------------------------------------------------

### Topics Covered

1. Divs
2. CSS Flexbox with Divs
3. CSS Grid
4. Wireframes

---------------------------------------------------------------------------

### Divs

A `<div>` tag is a HTML element that is used to divide other HTML elements into sections. It is often referred to as a **container** and is normally used as a block element. A **block element** is a element that aligns the content within it in a vertical manner. In contrast, an **inline element** aligns the content within it in a horizontal manner. To display a div as a block element, the `display` property value must be set to `block` - which is a layout module. For example, with also an inline layout module for comparison, in CSS Code:

```css
#div-block {
  display: block;
  background-color: lightblue;
}

#div-inline {
  display: inline;
  background-color: lightgrey;
}
```
And in HTML:

```html
<div id="div-block">div-block content 1</div>
<div id="div-block">div-block content 2</div>

<hr>

<div id="div-inline">div-inline content 3</div>
<div id="div-inline">div-inline content 4</div>
```

The output will result as the following: 

![alt div example](https://i.imgur.com/cTIpxF0.png)

Most browsers do not need `display: block;` to be written in code in order for the div to be displayed as a block element. This is because they're conventionally used as block elements.

Not only are divs, which is short for division, used to divide other HTML elements into sections, they're often used to help arrange content with other technologies like *CSS Flexbox* and *CSS Grid*.

---------------------------------------------------------------------------

###  CSS Flexbox with Divs

One way to arrange content within a `<div>` is with *flexbox*. As discussed in week 1, flexbox is a type of layout module. A `<div>` can be set with an id attribute that is an id selector that sets the property `display` with a value of `flex`. For example, in HTML:

```html
<div id="div-1">
  <div>Content 1</div>
  <div>Content 2</div>
  <div>Content 3</div>
</div>
```

And on CSS:

```css
#div-1 {
  display: flex;
  background-color: lightblue;
}
```

The output of this code will result as the following:

![alt Flexbox and Divs example 1](https://i.imgur.com/eg3z610.png)

The Flexbox Layout module has been applied to the `<div>`. Also, as seen above, flexbox has formatted the content to be inline but referred to as a row in flexbox. With the flexbox module added, more flexbox properties on the id tag selector can be added. Flexbox has many property and value pairs. The property and value pairs can affect the order, position, and the appearance of the content. Here are some code examples of the effects flexbox property and value pairs can have on HTML elements:

```css
#div-1 {
  display: flex;
  justify-content: center;

  background-color: lightblue;
}
```
![alt test ](https://i.imgur.com/9244nYl.png)

Also:

```css
#div-1 {
  display: flex;
  align-items: center;
  flex-direction: column;

  background-color: lightblue;
}
```

![alt column example](https://i.imgur.com/rkMU5uX.png)

Additionally:

```css
#div-1 {
  display: flex;
  justify-content: flex-end;

  background-color: lightblue;
}
```

![alt flex end example](https://i.imgur.com/pxkY92v.png)

> Here is a really good article on all Flexbox property-value pairs: [Flexbox Guide](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)

Flexbox gives computer programmers the ability to layout content only in one dimension at a time. That is, either in a horizontal (row) or in a vertical  (column) fashion.

---------------------------------------------------------------------------

### CSS Grid

Another way to arrange content within a `<div>` is with CSS Grid Layout. Unlike Flexbox, *Grid* gives computer programmers the ability to layout content in two dimensions - both rows and columns simultaneous. If a `<div>` is set as a flexbox container, it would be limited to laying out content in either a row or a column. In contrast, if a `<div>` was set as a grid container, it would be able to layout the content in both a row and a column. To use CSS Grid, you can define a `<div>` as a grid container using the `display` property. For example:

```css
#div-parent {
  display: grid;
}
```
And on HTML:

```html
<div id="div-parent">


</div>
```

Next, you have to define the grid's rows and columns using CSS Grid's dedicated properties:

```css
#div-parent {
  display: grid;

  grid-template-rows: 25% 50% 25%;
  grid-template-columns: 25% 50% 25%;
}
```

In the code above, the `grid-template-rows` property creates three rows. Two rows were set to take up 25% of space of the div's height and one row was set to take up 50% of it. The `grid-template-columns` property creates three columns. Two columns will take up 25% of space of the div's width and one will take up 50% of it.

To layout content when using grid, child elements need to be created as well:

```html
<div id="div-parent">
  <div id="div-child-1"><h1>Row 1</h1></div>
  <div id="div-child-2"><h1>Row 2</h1></div>
  <div id="div-child-3"><h1>Row 3</h1></div>
</div>
```

And on CSS:

```css
#div-parent {
  display: grid;

  grid-template-rows: 25% 50% 25%;
  grid-template-columns: 25% 50% 25%;
}

#div-child-1 {}

#div-child-2 {}

#div-child-3 {}
```

There's many CSS Grid property and value pairs that could help layout content. In example, on CSS:

```css
#div-child-1 {
  grid-row: 1;
  grid-column: 1 / 4;

  background-color: lightsalmon;
}

#div-child-2 {
  grid-row: 2;
  grid-column: 1 / 4;

  background-color: lightblue;
}

#div-child-3 {
  grid-row: 3;
  grid-column: 1 / 4;

  background-color: lightgrey;
}
```

The output would result as the Following:

![alt Grid output example 1](https://i.imgur.com/iI7U4qU.png)

> Learn how to use CSS Grid by playing Grid Garden: [CSS Grid Garden](https://cssgridgarden.com) 

Where `grid-row` tells the child element which row to reside in and grid-column tells the child element which row to reside in. An element can span to many columns and many rows at once.



---------------------------------------------------------------------------

### Wireframes

A **wireframe** is low fedelity representation of an intended design for an application. When creating a graphical user interface, a computer programmers workflow, normally starts with creating a wireframe. A wireframe can be created with the many wireframe software products that are made alvailable across the internet, but can also be done with a paper and pencil. Wireframes helps programmers have an idea of how they should iterate through the process of creating the interface. Furthermore, a wireframe can help give them an idea of what mark up elements, structure, and technologies they need to use to layout the content of their application.

![alt Wireframe visual example](https://balsamiq.com/assets/learn/articles/mobile-web.png)

---------------------------------------------------------------------------

### Summary

In summary, `<div>` tags are used to divide content on websites. Flexbox has many property and value pairs that gives computer programmers the ability to easily layout content. CSS Grid is a layout module based on the concept of a grid. Wireframes help web designers visualize how they should layout their content and it also helps them have an idea of how they should structure HTML elements.
