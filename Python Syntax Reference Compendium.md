# **Python Syntax Reference Compendium**

This document is a practical reference for common Python syntax. Each entry includes:

1. Title  
2. General purpose  
3. Example syntax with output

---

# **1\. Print Function**

## **Purpose**

Outputs text or variables to the console.

## **Example**

print("Hello, world\!")

Output:

Hello, world\!

---

# **2\. Variables and Assignment**

## **Purpose**

Stores data values in named variables.

## **Example**

x \= 10

print(x)

Output:

10

---

# **3\. Type Checking**

## **Purpose**

Determines the type of a value.

## **Example**

print(type(5))

Output:

\<class 'int'\>

---

# **4\. Input Function**

## **Purpose**

Gets user input.

## **Example**

name \= input("Name: ")

print(name)

Output:

Name: Bob

Bob

---

# **5\. If Statements**

## **Purpose**

Conditional execution.

## **Example**

if 5 \> 3:

    print("yes")

Output:

yes

---

# **6\. For Loop**

## **Purpose**

Iterates over sequences.

## **Example**

for i in range(3):

    print(i)

Output:

0

1

2

---

# **7\. While Loop**

## **Purpose**

Repeats while condition is true.

## **Example**

x \= 0

while x \< 2:

    print(x)

    x \+= 1

Output:

0

1

---

# **8\. Functions**

## **Purpose**

Reusable code blocks.

## **Example**

def f(x):

    return x \+ 1

print(f(2))

Output:

3

---

# **9\. Lists**

## **Purpose**

Ordered collections.

## **Example**

print(\[1,2,3\])

Output:

\[1, 2, 3\]

---

# **10\. Dictionaries**

## **Purpose**

Key-value storage.

## **Example**

print({"a":1}\["a"\])

Output:

1

---

# **11\. Tuples**

## **Purpose**

Immutable sequences.

## **Example**

print((1,2)\[0\])

Output:

1

---

# **12\. Strings**

## **Purpose**

Text data.

## **Example**

print("hi".upper())

Output:

HI

---

# **13\. Try/Except**

## **Purpose**

Error handling.

## **Example**

try:

    int("x")

except:

    print("error")

Output:

error

---

# **14\. File Read**

## **Purpose**

Reads files.

## **Example**

with open("a.txt","w") as f:

    f.write("hi")

with open("a.txt") as f:

    print(f.read())

Output:

hi

---

# **15\. List Comprehension**

## **Purpose**

Compact list creation.

## **Example**

print(\[x\*x for x in range(3)\])

Output:

\[0, 1, 4\]

---

# **16\. Lambda**

## **Purpose**

Anonymous functions.

## **Example**

print((lambda x:x+1)(5))

Output:

6

---

# **17\. Classes**

## **Purpose**

Custom objects.

## **Example**

class A:

    def f(self): return 1

print(A().f())

Output:

1

---

# **18\. Import**

## **Purpose**

Use modules.

## **Example**

import math

print(math.sqrt(9))

Output:

3.0

---

# **19\. Boolean Values**

## **Purpose**

Truth values.

## **Example**

print(True, False)

---

# **20\. Comparison**

## **Purpose**

Compare values.

## **Example**

print(3 \> 1\)

Output:

True

---

# **21\. Logical Operators**

## **Purpose**

Combine conditions.

## **Example**

print(True and False)

Output:

False

---

# **22\. Slicing**

## **Purpose**

Subsequences.

## **Example**

print(\[1,2,3\]\[1:\])

Output:

\[2, 3\]

---

# **23\. len()**

## **Purpose**

Length of collection.

## **Example**

print(len(\[1,2,3\]))

Output:

3

---

# **24\. enumerate()**

## **Purpose**

Index \+ value loop.

## **Example**

for i,v in enumerate(\["a"\]): print(i,v)

Output:

0 a

---

# **25\. zip()**

## **Purpose**

Combine sequences.

## **Example**

print(list(zip(\[1\],\[2\])))

Output:

\[(1, 2)\]

---

# **26\. set()**

## **Purpose**

Unique elements.

## **Example**

print(set(\[1,1,2\]))

Output:

{1, 2}

---

# **27\. List remove**

## **Purpose**

Remove value.

## **Example**

x=\[1,2,3\]

x.remove(2)

print(x)

Output:

\[1, 3\]

---

# **28\. List insert**

## **Purpose**

Insert at index.

## **Example**

x=\[1,3\]

x.insert(1,2)

print(x)

Output:

\[1, 2, 3\]

---

# **29\. Sorted**

## **Purpose**

Sort iterable.

## **Example**

print(sorted(\[3,1,2\]))

Output:

\[1, 2, 3\]

---

# **30\. Reverse**

## **Purpose**

Reverse list.

## **Example**

x=\[1,2\]

x.reverse()

print(x)

Output:

\[2, 1\]

---

# **31\. f-Strings**

## **Purpose**

Formatted strings.

## **Example**

x=5

print(f"value={x}")

Output:

value=5

---

# **32\. isinstance()**

## **Purpose**

Type checking.

## **Example**

