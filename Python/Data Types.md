In programming, data type is an important concept.

## Built-in Data Types
Python has the following data types built-in by default, in these categories:

|                 |                                    |
| --------------- | ---------------------------------- |
| Text Type:      | `str`                              |
| Numeric Types:  | `int`, `float`, `complex`          |
| Sequence Types: | `list`, `tuple`, `range`           |
| Mapping Type:   | `dict`                             |
| Set Types:      | `set`, `frozenset`                 |
| Boolean Type:   | `bool`                             |
| Binary Types:   | `bytes`, `bytearray`, `memoryview` |
| None Type:      | `NoneType`                         |

## Numeric `Complex` Type 
```python
4 + 7j # 4 is Real Number, And 7j is Imaginary Number
```

## কমপ্লেক্স সংখ্যার ব্যবহার
- **ইলেকট্রিক সার্কিট বিশ্লেষণঃ** 
   একটি সিরিজ RLC সার্কিটে নিম্নলিখিত উপাদানগুলো আছে:
   RLC সার্কিট হচ্ছে একটি সাধারণ ইলেকট্রিক সার্কিট যেখানে রেজিস্টর (R), ইন্ডাক্টর (L), এবং ক্যাপাসিটর (C) সিরিজ বা প্যারালেলভাবে যুক্ত থাকে।
   রেজিস্টর (R) = 100 Ω, ইন্ডাক্টর (L) = 0.05 H, ক্যাপাসিটর (C) = 0.0001 F, অ্যাঙ্গুলার ফ্রিকোয়েন্সি (ω) = 1000 rad/s

- সিগন্যাল প্রসেসিং: ধরুন দুটি 50 Hz এবং 120 Hz ফ্রিকোয়েন্সির দুটি সাইন ওয়েভের মিশ্রণ দিয়ে একটি সিগন্যাল তৈরি করতে পারি।
- কোয়ান্টাম মেকানিক্সঃ কোয়ান্টাম মেকানিক্সে একটি কণার অবস্থা বর্ণনা করার জন্য যে ওয়েভ ফাংশন ব্যবহার করা হয় তা সাধারণত কমপ্লেক্স সংখ্যার সাহায্যে প্রকাশ করা হয়।
- নিয়ন্ত্রণ তত্ত্ব: যেমন সিস্টেম স্ট্যাবিলিটি এবং ফ্রিকোয়েন্সি রেসপন্স বিশ্লেষণের জন্য 
- ইমেজ প্রসেসিং

## Python Sequence Data Types

Python-এ কিছু সাধারণ Sequence Data Types হলো:

1. **Lists**
2. **Tuples**
3. **Strings**
4. **Range**

প্রত্যেকটি Sequence Data Type-এর বৈশিষ্ট্য এবং উদাহরণ নিয়ে আলোচনা করা হলো:

### 1. Lists

Lists হলো মিউটেবল (পরিবর্তনযোগ্য) সিকোয়েন্স ডাটা টাইপ, যা বিভিন্ন ধরণের ডাটা আইটেম ধারণ করতে পারে।

```python
# List creation
fruits = ["apple", "banana", "cherry"]

# Accessing elements
print(fruits[0])  # Output: apple

# Modifying elements
fruits[1] = "blueberry"
print(fruits)  # Output: ['apple', 'blueberry', 'cherry']

# Adding elements
fruits.append("date")
print(fruits)  # Output: ['apple', 'blueberry', 'cherry', 'date']

# Removing elements
fruits.remove("cherry")
print(fruits)  # Output: ['apple', 'blueberry', 'date']

```

### 2. Tuples
Tuples হলো ইমিউটেবল (অপরিবর্তনীয়) সিকোয়েন্স ডাটা টাইপ, যা সাধারণত বিভিন্ন ধরণের ডাটা সংরক্ষণে ব্যবহৃত হয়।

```python
# Tuple creation
coordinates = (10, 20)

# Accessing elements
print(coordinates[0])  # Output: 10

# Tuples are immutable, so elements cannot be modified
# coordinates[0] = 15  # This will raise a TypeError

# Creating a new tuple
new_coordinates = coordinates + (30,)
print(new_coordinates)  # Output: (10, 20, 30)

```

### 3. Strings
Strings হলো ইমিউটেবল সিকোয়েন্স ডাটা টাইপ, যা অক্ষরের সিকোয়েন্স সংরক্ষণে ব্যবহৃত হয়।

