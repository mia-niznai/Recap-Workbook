# Programming Basics questions #

## Data basics ##


:question: **1. What are the differences between objects and arrays? What is the purpose of the object and what is the purpose of the array?**

* [x] arrays store data in a single variable, whistl objects store anything with characteristics (properties);                         

* [x] an array is a list of primitives data types (string, number, integer, float, boolean, undefined, null) stored between \[ \], whilst an object can be any kind of data (including arrays in JavaScript) with a key and a value, stored between \{ \};

* [x] you can acces an array's element by its index, whistl the properties of an object can be called by using dot notation and \[\] notation;

* [x] you can add or remove items of an array by using methods (such as: .pop(), .push(), .unshift(), .slice(), etc.), whilst when working with an object you have to acces the keys and values in order to add, remove or modify them;

* [x] you can delete key.value for an object to delete a property, but if you use *delete arr[num]* to delete an array's index you will only get undefined because in this case *delete* only replaces the value with undefined;

___

:question: **2. How can you access a key's value in an object?**

* if you wish to access a certain value of a certain key, there are more ways:
:black_nib:
    * `objectName.propertyName`;
    * `objectName["propertyName"]`;
    
* also, you can acces all keys' values of an object by using Object.values(obj);

___

-:question: **3. How can you access the first and the last item of an array?**

* first element of an array is the element with the index 0: arr[0]. Here's an example of how to get it:
:black_nib:
      *  `const firstItem = arr[0]`;
         `console.log(firstItem)`;

* last element of an array is: `arr[arr.length - 1]`. One way to get it is this:
:black_nib:
       * `const lastItem = arr[arr.length - 1]`;
        `console.log(lastItem)`; 
        
___

:question: **4. Name all the primitive types in JavaScript.**
    
    The primitive types in JavaScript are:

* [x] **Null**; :ballot_box_with_check:

* [x] **Undefined**; :ballot_box_with_check:

* [x] **Number**; :ballot_box_with_check:

* [x] **Boolean**; :ballot_box_with_check:

* [x] **BigInt**; :ballot_box_with_check:

* [x] **String**; :ballot_box_with_check:

* [x] **Symbol**; :ballot_box_with_check:

* [ ] ~~Object~~.

---
___

## Algorithms basics ##

:question: **5. What are the assignment operators? Name some of them.**

   Assignment operators in JavaScript give/ designate/ allocate a specific value to the ** left operand** based on the value given on the value given on the **right operand**. 

   Let's see some examples:

:black_nib: `let x = 23;` :heavy_check_mark:

  | **Assignment operator's name**| **Shorthand** | **Expected**  | **Result** |
  |:-------------------------:|:---------:|:---------:|:------:|
  | Assignment                | x = 23    |  x = 23   | 23     |
  |Addition assignment        | x += 23   | x = x + 23|   46   |
  |Substraction assignment    | x-= 23    | x = x-23  | 0      |
  |Multiplication assignment  | x* = 23   | x = x * 23| 529    |
  |Division assignment|x/=23  | x = x / 23| 23 / 23   | 1      |
  |Remainder assignment|x%23  | x = x % 23| 23 % 23   | 0      |
  |Exponentiation assignment  | x** = 23  | 23 = 23 ** 23| (Math.pow(23,23))|
  
___

:question: **6. What are the arithmetic operators? Name some of them.**
    An arithmetic operator establishes the operation between two operands.
    Let's see the arithmetic operators. In our case, the operands will be `a` and `b`.

| **Arithmetic operator**| **Description**        | **Operation**               |
|:------------------:|:------------------:|:-----------------------:|
| +                  | addition           |  a + b                  |
| -                  | substraction       |  a - b                  |
| *                  | multiplication     |  a * b                  |
| /                  | division           |  a / b                  |
| %                  | modulus (remainder)|  a % b                  |
| **                 | exponentiation     | a ** b = (Math.pow(a,b))|
| ++                 | increment          | +1                      |
| --                 | decrement          | -1                      |

___

:question: **7. What are the comparison operators? Name some of them.**

* Comparison operators determine differences or equality between values or variables. 
    Here are some examples:

`let x = 16;`

