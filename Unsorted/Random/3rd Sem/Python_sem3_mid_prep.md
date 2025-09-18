![](/ZettleKasten/Unsorted/Attachment/Pasted_image_20250915172049.png)


```python
print("Welcome to Python Built-in Functions Demo")
 # print(): Displays output
name = input("Enter your name: ")
 # input(): Takes user input
print("Hello,", name)
 # ----- Input and Output -----
```

#### ----- Type Conversion -----
```python
num_str = "123"
num_int = int(num_str)
 # int(): Converts to integer
num_float = float(num_str)
 # float(): Converts to float
num_bool = bool(num_str)
 # bool(): Converts to Boolean
num_str2 = str(num_int)
 # str(): Converts to string
print("int:", num_int, "| float:", num_float, "| bool:", num_bool, "| str:", num_str2)
```
#### ----- Math & Numeric -----
```python
print("abs(-7):", abs(-7))
 # abs(): Absolute value
print("pow(2, 3):", pow(2, 3))
 # pow(): x**y
print("divmod(10, 3):", divmod(10, 3))
 # divmod(): Returns (quotient, remainder)
print("round(3.14159, 2):", round(3.14159, 2))
 # round(): Rounds to 2 decimal places
print("sum([1,2,3]):", sum([1,2,3]))
 # sum(): Sum of iterable
expr = "2 + 3 * 4"
print("eval(expr):", eval(expr))
 # eval(): Evaluate Python expression
```
#### ----- Character and Ordinal -----
```python
print("ord('A'):", ord('A'))
 # ord(): Unicode code point of char
Dr. B Raj Kumar
print("chr(66):", chr(66))
 # chr(): Character for Unicode number
```

#### ----- Sequence Operations -----
```python
text = "Python"
print("len(text):", len(text))
print("sorted(text):", sorted(text))
print("reversed(text):", list(reversed(text)))

# len(): Length of object
# sorted(): Sort characters
# reversed(): Reverse order
```
#### ----- Type & Object Checking -----
```python
print("type(name):", type(name))
print("isinstance(10, int):", isinstance(10, int))
print("id(name):", id(name))
# type(): Type of variable
# isinstance(): Type check
# id(): Unique memory id of object
```
#### ----- Logical Utilities -----
```python
lst = [2, 4, 6]
print("all even?", all(x % 2 == 0 for x in lst))
print("any > 5?", any(x > 5 for x in lst))
print("enumerate(lst):", list(enumerate(lst)))
# all(): True if all elements true
# any(): True if any element is true
# enumerate(): Returns Index with value
```

#### ----- Iterables & Range -----
```python
print("list(range(5)):", list(range(5)))
zipped = list(zip([1,2], ['a','b']))
print("zip([1,2], ['a','b']):", zipped)
# range(): Sequence of numbers
# zip(): Pairs from multiple iterables
```
#### ----- Miscellaneous -----
```python
print("bin(10):", bin(10))
print("hex(255):", hex(255))
print("oct(8):",
 Dr. B Raj Kumar
 oct(8))
 # bin(): Binary string of integer
# hex(): Hexadecimal representation
# oct(): Octal representation
```

```python
print('fact of {} is {}'.format(i,fact(i)))
#The format() method formats the specified value(s) and insert them inside the string's placeholder { }.
print(f'fact of {i} is {fact(i)}')
```

lambda arguments: arithmetic_expression
```python
lambda x,y:x+y
```

list methods
```python
lst = [1,2,3,4,5]
lst.append(6)
lst.extend([7,8])
lst.insert(4,5)
lst.remove('5')
lst.pop() #removes n returns item
lst.copy() 
#To copy all elements in another varian=ble or else diff variable name is assigned for same list
#Both variables point to the same list
lst.clear() #clear all elements
lst.index(5)
lst.count(5)
lst.sort()
lst.reverse()
```

List comprehension
```python
lst=[expression for item in list if condition]
```

