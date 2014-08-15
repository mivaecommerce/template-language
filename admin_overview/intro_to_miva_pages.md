# Intro to Miva Pages

The core of customizing a Miva Merchant store starts with Pages. Pages are individual templates that define the layout of each webpage in a Miva Merchant Store. A Page is a mix of standard HTML, Items, Entities, and Miva Merchant conditional statements (foreach loops, if-else statements, etc.). You can also put things like CSS or JavaScript on a Miva Merchant Page. As of this writing, a default store has 53 page templates (PR8 Update 10) however new pages are constantly added as Miva adds new features. This includes everything from the SFNT page (Storefront) to the ORHL (Order History Lookup). It is very important to understand what each of the pages controls and when it is called within Miva Merchant.

See the [Page Reference Guide](http://www.mivamerchant.com/tutorials/articles/dts-102-article-page-reference-guide) to view the complete list of standard Miva Pages with a description of when each is used.

In Miva Merchant, the words Screen and Page are used interchangeably. If you are looking at a standard Miva Merchant URL you will always know what Page Template you are on by looking at the Screen=SFNT parameter in the URL. This tells you the Page Template that was rendered was the SFNT (Storefront) Page.
You also have the ability to create new Pages that contain any elements you want. This allows you to move all your content into Miva Merchant so that every page shares the same global elements. Miva Merchant not only acts as your shopping cart, but also as your Content Management System for your entire store. Common Pages to move into Miva Merchant are the about us page, contact us, policy pages, testimonials and FAQ’s.

## Pseudo Pages

These are Pages in Miva Merchant that don’t have Page Templates associated with them in the Miva Merchant Admin. An example of this would be the OINF page. It is used to initiate the checkout process however it does not have its own page template. Instead, the OINF page has logic built in that will direct you to either the OCST Page (Customer Information Page) if you are logged in or the ORDL Page (Order Login Page) if you are not logged in. This functionality is all built into the Pseudo Page, OINF.

Luckily there are only 4 Pseudo Pages in Miva: OINF, ACNT, AFAE and OUSL. A detailed description of each can be found in the Page Reference Guide.
