IS217 Final Exam
===================

Answer the following questions in 1-2 paragraphs.  Each one is worth 5 points.	

1.	What is a software design pattern? Why are they important?  
a.	A design pattern is a proven solution to a common problem. This solution is maintained in a guideline, which gives examples of its implementation. The problem, itself that the design pattern solves also has to be properly documented.  The design pattern will also document its advantages/disadvantages and might even document when not to use it and other patterns that should be used in conjunction.
b.	Design patterns allow programmers to explain complex functionality and logic with names. Many times a design pattern will have to be extended by a programmer, if the problem calls for it. Instead of explaining the whole process, the programmer only needs to explain the difference to the common design pattern, that everyone understands. 

2.	What is unit testing? Why is it important?  How would you use it?
a.	Unit testing is testing a specific module of code. The module has expected results for happy paths and  error exceptions. A unit test gives a coder confidence that changes to the module did not break anything. When he or she makes changes, they just run the unit tests.
b.	It is important to ensure that all code is intact and working.
c.	You could run the unit test cases manually, however it is much more resourceful to use a automated unit testing framework which plugins to the programming language written. The unit tests will assert the output of a function, or the current state of an object, to ensure that the correct result is made.

3.	Describe the relationship between HTML, CSS, and JavaScript.
a.	HTML is used to create the flow and the formatting of semantic blocks of information. CSS is used to style the elements formatted. Javascript is used to dynamically change the css or html when events happen. Javascript can also be used to retrieve data from a server to update the html and/or css.

4.	Describe the purpose of the Singleton design pattern.
a.	. It’s to have a manager object, which is used within a single namespace. It avoids a second object being created by mistake. When an manager object for an entire object Is used, it makes sense to only instantiate it once.  Furthermore, since it is a manager for an entire application it should have global scope. This avoids other modules from instantiating a second instance

5.	Describe the purpose of the Factory design pattern.
a.	The purpose of a factory is to create common objects used in an application. Each object must have the same structure and method, to ensure parts of the code, which access these objects, interact with them correctly. It returns an object based on the parameters passed to a constructor. It is a way of managing construction of similar objects. For example, a gui manager which returns gui objects such as buttons or links based off the parameters passed to it.  

6.	Describe the purpose of the publish and subscribe pattern.
a.	The purpose of this is to avoid coupling of objects. Messaging is abstracted in a separate object. This ensures that if the subscriber object doesn’t exist, or is missing proper information, the system does not malfunction. The pub/sub object will check to ensure that the subscriber only has event collection for each event, and add callbacks to it. This ensures that extra work is not being done.

7.	Describe the purpose of the decorator pattern.
a.	The purpose is to extend objects with common functionality. When objects are created they may not need certain functionality until a state in the application is reached. Instead of adding more overhead, by adding this functionality at the instantiation of the object, the object is extended with the decorate when it actually needs it. 
8.	Write the JavaScript code that illustrates a decorator pattern.
Var decoratorFunction = function(){return “decorate”;};
Var object1 = {};
object1.newMethod = decoratorFunction;


Write the JavaScript code that illustrates a factory pattern.
Type1Object = {};
Type2Object = {};
Function factory(){}

Factory.protoype.createobject = function(options){

Var object = {};

if( options.type == “type1”){
this.object =  new type1Object;

}
Else {
This.type = new type2Object;
}

return this.object

};

Type1factory = new Factory();
Type1factory.createobject({type: “type1”});