|**Comparison operator** | **Description**              | **Comparison**  | **Result** |
|:------------------:|:------------------------:|:-----------:|:------:|
|  ===    |equal value and equal type| 16 === "16" | false  |
|  ==     | equal to                 | 16 == "16"  | true   |
|   >     | greater than             | 16 > 28     | false  |
|   <     | less than                | 16 < 23     | true   |
|   >=    | greater than or equal to | 16 >= 11    | true   |
|   <=    | less than or equal to    | 16 <= 16    | true   |
|   !=    | not equal                | 16 != "16"  | false  |
|   !==   | not equal value and type | 16 !== "16" | true   |

___

:question: **8. What are the logical operators? Name some of them.**

* Logical operators help you write complex conditional statements.

| **Logical operator** 	| **Description**                                            	| **Example 1**                  	| **Example 2**                               	| **Order of operations** 	|
|----------------------	|------------------------------------------------------------	|--------------------------------	|---------------------------------------------	|-------------------------	|
|     ! NOT            	| reduce a value to boolean and reverse it                   	| !false == true                 	| if(isSaturday = true){!isSaturday == false} 	|         first           	|
|      \|\| OR           	| if at least one of the operands is true, statement is true 	| false \|\| true  returns true  	| false \|\| false returns false              	|        second           	|
|        && AND      	| returns true only if all operands are true                 	| true && true returns true      	| any combination with false returns false   	|        third            	|

___

:question: **9. What is the difference between `for`, `for of` and `for in`?**

* *for*, *for...in* and *for...of* statements (loops) are used in different circumstances to iterate over enumerable components of an object; 

* *for* and *for...in* loops only iterate over enumerable string properties of an object's values, whistl *for...of* statement loops over iterable data structures like: arrays, strings, Map, Set, Node lists, etc.;

* *for...in* loops through arrays and objects, while *for...of* only loops through arrays, Map, Set, arguments object;

* *for...in* iterates over property names, while *for...of* iterates over property values;

