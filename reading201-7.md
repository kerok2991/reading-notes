## HTML Tables, JS Constructor Functions

### [Domain Modeling and Constructor Functions](https://github.com/codefellows/domain_modeling#domain-modeling)

This talks about making constructor functions using function expressions:

```js
var constructorName = function(parameters) {
    [...]
}
var objectName = new constructorName(parameters);
```

The book has constructor notation of the same(?) thing:

```js
constructorName(parameters) {
    [...];
}
var objectName = new constructorName(parameters)
```

The github link also talks about prototype functions, which can be added to a constructor function. This is the preferred way to add functions to constructors; note that this goes outside of the constructor. There is not a way to modify/create this from within the constructor.

```js
constructorName.prototype.functionName = function(parameters2) {
    [...];
}
var objectName = new constructorName(parameters);
objectName.functionName(parameters2);
```

It mentions the benefit of using the prototype is it saves resources, because all the new object instances made with the constructor can use the same prototype, rather than creating a new function for each object instance. New properties inside the constructor are initialized with this (ie: "this" object's property value is...).

The entire point of the link was to discuss domain modeling, and how object oriented programming is used for that purpose. There's some guidelines for how to set up the domain model:

If there are multiple objects that are similar/the same, use a constructor. Instead of one large function/method, break it down into pieces. Storing the new instance of an object allows that instance to be later used. Properties in an object can be accessed using the this keyword.

### HTML Chapter 6: Tables

This chapter talks about tables. Basically, thead/tbody/tfoot are semantic tags are are just helpful for labeling or referencing purposes. Tr (table row) and td (table data) are what create the cells. Colspan/rowspan attributes are used to merge cells. Th element is to signify a heading row and by default makes the text bold; it's otherwise the same as a td element. Seeing the scope attribute to col or row will signify to screen readers whether the header label is for the row or column.

```html
<table>
    <thead>
        <tr>
            <th scope='col'>heading row, 1st column</th>
            <th scope='col'>heading row, 2nd column</th>
        </tr>
    </thead>

    <tbody>
        <tr>
            <td>2nd row, 1st column</td>
            <td>2nd row, 2nd column</td>
        </tr>
        <tr>
            <td colspan='2'>3rd row, 1st and 2nd column</td>
        </tr>
    </tbody>

    <tfoot>
        <tr>
            <td>footer row, 1st column</td>
            <td>footer row, 2nd column</td>
        </tr>
    </tfoot>
</table>
```

### JS Chapter 3 Continued: Constructors

See first section of notes above on comparison of how constructors are made in the book vs on that github page. In either case, the constructor is a template for creating new instances of an object. An example is if the constructor makes hotels, the new objects would be a new hotel at x location with y rooms. Page 116-117 is a really good summary/comparison of different ways data can be stored. Don't follow their examples of creating functions, even though it works. The reason is each time a new object is created, it also creates a new function; whereas using a prototype function (the preferred way) outside of the constructor, it only creates one function for all the objects. It's more resource efficient. It seems when properties are added to an object (or not added), the order that the property is shown is object itself, inherits from the constructor prototype, which inherets from the object prototype. So say the constructor doesn't define a property, but the Object prototype has that property, that object's property can still be used. I think, but am not sure, that if an object is created using a constructor that has a prototype function, ie a method, when that method is called from the object, it's calling the prototype method instead; and that the object can be given a new function with the same name, and the priority is that that new function will be used over the prototype... so two methods with the same name exist, and the more narrowly scoped one is used. I think, but am Not sure.