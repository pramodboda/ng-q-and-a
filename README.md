## ng  Questions and Answers

### What is the difference between Angular and jQuery?
| Features | jQuery | Angular |
|--|--|--|
| **DOM Manipulation** | Yes | Yes |
| **RESTful API** | No | Yes |
| **Animation Support** | Yes | Yes |
| **Deep Linking Routing** | No | Yes |
| **Form Validation** | No | Yes |
| **2 Way Data Binding** | No | Yes |
| **AJAX/ JSONP** | Yes | Yes |

### Name the key features of Angular?
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

### Explain data binding in Angular?

- According to AngularJS.org, "Data-binding in Angular apps is the automatic synchronization of data between the model and view components. The way that Angular implements data-binding lets you treat the model as the single-source-of-truth in your application. The view is a projection of the model at all times. When the model changes, the view reflects the change and vice versa."
- There are two ways of data binding:
1. Data mining in classical template systems.
2. Data binding in angular templates.

### What are directives in Angular?

- A core feature of Angular, directives are attributes that allows you to invent new HTML syntax, specific to your application. They are essentially functions that execute when the Angular compiler finds them in the DOM.
- Some of the most commonly used directives are `ng-app`, `ng-controller` and `ng-repeat`. 
- The different types of directives are: 
	 - Element directives.
	 - Attribute directives.
	 - CSS class directives.
	 - Comment directives.

### What are controllers in Angular?

- Controllers are JavaScript functions which provide data and logic to HTML UI. 
- As the name suggests, They control how data flows from the server to HTML UI. 

### What is Angular Expression? How do you differentiate between Angular expressions and JavaScript expressions?   

- Angular expressions are code snippets that are usually placed in binding such as `{{expression}}` similar to JavaScript.

- The main differences between Angular expression and JavaScript expression are:

|  | **Angular** | **JavaScript** |
|--|--|--|
|  **Context** | The expression are evaluted against a `scope object` in Angular. | while JavaScript expression are evaluated against the `global window`. |
| **Forgiving** | In Angular expression, the evaluation is forgiving to `null` and `undefined`.   | whereas in JavaScript `undefined` properties generate `TypeError` or `ReferenceError`. |
| **No Control Flow Statements** | We cannot use loops, conditionals or exceptions in an Angular expression. |  |
| **Filters** | In Angular, unlike JavaScript, we can use filters to format data before displaying it. |  | 

### What is the different between `link` and `compile` in Angular?
- `Compile` function is used for template DOM Manipulation and to collect all the directives.
- `Link` function is used for registering DOM listeners as well as instances DOM manipulation and is executed once the template has been cloned.


### What are the characteristics of  `scope`?

- Scope is an object that refers to the application model. It is an execution context for expressions.
- Scopes are arranged in hierarchical structure which mimic the DOM structure of the application. 
- Scope can watch expressions and propagate events. 
- The characteristics of Scope are:
	- Scope provide APIs ($watch) to observe model mutations.
	- Scope provide APIs ($apply) to propagate any model changes through the system into the view from outside of the "Angular realm" (controllers, services, Angular event handlers).
	- Scope can be nested to limit access to the properties of application components while providing access to shared model properties. Nested scopes are either "child scopes" or "isolate scope". A "child scope"(prototypically) inherits properties from its parent scope. An "isolate scope" dose not.
	- Scope provide context against which expressions are evaluated. For example `{{username}}` expression is meaningless, unless it is evaluated against a specific scope which deines the `username` property.

### What are the advantages of using Angular framework?

Angular frameworks has the following advantages:
- Supports two way data-binding.
- Supports MVC pattern.
- Supports static template and angular template.
- Can add custom directives.
- Supports RESTful services.
- Supports form validations. 
- Supports dependency injection.
- Applying Animations.
- Event Handlers.

### Explain what is injector in Angular?

An `injector` is a service locator, used to retrieve object instance as defined by provider, instantiate types, invoke methods, and load modules.

### What is factory method in Angular?
Factory method is used for creating a directive. It is invoked when the compiler matches the directive for the first time. We can invoke the factory method using `$injector.invoke`.

Syntax: `module.factory('factoryName', function);`

Results: When declaring factoryName as an injectable argument you will be provided with the value that is returned by invoking the function reference passed to module.factory.

### What is `ng-app`, `ng-init`, and `ng-model`?

- `ng-app`: Initializes application.
- `ng-model`: Binds HTML controls to application data.
- `ng-Controller`: Attaches a controller class to view.
- `ng-repeat`: Bind repeated data HTML elements. Its like a for loop.
- `ng-if` Bind HTML elements with condition.
- `ng-show`: Used to show the HTML elements.
- `ng-hide`: Used to hide the HTML elements.
- `ng-class`: Used to assign CSS class.
- `ng-src`: Used to pass the URL image etc.

### Does Angular use the jQuery library?