Remove duplicates
```python
original = [1, 2, 2, 3, 4, 4, 5, 1]
unique = []
for item in original:
if item not in unique:
unique.append(item)
```

IN operator
```python
Boolean test whether a value is inside a
container:
>>> t = [1, 2, 4, 5]
>>> 3 in t
 # False
>>> 4 not in t
 # False
>>> t1=(1,2,3,4,5)
>>> print(4 in t)
 # True
>>> print(4 not in t) # False

For strings, tests for substrings
>>> a = 'abcde'
>>> 'c' in a
True
>>> 'cd' in a
True
>>> 'ac' in a
False
```

Tuple methods
```python
tup = (1,2,3,4,5)
tup.count()
tup.index(2)
lst = list(tup)
lst.append(6)
tup = tuple(lst)
print(sorted(tup))
print(min(tup), max(tup))
```

### In tuple parenthesis in optional
t = (1,2,3,4)
t= 1,2,3,4

Set methods
```python
set1 = {1,2,3,4}
set1.add(3)
set1.update([3,4])
set1.remove(20) # Throws error wn ele isn't there
set1.discard(20)# No exception throw
set1.pop() # Remove randomly n return ele
set2 = set1.copy()
set2.clear()
union_set  = set1.union(set2)
intersection_set = set1.intersection(set2)
diff_set = set1.difference(set2)
set1.isdisjoint(set2)
set1.issubset(set2)
set2.issuperset(set1) 
'No indexing and slicing'
s={x*x for x in range(5)}
```

```python
user_input = eval(input("Enter a math expression: "))

'eval is necessary because input will also count spaces and commas in the absen ce of eval'

'We can give input as list or tuple or just by seperating with commas which is none other than tuple'
```

```python
s={10,20,30,40}
fs=frozenset(s)
type(fs) # <class 'frozenset'>
fs.add(70) # Not possible
fs.remove(10) # Not possible
```

Dictionary usage
```python
d1 = { 1:'ram' , 2:'shyam' , 3:'virinchi' , 4:'datta' }

d2 = dict([('sape', 4139), ('guido', 4127), ('jack', 4098)])

d3 = dict(sape=4139, guido=4127, jack=4098)

len(d1) = 4
print(d1[2]) #ram
print(d1.keys()) #[1,2,3,4]
print(d1.values) #['ram', 'shyam', 'virinchi', 'datta']
d1[2] = 'bro'
print(d1[2]) # 'bro'

#duplicate value overwritte
d1 = { 1:'ram' , 2:'shyam' , 3:'virinchi' , 3:'datta' }
print(d1) #  { 1:'ram' , 2:'shyam' , 3:'datta' }

#Dictionary comprehensions
dc={x: x**2 for x in (2, 4, 6)}

for k, v in d1.items():
print(k,v)  
```
![](/ZettleKasten/Unsorted/Attachment/Pasted_image_20250916075252.png)


![](/ZettleKasten/Unsorted/Attachment/Pasted_image_20250916075316.png)


**math.isnan()**
```python
#Safer to create new list instead of editing

import math
raw_data = [56.2,float('NaN'), 51.7, 47.8]
filtered_data= []
for v in raw_data:
	if not math.isnan(v)
		filtered_data.append(v)
		
filtered_data
```

**Enumerate**
```python
for i,v in enumerate(['tic', 'tac', 'toe']):
	print(i,v)
	
dict(enumerate(['tic', 'tac', 'toe']))
```

**zip()**
```python
qus = ['tic', 'tac', 'toe']
ans = ['b' , 'br' , 'bro']

for q,a in zip(qus, ans):
	print(q,a)
```

**sorted()**
```python
bask = ['a', 'b' , 'c' ,'a', 'v']
for f in sorted(set(bask)):
	print(f)
```

**reversed()**
```python
st = 'hello'
h = ''.join(reversed(st))
print(h)
```

---
### Things to do 

Diff bw list, tuple, set, dict
oops codes
threads
regex
butterfly pattern