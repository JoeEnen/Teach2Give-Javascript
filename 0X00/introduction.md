# Javascript
-a web-programming language for adding interactivity and dynamic functiona;lities to websites. 

# Including Javascript
You can add JS to HTML via eirthe rof the following ways:
1. Internal JS
2. External JS

## Internal JS
- In this case, we write JS inside a <script> tag in html.
## External JS
-This stores JS in a separate  -js file. The file is later linked to HTMLusing teh <script> tags with a src attribute.
eg. <script src" app.js"> </script>
-In this case, you may want to ensure that you put the link near the end of your html to ensure html loads last.
-Alternatively, ensure you add the (defer) keyword as shown below:
<script defer src" app.js"> </script>
-For the above case, you can put the link up near tite in html.

# Variable
-It is a labeled container for holding information.  
-Values (eg. numbers, texts etc) are stored inside variables.
-variables can be declared using either the var, let or const keyword.
-It is recommended that you use the let keyword as the var keywordis outdated.
-Const keyword is usually used for values that are bnot meant to change.

- It is reasonable to write variables in a .js file.
- To declare a var value, you write var>name= "value". name is the variable.
eg. var.name= "Annete"


-To declare a "let" value, you write,
eg. let name= "Annete";
    console.log(name)
    let firstname= "Mark"
    let age be =22

    Console.log(firstname, age).
    In this case, when you execute the code, the terminal will display (Annete, 22).

    -Cont. declares values that should not change, such as speed of light etc.
  
 ## Rules
    -Vairables can only start with letter, underscore r the dollar sign.
    -Variable names cannot be JS reserved keywords.
    -Not special characters in variables.
    - Use meaningful names.
    - Multible viaraible names can only be separated using camel case convesions or hyphen symbols.

 # Data Types
      - The most common datatypes include string, numbers, boolean, null, underfined, bigint an symbol.
## string
      - Characters are enclosed in "" or ' '.
## Numbers 
      -Can either be integers, decimals or NaN.
## Boolean
      -Can either be true or false.
## Undefined
      -Is decalred but uninitialized variables.
      eg. let age;
      console.log (age); //output: Undefined.
## Null
      -Uninetentional absence of value.
      eg. let man=null; // no man yet.
## Biglnt
      -for too many numbers beyong what JS can take.

## Checking variable types.
      -we use the "typeof" operator.
      eg. console.log(tyepeof age); //here will be displayed the variable.

# Operators
      -Symbols for performing operations such as calulations, comparisons an logical operations.
   ## Arithmentic operations
      -For maths.
      -include addition, exponentiation,  substraction, diviion, multiplications, and modulus.
   ## Increment Operators
      -for incraesing variable's value by 1.
      -include: post-increment (a++); pre-increment (--a)

   ## Assignment Operators
      -for assigning values to variables.
      eg. let.
      let x = 2
   ## comparison operations
      -compares values (true or false).
      -eg. equality operator (==),strict equalityoperator (===), not equal operator (!=) and strict not equal operator (!==).
      -Others include >, <, >=,  and <=.
   ## Logical Operators
      - Used for boolean logic.
      include: logican AND operator (&&); logical OR operator (||); logical NOT operator (!)

# String Concatenation
- Process fr joining 2 or more strings together.
- Available ways to do this include:
## + operator
-eg.
 let fisrtname= Annete
 let lastname= Error
 let fullName= firstsname + lastname
console.log("My full name is" = fullname)
## Using += Operators
- Helps add a string to a existing string.

## Template Literals
-They use (`) and '${}.

# Type coercion and Type conversion
-Involves changing a value from one data type to another, but they differ inhow they happen.
## Type conversion
- Happens automatically.
- common in comparisons (==), strng (+) and arithmetic operations.
## Type conversion
- Happens manually.
### Methods of Eplic Conve 
- convert to string using  string () or tostring ().
- convert to string using Number (), parseint () or parseFloat ().
- Convert to boolean using Boolean(). 





