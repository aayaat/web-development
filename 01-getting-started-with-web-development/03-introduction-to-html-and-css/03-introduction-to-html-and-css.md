# Introduction to HTML and CSS

Every language has to follow a set of rules for you to be able to effectively speak or write in that language. This is the same with HTML and CSS, and this is what syntax and construct means, the rules governing how you speak and/or write in a particular language.

## HTML

Hypertext Markup Language (HTML) is the World Wide Web's core markup language.

Originally, HTML was primarily designed as a language for semantically describing scientific documents. These days, we use HTML for things that were never thought of at that time. This is due to its general design, which enabled it to be adaptable, over time, to describe a number of other types of documents and even applications.

Please consider the following design and the equivalent HTML code

![HTML Design and Code](/home/ku/www/ayaat/web-development/01-getting-started-with-web-development/assets/html-design-and-code.png)



### HTML terminologies

The key syntax and constructs for HTML includes **Tags**, **Attributes**, **Elements**  and **Content**. Lets explore these important and often used terminologies below.

#### Elements

Elements (which are created using tags) are the building blocks of a web page. 

Every HTML document, contains such collections of many elements. If you look at the source code of web pages in the browser, you will see such collections of elements that makes up those pages.

Lets explore a visual representation of a HTML element.

![Anatomy of a HTML Element]()

This element has three parts: a opening tag,  content, and a closing tag. 

![Anatomy of a HTML Element]()

This element also has three parts: a opening tag,  content, and a closing tag. 

![Anatomy of a HTML Element]()

This element has four parts: a opening tag,  content, a closing tag, and an attribute.

---

There are six different **kinds of elements** as of the W3C Recommendation, 14 December 2017.

1. **Void elements** :: These elements cannot have any content (since they have no closing tag). Below are the list of void elements

   (`area`, `base`, `br`, `col`, `embed`, `hr`, `img`, `input`, `link`, `meta`, `param`, `source`, `track`, `wbr`)

2. The **raw text elements**(`script`, `style`)

3. **Escapable raw text elements** (`textarea`, `title`) and 

4. **Normal elements** (All other allowed HTML elements) are elements that we will be dealing with in this course. (`h1, p, a, img etc`)

5. The other remaining two (**the template elements** and the **foreign elements**) is beyond the scope of this course.

#### Tags

Tags are the bits that create elements. They are used to delimit the start and end of an element. Most of the time tags commonly occur in pairs of an opening and closing tag.

The **opening tag**: This consists the name of the element wrapped in opening and closing angle brackets.

The **closing tag**: This is the same as the opening tag, except that in includes a forward slash before the element name.

#### Elements vs. Tags

Now the most confusing stuff about elements and tags is that Elements are not tags. One thing, you should remember is that, HTML documents contain tags, but do not contain the elements. The elements are only generated after the parsing stage (elements are part of the DOM) by the browser, from these tags.

#### Attributes

Elements may have associated properties, called **attributes**, which may have values (by default, or set by authors or scripts). 

Attributes generally are in two parts: attribute **name** and  **value**

![Anatomy of an attribute]()

The attribute name comes before the equal to `=` symbol followed by the attribute value in quotation, written `name=value`.

Few things to remember when dealing with attributes are:

- All attributes goes into the opening tag
- A space between it and the attribute name
- The attribute name followed by an equal to `=` symbol and then followed by the attribute value.
- The attribute value in quotations, this not required, but helps to avoid many problems in your code
- If you have more than one attribute, they must be separated by space.
- Attributes can appear in any order

#### Content

The contents of an element are its children in the DOM. It is what goes in between the opening and a closing tag of an element. 

When the browser parsed the HTML, the content is what users see. 

#### Document Object Model (DOM)

The Document Object Model (DOM) is a cross-platform and language-independent application programming interface that treats an HTML, XHTML, or XML document as a tree structure where in each node is an object representing a part of the document. The objects can be manipulated programmatically and any visible changes occurring as a result may then be reflected in the display of the document.

![DOM tree of the profile page]()

#### Documents vs. DOM

HTML documents are delivered as **documents**. These are then parsed, which turns them into the Document Object Model (DOM) internal representation, within the web browser

### HTML Document Structure (Skeleton)

This sets the foundation for every HTML document. It is not useful by it self. 

HTML document structure is composed of the following:

1. `<!DOCTYPE html>` , the document type declaration, which describes the type of document

