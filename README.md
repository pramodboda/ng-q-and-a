## ng  Questions and Answers

### What is the difference between Angular and jQuery?
| Features | jQuery | Angular |
|--|--|--|
| **DOM Manipulation** | Yes | Yes |
| **RESTful API** | NO | Yes |
| **Animation Support** | Yes | Yes |
| **Deep Linking Routing** | No | Yes |
| **Form Validation** | No | Yes |
| **2 Way Data Binding** | No | Yes |
| **AJAX/ JSONP** | Yes | Yes |

## Name the key features of Angular?

The key features of Angular are:
- Scope
- Controller
- Model
- View
- Services 
- Data Binding
- Directives
- Filters
- Testable

## Explain data binding in Angular

- According to AngularJS.org, "Data-binding in Angular apps is the automatic synchronization of data between the model and view components. The way that Angular implements data-binding lets you treat the model as the single-source-of-truth in your application. The view is a projection of the model at all times. When the model changes, the view reflects the change and vice versa."
- There are two ways of data binding:
1. Data mining in classical template systems.
2. Data binding in angular templates.

## What are directives in Angular

- A core feature of Angular, directives are attributes that allows you to invent new HTML syntax, specific to your application. They are essentially functions that execute when the Angular compiler finds them in the DOM.
- Some of the most commonly used directives are `ng-app`, `ng-controller` and `ng-repeat`. 
- The different types of directives are: 
	 - Element directives.
	 - Attribute directives.
	 - CSS class directives.
	 - Comment directives.

## What are controllers in Angular?

- Controllers are JavaScript functions which provide data and logic to HTML UI. As the name suggests, 
- They control how data flows from the server to HTML UI. 

## What is Angular Expression? How do you differentiate between Angular expressions and JavaScript expressions?   

- Angular expressions are code snippets that are usually placed in binding such as `{{expression}}`similar to JavaScript.

- The main differences between Angular expression and JavaScript expression are:

|  | **Angular** | **JavaScript** |
|--|--|--|
|  **Context** | The expression are evaluted against a `scope object` in Angular. | while JavaScript expression are evaluated against the `global window`. |
| **Forgiving** | In Angular expression, the evaluation is forgiving to `null` and `undefined`.   | whereas in JavaScript `undefined` properties generate `TypeError` or `ReferenceError`. |
| **No Control Flow Statements** | We cannot use loops, conditionals or exceptions in an Angular expression. |  |
| **Filters** | In Angular, unlike JavaScript, we can use filters to format data before displaying it. |  | 

## What is the different between `link` and `compile` in Angular
- `Compile` function is used for template DOM Manipulation and to collect all the directives.
- `Link` function is used for registering DOM listeners as well as instances DOM manipulation and is executed once the template has been cloned.


## What are the characteristics of 	`scope`

- Scope is an object that refers to the application model. It is an execution context for expressions.
- Scopes are arranged in hierarchical structure which mimic the DOM structure of the application. 
- Scope can watch expressions and propagate events. 
- The characteristics of Scope are:
	- Scope provide APIs ($watch) to observe model mutations.
	- Scope provide APIs ($apply) to propagate any model changes through the system into the view from outside of the "Angular realm" (controllers, services, Angular event handlers).
	- Scope can be nested to limit access to the properties of application components while providing access to shared model properties. Nested scopes are either "child scopes" or "isolate scope". A "child scope"(prototypically) inherits properties from its parent scope. An "isolate scope" dose not.
	- Scope provide context against which expressions are evaluated. For example `{{username}}` expression is meaningless, unless it is evaluated against a specific scope which deines the `username` property.

## What are the advantages of using Angular framework

Angular frameworks has the following advantages:
- Supports two way data-binding.
- Supports MVC pattern.
- Supports static template and angular template.
- Can add custom directives
- Suppoe
<!--stackedit_data:
eyJoaXN0b3J5IjpbMzY5NDg0ODIzLDYwMzM2OTkxNiwtMTA4MD
E4MDY3NCwtNzk3ODczMDY2LDIyOTc0NTM4NywtODExMDkzNzQz
LDE1MzM4OTU1MDhdfQ==
-->