9.	Write JavaScript pseudo code that illustrates the singleton design pattern.
Var Singleton = function(){
Var object = {};

Return {
getobject:  function(){
If (object){
Return object;
}
Else{
Return new object;
}
}
}();

10.	What is jQuery and provide examples of why you would use it? When would you not choose to you it?
a.	Jquery is a library toolkit for help create front end web applications. It offers utility functions that simply coding, by shortening code through complex functions. This is called a façade pattern. You would use it to deal with cross-platform issues, such as adding events in different browsers and doing ajax calls. You would not use it just for selecting elements, unless you are using older IE browsers. Modern browsers and ECMA tend to learn from jquery and adapts some of its useful techniques in native javascript. F

11.	What is Backbone.js and how is it different than jQuery
a.	Backbone is not a library with tools to ease client side scripting. Although one of it’s prerequisites is underscore, which gives utility functions to handle collections. Backbone.js is a MVW (or MV*) framework which allows for data to be persistant using model/collections. Views are de coupled from data and are only updated by events that the model sends to it.

12.	Write the JavaScript code to select an element by tag.
Document.getElementsByTagName(‘p’)[0]; //gets the 1st p in the document

13.	Write the JavaScript code to select by ID
Document.getElementById(‘hello’); //gets element with id of hello

14.	Write the JavaScript code to select an id and then add html to it.
Var myElement = document.getElementByID(‘yo’);
myElement.innerHTML = myElement.innerHTML + “<p>My paragraph</p>”;

15.	Write the JavaScript code to create an element.
Var newLink = document.createElement(‘a’);
myElement.appendChildd(newLink);


16.	What is Node.js?
Node.js is an i/o service-side instance of JavaScript. It is infamous for being non blocking and extremely fast. Since it is only JavaScript, it is also very lightweight. It’s gaining popularity because it allows client side programmer, who know JavaScript, to also help out with server side code. Node has also gained infamy for its package manager NPM. Many client side coders use this to download and install dependencies for their applications. 

17.	What is the difference between unit and functional testing?
Unit testing is done on actual code. Functional testing is done on the actual application. Meaning, it is done using the same controls a user would use. However, tools and automation can be used to speed up the process. Furthermore, functional testing is normally done by a separate qa team or user rep, while unit testing is done by the coder who wrote the module.



Answer the following questions in 2-3 paragraphs.  Each one is worth 10 points.	

18.	You have been hired to design and manage a team of developers tasked with creating a web application.  How would you explain to your developer the importance of using standard design patterns when designing the system?  Provide some practical examples that illustrate to your team how you will use the concept of design pattern within the project.
a.	Design patterns allow programmers to explain complex functionality and logic with names. Many times a design pattern will have to be extended by a programmer, if the problem calls for it. Instead of explaining the whole process, the programmer only needs to explain the difference to the common design pattern, that everyone understands. 
b.	It is a guideline. The pattern will not work for every situation. There will always be times when a custom solution or extension must be used. However, it allows the team to have a starting basis. 
c.	We would use  MVC in the back-end using express and node, and backbone in the front. We would use jquery which gives is a façade pattern and a singleton and a pub/sub. The pub/sub makes it more efficient to update  objects using a callback and events. The façade will abstract some complicated code that is inconvenient and tedious to type. The singleton will ensure the jquery object is being used once by the application. 

19.	You have been hired to design and manage a team of developers tasked with creating a web application.  How would you explain to your developer the importance of creating unit tests?  Provide some practical examples that illustrate to your team why unit testing is important. 
a.	Unit testing makes coders accountable. It will use the technique red/green/refactor cycle. This gives a coder confidence. They can make the code better without fear of it breaking current functionality. It makes things easy when using automated testing frameworks. Simply hit run tests and you get a report with pass and fail. The failures will tell you exactly where the problem is. This helps the coder know what to change.
b.	It makes updates very easy. For example:
i.	New requirements are created. These requirements need to be turned in functional tests. Obviously they will fail because it’s not implemented yet. However, once you start writing the code you’ll know you’re done when it passes. This takes the mystery out of writing good code. Furthermore, by checking all the other test caes created before it, you know it did not break anything.
ii.	If something does break you know it’s not the fault of your code. It’s because a test case was missing. Since each test case is approved by management, this is to no fault to the coder. The new edge case error just needs to be made into a unit test.


Bonus Points:

Create a repository on github and commit any file to it to demonstrate your ability to use Github.  Include a link to the repository inside your test submission.
https://github.com/ChrisBras/is217final

