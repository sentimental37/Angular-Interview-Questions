* How can you add an active class to a selected element in a list component?

*routerLinkActive*
This directive lets you add a CSS class to an element when the link's route becomes active.

Consider the following example:

`<a routerLink="/user/bob" routerLinkActive="active-link">Bob</a>`

When the url is either '/user' or '/user/bob', the active-link class will be added to the a tag. If the url changes, the class will be removed.

You can set more than one class, as follows:


`<a routerLink="/user/bob" routerLinkActive="class1 class2">Bob</a>`

`<a routerLink="/user/bob" [routerLinkActive]="['class1', 'class2']">Bob</a>`

You can configure RouterLinkActive by passing exact: true. This will add the classes only when the url matches the link exactly.



`<a routerLink="/user/bob" routerLinkActive="active-link" [routerLinkActiveOptions]="{exact:true}">Bob</a>`


* What is a template variable. How would you use it?
* What is the difference of using a property binding verses a function binding on a template?
* What happens if you subscribe to a data source multiple times with async pipe?
* what is the difference between ng-content, ng-container and ng- template?
* When you create a data-binding in Angular, are you working with attributes or properties? What is the difference anyway?

n the world of Angular, the only role of attributes is to initialize element and directive state. When you write a data binding, you're dealing exclusively with properties and events of the target object. 
HTML attributes effectively disappear. [Read more](https://next.angular.io/guide/template-syntax#html-attribute-vs-dom-property)

 * When can you omit the brackets in template binding?

You should omit the brackets when all of the following are true:

The target property accepts a string value.
The string is a fixed value that you can bake into the template.
This initial value never changes.

[Read more](https://next.angular.io/guide/template-syntax#one-time-string-initialization)
