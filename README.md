# Reading-Notes-Class-3
notes and question answers from reading 3
## Class 3 
 
### HTML ordered list. 
 
An ordered list is a list of items rendered in an order<br>
Attributes<br> 
Reversed specifies list items are reversed<br>
Start stars a list at a certain number<br> 
aaa lowercase for letters use lowercase a <br>
A for uppercase letters<br> 
iii for lowercase use lowercase i<br> 
I for uppercase roman numbers<br>
1 for numbers default<br> 
     B. ol and ul for ordered list and unordered list<br>
1. Ordered list for things like recipes turn by turn directions and list of ingredients in decreasing proportion on nutrition information labels.<br> 
 
II. Unordered list of elements reps a list items typically rendered as a bulleted list<br>
A. Attributes<br>
1. Compact Boolean attribute hints that the list should be rendered in a compact 
    style. Doesn’t work with all browsers<br>
2. Type
sets bullet styles<br>
a) circle<br>
b) disc<br>
c) square<br>
3. If not present and no CSS list-style-type prop apps to element user agent 
    select a bullet type dep on nest level.<br>
B. Usage Notes<br>
1. ul ele for grouping items that do not have a numerical order. The order of the     list is meaningless<br>
2. ul and ol elements both rep a list of items differ that ol is meaningful and ul is     not<br>
 
### CSS the Box model
 
The Box Model<br>
Everything in CSS has a box around it. Understanding of this makes it possible to create more complex layouts<br>
Block and Inline<br>
CSS several boxes fit into categories of block boxed and inline boxes, refs to his box behaves. Boxes have inner display type and outer display type<br>
Can set various values for display type using display prop which has various values<br>
Outer display type IF box has outer display is Block then<br>
Box will break out onto new line<br>
Width and height properties respected<br>
Padding, margin, and border, cause elements to be pushed away from box<br> 
If width not spec’d box will extend in the inline direction to fill the space avail in its container. Box will become as wide as container.<br>
4. Some html such as h1 and p use block as their outer display type. <br>
 
5. If box has outer display type of inline then<br>
    a)   Box will not break onto new line<br>
    b)   Width and height props will not apply<br>
    c) top and bottom padding margins borders apply but not cause other inline boxed to         move away from box<br>
 
     C. Inner display Type<br>
  1. Boxes have inner display type dictates how element inside box are laid out. <br>
  2. Change inner display type by setting display: flex; element still use outer type block         but change inner to type flex children become flex items and behave according to 

      specs<br>
    
     D. Examples of diff display types all have outer display type of block<br>
1. Paragraph w. Border added in CSS browser renders as block box. Para starts on new 
    line and extends width<br>
2. List lated out using display flex list itself is a block box. <br>
3. Block level paragraph inside which are two span elements elements would normally     be inline however on elements has a class of block which gets set to display     block<br>  
           4. See https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model for how to lay out paragraphs and words with diff borders<br>
 
     E. What is the CSS box model applies to block boxes defines how parts of a box margin, border, padding and content work together. <br>
1. Content box area when your content is displayed and size it using properties like inline size and block-size or width and height<br>
2. Padding box padding sits around the content as white space using padding
3. Border Box wraps the content and any padding use border<br>
4. Margin box outer most layer wrapping contend padding and border as whitespace between this box and other elements using margin<br>
    
    F. Alternative CSS box model content drive with is that width minus the width for the padding and border. <br>
 
   G. Margin invisible space around your box. Pushes other element away from the box. Margins can be + or - vals setting to negative items will overlap<br>
1. Margin collapsing<br>
a) two + margins will combine to one margin it’s size = largest indi margin<br>
b) two negative margins collar and smallest furthest from zero will not be used<br>
c) if one margin is negative it’s value will be subtracted from the total<br>
2. Borders border is drawn between margin and the padding of box. If using standard box model  the size of the border is added to the width and height of the content box. If using alt. Size of border makes the conned box smaller and takes up some of avail width and height<br>
3. Padding sits between the corder and the content area and is used to push the cont. away from border. Unlike margins can’t have neg padding. Any background applied to element will display behind padding.<br>
    
   H. The box model and inline boxes All of above applies to block boxes some props apply to inline boxes like this created by span element<br>
 
   I. Using display: inline block <br>
1. display: inline-block special value of display provides middle ground betwixt inline and block. Use when don’t want new line. <br>
2. Element w. display: inline block does subset of colon things. 
a) width and height respected<br>
3. Padding, margin, border cause other elements to be pushed away from box.<br> 
4. Does not break into new line. <br>
 
 
 
