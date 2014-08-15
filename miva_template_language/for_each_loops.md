## `<mvt:foreach>` Loops

![](http://www.mivamerchant.com/images/foreach-loop.jpg)

Before we talk about `<mvt:foreach>` loops, we need to understand one more concept, *the array*. Think of an array as a group of objects. Sometimes the objects can be products, or sometimes they can be charges on a particular order. Let's think about a category page, every time it loads, the server is going to retrieve a group of products that are assigned to that category, and put them into our array. Once this group of objects are returned, naturally we'd want to access the data (in this case, products) and write them on the page. This is where a foreach loop comes in handy.

What a foreach loop does is take in data from an array, then execute some code for each item in the array.

The code for an foreach loop looks like this:

```
<mvt:foreach iterator="product" array="category_listing:products">
	Code to execute for each product in the array
</mvt:foreach>
```

A standard foreach loop will loop as many times as there are items in the array. If there are 10 products, it will execute 10 times. On pages with pagination (category, search, product list, etc.), there is a field in the admin where you can set the limit on each page. If you have 10 products and limit the loop to 8 per page, a button will appear at the bottom that says "Previous." On that page, you will be able to see the other two products.

In the above sample code you'll notice there is a parameter of "iterator" and one for "array". These change depending on what type of data you are looping through.

The above loop isn't very helpful, normally we'd be writing entities to the page, add to cart buttons, etc. to make this page more useful to the user. A real site might have a foreach loop that looks like this:

```
<mvt:foreach iterator="product" array="category_listing:products">
	<div class="product-item">
		<div class="product-details">
			<div class="product-name"><a href="&mvte:product:link;">&mvt:product:name;</a></div>
			<div class="product-code">Code: <span class="bold">&mvt:product:code;</span></div>
			<div class="product-price">Price: <span class="bold">&mvt:product:formatted_price;</span></div>
			<mvt:if expr="l.settings:product:inv_active">
				&mvt:product:inv_long;<br />
			</mvt:if>
			<div class="product-quantity">Quantity in Basket:
				<mvt:if expr="l.settings:product:quantity EQ 0">
					<span class="italic">none</span>
				<mvt:else>
					<span class="italic">&mvt:product:quantity;</span>
				</mvt:if>
			</div>
		</div>
	</div>
</mvt:foreach>
```

The code above retrieves the array for products in the category, then for each product, it will run the code inside of it. So if we have 10 products on our page, the code will run 10 times.

You can get even more advanced control by combining foreach loops with nested if statements.
