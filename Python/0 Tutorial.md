#### Installation 
##### Test Python 
> python --version 

#### Run python in terminal 
> python or python3

#### Print a data 
> print("Hello World")

#### Exit from terminal 
> exit() 

#### Run file in terminal
> python filename.py

---

## Comments 
#### Single Line Comment 
> use `#`

#### Multi Line Comment 
> use `'''`

--- 
## Variables 
- create variable 
- assign value 
- print variable 
- short discuss about data type 
-  print variable data type using `type()` method 
- variable rule  
	-  must start with a letter or the underscore character
	- cannot start with a number
	- can only contain alpha-numeric characters and underscores (A-z, 0-9, and _ )
	- case-sensitive `age` and `Age` not same 
- write meaning full name
- don't write more describe
- some writing case 
	- Camel Case `myVariableName` [each word capital except first]
	-  Pascal Case `MyVariableName` [each world capital]
	- Snack Case `my_variable_name` [each world sperate by _ (underscore)]
- many values to multiple values 
	- `x, y, z = "Orange", "Banana", "Cherry"`
	- Make sure the number of variables matches the number of values, or else you will get an error.
-  One Value to Multiple Variables `x = y = z = "Orange"`

---
## Data Types 
- String - `str()`
	- Numeric Type 
		- Integer `int()`
		- Float `float()`
		- complex `complex()`
	- Sequence Type 
		- `list` type or `[]`
			- The `remove()` method removes the specified item.
			- The `pop()` method removes the specified index. when empty it's remove from last one 
			- The `del` keyword also removes the specified index `del thislist[0]`
			- The `clear()` method empties the list.
			- `sort()` method will sort the list alphanumerically
			- To sort descending, use the keyword argument `reverse = True`
			- The `reverse()` method reverses the current sorting order of the elements.
			- Make a copy of a list with the `copy()` method
			- One of the easiest ways are by using the `+` operator to join Or you can use the `extend()` method
			
		- `tupple()` type or `()` 
			- order 
			- Unchangeable
			- Allow Duplicates
			- get Tuple Length use the `len()` function
			- Create one item tuple, remember the comma
			- Access Tuple Items by the the index number, The first item has index 0.
			- Negative indexing means start from the end.
			- Access by range of Indexes `thistuple[2:5]` Return the third, fourth, and fifth item. 
			-  beginning to range ``thistuple[:5]`` except 5th index 
			- Range of Negative Indexes `thistuple[-4:-1]`  -4 (included) to index -1 (excluded)
			- Check if Item Exists use the `in` keyword  `"apple" in thistuple`
			- Add Items using `append()` method
			- Remove Items using `remove()` method
			- The `del` keyword can delete the tuple completely
			- Unpacking a Tuple
			- Using Asterisk`*`
			- Multiply Tuples `mytuple = fruits * 2`
			- The `count()` method returns the number of times a specified value appears in the tuple.  `thistuple.count(5)`
			- The `index()` method finds the first occurrence of the specified value. `thistuple.index(8)`
			
		- `range` type 
	- Mapping Type 
		- `dict` dictionary type `{}`   key:pair 
			- Ordered in `3.7` or Unordered- `before 3.7` 
			- Changeable
			- Duplicates Key Not Allowed
			- Dictionary Length using the `len()` function
			- It is also possible to use the `dict() constructor` to make a dictionary. `name = "John",`
			- `thisdict["model"]` or `thisdict.get("model")`
			- The `keys()` method will return a list of all the keys
			-  Change Values
				- `thisdict["year"] = 2018` 
				- `thisdict.update({"year": 2020})`
			- Add a color item to the dictionary by using the `update()` method:
			- The `pop("key_name")` method removes the item with the specified key name or `del thisdict["model"]`
			- The `del` keyword can also delete the dictionary completely
			- The `clear()` method empties the dictionary:
			- Make a copy of a dictionary with the `copy()` method `or mydict = dict(thisdict)`
			- `values()` Returns a list of all the values in the dictionary|
	- Set Types 
		- `set()` type `{1,2,4}`
			- Sets are used to store multiple items in a single variable.
			- unchangeable
			- Duplicate values will be ignored:
			- `True` and `1` is considered the same value:
			- `False` and `0` are considered the same value
			- Access Items using the `in` keyword.
			- add new items `.add()` [you cannot change its items, but you can add new items]
			- To add items from another set into the current set, use the `update()` method.
			- Remove Item use the `remove()`, or the `discard()` method.
			- Remove a random item by using the `pop()` method
			- The `clear()` method empties the set:
			- `del` keyword will delete the set completely `del set_name` 
				-  **return new sets**
					- The `union()` and `update()` methods joins all items from both sets. except `update()`
					- The `intersection()` method keeps ONLY the duplicates.
					- The `difference()` method keeps the items from the first set that are not in the other set(s).
					- The `symmetric_difference()` method keeps all items EXCEPT the duplicates.
		- `frozenset()` type 
			- unchangeable 
			- `frozenset(x)` return frozen set 
	- Boolean 
		- `true`, `false`
		- all empty data type `false`
		- all numbers `true` except `0`, this means `false` 

