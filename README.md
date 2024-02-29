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
      -[Denounce Input Fields](#denounce-input-fields)
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
* function fib(n, memo = {}) {
* * if (n in memo) return memo[n];
* * if (n <= 2) return 1;
* * memo[n] = fib(n - 1, memo) + fib(n - 2, memo);
* * return memo[n];
* }
```

#### Tabulation (Bottom Up, Iterative)
Another dynamic programming technique is tabulation, where you solve problems by filling up a table (usually an array) from the bottom up. This method iterates through the table in a non-recursive manner, which can be more space-efficient and faster for some problems due to reduced call stack usage.
```
function fibTabulation(n) {
* * if (n <= 2) return 1;
* * let fibNumbers = [0, 1, 1];
* * for (let i = 3; i <= n; i++) {
* * * * fibNumbers[i] = fibNumbers[i - 1] + fibNumbers[i - 2];
* * }
* * return fibNumbers[n];
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

#### SvelteKit
Multiple rendering modes. As opposed to globally setting one rendering mode for a project, you can define which rendering mode to use on a per-page basis. With SvelteKit, choose between modes such as prerendering and static site generation (SSG), client-side rendering (CSR), and server-side rendering (SSR).
Automatic API endpoints. 
* API routes allow developers to create endpoints to interact with third-party services for data fetching.
* Developers can automatically generate API endpoints as a part of the server-side component of their SvelteKit application. This minimizes the need to manually set up the middleware or the server code that would traditionally be used to process such data calls.
* Consistent navigation experience. With SvelteKit, you can use hybrid rendering to combine server-side rendered pages with a client-side router. This makes the navigation experience similar to a typical single-page app (SPA) that doesn’t require full page reloads.
* Developer-friendly tooling. SvelteKit uses Vite for a modern scaffolding and development experience.

#### Next.js
Technology: Next.js is built on React, utilizing the virtual DOM for updates and rendering. It provides features like server-side rendering (SSR), static site generation (SSG), and incremental static regeneration (ISR), making it highly versatile for building a wide range of applications.
Developer Experience: Offers a robust set of features out of the box, including file-based routing, API routes, and automatic code splitting, which can enhance productivity but may also introduce a steeper learning curve for newcomers.
Performance: Next.js applications can be optimized for performance, especially with SSR and SSG, enabling fast page loads and interactive experiences. However, the runtime performance might be slightly heavier compared to SvelteKit due to the virtual DOM.
Use Cases: Suited for large-scale applications that require dynamic content rendering, extensive SEO optimization, and the robust ecosystem of React. It's also beneficial for projects that need to leverage a vast number of existing React libraries and components.

#### SvelteKit vs Next.js
Underlying Library/Framework: SvelteKit uses Svelte, while Next.js is based on React.
Rendering Techniques: SvelteKit compiles away the framework code for a smaller bundle size, whereas Next.js leverages React's virtual DOM.
Developer Experience: SvelteKit is often praised for its simplicity and ease of learning, while Next.js is known for its extensive feature set and flexibility.
Ecosystem: Next.js benefits from the larger React ecosystem, offering a vast range of libraries and tools. SvelteKit's ecosystem is growing but is smaller in comparison.

#### Svelte
```
<script>
* let count = 0;

* function increment() {
* * count += 1;
* }
</script>

<button on:click={increment}>Increment</button>
<p>{count}</p>
```

##### Component Compilation
For each Svelte component, the compiler generates a self-contained JavaScript module. This module includes the component's logic, the code to generate its DOM structure, and the reactive code to update the DOM when the component's state changes. The compilation of each component is optimized as follows:
Static Analysis: The compiler analyzes the component code to identify static parts of the template that do not change. These parts are turned into highly efficient code that runs once during component initialization.
Reactive Declarations: Svelte tracks the dependencies of each reactive statement. If a state variable changes, only the components and DOM elements that depend on that variable are updated. This minimizes the amount of DOM manipulation required.
Event Handling: Event handlers are directly attached to DOM elements, avoiding the need for a virtual DOM diffing algorithm to determine event changes.
Scoped CSS: CSS in Svelte components is scoped to the component, reducing the overall size of the CSS and avoiding conflicts. The compiler ensures that only the necessary CSS is included and applied to components.

#### Optimization Across Components
When dealing with many components, Svelte's compiler optimizes the overall application as follows:
Tree Shaking: Unused code, including components, functions, or library imports, is removed during the build process. This ensures that the final bundle includes only the code that is actually used.
Code Splitting: For larger applications, Svelte supports code splitting, allowing different parts of the application to be loaded on demand. This reduces the initial load time by loading only the necessary code for the initial view.
Minification and Compression: The compiled code is minified, removing unnecessary characters, whitespace, and comments. Additionally, modern build tools can further compress the code for efficient delivery over the network.
Example: Optimizing Nested Components
```
// ParentComponent.svelte
<script>
* import ChildComponent from './ChildComponent.svelte';
* let parentState = 'Hello';
</script>

<ChildComponent {parentState} />

// ChildComponent.svelte
<script>
* export let parentState;
</script>

<p>{parentState}</p>
```
Dependency Tracking: The compiler sees that ChildComponent depends on parentState from ParentComponent. It generates code so that changes to parentState automatically update the <p> tag in ChildComponent, without rerendering the entire component tree.
No Virtual DOM: Since there's no virtual DOM, the update is direct and efficient, manipulating only the affected text node.

##### Nested Components
Component Instances: Each component is compiled into a JavaScript class or function that manages its instance, including creating, updating, and destroying it.
Reactivity: Svelte's reactivity system is baked into the compiled code, ensuring that changes to reactive state variables trigger updates to the DOM.
Encapsulation: Child components have their own scope and state, which are encapsulated and cannot be directly accessed by the parent or other components unless explicitly passed down as props.
Instantiation: The ParentComponent creates an instance of the ChildComponent, passing down parentState as a prop.
Mounting: Both components have a mount function that attaches their content to the DOM. For the child, it's creating and appending a paragraph element.
Updating: The update method in ChildComponent takes new props and updates its DOM elements if necessary. This mimics Svelte's reactivity system, where changes in props trigger updates.
Destruction: Both components include a destroy method for cleanup, removing event listeners, or detaching from the DOM.

##### Svelte Compiler and AST
Svelte is a compiler that converts Svelte components (written in a mix of HTML, CSS, and JavaScript) into highly efficient imperative code that updates the DOM when the state of the application changes. The Svelte compiler uses an AST to understand the structure of a Svelte component.
Parsing: The Svelte compiler parses the source code of a component into an AST, which represents the component's structure in a hierarchical, tree-like form. This includes HTML structure, script tags, style tags, and template logic.
Transformation: The AST allows the Svelte compiler to perform optimizations and transformations on the source code. It can statically analyze the code, identify reactive statements, and optimize bindings and event listeners.
Code Generation: Finally, based on the transformed AST, the Svelte compiler generates optimized JavaScript code. This code is what gets executed in the browser, creating a fast and efficient web application.

#### React vs Svelte
##### Performance and Efficiency
React: Utilizes a virtual DOM to optimize rendering by diffing against the previous state, which can improve performance for dynamic, high-traffic applications. However, this layer of abstraction may introduce overhead in terms of both performance and bundle size, which could be significant for an in-car system that demands high efficiency and responsiveness.
Svelte: Compiles down to highly optimized vanilla JavaScript at build time, eliminating the need for a virtual DOM. This results in faster initial load times and smoother runtime performance.

##### Development Experience and Learning Curve
React: Offers a rich ecosystem, extensive community support, and a wealth of libraries and tools. Its component-based architecture and JSX syntax have a steeper learning curve for beginners but provide powerful patterns for building complex applications.
Svelte: Boasts a simpler, more intuitive syntax and a smaller learning curve, making it easier to get started with. Svelte's compile-time magic does a lot of the heavy lifting, allowing developers to write less boilerplate code. This can expedite the development process, beneficial for rapidly iterating design concepts and prototypes.

##### Reactivity and State Management
React: Manages state using hooks (e.g., useState, useReducer) or external libraries like Redux for more complex state management scenarios. This explicit state management can provide fine-grained control over application state.
Svelte: Has a built-in reactivity model that automatically updates the UI when state changes, with less boilerplate than React. This makes state management simpler and more straightforward.

##### Ecosystem and Community Support
React: Has a vast ecosystem, with a wide range of libraries and tools for nearly every use case, including state management, routing, and form handling.
Svelte: While growing, Svelte's ecosystem is smaller compared to React's.

#### Memory Management
##### Summary
From an optimization point of view, understanding the trade-offs between Svelte and React involves considering how each framework's approach to UI updates and state management impacts memory usage and garbage collection. Svelte's compile-time optimizations generally lead to lower memory usage and less frequent garbage collections, while React's use of a virtual DOM requires careful management to minimize its memory footprint and the impact of frequent updates. Both frameworks can perform efficiently when used correctly, but understanding their underlying mechanisms and how they interact with the JavaScript engine's memory management is crucial for optimization.
##### Svelte Memory Implications
Lower Memory Footprint: Since Svelte eliminates the need for a virtual DOM and compiles to minimal code, it generally uses less memory. There's no need to keep a virtual representation of the UI in memory.
Efficient Updates: By generating code that directly manipulates the DOM based on state changes, Svelte minimizes the amount of memory churn. Memory churn is when applications frequently allocate and deallocate memory, which can lead to increased garbage collection and reduced performance.w
##### React Memory Implications
Higher Memory Usage: The virtual DOM requires additional memory to maintain a representation of the UI. This increases the memory footprint compared to more direct DOM manipulation strategies.
Garbage Collection: The process of re-rendering and diffing can lead to more frequent allocations and deallocations, potentially triggering garbage collection more often. This can impact performance, particularly in memory-constrained environments.

#### React and Svelte Reactivity Models
In summary, Svelte's compile-time reactivity model provides optimization and performance benefits through smaller bundle sizes and direct DOM updates, making it well-suited for applications where performance is critical. React, with its virtual DOM and runtime reactivity model, offers a flexible and powerful way to build complex applications, with optimizations like concurrent mode aimed at improving performance in scenarios with intensive and complex UI updates.

#### Compile-time vs Run-time Reactivity
##### Comparative Analysis
Performance: Compile-time reactivity can offer superior performance for certain types of applications, particularly those requiring frequent, granular updates to the UI. Run-time reactivity, with its virtual DOM, can be more efficient for applications with complex UIs where optimizing the number of DOM manipulations is crucial.
Use Cases: Compile-time reactivity is well-suited for applications where bundle size and direct DOM update performance are critical. Run-time reactivity is advantageous in applications that benefit from React's ecosystem, developer tools, and the flexibility of the virtual DOM.
Learning Curve and Complexity: Svelte's compile-time approach may have a simpler mental model for reactivity, as it more closely resembles vanilla JavaScript with some reactivity extensions. React's run-time model, while potentially more complex due to the virtual DOM and lifecycle methods, benefits from extensive documentation, community support, and familiarity among web developers.

##### Compile-time Reactivity
Definition: Compile-time reactivity refers to a framework or compiler's ability to analyze and prepare reactive dependencies and updates during the build process, before the application is loaded in the browser.
How It Works in Svelte:
* In Svelte, the compiler looks at the component code and identifies reactive statements and variables. It then generates the minimal JavaScript code necessary to update the DOM when state changes occur.
* This process transforms your declarative component code into imperative code that directly manipulates the DOM without an intermediate representation (like the virtual DOM used in React).
* Because the reactivity is resolved at compile time, the runtime code is highly optimized for performance. It directly updates only the parts of the DOM that depend on changed state, leading to faster updates and less memory usage.
Advantages:
* Optimized Bundle Size: Since the compiler only includes code necessary for the detected reactivity patterns, the final bundle size can be significantly smaller.
* Performance: Direct DOM updates avoid the overhead of diffing and patching a virtual DOM, resulting in faster render times and smoother animations.
* Efficiency: Lower memory footprint, as there's no need to maintain a virtual DOM or reactivity system at runtime.

##### Run-time Reactivity
Definition: Run-time reactivity involves managing state changes and UI updates during the application's execution in the browser. The framework uses a virtual DOM or other abstractions to track changes and update the UI reactively.
How It Works in React:
* React maintains a virtual representation of the UI (the virtual DOM). When state changes, React creates a new virtual DOM tree, compares it with the previous one (diffing), and calculates the minimal set of changes needed to update the actual DOM (patching).
* This process allows React to batch updates efficiently and minimize direct DOM manipulations, which can be performance-intensive.
Advantages:
* Flexibility: The virtual DOM abstraction allows for powerful patterns like conditional rendering and components that automatically update based on state changes, without directly manipulating the DOM.
* Batched Updates: React can batch multiple state updates into a single DOM update cycle, improving performance for complex updates.
* Developer Experience: The declarative nature of React, along with its component-based architecture, provides a consistent and scalable way to build applications.

#### React.js

##### React Component Lifecycle:
React components have distinct lifecycle phases: mounting, updating, and unmounting. Key methods include constructor(), render(), componentDidMount(), shouldComponentUpdate(), getSnapshotBeforeUpdate(), componentDidUpdate(), and componentWillUnmount(). From React 16.3, lifecycle methods evolved to include getDerivedStateFromProps and getSnapshotBeforeUpdate for safer side-effects and state updates.

##### Hooks and Functional Components:
Functional components offer simplicity and better performance. useEffect is for side effects post-render, while useLayoutEffect is for synchronously executing DOM mutations. Custom hooks allow reusing stateful logic between components, enhancing code modularity and readability.

##### State Management:
Local state is managed within components, while global state is handled using Context API or libraries like Redux or MobX. The choice depends on the application's complexity, with Redux providing a more structured approach with middlewares and predictable state management, while Context API is simpler for light-weight applications.

##### Performance Optimization:
Optimize performance by minimizing re-renders through memoization, PureComponent, React.memo, and shouldComponentUpdate. Understanding React's virtual DOM helps in optimizing updates, and immutability ensures predictable state transitions, optimizing component rendering.

##### Advanced Patterns and Techniques:
HOCs enhance component functionality without modifying their structure, while render props share code between components using a prop whose value is a function. Error boundaries catch JavaScript errors in child components, preventing the entire app from crashing. Fragments group a list of children without adding extra nodes, and portals render components into a different DOM subtree.

##### React Internals and Principles:
The reconciliation algorithm compares current and new virtual DOMs to update the browser’s DOM efficiently. React Fiber is an overhaul of React's core algorithm, enabling incremental rendering of the component tree for better performance in complex applications.

##### Type Checking and TypeScript:
PropTypes provides runtime type checking; TypeScript offers static type checking, enhancing code robustness and maintainability. TypeScript’s advanced types like generics and unions help in building more flexible and reusable components.

##### Security in React:
Common vulnerabilities include XSS, where attackers inject malicious scripts. Mitigate these by sanitizing user input, validating content, and using React’s built-in escaping to prevent the injection of any unwanted scripts.

##### Testing and Debugging:
Effective testing includes unit, integration, and end-to-end tests, using tools like Jest and React Testing Library. Debugging can be done using React Developer Tools, which provides insights into the component tree, props, state, and hooks.

##### Next.js/SSR:
SSR improves performance and SEO by sending rendered HTML to the client, speeding up initial load times and ensuring content is crawlable by search engines. SSG pre-renders pages at build time, which is beneficial for static sites with no dynamic data dependencies.

##### Reconciliation Algorithm
The reconciliation algorithm is a fundamental concept within React that enables efficient updates to the UI. Here's a more detailed look:
* Virtual DOM: React maintains a lightweight representation of the actual DOM in memory, known as the virtual DOM. When a component’s state changes, React updates this virtual representation.
* Diffing Algorithm: The reconciliation process uses a diffing algorithm to compare the new virtual DOM with the previous one. It identifies what has changed between the two versions.
* Update Efficiently: Based on the differences, React calculates the most efficient way to update the browser’s DOM. Instead of updating the entire DOM every time, it only makes changes to the parts that actually changed.
* Batching and Updating: React batches multiple updates together for better performance, leading to fewer re-renders and quicker UI updates. This is crucial for maintaining high performance in complex applications.

##### React Fiber
React Fiber represents a complete rewrite of React's core reconciliation algorithm. Introduced in React 16, Fiber provides several enhancements over the old reconciliation engine:
* Incremental Rendering: One of the key features of Fiber is its ability to split rendering work into chunks and spread it out over multiple frames. This incremental rendering feature allows the main thread to stay responsive, improving the user experience in complex applications.
* Prioritization of Updates: Fiber can assign priority to different types of updates. For instance, animations and transitions can have higher priority compared to a data fetch update. This ensures that high-priority updates are not blocked by lower-priority work.
* Pause and Resume: The Fiber architecture can pause work on a lower-priority update and switch to a more urgent update if needed. After the higher-priority work is complete, it can resume the paused work.
* Error Handling: Fiber introduces improved mechanisms for error boundaries. Error boundaries are React components that catch JavaScript errors anywhere in their child component tree, log those errors, and display a fallback UI instead of the component tree that crashed.

##### React Compiler
React's introduction of a new compiler that aligns with approaches similar to Svelte marks a significant evolution in its development paradigm. While React traditionally relies on a runtime library to create and manage the virtual DOM, Svelte shifts this workload to compile time, generating highly optimized vanilla JavaScript that updates the DOM directly. This approach reduces the overhead and improves runtime performance, as there's no virtual DOM diffing required, and updates are surgically applied to the DOM.

React's exploration into a compiler-centric approach suggests a move towards embracing some of these compile-time optimizations. This could mean that React might generate more efficient code upfront, reducing the runtime work needed to manage and update the DOM, thereby improving performance, especially for large and complex applications.

##### The useOptimistic Hook
The useOptimistic hook is a concept that seems to draw inspiration from the realm of optimistic updates, a strategy often employed in modern web development to enhance user experiences. Optimistic updates assume that an operation (like a network request) will succeed and immediately reflect this success in the UI, rolling back the changes if the operation fails. This approach makes applications feel faster and more responsive, as users see instant feedback rather than waiting for the roundtrip of the request.

##### Higher-Order Components (HOCs)
HOCs are a pattern in React for reusing component logic. An HOC is a function that takes a component and returns a new component with additional props or functionality. Here's an example to illustrate how an HOC can be used to add additional functionality — for instance, to add user authentication logic to a component:
Step 1: Define the Higher-Order Component
```
import React from 'react';
import { Redirect } from 'react-router-dom'; // Assuming you're using react-router for navigation

// This is the HOC that checks for authentication
const withAuthentication = WrappedComponent => {
* return class extends React.Component {
* * render() {
* * * const isAuthenticated = /### logic to check if the user is authenticated */;

* * * if (!isAuthenticated) {
* * * * // Redirect to login page if not authenticated
* * * * return <Redirect to="/login" />;
* * * }

* * * // Render the wrapped component with all its props if authenticated
* * * return <WrappedComponent {...this.props} />;
* * }
* };
};
```
Step 2: Use the HOC
```
import React from 'react';

class Dashboard extends React.Component {
* render() {
* * // Dashboard component logic
* * return <div>Welcome to the Dashboard!</div>;
* }
}

// Wrap Dashboard with the withAuthentication HOC
const AuthenticatedDashboard = withAuthentication(Dashboard);

export default AuthenticatedDashboard;
```
##### useState vs useReducer
Summary:
* useState is best for simple states and straightforward updates.
* * useReducer shines in more complex scenarios where state logic benefits from being organized in a reducer function for clarity, maintainability, and predictability.
Use useState when:
* State is simple and independent: Ideal for simple pieces of state that don't depend on each other. For example, toggling a boolean flag, setting a string or a number.
* Updates are straightforward: When state updates are simple and can be done with a single call to setState without needing previous state or complex logic.
* Low complexity: For managing a single or a few unrelated pieces of state within a component.
Use useReducer when:
* Complex state logic: When you have complex state logic that involves multiple sub-values or when managing tightly coupled states where one state update might depend on another.
* State transitions are complex: For scenarios where the next state depends intricately on the previous one, making it beneficial to centralize state transition logic in one place.
* Related state actions: When dealing with multiple actions that affect the state in various ways, encapsulating these actions in a reducer function makes the component's state management more predictable and maintainable.
* Shared state logic: If the same state logic needs to be reused across multiple components, useReducer can make this easier, especially when combined with context.

##### Redux vs Context API
Summary
* Use Redux when dealing with complex state interactions, requiring middleware for side effects, needing robust debugging tools, or managing large-scale applications.
* Use the Context API for simpler global state management, to avoid prop drilling, and when working within smaller applications or alongside hooks for cleaner code.
When to Use Redux
* Complex State Logic: Redux is well-suited for managing complex state logic that involves multiple reducers, or when the state is heavily interdependent and needs to be accessed by many components at different nesting levels.
* Global State: For applications with a global state that needs to be shared across many components, Redux provides a centralized store that makes it easier to manage and debug state changes.
* Middleware and Side Effects: Redux's ecosystem includes powerful middleware, like Redux Thunk and Redux Saga, which are great for handling side effects such as asynchronous API calls.
* DevTools and Debugging: Redux comes with excellent dev tools for time-travel debugging, state inspection, and action replay, which can be invaluable for complex applications.
* Large-Scale Applications: For large-scale applications with complex data flows and many user interactions, Redux's predictability and structured state management can be very beneficial.
When to Use the Context API
* Simple Global State: For applications with a relatively simple global state that a few components need to access or modify, the Context API is a simpler and more straightforward choice.
* Avoid Prop Drilling: When you have deeply nested components and you want to avoid passing props through multiple levels of components, Context provides a way to share values directly with the components that need them.
* Use with Hooks: The Context API is often used in conjunction with the useContext hook to make it easier to access context values in functional components.
* Lightweight State Management: For smaller applications or when you're managing state that doesn't require the complexities of middleware or extensive debugging tools, the Context API offers a lightweight solution without the need for additional libraries.

##### Controlled Components
A controlled component is one where React controls the form data. In this scenario, the state of the form element is handled by React state, and every state mutation will have an associated handler function. This means:
* State Control: The value of the input is controlled by React state. For example, you would use useState to manage the form element's value.
* Data Flow: You explicitly set the value of the form element using React state (e.g., value={this.state.value}), making the React state the "single source of truth."
* Change Handling: You handle changes using a callback function that React calls in response to state changes (usually via onChange), which updates the React state with the new value.

#### Uncontrolled Components
An uncontrolled component works more like traditional HTML form elements. The form data is handled by the DOM itself, not by the React component state. Here's what characterizes an uncontrolled component:
* DOM as Source of Truth: The data for the form element is stored in the DOM, not in the component state. The component reacts to the data as needed but does not control it.
* Refs for Access: You typically use refs to access the DOM elements directly and retrieve their values when needed, rather than storing their values in state.
* Less Boilerplate: There’s less React code involved in managing the state and changes of form elements, which can simplify your component code for certain forms.

#### Denounce Input Fields
The concept of "denouncing" input fields might be a misunderstanding or typo, often confused with "debouncing." Debouncing is a technique used to limit the rate at which a function is executed. In the context of input fields, debouncing is valuable because it ensures that state updates (or other expensive operations) don't fire on every keystroke, but rather after a certain amount of inactivity or delay. This can be particularly useful in a controlled component where you might want to validate user input or run an autocomplete functionality based on user input but want to minimize the number of invocations for performance reasons.


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


