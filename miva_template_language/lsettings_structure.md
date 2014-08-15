#  `l.settings` Structure

Each Miva Merchant Entity has a scope. It is either a local variable which is accessed using ‘l.settings:” or a global variable accessed using “g.”

## Local Variables

* `l.settings:product:formatted_price`
* `l.settings:store:name`
* `l.settings:category:name`
* `l.settings:product:thumbnail`

The structure of a local variable starts with l.settings: followed by the item being referenced product: followed by the specific variable you are accessing formatted_price

Unlike printing an entity to the screen using &mvt:, when you reference a entity using the scope identifiers, there is no semicolon at the end.
