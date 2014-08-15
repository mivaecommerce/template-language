# Global & Local Variables

In the last article we reviewed what an entity was, and how to use Merchant Merchant’s &mvt Template Language (Also called Store Morph Technology - SMT) to write values to the screen.

### Examples
* `&mvt:product:formatted_price;` - prints: $9.99
* `&mvte:store:name;` - prints: Pet Emporium Super Store

These entities are parsed through the Miva Engine (Empresa) and are replaced with their actual value before they are sent to the browser.

If you are familiar with any other programming language like PHP, then you can think of an entity as a variable. They are essentially the same thing. However, when you call an entity using ‘&mvt’ the only thing you can do is print the value to the screen. You can’t assign them or perform operations on them. To do those types of things you will need to access the variable using its scope identifier.

## Scope Identifiers – Local and Global Variables

Each Miva Merchant Entity has a scope. It is either a local variable which is accessed using ‘l.settings:” or a global variable accessed using “g.”

## Local Variables

* `l.settings:product:formatted_price`
* `l.settings:store:name`
* `l.settings:category:name`
* `l.settings:product:thumbnail`

The structure of a local variable starts with l.settings: followed by the item being referenced product: followed by the specific variable you are accessing formatted_price

Unlike printing an entity to the screen using &mvt:, when you reference a entity using the scope identifiers, there is no semicolon at the end.

##  Global Variables

* `g.Screen`
* `g.Store_Code`
* `g.Product_Code`

The structure of a global variable is always g. than the variable that you are accessing, Screen. Unlike local variables, there is no item reference in the middle because it is a global variable.

The big question that this brings up is when to use a local variables `l.settings:` and when to use global variables `g.`. Luckily, this is pretty straight- forward. A variable is either one or the other. It will never be both. You can easily tell which to use by looking at how it is called in the page using `&mvt:`.

If it contains an item reference in the middle like: `&mvt:product:name;` you access it as  a local variable like this: `l.settings:product:name`

If it looks like this: `&mvt:global:Store_Code;` you access it as a global variable like this: `g.Store_Code`.

## In Summary

From a developers perspective, there really is no difference between local and global variables. You just need to know which one you are working with so that you can access it the correct way. The variable scope really only applies to the Miva Complier and Miva Engine. If you were working with the Miva Merchant API and writing modules in Miva Script then the variable scope would make a difference. However, from a web developer’s standpoint global and local variables are pretty much the same.

So lets review: `&mvt:product:name;` is used to write the entity value to the screen. In this case it would print the product name. Since this references the product item, we know it is a local variable and we can perform operations (equals, not equals, greater than, etc.) on it using `l.settings:product:name`.
