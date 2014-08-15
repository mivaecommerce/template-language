# Conditional Statements

Displaying Static Content is an essential part of creating websites. But what happens when we want to do more? What if we want to present specific data to a customer based on a choice they made or action they took? To do this, we need to be able to use conditional statements to let the browser know what content to display.

## `if` Statement

![If-statement Logic Diagram](http://www.mivamerchant.com/images/if-statement.jpg)

The most commonly used conditional statement is the if-statement. When the browser executes the statement, it checks to see if a condition is met. If this condition is met, it executes the code that it contains, if not, the code within the statement is skipped.

The code for an if statement looks like this:

```
<mvt:if expr="condition">
	Code to execute if condition is true
</mvt:if>
```

Conditional statements like this help us to serve more specific content to the user based on past actions or choices they have made. For example, if a user is on a specific product, we might want to show a banner with a discount code for checkout.

Before I move on, I want to talk about the "condition" part of the above if statement. For basic comparisons, there are three parts of a condition: the variable, a comparison operator, and a value.

In the previous article, we learned what entities and variables are and how to output them on a page. In a conditional statement, we can access variables like g.Screen and l.settings:product:code, compare their value to another value, then run conditional code if the statement is true.

A basic comparison looks like this:

```
<mvt:if expr="g.Screen EQ 'SFNT'">
	<p>Welcome to our awesome site!</p>
</mvt:if>
```

What we've done above is check to see if the value of `g.Screen` is equal to `SFNT`, if it is, then we write a welcoming paragraph tag for the user to see. You'll notice that instead of the word "EQUAL" or using an equal sign "=", I used just two letters `EQ`. You will want to remember to always do it this way, or else your statements will fail to execute.

The comparison operator `EQ` is just one of many in the Miva Merchant's templating language. There are many other ways to compare strings, numbers, and variables using other comparison operators, but you'll quickly realize there are a select few that always come into play. Take a quick look at the full list of comparison operators below.

## Comparison Operators

These operators are used to compare two numbers or two text strings.

| Operator | Example | Explanation |
| -- | -- | -- |
| `EQ` | `g.Screen EQ 'SFNT'` | If the global Screen variable is equal to `SFNT`, this returns `true` |
| `NE` | `g.Screen NE 'SFNT'` | If the global Screen variable is NOT equal to `SFNT`, this returns `true` |
| `GT` | `l.settings:product:price GT 15` | If the product's price variable is GREATER than 15, this returns `true` |
| `LT` | `l.settings:product:price LT 15` | If the product's price variable is LESS than 15, this returns `true` |
| `GE` | `l.settings:product:price GE 15` | If the product's price variable is GREATER than or EQUAL to 15, this returns `true` |
| `LE` | `l.settings:product:price LE 15` | If the product's price variable is LESS than or EQUAL to 15, this returns `true` |

Now that we have a quick overview of the comparison operators, lets dive into some more complicated conditional statements.

## `else` Statement

![](http://www.mivamerchant.com/images/if-else-statement.jpg)

We've got the hang of `if` statements now. We check a condition, and if it's true, we execute some code. That works, and it's very handy, but what if we want to run some code if the condition is false? That's where the if-else statement comes in handy, it looks exactly like if statement, but before the statement closes, we can add `<mvt:else>`, this gives us the option to run some different code if the first if statement is NOT true.

The code for an if-else statement looks like this:

```
<mvt:if expr="g.Screen EQ 'SFNT'">
	<p>Welcome to our awesome site!</p>
<mvt:else>
	<p>Be sure to check out our sale on all <a href="path-to-shirts">men's shirts</a>!</p>
</mvt:if>
```

The above code is the exact same as our original if statement, except now we have added some code to execute if the original condition is false. If we are on the Storefront page, we will see "Welcome to our awesome site!", but if we are on ANY other page besides SFNT, we will see a nice promotion for our sale on men's shirts.

## `elseif` Statement

The `<mvt:elseif>` statement can accomplish the same goal as writing two separate if statements, but why do that when we can simply combine it into one section? Using the elseif statement is simple, you open an if statement, check if a condition is true, then rather than exiting the if statement, we can check another condition with elseif.

The code for an elseif statement looks like this:

```
<mvt:if expr="g.Screen EQ 'SFNT'">
	<p>Welcome to our awesome site!</p>
<mvt:elseif expr="g.Screen EQ 'PROD'">
	<p>Spend over $50 and get FREE shipping!</p>
</mvt:if>
```

If you look at the code above, you'll notice that we are checking for the same condition as our original if statement, is the current Screen the SFNT. Immediately following that statement, rather than close the if statement, we put an elseif right after it. This time, we check if the Screen is PROD, if it is, we display a message about free shipping. If neither of those conditions are met, we exit the if statement and don't run any code at all. You can chain as many elseif together as your little heart desires.
