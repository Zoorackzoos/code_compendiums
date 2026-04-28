# **Racket Syntax Reference Compendium**

This document is a practical reference for common Racket syntax. Each entry includes:

1. Title  
2. General purpose  
3. Example syntax with output

---

# **1\. Program Header: `#lang`**

## **Purpose**

Declares which language the file uses. Almost all beginner Racket programs start with `#lang racket`.

## **Example**

\#lang racket

(+ 2 3\)

Output:

5

---

# **2\. Function Call**

## **Purpose**

Racket uses **prefix notation**. The operator comes first, followed by arguments.

## **Example**

(+ 2 3\)

Output

5

---

# **3\. Defining Variables: `define`**

## **Purpose**

Creates a variable binding.

## **Example**

(define x 10\)

(+ x 5\)

Output

15

---

# **4\. Defining Functions**

## **Purpose**

Creates reusable procedures.

## **Example**

(define (square x)

  (\* x x))

(square 5\)

Output

25

---

# **5\. Lambda (Anonymous Functions)**

## **Purpose**

Creates a function without naming it.

## **Example**

((lambda (x) (\* x x)) 6\)

Output

36

---

# **6\. Conditional: `if`**

## **Purpose**

Chooses between two expressions.

## **Syntax**

`(if condition true-expression false-expression)`

## **Example**

(if (\> 5 3\)

    "yes"

    "no")

Output

yes

---

# **7\. Multiple Conditions: `cond`**

## **Purpose**

Used when there are many conditional branches.

## **Example**

(cond

  \[(\> 5 10\) "big"\]

  \[(\> 5 3\) "medium"\]

  \[else "small"\])

Output

medium

---

# **8\. Logical AND**

## **Purpose**

Evaluates expressions left-to-right and stops on false.

## **Example**

(and (\> 5 3\) (\< 5 10))

Output

\#t

---

# **9\. Logical OR**

## **Purpose**

Returns the first true value.

## **Example**

