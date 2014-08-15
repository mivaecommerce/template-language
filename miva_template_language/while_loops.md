# `<mvt:while>` Loops

This is used to iterate through an array, similar to for each

**Sample Usage:**

```
<mvt:assign name="l.my_value" value="10" />
<mvt:assign name="l.settings:counter" value="0" />
<mvt:while expr="l.settings:counter LE l.my_value">
    The value of counter is: &mvt:counter; <br>
    <mvt:assign name="l.settings:counter" value="l.settings:counter + 1" />
</mvt:while>
```

**Output**
```
The value of counter is: 0
The value of counter is: 1
The value of counter is: 2
The value of counter is: 3
The value of counter is: 4
The value of counter is: 5
The value of counter is: 6
The value of counter is: 7
The value of counter is: 8
The value of counter is: 9
The value of counter is: 10
```