print(isinstance(5,int))

Output:

True

---

# **33\. None**

## **Purpose**

Represents no value.

## **Example**

print(None)

Output:

None

---

# **34\. pass**

## **Purpose**

Empty placeholder.

## **Example**

if True:

    pass

---

# **35\. break**

## **Purpose**

Exit loop.

## **Example**

for i in range(5):

    break

---

# **36\. continue**

## **Purpose**

Skip iteration.

## **Example**

for i in range(3):

    continue

---

# **37\. Global keyword**

## **Purpose**

Modify global variable.

## **Example**

x=1

def f():

    global x

    x=2

f()

print(x)

Output:

2

---

# **38\. Default Parameters**

## **Purpose**

Function defaults.

## **Example**

def f(x=5): return x

print(f())

Output:

5

---

# **39\. \*args**

## **Purpose**

Variable arguments.

## **Example**

def f(\*a): print(a)

f(1,2)

Output:

(1, 2\)

---

# **40\. \*\*kwargs**

## **Purpose**

Keyword arguments.

## **Example**

def f(\*\*k): print(k)

f(a=1)

Output:

{'a': 1}

---

# **41\. map()**

## **Purpose**

Apply function.

## **Example**

print(list(map(lambda x:x+1,\[1\])))

Output:

\[2\]

---

# **42\. filter()**

## **Purpose**

Filter elements.

## **Example**

print(list(filter(lambda x:x\>1,\[1,2\])))

Output:

\[2\]

---

# **43\. any()**

## **Purpose**

Any true?

## **Example**

print(any(\[False,True\]))

Output:

True

---

# **44\. all()**

## **Purpose**

All true?

## **Example**

print(all(\[True,True\]))

Output:

True

---

# **45\. sum()**

## **Purpose**

Add iterable.

## **Example**

print(sum(\[1,2\]))

Output:

3

---

# **46\. min/max**

## **Purpose**

Extremes.

## **Example**

print(min(\[1,2\]), max(\[1,2\]))

Output:

1 2

---

# **47\. round()**

## **Purpose**

Round numbers.

## **Example**

print(round(1.6))

Output:

2

---

# **48\. range()**

## **Purpose**

Generate sequence.

## **Example**

print(list(range(3)))

Output:

\[0, 1, 2\]

---

# **49\. open()**

## **Purpose**

Open files.

## **Example**

f=open("a.txt","w")

f.close()

---

# **50\. dir()**

## **Purpose**

List attributes.

## **Example**

print(dir(5))

---

# **51\. help()**

## **Purpose**

Documentation.

## **Example**

help(len)

---

# **52\. id()**

## **Purpose**

Object identity.

## **Example**

print(id(5))

---

# **53\. copy list**

## **Purpose**

Clone list.

## **Example**

x=\[1\]

y=x.copy()

print(y)

Output:

\[1\]

---

# **54\. Nested Lists**

## **Purpose**

Lists in lists.

## **Example**

print(\[1,\[2,3\]\])

Output:

\[1, \[2, 3\]\]

---

# **55\. Membership**

## **Purpose**

Check presence.

## **Example**

print(1 in \[1,2\])

Output:

True

---

# **56\. del**

## **Purpose**

Delete item.

## **Example**

x=\[1,2\]

del x\[0\]

print(x)

Output:

\[2\]

---

# **57\. assert**

## **Purpose**

Debug check.

## **Example**

assert 1==1

---

# **58\. with statement**

## **Purpose**

Context management.

## **Example**

with open("a.txt","w") as f:

    f.write("x")

---

# **59\. Generator**

## **Purpose**

Lazy iteration.

## **Example**

def f():

    yield 1

print(list(f()))

Output:

\[1\]

---

# 60\. .indexOf in python / .find / .index

1\. For Lists  
Use the [.index()](https://docs.python.org/3/tutorial/datastructures.html) method to find the first occurrence of a value. 

* Syntax: my\_list.index(element, start, end)  
* Behavior: Returns the lowest index where the element appears.  
* Error Handling: Unlike JavaScript’s indexOf (which returns \-1), Python's .index() raises a ValueError if the item is not found.  
* Multiple Occurrences: To find all indices of a repeating item, it is more efficient to use the enumerate() function within a list comprehension. 

2\. For Strings  
Python provides two primary methods for strings: [.find()](https://www.geeksforgeeks.org/python/difference-between-find-and-index-in-python/) and [.index()](https://www.w3schools.com/python/ref_string_index.asp). 

* .find(substring): This is the closest equivalent to JavaScript’s indexOf. It returns the index of the first occurrence or \-1 if the substring is not found.  
* .index(substring): This functions identically to .find(), but it raises a ValueError if the substring is missing.  
* Reverse Search: Use [.rfind()](https://builtin.com/software-engineering-perspectives/python-substring-indexof) or .rindex() to find the last occurrence of a substring. 

# 61\. how to reverse a string

\`\`\`  
original \= "backwards"  
reversed\_string \= original\[::-1\]  
print(reversed\_string)  \# Output: sdrawkcab  
\`\`\`