```python
# String creation
greeting = "Hello, World!"

# Accessing elements
print(greeting[0])  # Output: H

# Strings are immutable, so elements cannot be modified
# greeting[0] = 'h'  # This will raise a TypeError

# String slicing
print(greeting[7:12])  # Output: World

```

### 4. Range
Range হলো ইমিউটেবল সিকোয়েন্স ডাটা টাইপ, যা সাধারণত লুপে ব্যবহার করা হয়।

```python
# Range creation
numbers = range(1, 10)

# Converting range to list to see elements
print(list(numbers))  # Output: [1, 2, 3, 4, 5, 6, 7, 8, 9]

# Using range in a loop
for num in range(5):
    print(num)
# Output:
# 0
# 1
# 2
# 3
# 4

```


## Python Mapping Type: Dictionary
Python-এ Mapping Type এর মধ্যে সবচেয়ে সাধারণ হলো Dictionary।  এটি কী-ভ্যালু (key-value) পেয়ার সংরক্ষণ করে এবং দ্রুত ডাটা রিট্রিভ করার জন্য ব্যবহৃত হয়।

#### Dictionary

**Dictionary** হলো পরিবর্তনযোগ্য (mutable) ডাটা টাইপ, যা কী-ভ্যালু পেয়ার সংরক্ষণ করে। এটি একটি `{}` ব্রেসের মধ্যে ডিফাইন করা হয় এবং কী-ভ্যালু পেয়ারগুলো `:` দিয়ে পৃথক করা হয়।

```python
# Dictionary creation
student = {
    "name": "Alice",
    "age": 23,
    "major": "Computer Science"
}

# Accessing values
print(student["name"])  # Output: Alice
print(student["age"])   # Output: 23

# Modifying values
student["age"] = 24
print(student)  # Output: {'name': 'Alice', 'age': 24, 'major': 'Computer Science'}

# Adding new key-value pairs
student["university"] = "MIT"
print(student)  # Output: {'name': 'Alice', 'age': 24, 'major': 'Computer Science', 'university': 'MIT'}

# Removing key-value pairs
del student["major"]
print(student)  # Output: {'name': 'Alice', 'age': 24, 'university': 'MIT'}

# Iterating through dictionary
for key, value in student.items():
    print(f"{key}: {value}")
# Output:
# name: Alice
# age: 24
# university: MIT

# Checking if a key exists
if "name" in student:
    print("Name is present in the dictionary")
# Output: Name is present in the dictionary

```

### Dictionary-এর সুবিধা:
- **দ্রুত ডাটা রিট্রিভ:** কী-এর সাহায্যে দ্রুত ভ্যালু রিট্রিভ করা যায়।
- **পরিবর্তনযোগ্য:** ডিকশনারিতে কী-ভ্যালু পেয়ার সহজেই যোগ, পরিবর্তন, বা মুছে ফেলা যায়।
- **বিন্যাস:** বিভিন্ন ধরণের ডাটা টাইপের কী-ভ্যালু পেয়ার সংরক্ষণ করতে পারে।
- **ইটারেশন:** সহজেই ডিকশনারির মধ্যে ইটারেট করে কী এবং ভ্যালু পেতে পারেন।

### Dictionary Methods:
- **`.items()`**: সমস্ত কী-ভ্যালু পেয়ার রিটার্ন করে।
- **`.keys()`**: সমস্ত কী রিটার্ন করে।
- **`.values()`**: সমস্ত ভ্যালু রিটার্ন করে।
- **`.get(key, default)`**: নির্দিষ্ট কী-এর ভ্যালু রিটার্ন করে; যদি কী উপস্থিত না থাকে তবে ডিফল্ট ভ্যালু রিটার্ন করে।
- **`.pop(key, default)`**: নির্দিষ্ট কী-এর ভ্যালু রিটার্ন এবং মুছে ফেলে; যদি কী উপস্থিত না থাকে তবে ডিফল্ট ভ্যালু রিটার্ন করে।

```python 
# Dictionary methods examples
print(student.items())   # Output: dict_items([('name', 'Alice'), ('age', 24), ('university', 'MIT')])
print(student.keys())    # Output: dict_keys(['name', 'age', 'university'])
print(student.values())  # Output: dict_values(['Alice', 24, 'MIT'])
print(student.get("name"))  # Output: Alice
print(student.get("major", "Not Found"))  # Output: Not Found

student.pop("age")
print(student)  # Output: {'name': 'Alice', 'university': 'MIT'}

```

