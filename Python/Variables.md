Variables are containers for storing data values.

## Creating Variables
Python has no command for declaring a variable.
if you write anything without string its a variable and you  need to assign value that. 

```python 
x = 5 # this value is intiger data type 
y = 10.5 # this value is float data type 
name = "My Name" # this value is string data type 

print(x)

#print data type with the `type()` function.
print(type(x)) #output: <class 'int'>
print(type(y)) #output: <class 'float'>
print(type(z)) #output: <class 'str'>
```

## Case-Sensitive
Variable names are case-sensitive.
```python 
a = 4  
A = "Sally"  
#A will not overwrite a

print(a) #output: 4
print(A) #output: Sally
```

## Variable Names Rules
A variable can have a short name (like x and y) or a more descriptive name (age, carname, total_volume). Rules for Python variables:

- A variable name must start with a letter or the underscore character
- A variable name cannot start with a number
- A variable name can only contain alpha-numeric characters and underscores (A-z, 0-9, and _ )
- Variable names are case-sensitive (age, Age and AGE are three different variables)
- A variable name cannot be any of the [Python keywords](https://www.w3schools.com/python/python_ref_keywords.asp).

## Many Values to Multiple Variables
```python
x, y, z = "Orange", "Banana", "Cherry"
```
**Note:** Make sure the number of variables matches the number of values, or else you will get an error.

## One Value to Multiple Variables
```python
x = y = z = "Orange"
```

## Unpack a Collection
```python
fruits = ["apple", "banana", "cherry"]  
x, y, z = fruits
```

### ভেরিয়েবল ডিক্লেয়ার করার সেরা পদ্ধতি

ভেরিয়েবল ঘোষণা করার সেরা পদ্ধতিগুলো মেনে চলা আপনার কোডকে আরো পাঠযোগ্য, রক্ষণাবেক্ষণযোগ্য এবং ত্রুটিমুক্ত করতে সহায়ক হবে। এখানে কিছু সেরা পদ্ধতি তুলে ধরা হলো:

#### ১. অর্থবোধক নাম ব্যবহার করা

ভেরিয়েবলের নাম এমন হওয়া উচিত যা তার অর্থ বা উদ্দেশ্য স্পষ্ট করে।
```js
# খারাপ উদাহরণ
x = ৫
y = ১০

# ভালো উদাহরণ
student_age = ৫
student_grade = ১০

```

#### ২. কেসিং (Casing) নিয়ম মেনে চলা

ভেরিয়েবলের নাম লেখার সময় সঠিক কেসিং নিয়ম মেনে চলা উচিত। সাধারণত, পাইথনে স্নেক কেস (snake_case) ব্যবহার করা হয়।
```js
# স্নেক কেস
first_name = "রাহিম"
last_name = "আহমেদ"

# ক্যামেল কেস (অন্য ভাষায় প্রচলিত)
firstName = "রাহিম"
lastName = "আহমেদ"

```

#### ৩. নামের দৈর্ঘ্য নির্ধারণ

ভেরিয়েবলের নাম খুব ছোট বা খুব বড় না করা। যথেষ্ট দৈর্ঘ্যের অর্থবোধক নাম ব্যবহার করা উচিত।
\
```js
# খারাপ উদাহরণ
a = ২৫
b = "ঢাকা"

# ভালো উদাহরণ
student_age = ২৫
student_city = "ঢাকা"

```

#### ৪. ম্যাজিক সংখ্যা এড়ানো

কোডে ম্যাজিক সংখ্যা (magic numbers) বা হঠাৎ আসা সংখ্যা এড়ানো উচিত। এর পরিবর্তে, তাদের অর্থবোধক ভেরিয়েবলে সংরক্ষণ করা উচিত।

```js
# খারাপ উদাহরণ
total_price = ১০০ * ১.১৫

# ভালো উদাহরণ
tax_rate = ১.১৫
price = ১০০
total_price = price * tax_rate

```

#### ৫. কনস্ট্যান্ট ভেরিয়েবল

যেসব ভেরিয়েবলের মান পরিবর্তন হবে না, তাদের সব বড় হাতের অক্ষরে লেখা উচিত এবং আন্ডারস্কোর দিয়ে আলাদা করা উচিত।

```js
# কনস্ট্যান্ট ভেরিয়েবল
MAX_SPEED = ১০০
PI = ৩.১৪১৫৯

```

#### ৬. ভেরিয়েবল স্কোপ

ভেরিয়েবল যথাসম্ভব লিমিটেড স্কোপে ঘোষণা করা উচিত, যাতে তারা অপ্রয়োজনীয়ভাবে বড় স্কোপে অ্যাক্সেসযোগ্য না হয়।

```js
# খারাপ উদাহরণ (গ্লোবাল স্কোপে ভেরিয়েবল)
total = ০

def calculate_total(price):
    global total
    total = price * ১.১৫

# ভালো উদাহরণ (লোকাল স্কোপে ভেরিয়েবল)
def calculate_total(price):
    total = price * ১.১৫
    return total

```

#### ৭. কোডের পাঠযোগ্যতা নিশ্চিত করা

ভেরিয়েবল ঘোষণার সময় ইনডেন্টেশন ও স্পেসিং সঠিকভাবে ব্যবহার করা।

```js
# খারাপ উদাহরণ
student_name="রাহিম"
student_age=২০

# ভালো উদাহরণ
student_name = "রাহিম"
student_age = ২০

```

#### ৮. একসাথে একাধিক ভেরিয়েবল ঘোষণা এড়ানো

এক লাইনে একাধিক ভেরিয়েবল ঘোষণা করা এড়িয়ে চলা উচিত, কারণ এটি কোডের পাঠযোগ্যতা হ্রাস করে।

```js
# খারাপ উদাহরণ
name, age, grade = "রাহিম", ২০, "দশম"

# ভালো উদাহরণ
name = "রাহিম"
age = ২০
grade = "দশম"

```

ভেরিয়েবল ঘোষণা করার সময় অর্থবোধক নাম ব্যবহার করা, সঠিক কেসিং নিয়ম মেনে চলা, ম্যাজিক সংখ্যা এড়ানো, কনস্ট্যান্ট ভেরিয়েবল ব্যবহার করা, এবং ইনডেন্টেশন ও স্পেসিং সঠিকভাবে ব্যবহার করা কোডের পাঠযোগ্যতা, রক্ষণাবেক্ষণযোগ্যতা এবং ত্রুটিমুক্ত করার জন্য অত্যন্ত গুরুত্বপূর্ণ। এই সেরা পদ্ধতিগুলো অনুসরণ করে আপনি আরও পরিষ্কার এবং কার্যকর কোড লিখতে পারবেন।