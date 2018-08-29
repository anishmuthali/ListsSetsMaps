# Maps

### Maps in Java

`Map` in Java __maps__ a key to a value. The following example is in JSON (JavaScript Object Notation) and provides a visual example of what maps look like:

```
{
  "key1": "value",
  "key2": ["values", "of", "an", "array"],
  "key3": {
    "sub_key1": "nested",
    "sub_key2": "example"
  }
}

```

You can instantiate a map object in Java as shown below. This is an example, and the `<String, Integer>` can be any two objects.

```
Map<String, Integer> foodPrices = new Map<String, Integer>();

```
In JSON format:
```
{

}
```
The map is empty, and you are ready to add values now.

### Methods
__put(Object key, Object value)__: This method is used to insert an entry in this map.

__putAll(Map map)__: This method is used to insert the specified map in this map.

__remove(Object key)__: This method is used to delete an entry for the specified key.

__get(Object key)__:This method is used to return the value for the specified key.

__containsKey(Object key)__: This method is used to search the specified key from this map.

__containsValue(Object value)__: This method is used to search the specified value from this map.

__keySet()__: This method is used to return the Set containing all the keys.

__entrySet()__: This method is used to return the Set containing all the keys and values.

__values()__: Returns Collection of values.

__isEmpty()__: Checks if map is empty.

__size()__: Returns size of map.

__clear()__: Removes all entries in the map.

__equals(Object o)__: Returns true if o is a map with the same entries.

### Example
You can add a key-value pair to maps like this:
```
foodPrices.put("apples", 5);
```
In JSON format:

```
{
  "apples": 5
}
```
You can also get the value that is __mapped__ to a key.
```
int value = foodPrices.get("apples");
System.out.printf("The price of apples is: $%d\n", value);
```
The output of this block of code would be `The price of apples is $5`.

Updating the the values mapped to a certain key is also possible.
```
foodPrices.put("apples", 6);
```
This would overwrite the value mapped to the key `"apples"`.
Running the code above again:
```
int value = foodPrices.get("apples");
System.out.printf("The price of apples is: $%d\n", value);
```
The output this time would be `The price of apples is $6`.

It is also possible to remove key-value pairs from a map.
```
foodPrices.remove("apples");
```
In JSON format:
```
{

}
```
Now, your map is empty again.

### HashMaps
Using a `HashMap` in Java is very similar to using a generic Map in Java. The main difference is instantiation:
```
HashMap<String, Integer> foodPrices = new HashMap<String, Integer>();
```
Depending on your use-case, you may choose between using a `Map` and a `HashMap`. You would likely use a `Map` when you are creating a parent class, and children classes would need flexibility between a regular `HashMap` and a `TreeMap`. 

### TreeMaps
In essence, a `TreeMap` is a `Map` that keeps its keys sorted by whatever `Comparator` the object uses by default (ex: `int` would be sorted by value, `char` would be sorted by ascii value, `String` would be sorted using `compareTo`, etc.)

# Practice
http://usaco.org/index.php?page=viewproblem2&cpid=667

