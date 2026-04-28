# **TypeScript Syntax Compendium**

links  
[TutorialsPoint on typescript](https://www.tutorialspoint.com/typescript/index.htm)

---

## **1\. Variable Declarations (let, const, var)**

**Purpose:** Declare variables with different scoping rules.

**Example:**

let a: number \= 5;  
const b: string \= "hello";  
var c: boolean \= true;

console.log(a, b, c);

**Output:**

5 hello true

---

## **2\. Basic Types**

**Purpose:** Define explicit types for variables.

**Example:**

let num: number \= 10;  
let str: string \= "text";  
let bool: boolean \= false;

**Output:** (no runtime output)

---

## **3\. Arrays**

**Purpose:** Store ordered collections.

**Example:**

let nums: number\[\] \= \[1,2,3\];  
let strs: Array\<string\> \= \["a","b"\];

console.log(nums\[0\]);

**Output:**

1

---

## **4\. Tuples**

**Purpose:** Fixed-length arrays with known types.

**Example:**

let tuple: \[string, number\] \= \["age", 21\];  
console.log(tuple);

**Output:**

\["age", 21\]

---

## **5\. Enums**

**Purpose:** Define named constants.

**Example:**

enum Color { Red, Green, Blue }  
let c: Color \= Color.Green;  
console.log(c);

**Output:**

1

---

## **6\. Any Type**

**Purpose:** Disable type checking.

**Example:**

let x: any \= 5;  
x \= "now string";  
console.log(x);

**Output:**

now string

---

## **7\. Unknown Type**

**Purpose:** Safer alternative to any.

**Example:**

let x: unknown \= "hello";  
if (typeof x \=== "string") {  
  console.log(x.toUpperCase());  
}

**Output:**

HELLO

---

## **8\. Functions**

**Purpose:** Define reusable logic.

**Example:**

function add(a: number, b: number): number {  
  return a \+ b;  
}

console.log(add(2,3));

**Output:**

5

---

## **9\. Arrow Functions**

**Purpose:** Shorter function syntax.

**Example:**

const add \= (a: number, b: number): number \=\> a \+ b;  
console.log(add(1,2));

**Output:**

3

---

## **10\. Optional Parameters**

**Purpose:** Allow missing arguments.

**Example:**

function greet(name?: string) {  
  console.log(name || "Guest");  
}

greet();

**Output:**

Guest

---

## **11\. Default Parameters**

**Purpose:** Provide default values.

**Example:**

function greet(name: string \= "Guest") {  
  console.log(name);  
}

greet();

**Output:**

Guest

---

## **12\. Interfaces**

**Purpose:** Define object shapes.

**Example:**

interface Person {  
  name: string;  
  age: number;  
}

const p: Person \= { name: "Alice", age: 20 };  
console.log(p.name);

**Output:**

Alice

---

## **13\. Type Aliases**

**Purpose:** Create custom types.

**Example:**

type ID \= number | string;  
let id: ID \= 123;  
console.log(id);

**Output:**

123

---

## **14\. Union Types**

**Purpose:** Allow multiple types.

**Example:**

let value: string | number \= "hi";  
value \= 10;  
console.log(value);

**Output:**

10

---

## **15\. Type Assertions**

**Purpose:** Override inferred types.

**Example:**

let value: any \= "hello";  
let len: number \= (value as string).length;  
console.log(len);

**Output:**

5

---

## **16\. Classes**

**Purpose:** Object-oriented programming.

**Example:**

class Animal {  
  name: string;  
  constructor(name: string) {  
    this.name \= name;  
  }  
  speak() {  
    return this.name \+ " makes noise";  
  }  
}

console.log(new Animal("Dog").speak());

**Output:**

Dog makes noise

---

## **17\. Inheritance**

**Purpose:** Extend classes.

**Example:**

class Dog extends Animal {  
  bark() {  
    return "woof";  
  }  
}

console.log(new Dog("Rex").bark());

**Output:**

woof

---

## **18\. Generics**

**Purpose:** Reusable typed components.

**Example:**

function identity\<T\>(arg: T): T {  
  return arg;  
}

console.log(identity\<number\>(5));

**Output:**

5

---

## **19\. Modules (export/import)**

**Purpose:** Share code between files.

**Example:**

// file1.ts  
export const x \= 5;

// file2.ts  
import { x } from "./file1";  
console.log(x);

**Output:**

5

---

## **20\. Promises**

**Purpose:** Handle async operations.

**Example:**

const p \= new Promise\<number\>((resolve) \=\> {  
  resolve(42);  
});

p.then(console.log);

**Output:**

42

---

## **21\. Async/Await**

**Purpose:** Simplify async code.

**Example:**

async function getNum() {  
  return 5;  
}

getNum().then(console.log);

**Output:**

5

---

## **22\. Readonly**

**Purpose:** Prevent modification.

**Example:**

interface Point {  
  readonly x: number;  
}

const p: Point \= { x: 1 };  
// p.x \= 2; // error

**Output:** (compile-time error if modified)

---

## **23\. Partial Utility Type**

**Purpose:** Make all properties optional.

**Example:**

interface Person { name: string; age: number }  
let p: Partial\<Person\> \= { name: "Bob" };  
console.log(p);

**Output:**

{ name: "Bob" }

---

## **24\. Pick Utility Type**

**Purpose:** Select specific properties.

**Example:**

interface Person { name: string; age: number }  
let p: Pick\<Person, "name"\> \= { name: "Bob" };  
console.log(p);

**Output:**

{ name: "Bob" }

---

## **25\. Record Utility Type**

**Purpose:** Map keys to values.

**Example:**

let obj: Record\<string, number\> \= { a: 1, b: 2 };  
console.log(obj);

**Output:**

{ a: 1, b: 2 }

---

## **26\. Optional Chaining**

**Purpose:** Safely access nested properties.

**Example:**

let obj: any \= {};  
console.log(obj?.a?.b);

**Output:**

undefined

---

## **27\. Nullish Coalescing**

**Purpose:** Default for null/undefined.

**Example:**

let x \= null;  
console.log(x ?? "default");

**Output:**

default

---

## **28\. keyof Operator**

**Purpose:** Get keys of a type.

**Example:**

interface Person { name: string; age: number }  
type Keys \= keyof Person;

**Output:** (type \= "name" | "age")

---

## **29\. typeof Operator**

**Purpose:** Get type from value.

**Example:**

const x \= 5;  
type T \= typeof x;

**Output:** (type \= number)

---

## **30\. Mapped Types**

**Purpose:** Transform types.

**Example:**

type Options\<T\> \= {  
  \[K in keyof T\]?: T\[K\];  
};

**Output:** (new optional type)

---

(End of compendium — expand as needed\!)

