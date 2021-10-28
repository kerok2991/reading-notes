## Introductory HTML and JavaScript

Reading:

- Duckett HTML book: introduction and chapters 1, 8, 17, and 18.

- Ducket JS book: introduction and chapter 1.

### HTML/CSS Intro
This book covers HTML (handles the structure of a page) and CSS (handles the presentation and layout) which are the bare necessity of a webpage. A webpage is part of the internet, a large connected network of servers. The user accesses the specific page they want through a browser or screen reader, which uses a DNS server (like an address book) to look up the IP address (the network location of the website server) of the server they want to visit. The webserver sends back the HTML, CSS, and any other information needed to the browser, which then renders the page for the user to see.

### HTML/CSS Chapter 1: Structure (HTML)
HTML is a language used to structure websites, where behind the scenes is plain raw HTML that gets interepreted by a web browser and rendered into what the user sees. It consists of tags, some of which affect the intent of the content the tags surround. For example, in the raw HTML document, text can be surrounded by paragraph **tags** to suggest that the content between the tags is *paragraph* text, eg: `<p>text</p>`. The rendered page will show "text" formatted as paragraph text. This unit of an opening tag, a closing tag, and the content it surrounds is called an **element**. 

There's tags for many things, like headings, lists, links, images, and so on. Not all tags have a closing tag though. For example the image tag is an opening tag with an attribute, without a closing tag. An image tag looks like `<img src="[url]">`, where the `src="[url]"` is the **attribute**, consisting of a **name** (`src`) and a **value** (`"[url]"`). There's attributes for many tags, some of which have closing tags and some of which, like the image tag, don't.

A `<head>` tag and `<body>` tag are two main tags used within an HTML document. The contents between a pair of `<body>` tags is the entirety of the content on a rendered page. The contents between a pair of `<head>` tags are the aspects that are not shown on the rendered page. The only header tag mentioned within this chapter is `<title>` which sets the browsers tab/window title for the page. To be clear, it doesn't show a title within the page body itself.

### HTML/CSS Chapter 8: More HTML tags
This chapter introduces a few more tags.

`<!DOCTYPE [value]>` is used at the very start of the document to explain to the browser what the contents of the document is exactly. The value could be the specific version of HTML that is intended.

`<!-- [comment] -->` adds a comment.

`<div>` groups together the containing elements into a block. The compliment to a block (the item goes on a new line and uses the entire horizontal space available) is inline (the item goes within the same line).

`<span>` groups the containing elements into an inline section rather than block. Can be used to give an identifier/class to specific text.

`<iframe>` puts a website within the page. Similar to an image tag, except instead of an image, there's a website.

`<meta>` is placed into the `<header>` section, has no closing tag, and is used to convey information not visible on the page. Doesn't appear to be clear from the book how the information contained by these tags is used *exactly*, and I have a feeling things have changed since the book was written, so just remember to look up the details before using. Attributes are typically used in pairs, for example `name=["description"/"keywords"/"robots"] content="[values for description/keywords/robots]"` and `http-equiv=["author"/"pragma"/"expires"] content="[values for author/pragma/expiration]"`. There's some content set by the content attribute, and the kind of information of that content is described by the name/http-equiv attribute. This information is handled by whatever is reading meta tags; that thing might be looking for a name of "description" and handle the content according to what it does with descriptions.

`id="[value]"` gives an element an identifier to make that specific element uniquely identifiable. It is a global attributes meaning it can be placed within any element.

`class="[value]"` is similar to the identifier attribute, except the same value can be used on multiple elements.

### HTML/CSS Chapter 17: Layout (HTML)
Div tags with id and class attributes used to be used to group together items on the page. It seems the preference is to now instead use semantic tags that explain what the meaning of the grouping is: `<header>`, `<footer>` (can also be used for headers/footers of articles/sections), `<main>` (main page content), `<article>` (for standalone content, like an article), `<section>` (content with similar purpose, like contact info or a group of articles), `<hgroup>` (heading group), `<figure>` (like an image with caption), `<nav>` (main navigation), and `<aside>` (side content), and to only use `<div>` when no other suitable tag exists.

### HTML/CSS Chapter 18: Process and Design
The website is a product, and products are intended for a customer. The target audience (hopefully the end user) is that customer and the design of the website should be for that audience. It's important to keep in mind the goals of the audience, why they're visiting the website and what value they hope to gain from it. It's probably good to try to think about the website from their perspective, and in their shoes, what would I be looking for in an ideal website. The answer to that depends on many things, like who they are, what the purpose of the website is, how often they'll return to the site. In terms of content, too much irrelevant content can scare away customers; too little may not satisfy the goals of the customer and they'd look elsewhere for what they need. A swiss army knife of websites that appeals to the world might not be the most effective solution to communicate with the specific target audience.

The design of a website should be planned out. A site map is a diagram used to plan how the different pages link together. Group pages together when it makes sense and remember to organize the content for the target audience. Another aspect of planning is creating a wire frame, kind of a blue print sketch of what the page(s) would visually look like and how the content on the page would be organized. It's faster to iterate through wireframes than it is to draft/redraft a webpage.

Communication is imporant. Organization can improve the effeciency of that communication. Grouping together similar content is one aspect of organization. This grouping can be done visually. For example blocks of content with similar purpose can be grouped with spatial methods: group elements in close proximity, the group seperated from nearby unrelated content, or have a natural flow (continuance) between elements. Visual grouping can also depend on styles like color and size to differentiate the group and its relative importance to content not within the group. There should be some visual flow so when the user looks at the page, they are able to quickly skim the page and orient themselves rapidly to the main intent and where different groups of details are located. Consistency in styling between similar groups across pages or within a page can be used to convey meaning so that users can understand what the content type is without reading it.

### JS Intro
JavaScript in the context of this book is used to make websites interactive. It does this by accessing and modifying the HTML content when certain rules or events occur. The book gives four examples where JavaScript is used, and the most interesting one I think is replacing a section on a page when a link is clicked, rather than reloading the entire new page. I wonder how often navigation within a website is handled in this way rather than linking to an entirely new page. The other examples were about form validation, making a slideshow, and filtering what images are shown.

### Chapter 1a: Scripts
Scripts are a bunch of steps together which achieve a goal. A script is like a process, and process can be explained by a flow diagram. Similarly a script can be explained by a flow diagram. Not all parts of the diagram need to be executed if the conditions say so, and similary not all subcomponents of a script need to be executed. 

### Chapter 1b: Objects
Objects are things that have properties, methods, and events associated with them. A property is some value of the object, like its color, speed, temperature, etc. A method is a process that modifies its properties. An event is something that happens that triggers calling a method.

A website page is a document object. Within the page are HTML elements, each also an object called a node. When a webpage loads, the browser creates a tree model of the page consisting of these objects, then renders the page for the viewer to see. Modifications that javascript makes is to the document object model that the rendered page is build on, not the raw HTML itself.

### Chapter 1c: Objects in JavaScript
There's layers to a website: HTML handles the content, CSS handles the presentation, and JavaScript handles the behavior.

JavaScript objects: `object.method([parameters])` will access a method of an object, or `object.property` to access a property. The period is called a member operator and is how methods and properties of an object are accessed.

Insert `<script src="[path].js">` tags where the JavaScript file is supposed to run in the HTML page.

- [Back To Main](README.md)