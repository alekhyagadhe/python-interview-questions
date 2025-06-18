Python Interview Questions & Answers

1. Difference between List and Tuple in Python?

List is mutable (changeable), uses square brackets [].

Tuple is immutable (unchangeable), uses parentheses ().

```python

my_list = [1, 2, 3]
my_list[0] = 100  #  Allowed

my_tuple = (1, 2, 3)
my_tuple[0] = 100  #  TypeError: 'tuple' object does not support item assignment





