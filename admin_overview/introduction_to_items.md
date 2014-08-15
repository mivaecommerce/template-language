# Introduction to Items

Items can be one of the hardest concepts in Miva Merchant to grasp, however they are extremely important to how Miva Merchant Pages function.
An Item is a user interface component that provides specific functionality to a Page template.  All Pages have multiple items assigned to them. Some examples of commonly used items would be the nav bar, the category tree, and the head tag. Each of these are built in items that are assigned to almost all Pages of the store.

Items are the building blocks of Miva Merchant. Think of them as “includes” that can contain functions, HTML, and variables. For example, if you see the Global Header Item called on the page, all it is really doing is retrieving the content from that tab and printing it on the page.

The real power of Items comes from the ability for 3rd party module developers to create new items that extend Miva Merchant’s core functionality.  An item is just a reference to a Miva Merchant Component Module (See Miva’s API for more information on this). A Component Module is a compiled Miva Script file that follows Miva Merchant’s API. This allows developers to leverage the power of the Miva Script programming language to create almost any functionality imaginable all within a very flexible and highly secure framework.

![Illustration of Item Diagram](http://www.mivamerchant.com/images/dts-item-diagram.jpg)
