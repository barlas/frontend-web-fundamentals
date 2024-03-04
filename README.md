# The Web Development Primer

## Table of contents
- [The Web Development Primer](#the-web-development-primer)
  * [Computer Science](#computer-science)
    + [Data Structures](#data-structures)
    + [Algorithms](#algorithms)
    + [Big O Notation](#big-o-notation)
    + [Dynamic Programming](#dynamic-programming)
      - [Identifying Overlapping Subproblems:](#identifying-overlapping-subproblems-)
      - [Memoization (Top Down, Recursive)](#memoization--top-down--recursive-)
      - [Tabulation (Bottom Up, Iterative)](#tabulation--bottom-up--iterative-)
    + [Computer Systems](#computer-systems)
    + [Common Software Concepts](#common-software-concepts)
      - [Transpilers](#transpilers)
      - [Compilers](#compilers)
        * [V8's Just-in-time (JIT)](#v8-s-just-in-time--jit-)
        * [Svelte/compiler](#svelte-compiler)
      - [Interpreters](#interpreters)
      - [Package Managers](#package-managers)
        * [NPM, Cargo (Rust)](#npm--cargo--rust-)
      - [Testing Strategies](#testing-strategies)
      - [Debugging and Optimization](#debugging-and-optimization)
      - [Memory Pyramid](#memory-pyramid)
      - [Caches Matter](#caches-matter)
    + [Full Stack Development by Definition](#full-stack-development-by-definition)
      - [Visual Design (UI/UX)](#visual-design--ui-ux-)
      - [Infrastructure](#infrastructure)
        * [Systems](#systems)
        * [Network](#network)
      - [Backend](#backend)
      - [Frontend](#frontend)
    + [Web App Under the Hood](#web-app-under-the-hood)
      - [AWS](#aws)
      - [Netlify](#netlify)
      - [SvelteKit](#sveltekit)
      - [Next.js](#nextjs)
      - [SvelteKit vs Next.js](#sveltekit-vs-nextjs)
      - [Svelte](#svelte)
        * [Component Compilation](#component-compilation)
      - [Optimization Across Components](#optimization-across-components)
        * [Nested Components](#nested-components)
        * [Svelte Compiler and AST](#svelte-compiler-and-ast)
      - [React vs Svelte](#react-vs-svelte)
        * [Performance and Efficiency](#performance-and-efficiency)
        * [Development Experience and Learning Curve](#development-experience-and-learning-curve)
        * [Reactivity and State Management](#reactivity-and-state-management)
        * [Ecosystem and Community Support](#ecosystem-and-community-support)
      - [Memory Management](#memory-management)
        * [Summary](#summary)
        * [Svelte Memory Implications](#svelte-memory-implications)
        * [React Memory Implications](#react-memory-implications)
      - [React and Svelte Reactivity Models](#react-and-svelte-reactivity-models)
      - [Compile-time vs Run-time Reactivity](#compile-time-vs-run-time-reactivity)
        * [Comparative Analysis](#comparative-analysis)
        * [Compile-time Reactivity](#compile-time-reactivity)
        * [Run-time Reactivity](#run-time-reactivity)
      - [React.js](#reactjs)
        * [React Component Lifecycle:](#react-component-lifecycle-)
        * [Hooks and Functional Components:](#hooks-and-functional-components-)
        * [State Management:](#state-management-)
        * [Performance Optimization:](#performance-optimization-)
        * [Advanced Patterns and Techniques:](#advanced-patterns-and-techniques-)
        * [React Internals and Principles:](#react-internals-and-principles-)
        * [Type Checking and TypeScript:](#type-checking-and-typescript-)
        * [Security in React:](#security-in-react-)
        * [Testing and Debugging:](#testing-and-debugging-)
        * [Next.js/SSR:](#nextjs-ssr-)
        * [Reconciliation Algorithm](#reconciliation-algorithm)
        * [React Fiber](#react-fiber)
        * [React Compiler](#react-compiler)
        * [The useOptimistic Hook](#the-useoptimistic-hook)
        * [Higher-Order Components (HOCs)](#higher-order-components--hocs-)
        * [useState vs useReducer](#usestate-vs-usereducer)
        * [Redux vs Context API](#redux-vs-context-api)
        * [Controlled Components](#controlled-components)
      - [Uncontrolled Components](#uncontrolled-components)
      - [Denounce Input Fields](#denounce-input-fields)
      - [JavaScript](#javascript)
        * [Ternary Operator ? :](#ternary-operator----)
        * [Spread Operator …](#spread-operator--)
        * [apply, call, bind](#apply--call--bind)
        * [map, filter, reduce](#map--filter--reduce)
      - [HTML/CSS](#html-css)
      - [Client Side - Browsers (Chrome)](#client-side---browsers--chrome-)
        * [V8 Engine](#v8-engine)
        * [Browser's Lifecycle](#browser-s-lifecycle)
        * [Memory Allocation](#memory-allocation)
        * [Garbage Collection (GC)](#garbage-collection--gc-)
        * [Browser API](#browser-api)
      - [Server Side](#server-side)
      - [DNS (Domain Name System)](#dns--domain-name-system-)
      - [IP (Internet Protocol) Address Lookup](#ip--internet-protocol--address-lookup)
      - [XHR (XMLHttpRequest)](#xhr--xmlhttprequest-)
      - [HTTP (Hypertext Transfer Protocol)](#http--hypertext-transfer-protocol-)
        * [TCP (Transmission Control Protoco)](#tcp--transmission-control-protoco-)
        * [UDP (User Datagram Protocol)](#udp--user-datagram-protocol-)

## Computer Science

### Data Structures
### Algorithms
### Big O Notation
### Dynamic Programming
#### Identifying Overlapping Subproblems:
In JavaScript, you often encounter tasks like calculating Fibonacci numbers, finding the shortest path in a grid, or optimizing the way to cut rods or strings where the same subproblems are solved multiple times. Recognizing these overlapping subproblems is the first step toward a dynamic programming solution.
#### Memoization (Top Down, Recursive)
 Memoization is a common technique used in dynamic programming to store the results of expensive function calls and return the cached result when the same inputs occur again. In JavaScript, this is typically implemented using objects (for unordered key-value pairs) or arrays (for ordered lists of values) as caches.
```
function fib(n, memo = {}) {
 if (n in memo) return memo[n];
 if (n <= 2) return 1;
 memo[n] = fib(n - 1, memo) + fib(n - 2, memo);
 return memo[n];
}
```

#### Tabulation (Bottom Up, Iterative)
Another dynamic programming technique is tabulation, where you solve problems by filling up a table (usually an array) from the bottom up. This method iterates through the table in a non-recursive manner, which can be more space-efficient and faster for some problems due to reduced call stack usage.
```
function fibTabulation(n) {
 if (n <= 2) return 1;
 let fibNumbers = [0, 1, 1];
 for (let i = 3; i <= n; i++) {
   fibNumbers[i] = fibNumbers[i - 1] + fibNumbers[i - 2];
 }
 return fibNumbers[n];
}
```

### Computer Systems

### Common Software Concepts
#### Transpilers
#### Compilers
##### V8's Just-in-time (JIT)
##### Svelte/compiler
#### Interpreters
#### Package Managers
##### NPM, Cargo (Rust)
#### Testing Strategies
#### Debugging and Optimization
#### Memory Pyramid
#### Caches Matter

### Full Stack Development by Definition
#### Visual Design (UI/UX)
#### Infrastructure
##### Systems
##### Network
#### Backend
#### Frontend

### Web App Under the Hood
#### AWS
#### Netlify


#### JavaScript
##### Ternary Operator ? :
##### Spread Operator …
##### apply, call, bind
##### map, filter, reduce
#### HTML/CSS
#### Client Side - Browsers (Chrome)

##### V8 Engine
The V8 engine is a JavaScript engine developed by Google for the Chrome web browser and Node.js. It compiles JavaScript into native machine code using Just-In-Time (JIT) compilation techniques. V8's use of AST (**Abstract Syntax Tree**) is part of its parsing and compilation process.
JIT (Just-In-Time) compilation
* **Parsing:*### When V8 processes JavaScript code, it first parses the code into an AST. This AST represents the syntactical structure of the JavaScript code, including variables, functions, expressions, and statements.
* **Optimization:*### V8 has multiple compilation pipelines (like Ignition and TurboFan) that use the AST for optimizing code. It analyzes the AST to perform optimizations such as inlining functions, eliminating dead code, and optimizing loops.
* **Code Generation:*### After optimizations, V8 uses the AST to generate machine code that can be executed directly by the CPU. This process involves translating the high-level structures in the AST into lower-level instructions that the machine understands.
##### Browser's Lifecycle
The page-building phase
* Parsing the HTML, and building the DOM
* Executing JavaScript code
Event Handling phase
* Event Loop (Single-threaded)
* Callback Queue
##### Memory Allocation
Call Stack
* The Call Stack is used for managing function calls and storing primitive types and stack-allocated structures, operating in a Last In, First Out (LIFO) manner with automatic memory management.
* **Function Call Management:*### It tracks the point to which each active function should return control when it finishes executing. This includes the function's return address, its arguments, and its local variables.
* **Primitive Types Storage:*### While it's true that primitive types (like integers, booleans, and floating-point numbers) are often stored directly on the stack, the statement "kinda link list, points to heap locations?" is a misunderstanding. The call stack does not function like a linked list nor does it point to heap locations for storing primitives. However, references (or pointers) to objects stored on the heap can be kept on the stack.
Heap
* The Heap is used for dynamic memory allocation, storing objects, arrays, and other complex data structures that need to be manually managed or are managed by a garbage collector, allowing for more flexibility in memory usage at the cost of potential complexity in memory management.
* **Objects and Complex Data Structures:*### When you create objects, arrays, or other complex data structures, they are typically allocated on the heap. This is because the size of these data structures may not be known at compile time or they may need to outlive the call stack frame they were created within.
* **Function, Arrays, Objects Storage:*### It's not just about where "functions" are stored, as functions (especially in compiled languages) are generally not stored on the heap. However, the heap is used to store objects, arrays, and other data structures that require dynamic memory allocation.
##### Garbage Collection (GC)
V8 employs a generational approach to garbage collection, based on the observation that most objects die young ("infant mortality") and only a few live to old age.
New Generation (Nursery)
* * **Nursery:*### This is where objects are allocated when they are first created. Because many objects tend to become unreachable quickly (they "die young"), the nursery is designed to be small and to be collected frequently.
* * **Minor GC:*### The garbage collection that occurs in the new generation is known as Minor GC. It is fast and focuses on the nursery, where most objects are expected to die. During a minor GC, live objects that survive are typically moved to a more mature space within the new generation, often referred to as the "intermediate area" or directly promoted to the old generation if they survive multiple collections, indicating they have a longer lifespan.
Old Generation
* * **Old Generation:*### Objects that have survived several rounds of Minor GC in the new generation are promoted to the old generation. The rationale is that if an object has lived long enough, it is likely to continue to be in use, so moving it to the old generation reduces the overhead of examining it during frequent minor collections.
* * * * * **Major GC (Full GC):*### Garbage collection in the old generation is known as Major GC or Full GC. This process is more comprehensive and can be more time-consuming than Minor GC because it involves the entire heap, including both new and old generations. Major GCs are less frequent but necessary to reclaim more substantial amounts of memory and to manage the long-lived objects efficiently.
**Infant mortality*### refers to the observation that most objects in a program die young or become unreachable soon after their creation. The generational garbage collection strategy exploits this by optimizing for the fast allocation and collection of such short-lived objects, making Minor GCs very efficient.
Optimization Techniques
* Efficient Memory Usage
* * **Minimize Object Allocation:*### Objects consume memory. By reducing the number of temporary objects you create, you can decrease the frequency and duration of garbage collection pauses.
* * **Reuse Objects:*### Where possible, reuse objects instead of creating new ones. For instance, if you have a function that creates an array or object every time it is called, consider creating it once and then resetting its state after each use.
* * **Avoid Large Objects:*### Large objects can quickly fill up the heap, leading to major garbage collection cycles. If possible, break large data structures into smaller chunks.
* Optimize for the Garbage Collector
* * **Understand Generational Collection:*### Knowing that V8 uses a generational approach to garbage collection can help you design your objects for better memory management. Short-lived objects (like temporary variables in a function) are less of a concern, but managing the lifecycle of objects that could move to the old generation is crucial.
* * **Limit Global Variables:*### Global variables are never garbage collected unless you explicitly set them to null. Using globals sparingly helps reduce memory usage.
* * * * * Use WeakRefs and FinalizationRegistry with Caution: These features allow developers to create weak references to objects and to register callbacks to be executed once these objects are garbage collected, respectively. They can be useful for managing memory directly but should be used carefully to avoid unintended side effects.
* **Code Optimization Practices**
* * **Inline Caching:*### V8 uses inline caching to optimize method and property access on objects. You can improve performance by using stable object shapes (i.e., creating objects with the same properties in the same order) so V8 can optimize access to these objects.
* * * * * Hidden Classes: V8 creates hidden classes for objects that share the same properties to optimize access patterns. Avoid adding or deleting properties from objects after they are created, as this can cause V8 to generate multiple hidden classes, which reduces the efficiency of property access.
* * **Optimize Function Execution:*### Keep functions small and focused. V8 can optimize smaller functions more efficiently. Additionally, avoid using features that disable optimizations, such as with statements and eval.
* Profiling and Testing
* * **Performance Profiling:*### Use Chrome DevTools to profile your JavaScript's performance and identify bottlenecks. The Performance tab can show you where time is being spent in scripting, rendering, and garbage collection.
* * **Memory Profiling:*### The Memory tab in Chrome DevTools allows you to take heap snapshots and track memory leaks. Understanding how your application's memory usage grows over time can help you identify and fix leaks.
##### Browser API
DOM
Events
Timers
#### Server Side
#### DNS (Domain Name System) 
#### IP (Internet Protocol) Address Lookup
#### XHR (XMLHttpRequest)
#### HTTP (Hypertext Transfer Protocol)
##### TCP (Transmission Control Protoco)
##### UDP (User Datagram Protocol)


