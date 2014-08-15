# Entities & Encoding

Entities are variables that can be used throughout a Miva Merchant Page template to display a value on the screen.  Depending on which items you have assigned to a page, you have access to different entities that you can use to write a value to the screen.

## Entity Examples

All entities start with the ampersand ( & ) and end with a semicolon ( ; )

* `&mvt:store:name;` - Prints the store name
* `&mvte:category:name;` - Prints the current category name
* `&mvt:product:formatted_price;` - Prints the formatted price of the product

The first part, &mvt, tells us this is a Miva Merchant page template entity. The middle part, like store or category tells us what part of the store interface is being referenced.(Which item is being referenced).
The last part, like name, or formatted_price, gives the specific piece of information to use from the item being referenced.

An entity can contain different types of data, from integers to text strings to image urls.

When outputting an Entity to the screen you have different encoding methods to choose from. **How do I know which one I should use?**

* `&mvt` - Prints the value directly to the screen with no encoding.
* `&mvte` - Variables that begin with &mvte are “entity encoded.” All characters are encoded so they are not interpreted by the browser. This is used for all form input values and anywhere user input is written back to the page. Entity encoding variables prevents against cross side scripting and other harmful attacks.
* `&mvta` - Variables that begin with &mvta are “attribute encoded.” This means that any characters they contain will be converted to the correct format for use in a link. This is used for all links and will convert spaces and other characters to link friendly characters.

Still confused on which encoding Output to use? [See this thread in the forums](http://extranet.mivamerchant.com/forums/showthread.php?106612-mvt-vs-mvte-vs-mvta-clarification-needed&p=389046#post389046) for an example.
