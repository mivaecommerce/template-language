# `<mvt:assign>`

`<mvt:assign>` Executes the expression contained within `value` and saves that value to the variable defined in the `name` attribute.

*Requires 5.18 Engine or Higher*

## Psuedo Syntax

```
<mvt:assign name="variable" value="expression, string, or number" />
```

## Basic Example

```
<mvt:assign name="g.sum" value="1 + 2" />
The sum is: &mvt:global:sum;
```
*Output:* `The sum is: 3`

## Attributes

* `name`
    * This can be a local or global variable as defined by l. or g.
        * If no prefix (l. or g.) is given it defaults to be a global variable.
*  `value`
    *  The value can either be an expression a string, a number or a combination of all three.

## Note

* This function can create both global and local variables
* Global variables are always available to output in the page template. (&mvt:global:test)
* Local variables can only be output if they are a part of the l.settings structure (l.settings:test)
* Any string (text) needs to be wrapped in single quotes or else it will be treated as a variable
* Numbers do not need single quotes

---

# Examples

## Using Strings

Strings are always defined by single quotes

```
<mvt:assign name="l.settings:foo" value="'bar'" />
&mvt:foo;
```
*Output:* `bar`

## Using Numbers

Numbers do not need to be enclosed by single quotes

```
<mvt:assign name="l.settings:myvariable" value="(10+10) * 5" />
&mvt:myvariable;
```
*Output:* `100`

## Using Expressions

Any value contained in the value attribute will automatically be treated as an expression. This means text will be treated as variables and any function available with the Miva Empresa engine (link) will be evaluated.

```
<mvt:assign name="l.myvariable" value="substring(l.myvariable, 2, len(l.myvariable) " />
```

Finds the substring of `l.myvariable` starting at the second character until the end of the string and saves that value back into `l.myvariable`

## Using Concatenation

The `$` is the concatenation operator in the Miva Template Language can everyting is evaluated, it can be used in the value attribute within the mvassign tag.

```
<mvt:assign name="g.myvariable" value=" 'The length of this string is: ' $ len('hello world') " />
&mvt:global:myvariable;
```

*Output:* `The length of this string is: 11`

## Outputing Values to the Page

If you want to display a value to the screen it needs to a global variable or part of the l.settings structure.

```
<mvt:assign name="g.myvariable" value="10" />
&mvt:global:myvariable;
```
*Output:* `10`

```
<mvt:assign name="l.settings:myvariable" value=" 'hello world' " />
&mvt:myvariable;
```
*Output:* `hello world`


```
<mvt:assign name="l.myvariable" value=" 'this is a test' " />
&mvt:myvariable;
```
*Output:* This will NOT print anything to the page since it is not part of the l.settings structure
