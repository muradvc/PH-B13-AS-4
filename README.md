
## Answers to Questions

### 1. What is the difference between getElementById, getElementsByClassName, and querySelector / querySelectorAll?

ANS: getElementById() – Selects an element by its id and returns a single element. We use it when we want to target one specifiq element.

getElementsByClassName() – Select elements by their class name and returns multiple elements. If several elements share the same class, it will return all of them.

querySelector() – Uses a CSS selector to select elements, but it always returns only the first matching element, even if multiple elements match the selector.

querySelectorAll() – Uses a CSS selector to select elements and returns all matching elements. It will return as many elements as match the selector.


### 2. How do you create and insert a new element into the DOM?
ANS:To create a new element in dom,we can use document.createElement() method.Then we can add text,class,id,anotber attributes.example : innerText,innerHtml etc.but this elements no visible on our webpage.if we want to visible this elements in our webpage we use appen(),appendChild(),insertBefore to insert element into the dom.After It's visible on our webpage



### 3. What is Event Bubbling? And how does it work?
ANS: Event Bubbling is a behavior in JavaScript. When a event occurs at a specific element, the event starts from that element and then gradually moves upward to its parent element.
For example, if we click on a button, not only the button’s event is triggered, but the event can also trigger on its parent div, then on the body, and finally on the document.



### 4. What is Event Delegation in JavaScript? Why is it useful?
ANS:Event Delegation is a method in JavaScript where instead of adding separate event listeners to many child elements, we add only one event listener to their parent element. It works because of Event Bubbling.When an event happens on a child element, the event moves upward to the parent element. Then the parent element can handle that event.
For example, if there are many buttons inside a div, instead of adding a click event to each button, we can add one click event to the div. When we click any button, the event bubbles up to the div, and the div can understand which button was clicked.

### 5. What is the difference between preventDefault() and stopPropagation() methods?
ANS:preventDefault() stops the browser’s default behavior. If we use it, then those default actions will be stopped.

stopPropagation() prevents the event from going to the upper parent element. That means it stops event bubbling.

If a button’s parent div also has an event, then if we use stopPropagation(), clicking the button will not trigger the event on the parent.