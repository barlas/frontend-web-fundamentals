# The Web Development Primer



# Index

* Computer Science
  * Data Structures
  * Algorithms
  * Big O Notation
  * Dynamic Programming
    * Memoization (Top Down, Recursive)
    * Tabulation (Bottom Up, Iterative)
* Computer Systems

* Common Software Concepts
  * Transpilers
  * Compilers
    * V8's Just-in-time (JIT)
    * Svelte/compiler
  * Interpreters
  * Package Managers
    * NPM, Cargo (Rust)
  * Testing Strategies
  * Debugging and Optimization
  * Memory Pyramid
  * Caches Matter

* Full Stack Development by Definition
  * Visual Design (UI/UX)
  * Infrastructure
    * Systems
    * Network
  * Backend
  * Frontend

* Web App Under the Hood
  * AWS
  * Netlify
  * Next.js
    * Routing
    * SSG, CSR, SSR
  * React.js
    * Controlled / Uncontrolled
    * Denounce Input Fields
  * JavaScript
    * Ternary Operator ? :
    * Spread Operator …
    * apply, call, bind
    * map, filter, reduce
  * HTML/CSS
  * Client Side - Browsers (Chrome)
    * V8 Engine
      * The V8 engine is a JavaScript engine developed by Google for the Chrome web browser and Node.js. It compiles JavaScript into native machine code using Just-In-Time (JIT) compilation techniques. V8's use of AST (**Abstract Syntax Tree**) is part of its parsing and compilation process.
      * JIT (Just-In-Time) compilation
        * **Parsing:** When V8 processes JavaScript code, it first parses the code into an AST. This AST represents the syntactical structure of the JavaScript code, including variables, functions, expressions, and statements.
        * **Optimization:** V8 has multiple compilation pipelines (like Ignition and TurboFan) that use the AST for optimizing code. It analyzes the AST to perform optimizations such as inlining functions, eliminating dead code, and optimizing loops.
        * **Code Generation:** After optimizations, V8 uses the AST to generate machine code that can be executed directly by the CPU. This process involves translating the high-level structures in the AST into lower-level instructions that the machine understands.
    * Browser's Lifecycle
      * The page-building phase
        * Parsing the HTML, and building the DOM
        * Executing JavaScript code
      * Event Handling phase
        * Event Loop (Single-threaded)
        * Callback Queue
    * Memory Allocation
      * Call Stack
        * The Call Stack is used for managing function calls and storing primitive types and stack-allocated structures, operating in a Last In, First Out (LIFO) manner with automatic memory management.
        * **Function Call Management:** It tracks the point to which each active function should return control when it finishes executing. This includes the function's return address, its arguments, and its local variables.
        * **Primitive Types Storage:** While it's true that primitive types (like integers, booleans, and floating-point numbers) are often stored directly on the stack, the statement "kinda link list, points to heap locations?" is a misunderstanding. The call stack does not function like a linked list nor does it point to heap locations for storing primitives. However, references (or pointers) to objects stored on the heap can be kept on the stack.
      * Heap
        * The Heap is used for dynamic memory allocation, storing objects, arrays, and other complex data structures that need to be manually managed or are managed by a garbage collector, allowing for more flexibility in memory usage at the cost of potential complexity in memory management.
        * **Objects and Complex Data Structures:** When you create objects, arrays, or other complex data structures, they are typically allocated on the heap. This is because the size of these data structures may not be known at compile time or they may need to outlive the call stack frame they were created within.
        * **Function, Arrays, Objects Storage:** It's not just about where "functions" are stored, as functions (especially in compiled languages) are generally not stored on the heap. However, the heap is used to store objects, arrays, and other data structures that require dynamic memory allocation.
    * Garbage Collection (GC)
      * V8 employs a generational approach to garbage collection, based on the observation that most objects die young ("infant mortality") and only a few live to old age.
      * New Generation (Nursery)
          * **Nursery:** This is where objects are allocated when they are first created. Because many objects tend to become unreachable quickly (they "die young"), the nursery is designed to be small and to be collected frequently.
          * **Minor GC:** The garbage collection that occurs in the new generation is known as Minor GC. It is fast and focuses on the nursery, where most objects are expected to die. During a minor GC, live objects that survive are typically moved to a more mature space within the new generation, often referred to as the "intermediate area" or directly promoted to the old generation if they survive multiple collections, indicating they have a longer lifespan.
      * Old Generation
          * **Old Generation:** Objects that have survived several rounds of Minor GC in the new generation are promoted to the old generation. The rationale is that if an object has lived long enough, it is likely to continue to be in use, so moving it to the old generation reduces the overhead of examining it during frequent minor collections.
          **Major GC (Full GC):** Garbage collection in the old generation is known as Major GC or Full GC. This process is more comprehensive and can be more time-consuming than Minor GC because it involves the entire heap, including both new and old generations. Major GCs are less frequent but necessary to reclaim more substantial amounts of memory and to manage the long-lived objects efficiently.
      * **Infant mortality** refers to the observation that most objects in a program die young or become unreachable soon after their creation. The generational garbage collection strategy exploits this by optimizing for the fast allocation and collection of such short-lived objects, making Minor GCs very efficient.
      * Optimization Techniques
        * Efficient Memory Usage
          * **Minimize Object Allocation:** Objects consume memory. By reducing the number of temporary objects you create, you can decrease the frequency and duration of garbage collection pauses.
          * **Reuse Objects:** Where possible, reuse objects instead of creating new ones. For instance, if you have a function that creates an array or object every time it is called, consider creating it once and then resetting its state after each use.
          * **Avoid Large Objects:** Large objects can quickly fill up the heap, leading to major garbage collection cycles. If possible, break large data structures into smaller chunks.
        * Optimize for the Garbage Collector
          * **Understand Generational Collection:** Knowing that V8 uses a generational approach to garbage collection can help you design your objects for better memory management. Short-lived objects (like temporary variables in a function) are less of a concern, but managing the lifecycle of objects that could move to the old generation is crucial.
          * **Limit Global Variables:** Global variables are never garbage collected unless you explicitly set them to null. Using globals sparingly helps reduce memory usage.
          Use WeakRefs and FinalizationRegistry with Caution: These features allow developers to create weak references to objects and to register callbacks to be executed once these objects are garbage collected, respectively. They can be useful for managing memory directly but should be used carefully to avoid unintended side effects.
        * **Code Optimization Practices**
          * **Inline Caching:** V8 uses inline caching to optimize method and property access on objects. You can improve performance by using stable object shapes (i.e., creating objects with the same properties in the same order) so V8 can optimize access to these objects.
          Hidden Classes: V8 creates hidden classes for objects that share the same properties to optimize access patterns. Avoid adding or deleting properties from objects after they are created, as this can cause V8 to generate multiple hidden classes, which reduces the efficiency of property access.
          * **Optimize Function Execution:** Keep functions small and focused. V8 can optimize smaller functions more efficiently. Additionally, avoid using features that disable optimizations, such as with statements and eval.
        * Profiling and Testing
          * **Performance Profiling:** Use Chrome DevTools to profile your JavaScript's performance and identify bottlenecks. The Performance tab can show you where time is being spent in scripting, rendering, and garbage collection.
          * **Memory Profiling:** The Memory tab in Chrome DevTools allows you to take heap snapshots and track memory leaks. Understanding how your application's memory usage grows over time can help you identify and fix leaks.
    * Browser API
      * DOM
      * Events
      * Timers
  * Server Side
  * DNS (Domain Name System) 
  * IP (Internet Protocol) Address Lookup
  * XHR (XMLHttpRequest)
  * HTTP (Hypertext Transfer Protocol)
    * TCP (Transmission Control Protoco)
    * UDP (User Datagram Protocol)