Yes, Angular can use jQuery if it's present in the app when the application is being bootstrapped. 
- If jQuery is not present in the script path, Angular falls back to its own implementation of the subset of jQuery that we call jQLite.

### Can Angular have multiple `ng-app` directives in a single page?

No. Only one Angular application can be auto-bootstrapped per HTML document.
- The first `ngApp` found in the document will be used to define the root element to auto-bootstrap as an application. 
- If another `ng-app` directive has been placed then it will not be processed by Angular and we will need to manually bootstrap the second app, instead of using second `ng-app` directive.

### Can Angular applications(ng-app) be nested within each other?

No. Angular applications cannot be nested within each other.

### What is internationalization and how to implement it in Angular?
Internationalization is a way in which you can show locale specific information on a website. 
- Angular supports inbuilt internalization for three types of filters: currency, date and numbers. 
- To implement internalization, we only need to incorporate corresponding js according to locale of the country. By default it handles the locale of the browser.

### On which types of component can we create a custom directive?
Angular provides support to create custom directives for the following:
- **Element directives** - Directive activates when a matching element is encountered.
- **Attribute** - Directive activates when a matching attribute is encountered.
- **CSS** - Directive activates when a matching css style is encountered.
- **Comment** - Directive activates when a matching comment is encountered.
### What is `$rootscope` in Angular?
- Every application has a single root scope.
- All other scopes are descendant scopes of the root scope.
- Scopes provide separation between the `model` and the `view`, via a mechanism for watching the model for changes.
- They also provide event emission/ broadcast and subscription facility.

### Can we have nested controllers in Angular?
Yes, we can create nested `controllers` in Angular. Nested `controllers` are defined in hierarchical manner while using in `view`.

### What is bootstrapping in Angular?
Bootstrapping in Angular is nothing but initializing, or starting the Angular app. Angular supports automatic and manual bootstrapping.
- **Automatic Bootstrapping:** this is done by adding `ng-app` directive to the root of the application, typically on the tag or tag if you want angular to bootstrap your application automatically. When angular finds `ng-app` directive, it loads the module associated with it and then compiles the DOM.
- **Manual Bootstrapping:** Manual bootstrapping provides you more control on how and when to initialize your angular app. It is useful where you want to perform any other operation before Angular wakes up and compile the page.

### What does SPA (Single Page Application) mean? How can we implement SPA with Angular?

- Single Page Application (SPAs) are web apps that load a single HTML page and dynamically update that page as the user interacts with the app.
- In an SPA the page never reloads, though parts of the page may refresh. This reduces the round trips to the server to a minimum.
- It's a concept where we create a single shell page or master page and load the web-pages inside that master page instead of loading pages from the server by doing post backs. We can implement SPA with Angular using Angular `routes`. 

### Why Angular?
Angular lets us extend HTML vocabulary for our application resulting in an expressive, readable, and quick to develop environment. Some of the advantages are:

- MVC implementation is done right.
- It extends HTML using directives, expression and data binding techniques to define a powerful HTML template.
- Two way data-binding, form validations, routing supports, inbuilt services.
- REST friendly.
- Dependency injection support.
- It helps you to structure and test your JavaScript code.

### Is Angular compatible with all browsers?
Yes Angular is compatible with the following browsers: Safari, Chrome, Firefox, Opera 15, IE9 and mobile browsers(Android, Chrome Mobile, iOS Safari).

### How to implement routing in Angular? 
It is a five-step process:
- Step1: - Add the `angular-route.js` file to your view.
- Step2: - Inject `ngroute` functionality while creating Angular app object.
- Step3: - Configure the route provider.
- Step4: - Define hyperlinks.
- Step5: - Define sections where to load the `view`.

### Explain `$q` service, `deferred` and `promises`.

- `promises` are post logic's which are executed after some operation/ action is completed whereas `deferred` is used to control how and when those promise logic's will execute.
- We can think about `promises` as "WHAT" we want to fire after an operation is completed while `deferred` controls "WHEN" and "HOW" those promises will execute.
- `$q` is the angular service which provides `promises` and `deferred` functionality.
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTEyNTAzMzI2NTYsMjAzNjc0MTkwNiwxNz
Y3MDc5OTYwLDQyODI5MTM4OCwyMjYyNjMzMjAsLTU0MjkyMzI0
MiwtNDEzMTM3MDMwLC0zNDc0OTMxMTAsNjc1MTMzNzQ5LDE2Mz
UxMDU4MjEsLTkzMDUzMjQ2Myw2MzUwNTg3NTAsNjMwNjcxMjY0
LDYwODc2ODI4MywtMjA3MDI1NjE1MCw2MDMzNjk5MTYsLTEwOD
AxODA2NzQsLTc5Nzg3MzA2NiwyMjk3NDUzODcsLTgxMTA5Mzc0
M119
-->