### JS 
 
Arrays. Neat way of storing list of data items under single var name. <br>
What is an array describe list like object; single objects contain multiple values stored in a list. Arrays can be stored in variables and dealt with like any other type of val. <br>ARRAYS ARE IMPORTANT OR WE WOULD HAVE TO STORE EVERYTIHNG IN A SEPARATE VARIABLE.<br>
Creating an array const colors = [“black”, “white”, “grey”, “orange” ]
const
dogs = [“German Shepard”, “corgi”, ]<br>
     
     C. Finding
length of array using .length see example on https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/Arrays
<br>
 
    D. Accesing and Modifying array using it’s index number and bracket notation [0] ex<br>
1) can also modify an item in an array by giving it a single array  like shopping [blah1, blah2, blah3, blah4]<br>
shopping [0] = “blah1”<br>
Console.log(shopping)
output is blah1<br>
 
E. An array inside of an array is a multidimensional array. Accessing item by chain together two index like <br>
Const random = [ “tree”, 795, [0,1, 2]]; <br>
Random [2][2]; <br>
 
F. Finding index of items in an array use . indexOf attach it to the array and console log it. Ex console.log(birds.indexOf(‘Owl”)); // 2<br>
 
G. Adding items can<br>
1. use push() Need to include one or more items to add to the end of the array<br>
2. to add to the front of the array use unshift()<br>
 
H. Removing items<br>
                1..pop() to remove last item of array<br>
                2. shift() remove first item<br>
                3. if know index of item can remove from array using splice() arrayName.splice(index, 1) If call to splice first argument says where to start removing items and second  argument says how many items should be removed so you can remove more than one item<br>
 
J. Accessing every item.
                1. use for…of example for (const bird of birds) { console.log(bird)}
                2. sometimes want to do same thing to each item in array. Leaving you with an array changed many times. Map() calls a function<br>
 
K. Converting between string and arrays<br>
                1. Data too long need to split it up to make it useful use split() method, takes single param the char you want to separate the string at and returns substring between the separator as items in an array.<br>
                2. can go opposite way using .join() method<br>
                3. another way to converta an array to string is using toString() method. Simpiler than join() can spec diff seperators where toString always uses comma.<br>
 
 
 L. Expressions and operators. Goes over expressions operators, assignment comparison, arithmetic, bitwise, logical string, string, ternary and more.
