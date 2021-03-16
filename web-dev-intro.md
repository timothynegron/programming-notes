# What I learned in Week 1 at Code Immersives

### About

In this README file I try to simply explain the concepts I learned in week 1 at Code Immersives.

---------------------------------------------------------------------------

### Topics Covered

1. Markup Languages
2. Markdown
3. Introduction to HTML
4. Introduction to CSS
5. The Box Model
6. Introduction to CSS Flexbox Layout Module
7. Introduction to the Command Line Interface

---------------------------------------------------------------------------

### Markup Languages

Markup languages are used by computer programmers to arrange content within what they're creating in code. Markup languages come with a set of tags that can be used to tell a computer how the content assigned to the tag is intended to be displayed, arranged, or behave. The content and tag make up what is referred too as an **element**. 

In software development, a **tag** is a piece of code that tells the computer what type of content is within the tag. Tags are made with characters and or or symbols which are used to tell the computer what to do with the content that is after or between it. If the syntax within the tag is erroneous, or logically incorrect, then the computer would not translate the content correctly or at all.

---------------------------------------------------------------------------

### Markdown

Markdown is one of many markup languages. In Markdown, tags can contain content types such as text or a link source of a website, image, or YouTube video. 

In example, a header tag can be used to create a title. Emphasis tags can be used to make text in **bold** or *italics*. And an image tag can be used to display an image within the document. Here's how the source code for those examples would look in a Markdown file:

```markdown
# Title
**bold**
*italics*
![alt My Image](image.png)
```
>Markdown files require a .md file extension.

Markdown's source code is much easier for a human to read and write compared to other markup languages such as HTML. This is why Markdown is widely used by computer programmers to create quick documents that explain a computer program they've written. As another example, Markdown is also used to write down instructions like how to install and execute an application in discussion within GitHub.

#### **Here is a comparison of HTML source code versus Markdown source code:**