Python-এর Dictionary হলো একটি শক্তিশালী ডাটা টাইপ যা কী-ভ্যালু পেয়ার সংরক্ষণ করে। এটি ডাটা ম্যানেজমেন্ট এবং দ্রুত রিট্রিভ করার জন্য খুবই কার্যকর। Dictionary-এর ফ্লেক্সিবিলিটি এবং পরিবর্তনযোগ্যতা এটিকে Python প্রোগ্রামারদের মধ্যে জনপ্রিয় করে তুলেছে।

## Python Set Types
Python-এ Set হলো একটি ডাটা টাইপ যা ইউনিক আইটেমের একটি অনিয়ন্ত্রিত সংগ্রহ সংরক্ষণ করে। সেটের মধ্যে থাকা সকল আইটেম ইউনিক এবং অপরিবর্তনীয় (immutable) হয়, তবে সেট নিজে পরিবর্তনযোগ্য (mutable) হয়। সেটের মধ্যে কোনো ডুপ্লিকেট আইটেম থাকে না।

### Set
Set তৈরি করার জন্য `{}` ব্রেস অথবা `set()` ফাংশন ব্যবহার করা হয়।

```python
# Set creation
fruits = {"apple", "banana", "cherry"}
print(fruits)  # Output: {'banana', 'apple', 'cherry'}

# Adding elements to a set
fruits.add("date")
print(fruits)  # Output: {'banana', 'apple', 'cherry', 'date'}

# Removing elements from a set
fruits.remove("banana")
print(fruits)  # Output: {'apple', 'cherry', 'date'}

# Set operations
more_fruits = {"apple", "blueberry", "cherry"}
print(fruits.union(more_fruits))         # Output: {'blueberry', 'apple', 'cherry', 'date'}
print(fruits.intersection(more_fruits))  # Output: {'apple', 'cherry'}
print(fruits.difference(more_fruits))    # Output: {'date'}
```

### Frozen Set
Frozen Set হলো একটি অপরিবর্তনযোগ্য (immutable) সেট। একবার Frozen Set তৈরি করা হলে সেটির কোন আইটেম পরিবর্তন করা যায় না।

```python
# Frozen set creation
frozen_fruits = frozenset(["apple", "banana", "cherry"])
print(frozen_fruits)  # Output: frozenset({'banana', 'apple', 'cherry'})

# Frozen sets are immutable
# frozen_fruits.add("date")  # This will raise an AttributeError

```

### Set Methods
- **`.add(element)`**: সেটে একটি নতুন আইটেম যোগ করে।
- **`.remove(element)`**: সেট থেকে একটি আইটেম সরিয়ে দেয়; আইটেম না থাকলে `KeyError` ওঠায়।
- **`.discard(element)`**: সেট থেকে একটি আইটেম সরিয়ে দেয়; আইটেম না থাকলে কিছুই করে না।
- **`.union(other_set)`**: দুটি সেটের ইউনিয়ন রিটার্ন করে।
- **`.intersection(other_set)`**: দুটি সেটের ইন্টারসেকশন রিটার্ন করে।
- **`.difference(other_set)`**: দুটি সেটের ডিফারেন্স রিটার্ন করে।
- **`.issubset(other_set)`**: সেটের সব আইটেম যদি অন্য সেটের মধ্যে থাকে তবে `True` রিটার্ন করে।
- **`.issuperset(other_set)`**: সেটের সব আইটেম যদি অন্য সেটে থাকে তবে `True` রিটার্ন করে।

```python 
# Set methods examples
fruits = {"apple", "banana", "cherry"}

# Add an element
fruits.add("date")
print(fruits)  # Output: {'banana', 'apple', 'cherry', 'date'}

# Remove an element
fruits.remove("banana")
print(fruits)  # Output: {'apple', 'cherry', 'date'}

# Discard an element
fruits.discard("apple")
print(fruits)  # Output: {'cherry', 'date'}

# Union of sets
more_fruits = {"banana", "date", "fig"}
print(fruits.union(more_fruits))  # Output: {'banana', 'apple', 'cherry', 'date', 'fig'}

# Intersection of sets
print(fruits.intersection(more_fruits))  # Output: {'date'}

# Difference of sets
print(fruits.difference(more_fruits))  # Output: {'cherry'}

```

