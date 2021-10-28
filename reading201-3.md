HTML Lists, CSS Boxes, JS Control Flow
Chapter 3: Lists
This one is simple to summarize: theres ordered lists (<ol>) and unordered lists (<ul>), each containing list items (<li>). Similar deal with definition lists (<dl>) except instead of list items it has definition terms (<dt>) paired with a definition (<dd>). Useful for definitions. All of these tags have closing tags. And, they can be nested by plopping a new ul, ol, or dl list where you want the sublist to be.

Chapter 13: Boxes
An HTML page consists of many containers (boxes). Useful for page layouts since the size of each container can be set with css. The dimensions of the box is the distance of the content and does not include borders/margins/padding in that dimension (but it can be changed away from that default, or client-dimensions can be used instead (todo: check)). Margin is any extra space outside of the border. Padding is any extra space inside the border for any content that is contained within it. The size of the container can be set with pixels, em's for sizes relative to the font size, or percents. Percents are relative to the parent container's dimensions. Contents of a box can be hidden with the visibility (hidden or visible) property, while the container itself will remain with the same dimensions. On the other hand using display property set to none removes the box and its contents entirely. For lists its useful to switch the default block styling to inline using the display property; useful for horizontal navigation bars.

For borders, margins, padding that take 4 fields of dimenions, the order starts at the top and goes clockwise. Borders can be images using the border-image property. The edges of the image border are the edge segments of an input image segmented into 9 sections, either repeated or stretched (or repeated with a little scaling to fit). Shadows and rounded corners can be added to boxes, probably best to look up how to use it each time.

Centering a container on a page, set the margins on either side to auto and the spacing for the margin will split evenly. Will need to also set the dimension of the box to do so it knows how much space the margins are working within. Minimum and maximum dimensions can also be specified.

JS Chapter 2: Basic JS (Arrays)
An array is a set of values. var arrayName = ['element1', 'element2', ..., 'elementn']. (literal) or var arrayName = new Array('element1', 'element2', ..., 'elementn') (constructor) to make a new array. Can grab an element using arrayName[elementNumber] and use arrayName.length to get the number of elements in the array. arrayName[elementNumber] = value to replace. ElementNumber is also called the index and the count starts at 0. arrayName.push(value) to add to an element to an array, arrayName.concat(arrayName2) to concatenate arrayName with arrayName2. There's a sort method, reverse, indexOf, shift (remove first elemnent), unshift (add to beginning), filter, fill, copyWithin, etc.

JS Chapter 4: Decisions and Loops (Continued)
A switch statement can also be used for flow control. Break statements are commonly added to the end of each case to break out from the switch statement. Switch statements fall through if there is no break statement, meaning, somewhat unintuitively, that everything between the matching case and the next break is run, even if there are additional cases in between.

switch (expression) { 
    case [value]: 
        [statements]
    case [value2]: 
        [statements]
    default:
        [statements]
}
Truthy and falsy values are possible because javascript is a loosely typed language and will try its best to match up types because of type coercion. Similar to how a string of '1' is coerced into being a number 1, the similar weirdness can happen with booleans. Just note that strings of 'true' and 'false' are both truthy; my understanding is the truthness is the presence of a nonzero value. Things like the number zero, an empty string, an empty variable would all be falsy. Where as a string of '0' is a nonzero value before its coerce to a number 0. This only applies to non-strict operators.

Short circuit is a trick that depends on left to right processing and truthyness. The evaluation of the logical operation uses the truthy/falsy boolean values, and as soon as the logical operation is guaranteed to be a truthy boolean, it returns the actual value of that truthy boolean, not true/false. Another way to explain, the logical operation uses the true/false equivalent like normal, but the result is the first uncoerced value that caused the expression to evaluate as true.

For loops take the form of for ([1. declare a loop variable and its starting value], [2. condition to check before entering the next loop, usually utilizing the declared loop variable], [3. modification to the loop variable after each loop completes]) {loop statements}.

While loops are: while ([condition to check before the loop runs]) {loop statements}.

Do while loops are: do {loop statements} while ([condition to check after the loop runs]).

Continue (skip to the next loop iteration) and break (escape current loop or to the keyword) exist.

Loops will hold up the remaining lines of code or HTML from running until they complete.

- [Back To Main](README.md)