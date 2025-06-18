                                  
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
  

  
   