* in general, it might be best that you use *for...of* for arrays, *for...in* for objects and *for*/*forEach* to acces indexes of arrays;

* *for...in* supports control flow in the loop body (*continue*, *break*, etc.);

* the *for* loop is the oldest and most widely supported JavaScript loop, but it is better to use the other loops instead, when appropriate

___

:question: **10. How do you find the average of values in an array if you can’t use any built-in functions or methods?**

* sum of the values of the array and divide the sum by the length of the array, like this:
:black_nib:
        `let arr = [1, 2, 3]`;
        `let average = 0`;
            `for(let i = 0; i < arr.length; i++){`
                `average += arr[i]/arr.length`
            `};`


---
___

## Function basics ##

:question: **11. What are the main parts of a function?**

* an (optional) name - the function can also be anonymous;

* one or more parameters (when defining/declaring the function) or arguments (when calling/invoking the function), separated by coma and enclosed into round parantheses;

* the function body or content is a sequence of statements that define the function, enclosed between curly brackets.

___

:question: **12. What is the difference between parameters and arguments?**

* parameters are variables *passed* into a function when declaring/defining the function, whistl arguments are variables *imported* into a function when calling/invoking the function.

___

:question: **13. What are the differences between function expression and function statement?**

|       Differences       	|                        **Function statement** (F.D.)                        	|                             **Function expression** (F.E.)                            	|
|:-----------------------:	|:-----------------------------------------------------------------------------:	|:-------------------------------------------------------------------------------------:	|
|        *Syntax*       	| function add(a,b){return a + b} /  const add = (a,b) => {return a+b}          	|             let sum = function(a,b){return a+b};   ~~let sum = add(a,b)~~             	|
|         *Name*        	|                           must have a function name                           	| similar to the declaration, but without the function name                             	|
| *Variable assignment* 	|                                does not require                               	|                         can be stored in a variable assignment                        	|
| *Moment of execution* 	|                             before any other code                             	|                loads and executes only when its line of code is reached               	|
|       *Hoisting*      	|                  hoisted (can be used  before  it is defined)                 	| not hoisted (loads only when the interpreter  reaches the definition of the function) 	|
|   *Moment to access*  	| the function in the F.D. can be accessed before and after function definition 	|    the function in the function F.E. can only be accesed after function definition    	|


---
___

## OOP Basics ##

:question: **14. What is a method?**

*   A JavaScript *method* is an action that can be performed on an object by a function, meaning it is an *object property that has a function value*.
*   According to [MDM web docs](https://developer.mozilla.org/en-US/docs/Glossary/Method), 
> a method is a function which is the property of an object.

___

:question: **15. Name 3 builtin functions (and/or methods) regarding strings.**

    Let's list some methods for strings:
* [x] .concat(); :ballot_box_with_check:
* [x] .toUpperCase(), .toLowerCase(); :ballot_box_with_check:
* [x] .substring() :ballot_box_with_check:
* [x] .substr() :ballot_box_with_check:
* [x] .split() :ballot_box_with_check:
* [x] .charAt() :ballot_box_with_check:
* [x] .indexOf() lastIndexOf(); :ballot_box_with_check:
* [x] .search() :ballot_box_with_check:
* [X] .match :ballot_box_with_check:
___

:question: **16. Name 3 builtin functions (and/or methods) regarding arrays.**

    Some build-in functions used for arrays:
* .pop(); :ballot_box_with_check:
* .shift(), .unshift(); :ballot_box_with_check:
* .length; :ballot_box_with_check:
* concat(); :ballot_box_with_check:
* .splice(); :ballot_box_with_check:
* .slice(); :ballot_box_with_check:
* .toString(); :ballot_box_with_check:
* .sort(); :ballot_box_with_check:
* .reverse(); :ballot_box_with_check:


___

:question: **17. Name 3 builtin functions (and/or methods) regarding numbers.**

* Math.max(); :ballot_box_with_check:
* Math.min(); :ballot_box_with_check:
* Math.random(); :ballot_box_with_check:
* sort(); :ballot_box_with_check:
* toString(); :ballot_box_with_check:
* ValueOf(); :ballot_box_with_check:
* parseFloat(); :ballot_box_with_check:


---
___

## FP Basics ##

:question: **18. What is a callback function?**

* A callback function is passed as an argument to another function and will be executed in the order it's been called.

___

:question: **19. What are the differences between `for` loops and `forEach`?**

|         **Differences**        	| **for loop**                                 	| **forEach loop**                                                                                  	|
|:------------------------------:	|:----------------------------------------------:	|:---------------------------------------------------------------------------------------------------:	|
|            *Syntax*            	| `for(let i =0; i <=5; i++){ console.log(i)}` 	| `let numbers = [1, 2, 3, 4, 5]; numbers.forEach(number, index, array) => {console.log(number)});` 	|
|          *Description*          	|                 older, faster, harder to follow                	|                                           newer, slower, easier to follow                                           	|
|          *Parameters*          	|     initialization, condition, increment     	|                                       element, index, array                                       	|
| Acceptance of `break`, `await` 	|                      yes                     	|                                                 no                                                	|

___

## File basics ##

:question: **20. What is the difference between JavaScript data structures and JSON data structures?**

* JS data structures include objects and arrays, which can contain any kind of data (numbers, booleans, etc.), even other objects and arrays. 
* JSON data structures (JavaScript Object Notation) are a subset of JS data structures, easy to read for humans and easy to parse and generate by computers, used to send data between a server and a web app.
___

:question: **21. How do you create JavaScript data structure from a JSON file's data?**

* In order to create a JavaScript data structure from a JSON file's data, you need to use `JSON.parse()` - a method to parse a JSON string into a JS array or object.

___

## View Basics ##

:question: **22. What is the difference between JavaScript data structures and DOM (HTML document) data structures?**

* JS data structures include any kind of data and are used to store and manipulate these data into a JS program, whistl DOM (Document Object Model) is an interface that allows JS to manipulate the structure, content and style of HTML and XML documents.

___

:question: **23. What are the steps of changing a HTML element's content with JavaScript?**

* First, you need to select the element. You can do that either with `document.getElementById()`, either with `querySelector` or `querySelectAll` or `getElementsByClassName()`.
* Then, you can change the content of the element with `innerHTML` or `textContent` or `innerText`. Another way to change the content of the element would be to replace (`replaceWith`) the element with a new created one.

___

## Event basics ##

:question: **24. What is an event listener?**

* An event listener is a JS function which makes a specific event to occur on a HTML element and allows a web page to respond to user's interaction.
                        Example: 

        `addEventListener('click', (theEvent) => {});

        onclick = (theEvent) => { };`

___

:question: **25. What are the steps of changing a HTML element's content when the element clicked?**

* First, you need to select the element. You can do that either with `document.getElementById()`, either with `querySelector` or `querySelectAll` or `getElementsByClassName()`.
* The, you have to add an event listener to the element, to listen to the "click" event.
* Inside the event listener, call a function that returns the changed content of the element.
                Example:
    `let demo = document.getElementById("demo");
    demo.addEventListener("click", changeContent);
    changeContent = () => {
        demo.innerHTML = "new content"
    }`

___

:question: **26. Inside a `click` event listener, how can you access the element that has been clicked?**

* The element that has been clicked can be accessed using `event.target` - you can console.log(event.target) inside the event listener.

---
___

## Design Basics ##

:question: **27. What are the differences between `display: block` and `display: inline` CSS properties?**

* You can use `display: block` for block-level elements, such as: div, h1, p, form, section, footer, in order to create a new line after the parent container.
* You can use `display: inline` or `display: inline-block` for inline level elements, such as: button, a, img, input, span, em, when you don't need to create a new line after the element.
___

:question: **28. What are the differences between `position: relative` and `position: absolute` CSS properties?**
* The `position: relative` property allow the element to be moved with the top, bottom, left, right properties.
* The `position: absolute` property removes the element from the flow of the document and adds a specific set of coordinates to its position.

___

:question: **29. What is the box model, name the CSS properties connecting to it?**

* The CSS box model represents the layout of a web page, including margins (margin-top, margin-right, margin-bottom, margin-left), borders (border-top, border-right, border-bottom, border-left), paddings (padding-top, padding-right, padding-bottom, padding-left) and content (height, width).

___

:question: **30. What CSS properties affect font and text appearance?**

* The CSS properties that affect font and text appearance are:
* [x] font-size: size of text;
* [x] font-style: italic or another;
* [x] text-align: horizontal alignment (left, center, right, justify);
* [x] text-shadow: shadow efect added to the text;
* [x] text-indent: number of spaces before first line of text in block-level element;
* [x] word-spacing: space between words;
* [x] text-decorations: underlines, strikesthrough, etc.
* [x] font-weight: boldness of the text;
* [x] text-transform: lowercase or uppercase;
etc.

___

:question: **31. What are the steps of adding or removing a HTML element's class name?**

* First, select the element with `document.querySelector()`. Then, use `classList.add("new class")` or `classList.remove("existing class")`. Or you can use `classList.toggle()` method (adds or removes class name).

---
___

## JavaScript - language specialties ##

:question: **32. Is `null` an object or a primitive?**
    *Null* is a primitive that *represents the intentional absence of any object value*, according to [MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/null).
___

:question: **33. What is `undefined`?**
    *Undefined* is a primitive that indicates a variable without an assigned value or a variable that has not been declared.
___

:question: **34. What does it mean that a data type is mutable and what does it mean that it is immutable? Mention some examples.**

| **Differences** 	|                                                         **Mutable**                                                        	|                                      **Immutable**                                      	|
|:---------------:	|:--------------------------------------------------------------------------------------------------------------------------:	|:---------------------------------------------------------------------------------------:	|
|   *Data type*   	|                                                 arrays, objects, functions                                                 	|                                        primitives                                       	|
|    *Meaning*    	| can be changed without creating an entire new value; a JavaScript object can become immutable if you use `object.freeze()` 	|   cannot be changed, but its variable can be assigned another value (except for const)  	|
|   *Advantages*  	|                                                      more flexibility                                                      	|                     higher performance, less memory use, consistency                    	|
|    *Examples*   	|                                             let name = Mia; let name2 = Maira;                                             	| let person = {name: "Mia", age: 33}; let person2 = {...person}; person2.name = "Maira"; 	|

___

:question: **35. What does it mean that a data type is passed by value and what does it mean that it is passed by reference? Mention some examples.**

* When a variable is passed to a function by value, it means that the original variable outside the function will not be affected (updated/modified), but only the copy of it.
Example:
   ```
    let number = 1;
    addOne = (value) => {
    value++;
    };
    addOne(number);
    console.log(number); //number is still 1
    ```

* When a variable is passed to a function by reference or type, the original variable outside the function will be changed (updated/modified) according to the modifications made by the function.
Example:
        ```
        let arr = [1, 2, 3];
        addOne = (array) => {
            for(let i=0; i< array.length; i++){
                array[i]++
            }
        }
        addOne(arr);
        console.log(arr); // output: [2,3,4]
        ```


___

:question: **36. When to use `var`, `let`, and `const`?**

* `var` is an older version for initializing a variable; it is still used to declare local variable inside functions or globally-scoped; can be re-declare and updated;

* `let` is a modern alternative for `var` to declare a variable; can be updated, but not re-defined; it is block-scoped;

* `const` declaration of an object cannot be changed, but the object's properties can be updated; it is block-scoped.

___

:question: **37. What is hoisting?**

* Hoisting* consists in moving all the JavaScript declarations to the top of the scope (current script/ current function). 

---
___

## Git ##

:question: **38. What are the advantages of using a version control system?**

 * The advantages of using a version control system, such as Git, are: trackability of changes, collaboration, branching, merging, back-up, eficiency, etc.

___

:question: **39. What’s the difference between Git and GitHub?**

* Git is a version control system, whistl Github is a web platform that host repositories.

___

:question: **40. What are remote repositories in Git?**

* A remote repository is stored online (on a server) and can be accesed by multiple persons, in order to be able to collaborate.

___
:question: **41. Why does a merge conflict occur?**

* Merging conflicts can occur when more people are using different branches on Git in order to make different updates to a code and Git cannot automatically merge those branches, because it needs to know which changes to keep and which not.

---
___

## Terminal ##

:question: **42. How do you run a JavaScript file in the terminal?**

* You use the command `node` followed by the JS file name (for example, node index.js) and then you press enter. 

___

:question: **43. How do you stop a running a command in the terminal?**

* Control+C or Control+break stops the running command.

___

:question: **44. How go you get the previous command in the terminal?**

* You get the previous command in the terminal by pressing the `up arrow key`.

___

:question: **45. How do you get to the current directory's parent directory in the terminal?**

* To get to the current directory's parent directory in the terminal, use the command cd followed by space and two dots (`cd ..`).


**Resources:**

[Logical operators](https://journey.study/v2/learn/courses/1252/modules/13402/units/3/materials/19252) 

[Markdown table generator](https://www.tablesgenerator.com/markdown_tables) 

[StackAbuse](https://stackabuse.com/working-with-javascripts-built-in-string-functions/)



## The old version of the Workbook ##  

## Programming Basics Questions

## Computer science

### Data structures

**1. What is the purpose of a list (array in some programming languages) data structure? Name some methods of it!**

* An array (list) stores any kind of data in a linear order, so that the items can be easily manipulated. 
Examples for some methods of arrays:
[x] .pop(),
[x] .push(),
[x] .unshift(),
[x] .slice(),
[x] .append(),
[x] .extend(),
[x] .insert(),
[x] .remove()
etc.

___

**2. What is the difference between a list/array and a set?**

* An array (list) is an ordered collection of items that can be accesses using index, can have duplicate elements and can have mutable elements (that can be added, deleted or moved around).
* A set is an unordered collection of unique and immutable items (can't be changed once they've been assigned).

___

**3. What is the purpose and methods of a dictionary/map data structure?**

* Dictionary/ map data structure stores a collection or an array of keys and values (in pairs, each key is associated with a value). Using dictionary/ map data structure is easier to store, acces and manipulate data.
* Some methods of a dictionary are: _items()_, _keys()_, _values()_, _get()_ and _popitem()_.

___
---

### Algorithms

**4. Fibonacci sequences. Write a method (or pseudo code), that generates the Fibonacci sequences.**

```
function generateFib(x) {
  let fibo = [0, 1]; 
  for (let i = 2; i < x; i++) {
    fib.push(fibo[i - 1] + fibo[i - 2]); 
  }
  return fibo;
}
```

___


**5. How do you find a max value in a list/array if you can’t use any built-in functions?**

```
function findMax(arr) {
    let maxVal = arr[0]; 
    for (let i = 1; i < arr.length; i++) {
        if (arr[i] > maxVal) {
            maxVal = arr[i]; // Update the maximum value if a larger value is found
        }
    }
    return maxVal;
}
```
___


**6. How do you find the average of values in a list/array if you can’t use any built-in functions?**

```
function average(arr) {
    let sum = 0;
    for (let i = 0; i < arr.length; i++) {
        sum += arr[i];
    }
    return sum / arr.length;
}
```
___

**7. What do we call an _in-place_ sort?**

* An in-place sort is an algorithm to sort the elements of an array using the same memory space to store them, instead of creating a new copy. It updates a given list in-place (it changes the actual list on the spot, not returning a new one).

___

**8. Explain an algorithm which sorts a list!**

```
finished = False                    # declare a boolean variable to check if we finished sorting the list
list_length = len(a_list)           # get the number of items in a list so that we don't call len() for each iteration
while not finished:                 # we keep looping until we finished sorting (finished == True)
    finished = True                 # we assume it's finished (the condition to break out of the while loop)
    for i in range(list_length - 1):               # iterate through the list without the last item
        if a_list[i] > a_list[i + 1]:              # if the current item is bigger than the next..
            a_list[i], a_list[i + 1] = a_list[i + 1], a_list[i]         # we swap them
            finished = False        # keep looping until we have nothing left to swap
```

---
___

### Programming paradigms - procedural

**9. What are the main parts of a function?**

* Main parts of a function: _parameters_, _function body_, _variables_, _statements_, _expressions_, _function call_ and _arguments (input parameters)_.

___
---

## Software engineering

### Debugging


**10. What does step over, step into and step out mean while using the debugger?**

- **_step into_** A function is about to be invoked and you want to debug into the code of that function, so the next step is to go into that function and continue debugging step-by-step.
- **_step over_** A function is about to be invoked, but you're not interested in debugging this particular invocation, so you want the debugger to execute that function completely as one entire step.
- **_step out_** You're done debugging this function step-by-step and you just want the debugger to run the entire function until it returns as one entire step.

___

**11. How can you start to debug a program from a certain line using the debugger?**

* - **_line breakpoint_**

___

### Version control

#### What are the advantages of using a version control system?
* Using a version control system (such as Git) makes it easier to collaborate, back-up, merge projects, work on the same project in different branches, work more efficiently, keep track of the changes being made (and by whom), store an archive of the previous versions of the project.

#### What is the difference between the working directory, the staging area and the repository in git?

* The working directory is the local, work in progress version of the project.
* The staging area is where the work from the local directory is added (with git add), before being commited (git commit) to the remote repository. 
* The Git repository is the work commited to Git and stored on an online server.

#### What are remote repositories in git?

* The remote repositories in Git are online versions of the project (stored on an online server).

#### Why does a merge conflict occur?

* Merge conflicts in Git occur when different changes were made on the same line of code in different branches and Git is waiting to be told which changes to keep and which not, in order to merge. The user has to resolve the conflict before merging.

#### Through what series of commands could you put a new file into a remote repository connected to your existing local repository?

* Git add - adds the files in the staging area
* Git commit -m "commit message" - commits the files
* git push - send the files to the online (remote) repo.

#### What does it mean atomic commits and descriptive commit messages?

* Atomic commit messages are usually grouped around a same idea for the code. You make one commit on a specific topic, not multiple.
* Descriptive commits describe multiple steps being made to update de project.

#### What’s the difference between git and GitHub?

* Git is a version control system, whistl GitHub is an online platform hosting remote repositories.

## Software design

### Clean code

#### What does clean code mean?
* Clean code: easy to understand, easy to follow, correct syntax, up-to-date (according to best practices).

#### What steps do we usually do during a clean code refactoring?

[x] read the code carefully and understand every line of the code;
[x] add comments to explain the code;
[x] identify ideas to improve/ refactor the code;
[x] test the possible improvements (one at a time) - with the help of the console/debugger;
[x] add more comments where needed;
[x] test and review the code.

### Error handling

#### What is exception handling?

* The coder should be able to anticipate, identify and fix problems, errors and exceptions in the code. Exception/ error handling means to write the code so that, if the execution of a program encounters an error or an exception, it should be handled in a specific manner.

#### In which case should we catch an exception? Why?

* Catching an exception is useful when you want to handle an error in the code.

#### What can/should we do with an exception in the ‘except’ block?

```
try {
   // code having an exception
} catch (exception) {
   code how to handle the exception
}
```
* You identify the code with the exception and you write the code to handle the exception.

## Software Development Methodologies

#### What is the main goal of a retrospective meeting?

* A retrospective meeting summarizes the progress being made by the team and identifies ways of improving the work of the team in the future.

## Programming environment

### Unix

#### What is UNIX and what is Linux?

* UNIX is a consortium of operating systems.
* Linux is an open-source operating system developed by Linus Torvalds as a replica for UNIX.






