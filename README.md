1. Difference between List and Tuple

List is mutable (can change), Tuple is immutable (can’t change).

Lists use [], Tuples use ().

Lists are slower but more flexible.


Example:

my_list = [1, 2, 3]
my_list[0] = 100  # OK

my_tuple = (1, 2, 3)
my_tuple[0] = 100  # ❌ Error (can't modify)


---

2. How do Sets remove duplicates from a List?

Sets in Python store only unique values.

When you convert a list to a set, it removes duplicates automatically.


Example:

nums = [1, 2, 2, 3, 1]
unique_nums = list(set(nums))  # [1, 2, 3]


---

3. Why are Dictionaries faster than Lists for lookups?

List searches each item one-by-one (O(n) time).

Dictionary uses hashing, so lookup is O(1) (very fast).


Example:

d = {"name": "Alex"}
print("name" in d)  # Fast lookup

names = ["Alex", "Bob"]
print("Alex" in names)  # Slower, searches one by one


---

4. Are Python Strings Immutable? Then how does replace() work?

Yes, strings are immutable – you can’t change the original string.

Functions like replace() return a new string.


Example:

text = "hello"
new_text = text.replace("h", "y")  # "yello"


---

5. How to merge two dictionaries in Python 3.9+?

Use the | (pipe) operator to merge.


Example:

a = {"x": 1}
b = {"y": 2}
c = a | b  # {'x': 1, 'y': 2}


---

6. What is Dictionary Comprehension?

It's a short way to create dictionaries.


Example:

squares = {x: x*x for x in range(3)}  # {0: 0, 1: 1, 2: 4}


---

7. What are Nested Dictionaries?

A dictionary inside another dictionary.

Access using multiple keys.


Example:

student = {
  "name": "Amit",
  "marks": {"math": 90, "science": 85}
}
print(student["marks"]["math"])  # 90


---

8. How to convert list of tuples to dictionary?

Use dict() on list of tuples (key-value pairs).


Example:

data = [("a", 1), ("b", 2)]
print(dict(data))  # {'a': 1, 'b': 2}


---

9. How to handle missing keys in a dictionary?

Use get() to avoid errors.

You can also give a default value.


Example:

d = {"a": 1}
print(d.get("b", 0))  # 0 (default)


---

10. Can we use List as Dictionary Key?

❌ No, because lists are mutable and dictionary keys must be immutable.

✅ Use tuples instead.


Example:

d = {(1, 2): "ok"}  # ✅
# d = {[1, 2]: "error"} ❌


---

11. What happens if you try to add mutable object to set?

❌ You get an error because sets need hashable (immutable) items.

✅ Use tuples.


Example:

s = set()
s.add((1, 2))  # ✅
# s.add([1, 2]) ❌ Error


---

12. Find common elements using Set Operations

Use & operator or .intersection().


Example:

a = [1, 2, 3]
b = [2, 3, 4]
print(set(a) & set(b))  # {2, 3}


---

13. Difference between is and == in Python?

== checks value.

is checks memory/location.


Example:

a = "hello"
b = "hello"
print(a == b)  # True
print(a is b)  # True (sometimes, depends on Python)


---

14. How does slicing work in strings and tuples?

Syntax: [start:stop:step]

Works with strings, lists, tuples.


Example:

text = "python"
print(text[1:4])  # "yth"


---

15. How to reverse a string or list using slicing?

Use slicing with step = -1.


Example:

print("hello"[::-1])  # "olleh"
print([1, 2, 3][::-1])  # [3, 2, 1]
