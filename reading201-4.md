## HTML Links, CSS Layout, JS Functions

### HTML Chapter 4: Links

This chapter talks about links, the `<a href="[path]">link</a>` kind of links. Path is typically relative to current location. If no folder is specified, it'll usually open the index.html if it exists. Okay to specify file names too. Can link to other elements on the same page by using `#[name]`, if that element is named by its idenfifier attribute (`id="[name]"`). Can also link to open up default email application using `mailto:[email]` for the path. Can open a page in a new window using a `targt="_blank"` attribute.

### HTML Chapter 15: Layout

Positioning of an element (`position:[method]`) can be static (normal flow), relative (offset away from where it would've been in the normal flow), absolute (relative to parent element). These can be used with top, bottom, left, right properties, or fixed (relative to browser window). Overlapping containers is possible. There are layers, and the layer order is set with z-index. Float property will push the element in the direction specified (can still float in the perpendicular direction if it will get the element further in the specified direction), bounded by the parent container. Clear property uses the specified direction to clear sibling elements out of the way in that direction. 

It mentions grids can be useful for planning layout and that the page can adjust with the window size or be fixed, and there's advantages/disadvantages to each because not all devices display with the same size, resolution, or aspect ratio. CSS frameworks are help pieces of css, like a template, to help design pages on a grid system. 960gs is one example framework. Google would probably be handy to find some of those. `@import` can be used to add extra files, like fonts or other style sheets. If multiple style sheets are used, the last one takes priority.

### JS Chapter 3: Functions, methods, objects (pages 86-99)

This chapter introduces functions, which are recipes to run blocks of code. They can be defined like `function [functionName]([input1],[input2],...,[inputn]) {[statements]}`, and anytime that recipe needs to be used, call it using `[functionName]([input1],[input2],...,[inputn])`. Just note that when calling a function it's not giving the variables/inputs to the function, it's just giving the values of the variables and dumping them into the variable names used when the function was defined. Book alludes to this by pointing out the subtle difference between the terms argument and parameter. Parameter is the variables used within the function. Arguments are the values passed into the function. Functions can return values, using `return [value];` at the end of the function. Use an array to return multiple values out. Anonymous functions are nameless function expressions that take the form of `function([inputs]) {statements}`. Can immediately invoke the function by doing this: `(function([inputs]) {statements}())`. Not mentioned in this reading but there's also arrow functions: `(input => {statments that use input})`.


### Pair programming

It's good. One person drives, the other person guides. Practicing it teaches all four areas of communication (hearing, speaking, listening, and writing). It's probably more efficient in the long run to use. It forces focus on the task with collaboration.  Teaching is a good learning method, and learning from alternative viewpoints is also thing, so it's good for learning. Builds social skills, confidence, interview skills, and prepares for real world work situations.

- [Back To Main](README.md)