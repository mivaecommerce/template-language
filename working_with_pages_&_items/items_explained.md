# Items Explained

Items can be one of the hardest concepts in Miva Merchant to grasp, however they are extremely important to how Miva Merchant Pages function.
An Item is a user interface component that provides specific functionality to a Page template.  All Pages have multiple items assigned to them. Some examples of commonly used items would be the nav bar, the category tree, and the head tag. Each of these are built in items that are assigned to almost all Pages of the store.

Items are the building blocks of Miva Merchant. Think of them as “includes” that can contain functions, HTML, and variables. For example, if you see the Global Header Item called on the page, all it is really doing is retrieving the content from that tab and printing it on the page.

There can be global items such as the nav bar, cat tree and head tag or there can be page specific items such as the Page header/footer. Once an item is assigned to a page you then call in the item through the item tag.

Item Tags can have 3 forms:

* Self closing Item with no parameter.
    `<mvt:item name="html_profile" />`
* Self closing Item with parameter.
    `<mvt:item name="head" param="css_list" />`
* Item with opening and closing tags:
    `<mvt:item name="body"></mvt:item>`

When an item is assigned to a page, a lot of times a new tab will show up that will allow you to access the content of that item. If a tab has an asterisk next to it that means it is a global item and any changes you make the template will affect all Pages of the site that use that item.

Sometimes an item can be assigned to a page and no tab will show up. This does not mean that the item is not working correctly; it just means that the item does not have a tab or template you can access. Instead, the item may be assigned to give you access to specific variables on that page. An example of this would be the store item. When assigned to a page there is no new tab that shows up. Instead, it gives you access to global variables called Entities that allow us to print data like the Store Name. **Example:** `<title>Welcome to &mvt:store:name;</title>`

There is an Items tab for each page in Miva Merchant which will show you exactly which items are assigned to that page, and also which ones aren’t assigned.

One pitfall that new developers run into frequently is forgetting to assign non-default items to pages when they want to access them. After spending a while debugging, they will find out that all they had to do was assign them item!

The real power of Items comes from the ability for 3rd party module developers to create new items that extend Miva Merchant’s core functionality.  An item is just a reference to a Miva Merchant Component Module (See Miva’s API for more information on this). A Component Module is a compiled Miva Script file that follows Miva Merchant’s API. This allows developers to leverage the power of the Miva Script programming language to create almost any functionality imaginable all within a very flexible and highly secure framework.

![Illustration of Item Diagram](http://www.mivamerchant.com/images/dts-item-diagram.jpg)