![alt Markdown Vs HTML](https://steemitimages.com/p/9vWp6aU4y8kyJM9JABQLRPjsM1uPXZuvARzQeXR3gBfvbngzeiXd5k7dtSQG9ZwyWcvXbQ886oKmBehKC5PsSjqHq8UYPLKnwFmpEwEtGw6xd9zZTfeAKJy3WvMdirKx3iUBQTX6V6FeiskRu?format=match&mode=fit&width=640)

---

### Introduction to HTML

HTML is another markup language that is used in software development. Like Markdown, HTML has tags to create and format elements, however, in HTML the tags can also contain attributes. In HTML, **attributes** give a computer more data about how an element should be presented. This gives someone programming a computer more control over the contents within the tag. An attribute is a component of an element that can be added if desired.

##### **Here is a visual break down of an element in HTML:**

![alt HTML Element Break Down](https://wikimedia.org/api/rest_v1/media/math/render/svg/37506127f0730d9b6035530f46c706af4e2319d4)


In example, a header tag can use a style attribute with a color property and red as its value to change the color of the text to red. Here's the source code for that example in HTML:

```html
<h1 style="color: red;">Title</h1>
```

> In order to get a similar result in Markdown, you would have to use HTML.

As you can see in the code above, not only is the syntax different compared with Markdown but HTML tags also always requires a closing tag - unlike most Markdown tags. Attributes must be referenced in the opening tag. The difference between Markdown and HTML expand dramatically when utilizing its ability to integrate CSS and Javascript.

> HTML stands for Hypertext Markup Language and has a .html file extension.

---------------------------------------------------------------------------

### Introduction to CSS

CSS is known as a styling language - not a markup language. It is supported by a number of languages. In HTML, CSS is used by computer programmers to style HTML elements. Where HTML is designed for structuring elements, CSS is designed for styling them. They are countless ways to present your content with CSS with how your font looks, the color of your background, how your elements are arranged, and you can even add some animation to your elements.

In CSS, a string of characters, and regularly with also one or two symbols, identify a selector. **Selectors** can contain a number of property and value pairs. Here is an example of how to define a selector when writing CSS code:

```css
name-of-selector {
  property: value;
  property: value;
}
```
> CSS code can be stored in a .html file but is conventionally stored in a .css file.

A **property** is a characteristic that is assigned to an element and a **value** is the data representing the details of that characteristic.

The most commonly used selectors in CSS are *tag selectors*, *class selectors*, and *id selectors*. 

Selectors with the same name as an HTML tag, such as `<h1>`, do not have to be referenced, assigned an attribute-value pair, in an opening tag. These selectors are referred to as tag selectors. For example:

```css
  h1 {
    property: value;
  }
```
Where `h1` is a known element in HTML. 

Class selectors, however, must be referenced in HTML by utilizing the **class attribute** inside the opening tag of an element. They are used to set elements with a specific set of properties like tag selectors but class selectors are not limited to affecting only one element. For example, in CSS:

```css
.class-selector-name {
  property: value;
  property: value;
  property: value;
}
```
And in HTML:
```html
<ol class="class-selector-name"><li>Hello</li></ol>

<ul class="class-selector-name"><li>World!</li></ul>
```
> It's also important to point out that **more than one class can be used in a HTML tag**. 

While tag selectors affect all elements with the same tag name and class selectors are used for groups of elements or more than one element, ID selectors are used to be set only with one element. ID selectors have to be referenced in HTML with a **id attribute**. Here's how that looks in CSS:

```css
#id-selector-name {
  property: value;
  property: value;
  property: value;
}
```
And in HTML:
```html
<button id="id-selector-name">Click Here!</button>
```

#### **Here is a picture of how Amazon.com looks without CSS:**

![alt HTML without CSS](https://i0.wp.com/css-tricks.com/wp-content/uploads/2019/04/s_601945040BCA3610D759145A4442799C97B904D9A9F8326DD30FDF0CF48A96B7_1555166166426_ScreenShot2019-04-13at7.35.27AM.png?ssl=1)

---------------------------------------------------------------------------

### The Box Model

*The Box Model* is a phrase that's used in CSS which refer's to how a web browser determines a element's size and distance from other elements. **Each element contains a content box enveloped by a padding box, border box, and margin box**. A computer programmer can control each of these components by manipulating their property values in code. This gives them the ability to arrange content wherever they wish.

#### **Here is a Box Model visualization:**

![alt Box Model](https://miro.medium.com/max/725/1*2jZwpWH9XO_QllhEpyGqMA.png)

#### **Here is a picture that highlights all  boxes on the Google home page:**

![alt All Boxes On Google Home Page](https://i.imgur.com/hfl6JWg.png)

---------------------------------------------------------------------------

### Introduction to CSS Flexbox

*Flexbox* is a CSS Layout Module that gives computer programmers the ability to easily arrange or change the appearance of HTML elements. It also helps computer programmers create responsive websites effortlessly. 

**Responsive websites** display elements the way a computer programmer intends for it to be displayed regardless of window size, screen size, and device type. In example, with responsive web design, if a browser's window on a personal computer is expanded or reduce horizontally or vertically, the elements that are rendered will adapt to the window's new dimensions.

In CSS, the Flexbox module can be added by simply writing `display: flex` within the curly braces of a selector. Then, a computer programmer can add one or two more simple lines of code to quickly place the elements where they wish. The results Flexbox has the ability to output can be accomplished without Flexbox but would require more lines of code and skill.  

#### Here is an image of what Flexbox can accomplish with just three lines of code:

![alt Flexbox Froggy Code And Result](https://i.imgur.com/PnEVWZy.png)

> Play Flexbox Froggy and learn how to use Flexbox: [Flexbox Froggy](https://www.flexboxfroggy.com)

The elements were spaced evenly with `justify-content: space-around;` and then moved to the bottom of the screen with `align-items: flex-end;`.



---------------------------------------------------------------------------

### Introduction to the Command Line Interface

A *command line interface*, also often referred to as CLI in text, is a way of interacting with a computer like a graphical user interface, however, it is a text based interface. Like a graphical user interface, with a command line interface, the user can create, read, update and delete files and folders. They can also run applications, view a calendar, install applications from the internet, and much more. 

A command line interface program must be given **commands** as inputs, and can also receive arguments after the command, to perform task and navigate through the interface. Computer programmers should learn how to use the command line interface because of how much can be accomplish with one single line of characters and symbols.

#### Here's how a command line interface looks:

![alt A Picture of a Command Line Interface](https://i.imgur.com/DkytKYy.png)

---------------------------------------------------------------------------

### Summary

In summary, in software development, markup languages are used for structuring content within a screen display. HTML is used for structuring elements and CSS is used for styling elements. Markdown is a simple markup language that can be used to write clear plain text media. The box model is a way of thinking about how a browser determines the size and distance of elements. Flexbox is a CSS Module that can be used to arrange or change the appearance of HTML elements. Finally, a command line interface is another way to interact with a computer like a graphical user interface, however, it is more time efficient and as a result gives computer programmers more power.