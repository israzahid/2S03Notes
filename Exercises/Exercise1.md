# Exercise 1

1) What are the differences between statically and dynamically typed langauges, what are the advantages of each?
   <br/> 
   <br/>
   **Statically Typed:**
   - if the variable type is known at compile time
   &nbsp; 
      - must specify what type each variable is
   - some languages have a *type interface*
   &nbsp;
      - the ability to deduce the type of a variable on its own
   
   *Advantage:* all kinds of checking can be done by the compiler, therfore a lot of trivial bugs can be caught earlier on
   
   **Dynamically Typed:**
      - the type is associated with run time values
   <br/>
   *Advantage:* quicker writing

2) Java has 8 primitive data types. What are they, how are they used? 
    | Type | What is it? | How is it used? |
    | ---- | ----------- | --------------- |
    | boolean | Boolean value, either true or false | Used a lot in for loops, if statements etc. Whenever evaluating something to be yes or no |
    | byte | Integer, 8 bits | From +127 to -128 |
    | char | Integer/single character | All unicode characters | 
    | short | Integer, 16 bits | From +32 767 to -32 768 |
    | int | Integer, 32 bits | From + 2 147 483 647 to - 2 147 483 648 |
    | long | Integer, 64 bits | From +9 223 372 036 854 775 807 to -9 223 372 036 854 775 808 |
    | float | Decimal, 32 bits | From 3.402,823,5 E+38 to 1.4 E-45 |
    | double | Decimal, 64 bits | From 1.797,693,134,862,315,7 E+308 to 4.9 E-324 |

3) If a and b are instaniated boolean variables, what does the following evaluate to? Do you need more information? Why?

	`!((a || b) && !(b || ! a || ! b))`
   

4) Consider these variable declarations:
int x = 2;
char c = 'a';

What do the following lines of Java evaluate to? Explain why. Hint: Look up the ACSII index table.
a) x + c;
b) "" + c + x;
c) x + c + "";

5) a)

Tinker around with some of the Java operations. Find something which suprised you. Does something behave differently from other languages you've used? Hopefully, some of you will be willing to share what you found with the class. 

b) Do some indepdent research what are & and | actually doing? Why does it functionally look equivalent to && and ||?

6) NO IF STATEMENT CHALLANGE: Implement the following methods without using an if statement; only using material we have covered thus far.

a) public static double myAbsoluteValue(double x){
	//returns the absoluate value of x
}

b) You're ordering pizzas for a party. In general, a child eats 2 slices of pizza, and adult eats 3, and a teenager eats 4. Pizzas have 8 slices total. Implement the function below which gives you the number of guests of each age group and returns the number of pizzas you should order. Bonus: find a solution without using the math library.

public static int pizzasToOrder(int child, int adult, int teen){
...
}

Potentially more exercises to come, we'll see how fast we get through them in lecture.
