                                Python Interview Questions & Answers
                                 
**1)Difference between List and Tuple in Python?**
  
  Lists are mutable (you can change, add, delete elements), whereas tuples are immutable (cannot be changed once created).
  Lists are defined with square brackets [], and tuples with parentheses ().
  Tuples are generally faster and used when data shouldn't be changed.


 ```python
 my_list = [1, 2, 3]
 my_list[0] = 10         # allowed

 my_tuple = (1, 2, 3)
 # my_tuple[0] = 10      # Error: Tuples cannot be changed
```

**2)How do sets help remove duplicates from a list?**

  Sets automatically remove duplicate items.Converting a list to a set removes duplicates.

  ```python
  numbers = [1, 2, 2, 3, 3, 3]
  unique_numbers = list(set(numbers))
  print(unique_numbers)  # Output: [1, 2, 3]
  ```

**3)Why are dictionaries faster than lists for lookups?**

  Lists perform linear search (O(n)).
  Dictionaries use hash tables (O(1) average time).

  ```python
  # List lookup
 names = ['Alice', 'Bob', 'Charlie']
 print('Bob' in names)  # O(n)

 # Dictionary lookup
 students = {'Alice': 25, 'Bob': 30}
 print('Bob' in students)  # O(1)
 ```

**4)How are strings immutable if replace() works?**

  Strings are immutable. Methods like replace() return a new string.The original string remains unchanged.

   ```python
   s = "cat"
   new_s = s.replace("c", "b")
   print(s)      # Output: "cat"
   print(new_s)  # Output: "bat"
```

**5)How to merge two dictionaries in Python 3.9+**

  Use the | operator or dict.update() to merge dictionaries.

  ```python
   a = {'x': 1}
   b = {'y': 2}
   merged = a | b
   print(merged)  # Output: {'x': 1, 'y': 2}
   ```
**6)Explain dictionary comprehension with an example**

   A concise way to create a dictionary using loops in a single line.

   ```python
    squares = {n: n*n for n in range(4)}
    print(squares)  # Output: {0: 0, 1: 1, 2: 4, 3: 9}
   ```

**7)What are nested dictionaries and how do you access inner values?**

   A dictionary inside another dictionary is known as nested dictionaries
   we can acces inner values using multiple keys.

   ```python
    data = {
    'emp1': {'name': 'John', 'age': 30},
    'emp2': {'name': 'Sara', 'age': 25}
    }
    print(data['emp1']['name'])  # Output: John
   ```
**8)How can you convert the list of tuples in to a dictionary?**

   dict() can convert a list of key-value pairs (tuples) into a dictionary.

   ```python
   pairs = [('a', 1), ('b', 2)]
   result = dict(pairs)
   print(result)  # Output: {'a': 1, 'b': 2}
   ```

**9)How would you handle missing Key in a dictionary ?**

   Use .get() to return a default value if the key doesn't exist.

   ```python
    d = {'name': 'Alice'}
    print(d.get('age', 'Not Available'))  # Output: Not Available
  ```

**10)Can we use a list as a key in a dictionary? why and why not?**

   No. Lists are mutable and unhashable, so they can't be used as keys.

   ```python
    # This will raise TypeError
    # d = {[1, 2]: 'value'}  # TypeError: unhashable type: 'list'
  ```

**11)What happens if you try add a mutable object to set?**

   Sets require elements to be hashable.Mutable objects like lists can't be added.

   ```python
    # TypeError: unhashable type: 'list'
    # my_set = set()
    # my_set.add([1, 2, 3])
   ```

**12)write a code to find common elements in two lists using set operations?**

   ```python
    a = [1, 2, 3, 4]
    b = [3, 4, 5, 6]
    common = list(set(a) & set(b))
    print(common)  # Output: [3, 4]
   ```
    
**13)what is the difference between is and ==for string ? what is the syntax?**
 
  == compares values: It checks whether the contents of two variables are the same.
   is compares identities: It checks whether two variables refer to the exact same object in memory.
   
    **Syntax**
    ```python
     a == b # checks value equality
     a is b # checks object identity (memory location)
      ```
      ```python
      # Case 1: Comparing string literals
     a = "hello"
     b = "hello"
     print(a == b)  # True – values are the same
     print(a is b)  # True – both point to same memory (due to interning)

     # Case 2: Comparing dynamically created strings
    x = "".join(["hel", "lo"])
    y = "hello"
    print(x == y)  # True – contents are the same
    print(x is y)  # False – different memory locations
    ```

**14)How does sciling works in tuple and string? what are the syntax?**

  Syntax: [start:stop:step]
  Slicing works the same for strings and tuples.

  ```python
    t = (0, 1, 2, 3, 4)
    s = "Python"
    print(t[1:4])  # Output: (1, 2, 3)
    print(s[0:3])  # Output: "Pyt
  ```

**15)How can you reserve a string or list in python using sciling?**

   Use slicing with step -1 to reverse.

   ```python
     s = "hello"
     l = [1, 2, 3]
     print(s[::-1])  # Output: "olleh"
     print(l[::-1])  # Output: [3, 2, 1]
   ```

   
    
    

   
   
    
   


   



   





  
  

  
   

