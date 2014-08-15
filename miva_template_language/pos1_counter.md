# `POS1` Counter

Now that you have a little background on foreach loops with Miva Merchant's Template Language there is one more important concept that will give you a lot more control when working with foreach loops; it is called `POS1`. `POS1` is a counter within a foreach loop. It always starts a 1 and contains the current iteration of the foreach loop. `POS1` gets incremented each time the loops runs so it will always contain the current number of times the loop has been executed. You can also think of it as containing the current index of the array. For example, if we have eight products in our array, the first product it executes the code on, `POS1` will be 1, on the next it will be 2, and so on until it reaches 8.

For example, on the category page there is a foreach loop that looks like this:

```
<mvt:foreach iterator="product" array="category_listing:products">
...
</mvt:foreach>
```

This foreach loops though all the products assigned to whatever category you happen to be on. Now, say for example you wanted to give the 4th product a border. We can use `POS1` to help us test for the 4th iteration of the loop. Within the foreach loop you would add this code:

```
<mvt:if expr="POS1 EQ 4">
	//add border here
</mvt:if>
```

### Some Important Notes About `POS1`

* `POS1` can only be tested for in if statements. It cannot be output to the screen.
* `POS1` always starts with 1.
* If you nest foreach loops, every level you go down `POS1` becomes `POS2`, `POS3` etc.

**Example of nested foreach loops using `POS1`:**

```
<mvt:foreach iterator="product" array="category_listing:products">
	//POS1 contains the current iteration number of the category_listing:products array
    <mvt:foreach iterator="product" array="category_listing:products">
    	//you would use pos2 here because it is nested within another for each loop
	</mvt:foreach>
</mvt:foreach>
```

### More Examples

The most common use for `POS1` is on the category page when you are trying to create 2, 3 or 4 column layouts for products. A lot of times you will need to apply a change in margin to the first product in a row that the rest of the products do not need.

Take this layout for example, it has a margin on the left of each product, except the first.

Here the second, third and fourth products all have a border left. However the first product does not. Every first product in every new row will not have a border left. This means the 1st, 5th, 9th, etc products all need a different class to achieve this layout. This is easily done using `POS1` and the modulus (MOD) operator.

First a quick background on the `MOD`. It returns the remainder when you divide two numbers. So `6 MOD 3` will return 0 because 3 divides into 6 twice with a remainder of 0. However, `5 MOD 4` would return 1 because 4 divides into 5 once with a remainder of 1.

To make things a little bit more complicated, modulus will throw you a curveball when you are trying to divide a bigger number by a smaller number. I'll give you this example. If you are trying to divide something like 1 MOD 4, you will get a remainder of 1. The reason is that modulus only works with whole numbers, so 4 goes into 1 zero times, with a remainder of 1 (the original number).

We can use this to create the following If statement:

```
<mvt:if expr="(POS1 MOD 4) EQ 1">
	<div class="first-item">
		// This will be executed of every 4th product starting at 1: 1,5,9,13 etc.
	</div>
<mvt:else>
	// This code will be executed when the above condition is NOT met
</mvt:if>
```

That is how you'd get it to show on the first, fifth, ninth and so on elements of the array. Remember, it works on the first element because 4 goes into 1 zero times, with a remainder of 1.

If you wanted to do some special code for the 4th, 8th, 12th and so on elements, you could use some code like this:

```
<mvt:if expr="(POS1 MOD 4) EQ 0">
	<div class="last-item">
		// This will be executed of every 4th product starting at 4: 4,8,12,16 etc.
	</div>
<mvt:else>
	// This code will be executed when the above condition is NOT met
</mvt:if>
```

`POS1` is a powerful feature of SMT that will allow you to create dynamic layouts quickly and easily using just CSS.