(or \#f \#f 10\)

Output

10

---

# **10\. Lists**

## **Purpose**

Creates a list data structure.

## **Example**

(list 1 2 3 4\)

Output

'(1 2 3 4\)

---

# **11\. Quoting Data**

## **Purpose**

Prevents evaluation and treats data literally.

## **Example**

'(1 2 3\)

Output

'(1 2 3\)

---

# **12\. Accessing List Elements**

## **Purpose**

Extract elements from lists.

## **Example**

(define L '(10 20 30))

(first L)

Output

10

---

# **13\. Rest of List**

## **Purpose**

Returns everything except the first element.

## **Example**

(rest '(1 2 3 4))

Output

'(2 3 4\)

---

# **14\. List Length**

## **Purpose**

Counts elements in a list.  
this is the same as size.

## **Example**

(length '(1 2 3 4))

Output

4

---

# **15\. Checking Types**

## **Purpose**

Determines the type of a value.

## **Example**

(list? '(1 2 3))

Output

\#t

---

# **16\. Local Variables: `let`**

## **Purpose**

Creates temporary bindings.

## **Example**

(let (\[x 5\]

      \[y 7\])

  (+ x y))

Output

12

---

# **17\. Recursion**

## **Purpose**

Functions calling themselves.

## **Example**

(define (factorial n)

  (if (= n 0\)

      1

      (\* n (factorial (- n 1)))))

(factorial 5\)

Output

120

---

# **18\. Mapping Over Lists**

## **Purpose**

Apply a function to each element.

## **Example**

(map square '(1 2 3 4))

Output

'(1 4 9 16\)

---

# **19\. Filtering Lists**

## **Purpose**

Keep elements matching a predicate.

## **Example**

(filter even? '(1 2 3 4 5 6))

Output

'(2 4 6\)

---

# **20\. Folding (Reducing)**

## **Purpose**

Combine list elements into one value.

## **Example**

(foldl \+ 0 '(1 2 3 4))

Output

10

---

# **21\. Boolean Values**

## **Purpose**

Logical truth values.

## **Example**

\#t

\#f

---

# **22\. Equality**

## **Purpose**

Compare values.

## **Example**

(= 5 5\)

Output

\#t

---

# **23\. Strings**

## **Purpose**

Text data.

## **Example**

(string-append "Hello " "World")

Output

"Hello World"

---

# **24\. Printing**

## **Purpose**

Display output.

## **Example**

(displayln "Hello")

	This is used for human-readable output

(println “hello”)

	This is used for debugging and dev-readable output

Output

Hello

“hello”

---

# **25\. Comments**

## **Purpose**

Ignored text for documentation.

## **Example**

;; This is a comment

(+ 2 3\)

Output

5

---

# **26\. Accessing List Elements by Index: `list-ref`** aka list ref aka list\[x\]

## **Purpose**

Returns the element at a specific position in a list. Lists are **0-indexed**.

## **Syntax**

`(list-ref list index)`

## **Example**

(list-ref '(10 20 30 40\) 2\)

Output

30

---

# **27\. Constructing Lists: `cons`**

## **Purpose**

Adds an element to the front of a list.

## **Example**

(cons 1 '(2 3 4))

Output

'(1 2 3 4\)

---

# **28\. First Element: `car`**

## **Purpose**

Returns the first element of a list.

## **Example**

(car '(5 6 7))

Output

5

---

# **29\. Rest of List: `cdr`**

## **Purpose**

Returns everything except the first element.

## **Example**

(cdr '(5 6 7))

Output

'(6 7\)

---

# **30\. Building Lists From Values**

## **Purpose**

Create lists dynamically.

## **Example**

(list "a" "b" "c")

Output

'("a" "b" "c")

---

# **31\. Checking Symbols**

## **Purpose**

Determines whether a value is a symbol.

## **Example**

(symbol? '+)

Output

\#t

---

# **32\. Checking Numbers**

## **Purpose**

Determines whether a value is a number.

## **Example**

(number? 42\)

Output

\#t

---

# **33\. Checking Booleans**

## **Purpose**

Determines whether a value is a boolean.

## **Example**

(boolean? \#t)

Output

\#t

---

# **34\. Nested Lists**

## **Purpose**

Lists can contain other lists.

## **Example**

(list 1 (list 2 3\) 4\)

Output

'(1 (2 3\) 4\)

---

# **35\. Taking Part of a List: `take`**

## **Purpose**

Returns the first N elements of a list.

## **Example**

(take '(1 2 3 4 5\) 3\)

Output

'(1 2 3\)

---

# **36\. Dropping Part of a List: `drop`**

## **Purpose**

Removes the first N elements of a list.

## **Example**

(drop '(1 2 3 4 5\) 2\)

Output

'(3 4 5\)

---

# **37\. Getting the Second Element**

## **Purpose**

Convenience function for the second element.

## **Example**

(second '(10 20 30))

Output

20

---

# **38\. Getting the Third Element**

## **Purpose**

Convenience function for the third element.

## **Example**

(third '(10 20 30 40))

Output

30

---

# **39\. Flattening Nested Lists: `flatten`**

## **Purpose**

Removes nesting inside lists.

## **Example**

(flatten '(1 (2 3\) (4 (5))))

Output

'(1 2 3 4 5\)

---

# **40\. Arithmetic Operations**

## **Purpose**

Perform mathematical calculations.

1. addition  
2. subtraction  
3. multiplication  
4. divizion 

## **Example**

(+ 2 3 4\)

Output

9

---

# **41\. Comparison Operators**

## **Purpose**

Compare numbers.

## **Example**

(\< 3 5\)

Output

\#t

---

# **42\. Boolean Negation: `not`**

## **Purpose**

Flips a boolean value.

## **Example**

(not \#t)

Output

\#f

---

# **43\. Nested Expressions**

## **Purpose**

Racket evaluates expressions from the inside out.

## **Example**

(+ 1 (\* 2 3))

Output

7

---

# **44\. Equality for General Values: `equal?`**

## **Purpose**

Compares lists, symbols, numbers, and more.

## **Example**

(equal? '(1 2 3\) '(1 2 3))

Output

\#t

---

# **45\. Symbol Literals**

## **Purpose**

Symbols represent identifiers or operators.

## **Example**

'+

Output

'+

Gotchu — here’s a clean **addendum section** in your exact format. I’ll include the ones you asked for (`length`, appending) and then add some **useful new ones you haven’t covered yet**.

---

# **46\. Length of a List: `length`**

## **Purpose**

Returns the number of elements in a list.

## **Example**

(length '(1 2 3 4))

Output

4

---

# **47\. Appending Lists: `append`**

## **Purpose**

Combines multiple lists into one list.

## **Example**

(append '(1 2\) '(3 4))

append

Output

'(1 2 3 4\)

---

# **48\. Adding to End of List (Common Pattern)**

## **Purpose**

Racket has no built-in “add to end”, so you use `append`.

## **Example**

(append '(1 2 3\) (list 4))

Output

'(1 2 3 4\)

---

# **49\. Reverse a List: `reverse`**

## **Purpose**

Reverses the order of elements in a list.

## **Example**

(reverse '(1 2 3))

Output

'(3 2 1\)

---

# **50\. Check if Empty List: `null?`**

## **Purpose**

Checks if a list is empty.

## **Example**

(null? '())

Output

\#t

---

# **51\. Combining Conditions: `and`**

## **Purpose**

Returns true if all conditions are true.

## **Example**

(and \#t \#t \#f)

Output

\#f

---

# **52\. Either Condition: `or`**

## **Purpose**

Returns true if at least one condition is true.

## **Example**

(or \#f \#f \#t)

Output

\#t

---

# **53\. Conditional Branching: `if`**

## **Purpose**

Executes one of two expressions based on a condition.

## **Example**

(if (\> 3 2\) 'yes 'no)

Output

'yes

---

# **54\. Multi-branch Condition: `cond`**

## **Purpose**

Handles multiple conditions.

## **Example**

(cond

 \[(\> 3 5\) 'big\]

 \[(\< 3 5\) 'small\]

 \[else 'equal\])

Output

'small

---

# **55\. Quoting Lists: `'`**

## **Purpose**

Prevents evaluation of lists and symbols.

## **Example**

'(1 \+ 2\)

Output

'(1 \+ 2\)

---

# **56\. Evaluating Expressions (conceptual): evaluation rule**

## **Purpose**

Racket evaluates lists as function calls unless quoted.

## **Example**

(+ 1 2\)

Output

3

---

# **57\. Checking List Type: `list?`**

## **Purpose**

Checks if a value is a list.

## **Example**

(list? '(1 2 3))

Output

\#t

---

# **58\. Nested Access (Manual)**

## **Purpose**

Access deeply nested list elements using `car`/`cdr`.

## **Example**

(car (cdr '(10 20 30)))

Output

20

---

# **59\. Combining Values into Lists Dynamically**

## **Purpose**

Build lists using computed values.

## **Example**

(list (+ 1 2\) (\* 2 3))

Output

'(3 6\)

---

# **60\. Equality for Numbers: `=`**

## **Purpose**

Checks if numbers are equal.

## **Example**

(= 3 3\)

Output

\#t

---

# **61\. Structural Equality vs Identity**

## **Purpose**

`equal?` compares structure, not memory.

## **Example**

(equal? '(1 2\) '(1 2))

Output

\#t

