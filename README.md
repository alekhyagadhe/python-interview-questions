                            # Python Interview Questions & Answers 
1)Difference between List and Tuple in Python?

  Lists are mutable (you can change, add, delete elements), whereas tuples are immutable (cannot be changed once created).
  Lists are defined with square brackets [], and tuples with parentheses ().
  Tuples are generally faster and used when data shouldn't be changed.


 ```python
 my_list = [1, 2, 3]
 my_list[0] = 10         # allowed

 my_tuple = (1, 2, 3)
 # my_tuple[0] = 10      # Error: Tuples cannot be changed
```

