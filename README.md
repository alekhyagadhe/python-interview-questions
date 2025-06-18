1. Difference between List and Tuple in Python?
Lists are mutable (you can change, add, delete elements), whereas tuples are immutable (cannot be changed once created).
Lists are defined with square brackets [], and tuples with parentheses ().
Tuples are generally faster and used when data shouldn't be changed.

<pre>
```python
my_list = [1, 2, 3]
my_list[0] = 10         # allowed

my_tuple = (1, 2, 3)
# my_tuple[0] = 10      # Error: Tuples cannot be changed
```

---

2. How do sets help in removing duplicates from a list?

A set is an unordered collection that doesn't allow duplicate elements.

So, if you convert a list to a set, all duplicate values are automatically removed.

```python
numbers = [1, 2, 2, 3, 4, 4, 5]
unique_numbers = list(set(numbers))
print(unique_numbers)  # Output: [1, 2, 3, 4, 5]


---

3. Why are dictionaries faster than lists for lookups?

Dictionaries use a technique called hashing to access values using keys, which makes lookup fast (almost constant time).

In contrast, lists search one item at a time, which is slower if the list is large.

```python
names = ['John', 'Mary', 'Tom']
print('Tom' in names)  #  but slower for large lists

data = {'John': 25, 'Mary': 30}
print(data['Mary'])    #  fast using key


---

4. How are Python strings immutable if they allow replace()?

Strings in Python cannot be changed after they are created (immutable).

Functions like .replace() or slicing create new strings without modifying the original.

```python
text = "hello"
new_text = text.replace("h", "y")
print(text)      # "hello" – original remains same
print(new_text)  # "yello" – new string created


---

5. How do you merge two dictionaries in Python (latest version)?

In Python 3.9 and above, you can use the | operator to merge dictionaries.

Earlier, you could use the update() method or dictionary unpacking.

```python
a = {'x': 1}
b = {'y': 2}
merged = a | b
print(merged)  # Output: {'x': 1, 'y': 2}


---

6. Explain dictionary comprehension with example?

Dictionary comprehension lets you create dictionaries in a short and clean way using loops.

Syntax: {key: value for item in iterable}

```python
Square of numbers from 1 to 3
squares = {x: x*x for x in range(1, 4)}
print(squares)  # Output: {1: 1, 2: 4, 3: 9}


---

7. What are nested dictionaries and how do you access inner values?

A nested dictionary has another dictionary inside it.

You can access the inner values by chaining the keys.

```python
student = {
    'name': 'Alice',
    'marks': {'math': 90, 'science': 85}
}

print(student['marks']['science'])  # Output: 85


---

8. How can you convert list of tuples into dictionary?

Use dict() to convert a list of key-value tuples into a dictionary.

Each tuple should have exactly 2 elements.

```python
pairs = [('a', 1), ('b', 2), ('c', 3)]
result = dict(pairs)
print(result)  # Output: {'a': 1, 'b': 2, 'c': 3}


---

9. How would you handle missing key in a dictionary?

If you try to access a missing key, Python raises a KeyError.

To avoid this, use .get() which returns a default value instead of an error.

```python
person = {'name': 'Ravi'}
print(person.get('age'))           # Output: None
print(person.get('age', 'N/A'))    # Output: N/A


---

10. Can we use a list as a key in a dictionary? Why or why not?

 No, because lists are mutable and unhashable.

But you can use a tuple, which is immutable and hashable.

```python
# Invalid: list as key
# my_dict = {[1, 2]: "value"}  #  Error

# Valid: tuple as key
my_dict = {(1, 2): "value"}     


---

11. What happens if you try to add a mutable object to a set?

Sets only allow immutable (hashable) objects.

If you try to add a list or dictionary, Python throws an error.

```python
# my_set = {[1, 2]}  #  Error: unhashable type: 'list'
my_set = {(1, 2)}    # Tuples are allowed               



