# Sets
## Definition
- A set is an abstract data type that can store unique values, without any particular order
- Does not allow duplicate entries
- No index number
- Difference between sets and lists
  - Packaged, unindexed: set
  - Packaged, indexed: list (array)

## Sets in Java
- Java Set is a part of java.util package and extends java.util.Collection interface. It does not allow the use of duplicate elements and at max can accommodate only one null element.
- The set interface is an unordered collection of objects in which duplicate values cannot be stored.
- The Java Set does not provide control over the position of insertion or deletion of elements.
- Basically, Set is implemented by HashSet, LinkedHashSet or TreeSet (sorted representation).
- Set has various methods to add, remove clear, size, etc to enhance the usage of this interface

```java
HashSet<String> set = new HashSet<String>();
 
        // Use add() method to add elements into the Set
        set.add("Welcome");
        set.add("to");
        set.add("Capstone:");
        set.add("Data");
        set.add("Structure");
        set.add("Geeks");
        set.remove("Geeks");

        // Displaying the HashSet
System.out.println("HashSet:"+set+set.isEmpty());

```
