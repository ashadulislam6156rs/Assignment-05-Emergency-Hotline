### 6. Answer the following questions clearly:

1. What is the difference between **getElementById, getElementsByClassName, and querySelector / querySelectorAll**? <br>
#### Answer:<br>
| Method                        | By returning     | Selector type | Use                                 |
|-------------------------------|------------------|---------------|-------------------------------------|
| getElementById("id")          | Single element   | id            | To capture a specific element       |
| getElementsByClassName("class") | HTMLCollection  | class         | To capture multiple elements        |
| querySelector("cssSelector")  | Single element   | CSS selector  | To catch the first matching element |
| querySelectorAll("cssSelector") | NodeList        | CSS selector  | To catch all matching elements      |
   
2. How do you **create and insert a new element into the DOM**?
#### Answer:<br>
// Initial DOM      

<div id="myName"></div>  
// Create a new element 
let newElement = document.createElement("p");
 // Set content 
newElement.innerText = "My Name is Ashadul islam"; 
 // Select the DOM parent element 
let myName = document.getElementById("myName"); 
 // Inserting into the DOM 
myName.appendChild(newElement);  

3. What is **Event Bubbling** and how does it work?
#### Answer:<br>
Event Bubbling is a process where an event starts from the innermost element and propagates step by step up to its parent to grandparent then the entire DOM tree.

//Then  Initial DOM
<div id="parent"><button id="child">Click Me</button></div> 

//Parent Element

document.getElementById("parent").addEventListener("click", () => {
  console.log("Parent div clicked");
});

//Child Element

document.getElementById("child").addEventListener("click", () => {
  console.log("Child button clicked");
});

### Output:

Child button clicked

Parent div clicked

Here you can see that the event first started from the child button then bubbled up and went to the parent div.

4. What is **Event Delegation** in JavaScript? Why is it useful?
#### Answer:<br>
Event Delegation is a JavaScript technique where, instead of having separate event listeners for many child elements, an event listener is placed on a parent element.
The event is then passed to the parent using event bubbling, and the parent is identified to a specific child.

-Performance is better
-Dynamic elements can be handled
-Clean code & less memory usage

6. What is the difference between **preventDefault() and stopPropagation()** methods?
| Method                | Purpose                                        | Example Use Case                        |
|-----------------------|-----------------------------------------------|----------------------------------------|
| `preventDefault()`    | Stop default browser action                   | Form submit, link click                 |
| `stopPropagation()`   | Stop event from bubbling or capturing        | Nested elements event handling control |


