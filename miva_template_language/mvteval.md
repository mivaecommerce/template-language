# `<mvt:eval>`

`<mvt:eval>` Executes the expression contained within `expr` attribute and outputs the expression's value directly to the page. It opperates just like `<mvt:assign` exept that instead of saving the value/expression to a variable, it will output it directly to the page.

*Requires 5.18 Engine or Higher*

## Psuedo Syntax

```
<mvt:eval expr="expression, string or number" />
```

## Basic Example

```
The sum is: <mvt:eval expr="1 + 2" />

```
*Output:* `The sum is: 3`

## Attributes

*  `expr`
    *  This can either be an expression a string, a number, or a combination of all three.

---

# Examples

## Using Strings

Strings are always defined by single quotes

```
<mvt:eval expr="'bar'" />
```
*Output:* `bar`

## Using Numbers

Numbers do not need to be enclosed by single quotes

```
<mvt:eval expr="(10+10) * 5" />
```
*Output:* `100`

## Using Expressions

Any value contained in the value attribute will automatically be treated as an expression. This means text will be treated as variables and any function available with the Miva Empresa engine (link) will be evaluated.

```
<mvt:eval expr="substring(l.myvariable, 2, len(l.myvariable) " />
```

Finds the substring of `l.myvariable` starting at the second character until the end of the string and outputs that value to the page.

## Using Concatenation

The `$` is the concatenation operator in the Miva Template Language can everyting is evaluated, it can be used in the value attribute within the mvassign tag.

```
<mvt:eval expr=" 'The length of this string is: ' $ len('hello world') " />
```

*Output:* `The length of this string is: 11`
