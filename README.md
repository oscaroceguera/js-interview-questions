# JavaScript interview questions

## The Question

1. [Difference between undefined and null](#difference-between-undefined-and-null)
2. [DOM](#dom)
3. [Event Propagation](#event-propagation)
4. [Difference between event preventDefault and stopPropagation](#difference-between-event-preventDefault-and-stopPropagation)
5. [Event target](#event-target)
6. [Difference between abstract and strict equality](#difference-between-abstract-and-strict-equality)
7. [Hoisting](#hoisting)
8. [Scope](#scope)
9. [Closures](#closures)
10. [This](#this

### Difference between undefined and null

`undefined` is the default value of a variable that has not been assigned a specific value.

`null` is a **value that represent no value**. It's a valuethat has been **explicitly** defined to a variabe.

### DOM

**Document Object Model** is an interface (API) for HTML and XML documents. When the browser first redas our HTML document it creates a biig object, a really big oobject baased on the HTML document it creates a biig object.

The `document` object in **JavaScript** represents the DOM. It provides us many methods that we can use to selecting elements to update element conotents and many more.

### Event propagation

When an **event** occours on a **DOM** element, tht **event** does not entirely occur on that just one element. In the Bubbling Phase, the event bubbles up or it goes to its parent, to its grandparents, to its grandparent's parent util it reaches all the way to the `window` whle in the capturing phase the event starts from the `window` down too the element that triggered the event or the `event.target`.

Event propagations has 3 phases:

1. **Capturing** - the event starts from `window` then goes down to every element util it reaches the target element.
2. **Target** - the event has reached the target element
3. **Bubbling** - The event bubbles up from the target element then goes up every element until it reaches the `window`

### Difference between event preventDefault and stopPropagation

`event.preventDefault()` method prevents the default behavior of an element. If used in a from element it prevents it from submiting.

`event.stopPropagation()` method stops the propagation of an event or it stopos the event from occurring in the bubbling or ccapturing phase.

### Event target

`event.target` is the element on which the event occurred or the element that triggered the event.

### Difference between abstract and strict equality

the difference between `==` **(abstract equality)** and `===` **(strict equality)** is that the `==` compares by value afeter coercin and `===` compares by **value** and **type** without coerccion.

### Hoisting

Is the term used to describe the moving of variables and functions to the top of their (global or function) scope on where we define that variable or function.

The **Execution Context** is the "enviroment of code" that is currently executing and has two pahses **compilation** and **execution**.

**Compilation** - in this phase it gets all the function declarations and hoists them up to the toop of theiir scope so we can reference them later and gets all variables declaration (declare with the var keyword) and aalso hoists them up and give a default of undefined.

**Execution** - in this phase it assigns values to the variables hoisted earlier and it executes or invookes functions (methods in objects).

**NOTE:** only **function declarations** and variables declared with the `var` keyword are hoisted not **funcction expressions** or **arrow functions**, `let` and `const` keyword.

### Scope

Is the area where we have valid access to variables or functions. Js has three types of Scopes. **Global Scope, Function Scope** and **Block Scope(ES6)**

**Global Scope** - variables or functionos declared in the global namespace are in the global scope and therefore is accessible weverywhere in our code.

**Function Scope** - varibales, functions and parameters declared within a function are accesible inside that function but not outside of it.

**Block Scope** - variables **(let, const)** declared within a block `{}` can only be access within it.

### Closures

Closures is simply the ability of a function at the time of declaration to remember the references of variables and parameters on its current scope, on its parent's parent functioon scope until it reaches the global scope with the help of **Scope Chain**. Basically it's the Scope created when the funciton was declared.
