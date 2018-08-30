# Lists
### Lists Definition
- Stores objects of any type
- Allows null and duplicate elements
- They have an index unlike sets and are ordered
- Foundation for `ArrayLists` and `LinkedLists`

### Linked Lists
- List that is comprised of seperate objects as elements
- Each object is comprised of the data and the reference to the next object
- Last object references to null

### Lists Declaration
With Generic type parameter:
```
List<Object> listAnything = new ArrayList<Object>();
List<String> listWords = new ArrayList<String>();
List<Integer> listNumbers = new ArrayList<Integer>();
List<String> linkedWords = new LinkedList<String>();
```
Can do without
```
List<Integer> listNumbers = new ArrayList<>();
List<String> linkedWords = new LinkedList<>();
```
Also recommended to specify size if you can
```
List<Integer> listNumbers = new ArrayList<>(1000);
```
Also can construct lists from an existing collection
```
List<Integer> listNumberOne;  // existing collection
List<Integer> listNumberTwo = new ArrayList<>(listNumberOne);
```
### Operations
- Adding
  - Must be of same type or subtype declared
  - `.add(Object)`
    - Adds at end of list
  - `.add(index, Object)`
    - Adds at index
  - `.addAll(index, Object)`
    - If a list is used as an object, adds the entire list to the index or if no index is selected adds to end of the list
- Retrieving
  - `.get(index)`
    - Returns element of list at that index
  - `.getFirst()` and `.getLast()`
    - For linked lists returns first or last elements
- Updating
  - `.set(index, Object)`
    - Updates value for element at index
- Removing
  - `.clear()`
    - Removes all elements in a list
  - `.remove(index)` and `.remove(Object)`
    - Removes element at index or first instance of object
    - Notes
      - Does not replace with null but rather shifts all indices after it by one left
      - `.remove()` returns true if it is executed properly
- Searching
  - `.contains(Object)`
    - Returns true if object is contained anywhere in list
  - `.indexOf(Object)`
    - Returns index of first instance of object
  - `.lastIndex(Object)`
    - Returns index of last instance of object
- Sorting
  - `Collections.sort(list)`
    - Static method that sorts elements in natural ascending order but does not work with newly defined types
- Copying
  - `Collections.copyList(dest, src)`
    - Copies elements of list from source to destination. Destination list must be large enough to contain source list
- Shuffling
  - `Collections.shuffle(list)`
    - Scrambles elements in list
- Reversing
  - `Collections.reverse(list)`
    - Reverses order of elements in list
- Extracting
  - `.subList(from, to)`
    - Allows view from "from" index to "to" index. Changes in actual list will reflect on sublist
    
# Practice
  Transfer all elements of the ArrayList A to the LinkedList L
  <br><br><br><br><br><br><br><br><br><br><br>
  ```
  size = A.size();
  for (int counter = 0; counter < size; counter++)
  {
    L.add(A.getFirst);
    A.remove(0);
  }
  ```
   <br><br><br>
  What is the order of elements after executing this code
  ```
  LinkedList<Integer> l = new LinkedList<>();
  l.add(5);
  l.push(0);
	l.add(8);
	l.push(7);
  ```
  <br><br><br><br><br><br><br><br><br><br><br>
  [7, 0, 5, 8]
  <br><br><br>
  Convert the ArrayList into a HashSet
  ```
  ArrayList<Integer> a = new ArrayList<>();
  HashSet<Integer> h = new HashSet<>()
  a.add(4);
  a.add(4);
  a.add(3);
  a.add(2);
  a.add(3);
  a.add(19);
  ```
  <br><br><br><br><br><br><br><br><br><br><br>
  ```
  h.addAll(a);
  ```
  <br><br><br>
  Remove all duplicate entries in an ArrayList (order does not need to be maintained)
  <br><br><br><br><br><br><br><br><br><br><br>
  ```
  h.addAll(a);
  a.clear();
  a.addAll(h);
  ```
  
  
