### Inactivating sold clothing items

Expected time required: 10 min

In the reading we introduced the online clothing store you're starting to sell some of your old clothes. To simplify
your table, you're changing the attribute `'status'` to just keep track of whether an item is active. The value for 
`status` is `'active'` if the item hasn't been sold yet and `'inactive'` if the item has been sold. 

The `ClothingItems` table looks like this:

* `id` : partition key—unique `String` identifier for each clothing item
* `status` : sort key—`String` with a value of either 'active' or 'inactive'
* `clothingType` : `String` that specifies the type of the clothing item
* `color` : `String` that specifies the color of the clothing item
* `price` : `Double` that specifies the price of the clothing item

Add code to the `getActiveClothingItem()` method in the `ClothingDAO` class to implement functionality that loads an item
*only* if `status` = 'active'. The `Clothing` class is already written and annotated for you and the `ClothingDAO` class
also includes a `saveTask()` method.

The unit tests in `ClothingDAOTest` are set-up with a mock database so that you can test your methods offline. The
`main()` method is set-up in `ClothingApp` so that you can connect to the real ClothingItems table and test your methods
that way.

HINTS:
* [The `getActiveClothingItem()` method only accepts a partition key even though the table uses a partition and sort key!](hints/hint-01.md)