High level expression is unit of code that resolves to a value.<br>
Expression sets val of something like x = 7 so x is 7<br>
3 + 4 is the second it does something produces a va<br>l. 
Assignment operators see table on https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators<br>
Do not chain or nest assignments in other expressions it does not end well<br>
Comparison operators see table on https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators<br>
Arithmetic operators, % remainder ++ increment –decrement – unary negation +unary plus ** exponentiation operator<br>
Bitwise operators, trat their aperands as a set of 32 bits zeros and ones not dec, hex or octal<br>
Logical operators Logical and && logical OR || logical not ! <br>
Conditional (ternary) operator only js operator takes 3 operands the operator can have one of to vales based on cond. If condition is true the operator has the value of val1 or it has value of val2 can use cond operator anywhere you would use a standard operator<br>
Comma operator evals both its operands and returns val of last operand. Used mostly inside for loop DO NOT USE ANYWHERE ELSE<br>
Unary operators operation with only one operand<br>
Delete- deletes an objects property use splice in array and not delete<br>
Type of returns the type of thing that the variable or object is like number or string<br>
Relational operators, in operator returns true if the spec’d prop is in the spec’s object<br>
Basic expressions <br>
This refs to current object general this refs to calling object in method<br>
Grouping operator ( )  just like in math pemdas.<br>
JS conditionals
Conditional statements let us make decisions in js<br>
If…Else     if ( condition ) { code to run } else { code to run if the if isn’t true} <br>
If else if( condition) { code to run } if else ( another condition { more code to run } can continue on. When you get to a point ther eis only one remaining choice you else at the end.<br>
Logical operators === and !== check if one value is identical or not identical<br>
< and > test if one val is greater than or less than another<br>
<= and >= test if one val is greater than or equal to another.<br>
&& AND chain together two or more expressions so that all of them have to individually eval to true for whole expression to return true<br>
|| OR allows chaining to check if one or the other is true<br>
Switch statements a more concise way to break things, but they are confusing please see https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/conditionals#ternary_operator on switch statement about half way to down the page<br>
Ternary operator very small syntax that tests a condition and returns one val/ex if it si true and another if iti is false. Takes up less space than an if     else block<br>
IV .JS looping looping is great for using code you need to use over and over <br> 
Most things get looped though a collection like an array<br> 
Can use a for …. Of loop like for ( const cat of cats) { console . Log ( cat )<br> 
Standard loop if you want to do something identical over and over and over again you can use just a for loop for ( initializer; condition ; final-expression) {///////////code to run goes here}<br>
Can use for loop to loop though collection of things<br>
Can exit loop with a break, think like using switch statements.<br>
	2. Skipping iteration with continue / continue works like break instead of breaking out of loop it skips to the next iteration of loop<br> 
	3. While and do while…while is like a for can convert easily view documentation and Khan academy for review of how to do this.<br>
	4. Do while very similar provide a variation on the structure<br> 





READING QUESTIONS
Learn HTML

When should you use an unordered list in your HTML document?
You should use an unordered list, when the order does not matter, so if it is a collection of items that do not need numbers…such as popcorn toppings, but not popcorn toppings rates. 

How do you change the bullet style of unordered list items?
You can change the bullet style in your css file by using list-style-type:square;

When should you use an ordered list vs an unorder list in your HTML document?
You should use an ordered list when something needs to be done in a certain order like directions, or steps in a recipe. 

Describe two ways you can change the numbers on list items provided by an ordered list?
To change the numbers on an ordered list. You can use <ol type=“i"> which will give you roman numerals. Or you can use <ol reversed start=“10"> to get a list to count down.

Learn CSS
The Box Model.
Describe the CSS properties of margin and padding as characters in a story. What is their role in a story titled: “The Box Model”?
Together Margin and Padding, work together in and onscreen romance, Margin is holding it all together, wrapping the outer content in a nice hug, and keeping some well needed space between the content and the border. The margin likes to be on the sidelines as a whitespace wall flower, it doesn’t count towards the size of the box, but it does take up space in the relationship. Padding sits right between content and margin. Padding takes up space in the relationship, padding can be quite big if it wants to. Padding blends in with the background anything your background is set your your padding is displayed as padding can be quite the chameleon. Padding and Margin, are quite the onscreen romance, emo on the sidelines but running the show. 

List and describe the four parts of an HTML elements box as referred to by the box model.
The four parts of the box model are as follows. 
Content box, where content is displayed you can change the size with various properties. 
Padding box, padding sits around content as whitespace, can also be changed in size. 
Border box wraps the content and any padding, you can change it to many things using border
Margin Box, the bit that wraps it all up. It wraps everything ti content the padding the border all of it. You can change it using margin
Learn JS
Arrays. Operators and Expressions. Conditionals. Loops.
What data types can you store inside of an Array?
You can store many different types of data types in an array such as strings, objects, numbers or other arrays. 

Is the people array a valid JavaScript array? If so, how can I access the values stored? If not, why?
This is a valid array arrays can be made of many types and contain other arrays, or arrays of arrays you can access the values stored by typing the name the array followed by parentheses, followed by square brackets. To solve this problem I used console.table to give myself a visual, when you are accessing 2d array the first square bracket indicates the row you would like to select the second indicates the column. https://www.freecodecamp.org/news/javascript-2d-arrays/#:~:text=You%20use%20two%20square%20brackets,element%20in%20the%20specified%20row.
3. List five shorthand operators for assignment in javascript and describe what they do.
	1. = assigns example x = cat , let x be assigned cat x now stands for cat
	2. += addition assignment, when you want to add something to itself rather than writing listItem = listItem + 3 it is listItem += 3 
	3. -= subtraction assignment works the same as addition only subtraction so if you wanted to removed one thing from itself it instead of listItem - listItem -1 it is just listItem -= 1 
	4. *= multiplication assignment works basically the same as subtraction and multiplication instead of listItem = listItem * 7 it’s just listItem *= 7
	6. /= division assignment works the same as the other operators. 
4. Read the code below and evaluate the last expression and explain what the result would be and why.
	let a = 10
	let b = ‘dog’
	let c = false;
	evaluate (a+c) + b
	1. Breaking this down into little bits, when you run a + c you still get 10 because the false doesn’t affect the 10 then we are adding on + b which is dog so we end up with 10 dog. 

5. Describe a real world example of when a conditional statement should be used in a JavaScript program.
	1. A real world example of a conditional statement If your alarm goes off and you are not sleepy get up and greet the day. Else go back to sleep the day will be there later. 


6. Give an example of when a Loop is useful in JavaScript.
	1. Loops are useful when you need to count things in javascript. 

### things i want to know more about
The correct way to use a class and an id in html/css I am pretty sure mine are all over the place





