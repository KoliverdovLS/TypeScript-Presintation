-Main slide
In my presentation we will talk about TypeScript

-Slide1
TypeScript is hardly a separate programming language. It is a typed superset of JavaScript.
Any TypeScript file is compiled into regular Ecmascript, 
and you can choose which version of Ecmascript to support this code for older browsers.
-Slide1_1
Example.
In this slide we can see how TypeScript code turns into regular JavaScript
-Slide1_2
In addition, TypeScript files can be supplemented with regular valid JavaScript code,
and it will work. It turns out that if we have a ready-made piece of code in JavaScript,
then we can use it, in a TypeScript project and it will work.

-Slide2
Why do we need TypeScript?
TypeScript helps you find errors in the code, right at the time of writing.
Improves code readability and support.

-Slide3
How is this achieved?

-Slide4
In Javascript dynamic typing, we can change the type of a variable as we write code.
In large projects, this can lead to errors, and also complicates reading the code,
because we can not accurately determine the type of variable in the code segment.
Therefore, TypeScript has strict typing, variable types are set explicitly and cannot be changed later.
-Slide4_1
This also applies to functions.
The types of input and output parameters are set when writing the function.
All this, makes it easier to read the code.
The IDE also knows exactly what data types are in variables and functions,
which allows you to correct errors when writing code.

-Slide5
TypeScript supports the following data types.
The first three types are familiar to us with JavaScript, and there is nothing new in them.
-Slide5_1
In arrays, we can now explicitly specify the data type for all variables.
-Slide5_2
Tuples, like arrays, represent a set of elements, only for each element we explicitly specify its type.
-Slide5_3
The enum type is used to describe a set of numeric data using string constants.
Numeric values can be overridden.
We can get a numeric value from the text value.
And by a numeric value, we can get a text value.
-Slide5-4
The "Any" type, corresponds to its name.
You can put any data type in a variable of type "Any".
-Slide5-5
Type "void".
When writing code, there are functions that do not return anything,
for example, output a message to the console, 
and in TypeScript, you can clearly denote this, with the type "void".
-Slide5-6
The "never" type is also used as the output parameter type of the function. At first glance, 
it may seem that this type is similar to the "void" type, but it is not.
The "never" type is specified when the function is interrupted or cannot pass to the end, 
for example, it can be an infinite loop, or an error interrupt.
The "void" and "never" types help you understand what a function does.

-Slide6
Interfaces.
As the documentation says, one of the main features TypeScript:
is that typing is based on the structure of objects.
To do this, TypeScript has interfaces.
The interface defines the properties and methods that the object must implement.
In other words, an interface is a definition of a custom data type, but without an implementation.
In this case, the interfaces in TypeScript are similar to those in Java and C#.
Interfaces are defined using the "interface" keyword.
In this slide, we can see how the "IUser" interface is defined.
Interface "IUser" contains three properties, the types of which are explicitly defined.
As well a method, that specifies the type of input and output data.
-Slide6-1
Here we see the creation of as objects with the type "IUser".
Unlike a regular object, an object with the "IUser" type can contain three properties:
   -id with a type "number",
   -age with a type "number",
   -name with a type "string'
The "user" object fully satisfies the interface conditions.
In the "user2" object, the "id" property is of type "string",
which does not satisfy the interfest condition. Therefore,
the IDE notifies you of an error, and when you hover the mouse,
there will be a hint about the wrong data type.
The "user3" object has an additional property, the IDE also notifies you of an error.
In addition, such errors do not allow you to compile the code in JavaScript.
Slide6-2
For such cases, there are optional parameters that are set explicitly in the interface.
Let's add the optional "country" parameter to our interface.
To do this, you need to put a question mark after the parameter, as you can see on the slide.
Slide6-3
Now we don't see any errors in "user3". Because the "country" property is optional.
Such code can be compiled in JavaScript.
In projects with many objects of the same type, TypeScript allows you to avoid errors.
And it also makes it much easier to read the code, by the interface of the object,
you can immediately clearly understand what data is stored in it.
Slide6-4
In addition, it is convenient to use such objects as a function argument.
You don't need to write a long line, with a bunch of arguments and their types,
you can just pass an object that contains all the necessary data.
Slide6-5
In this slide, we can see how the IDE gives hints on object properties.

-Slide7
So, where can all this be used?
-Slide7-1
First, such typing helps a lot in large projects,
because it will be very difficult to find a typo error in a bunch of lines code, for example,
if we incorrectly accessed an object property.
TypeScript allows you to find such errors even, at the time of writing.
Slide7-2
Equally important, it will be much easier for people to read and maintain code in a team environment.
Strict typing allows you to understand what type of variable is in a given section of code.
And also because of strict typing,
the IDE will give hints what type can be put in a variable or property of an object,
which will allow you to modify someone else's code much faster.