2. The `html` element: Main root element, it represents the root (top-level element) of an HTML document, so it is also referred to as the *root element*. All other elements must be descendants of this element.


   Within the main root, we have two main parts:

   1. The `head` element: Document metadata contains information about the page. This includes information about styles, scripts and data to help software ([search engines](https://developer.mozilla.org/en-US/docs/Glossary/Search_engine), [browsers](https://developer.mozilla.org/en-US/docs/Glossary/Browser), etc.) use and render the page.
   2. The `body` element: Sectioning root represents the content of an HTML document. There can be only one `<body>` element in a document.

Here is an example of the HTML Document Structure

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    
</body>
</html>
```

Let's explore a visual representation of a HTML document structure

![HTML document structure]()



## CSS

**C**ascading **S**tyle **S**heets (CSS) is a style sheet language that is use to selectively style HTML elements.

### CSS terminologies

The key syntax and constructs for CSS includes  **rules**, **selectors**, **declarations**, **properties**, and **property values**. Lets explore these important and often used terminologies below.

#### Rules

A CSS document is a series of qualified rules, which are usually **style rules** that apply CSS properties to elements, and **at-rules**, which define special processing rules or values for the CSS document. 

A qualified rule starts with a **prelude** then has a block `{  }`  (curly braces) attached to the prelude. The block contains a sequence of declarations.

```css
prelude {
    declaration(s)
}
```

The meaning of the prelude varies based on the context that the rule appears in - for style rules, it’s a selector, which specifies what elements the declarations will apply to.

Example

```css
h1 {
    font-size: 3.2rem;
    color: green;
}
```

In the example above, `h1` is the selector (to be specific, an element selector), followed by a declaration block, which has two declarations in it. 

Every CSS document, contains such collection of many CSS rules.

#### Declarations 

A single rule within the block of a rule set. eg ` font-size: 3.2rem;` you can have one or more declarations (a set of properties and values) within a rule set block.

Each declaration has a **property**, followed by a colon and a **value** followed by a semi-colon, which terminates the declaration. Example, `font-size` is the property and its value is set to `3.2rem`.

#### Properties

The way/s, in which you can style a given element. eg `font-size` is a property of a given element.

#### Property Value

This chooses one out of the many possible styles for a given property. eg `3.2rem`. 

**Note**:  not all pairs of properties and values are allowed, each property has a specific list of valid values defined for it.

Lets explore a visual representation of a CSS Ruleset

![CSS ruleset]()

#### At rules

At-rules are all different, but they have a basic structure in common. They start with an `@` code point followed by their name.

Consider the examples below

```css
@media print {
    body {
    	font-size: 12pt
    }
}

@media (min-width: 800px) {
    body {
        margin: 0 auto;
        width: 70%;
    }
}
```

The @media at-rule begins with a media type and a list of optional media queries. Its block contains entire rule sets, which are only applied when the @medias conditions are fulfilled.

- The first at-rule, only applies the nested style rule when printing, this will set the body font size to 12pt.
- The second at-rule, only applies the nested style rule when the page's width is at 800px.  

**Note:**

Some at-rules are simple statements, with their name followed by more CSS values to specify their behavior, and finally ended by a semicolon. 

Others are blocks; they can have CSS values following their name, but they end with a block `{ }`. Even the contents of these blocks are specific to the given at-rule: sometimes they contain a sequence of declarations, like a qualified rule; other times, they may contain additional blocks, or at-rules, or other structures altogether.

Examples are: `@import`, `@page`, `@supports ` etc. We will definitely discuss and use some of them in the projects.

**Note**: property names and at-rule names are always identifiers, which have to start with a letter or a hyphen followed by a letter, and then can contain letters, numbers, hyphens, or underscores.

## Applying CSS to HTML

Normally, there are three ways to apply CSS to HTML document(s). We will quickly review and see an example of each one.

### Inline CSS

Inline styles are CSS declaration(s) contained within a style attribute inside a html element.

Consider the following example

![](inline style)

In the above code, we have a `style` attribute, which has three declarations as a value for the attribute. The declarations (which consist of properties and values) will affect the `h1` element.

Can you imagine if you have to do this for every element you have to style in your HTML?

### Internal CSS

Internal/embedded stylesheet is when, you place your CSS code inside a `style` element within the `head` element.

Consider the following example 

![](internal style)

### External CSS

External CSS is when you have your CSS in a separate file with a `.css` extension. You connect to it by referencing it from a HTML page using the `link` element in the `head` element.

In this method, you are expected to have the two documents in their own separate files, meaning a html file and a css file. 

Consider the following example

![](external style)