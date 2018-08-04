# Sabercat Style Guide

This guide outlines the best practices for robot programming in `java` all current code should be written in accordance to this guide. Any legacy code that is used in a modern setting should be converted to this style. 

## White Spaces

#### 1) One line may *not* exceed 99 characters.

This code in one line is in violation of this rule. It is 115 characters long excluding an tabs prior. In a case like this, consider shortening the method name or even breaking up the method into several methods for better compartmentalization. 

``` java
public static void BigTestMethodForMakingRobotGoStraight(boolean extraBit, double bigNumber, float littleNumber) {
```

#### 2) No trailing whitespaces at the end of lines or files.

Don't put spaces or tabs at the end of lines. Don't make a bunch of new lines at the end of your file. 

#### 3) No pillow spaces inside of parenthesis, unless you're using a for loop. 

Pillow spaces are where you make spaces before or after parentheses for readability purposes. As much as some of our programmers love pillows, these are banned everywhere except for loops. 

````java	
// Pillow space example.
if ( robot.wins() ) { // <== these are pillow spaces
    robot.dance();
}
if (robot.loses()){ // <== no pollow spaces
    robot.sadDance();
}
// For loop example.
for ( int i = 0; i < 10; i++ ) { // <== this is allowed :D
    //TODO: program robot.
}
````

#### 4) Open curly brackets must always have a space before them

``` java
// curly bracket space example.
if (code.compiled()) { // <== you need that space.
    programmer.setHappy(true);
}
if (code.hasNoCurlySpace()){ // <== this is not ok.
    programmer.setHappy(false);
}
public void setHappy(boolean isHappy) { // <== you need it for methods too
    // We don't know how to do this yet.
}
```



#### 5) conditional statements need that little space so they don’t look like a function

``` java
// conditional statement space examples
if (robot.wins()) { // <== acceptable
    robot.dance();
}

// why?
functionToCall(); // <== because this
if(robot.wins)   // <== looks like this
```



#### 6) When optional, curly brackets must be used.

``` java
// optional curly example
if (auto.works()) { // <== always use curly brackets even when it's optional.
    crowd.cheer();
}

if (auto.works()) // <== don't do this. What if someone comments out the condition body?
    crowd.cheer();
```



#### 7) No line break before the opening brace.

``` java
// line break before brace example
if (pizza.arrived()) { // <== do this
    lunch.enable();
}
if (pizza.arrived()) // <== don't do this. This isn't Microsoft...
{
    luch.enable();
}
```



#### 8) Line break after the opening brace.

``` java
// line brak after opening brace example
if (coffee.brewed()) { // <== take note of the new line here
    programmers.setHappy(true);
}
if (coffee.brewed()) {programers.setHappy(true)} // <== you will be fired for this.
```



#### 9) Line break before the closing brace.

``` java
// line break before closing brace example
if (kickoff.starts()) { 
    schedule.fallBehind();
} // <== this little guy deserves his own line

if (kickoff.starts()) {
    schedule.fallBehind();} // <== have mercy. Don't do this.
```



#### 10) Line break after the closing brace, unless it precedes a logic chain.

``` java
// Line break after closing brace example
while (!robot.isComplete()) {
    programmers.complain();
} // <== remeber, this brace gets its own line.
programmers.complainMore();

while (!robot.isComplete()) {
    programmers.complain();
} programmers.complainMore(); // <== NO. Stop that.
```



#### 11) Use spaces around binary operators, including the equals sign in attributes.

``` java
// Binary operator spacing example
if (issue == "mechanical") { // <== binary operators need elbow room
    mechanicalTeam.blameProgrammers();
}
if (issue=="mechanical") { // <== that's too hard for mortal programmers to read
    mechanicalTeam.blameProgrammers();
}
```



#### 12) Use a space after colons and commas.

``` java
// space after colons and comma examples
for (Programmer p : programmingTeam) { // <== wow. such spacing
    p.drinkTea();
}
for (Programmer p :programmingTeam) { // <== wow. such gross (don't do this)
    p.drinkTea();
}
// comma example
int[] luckNumbers = [2, 3, 7]; // <== readable, do this.
int[] luckNumbers = [2,3,7]; // <== less readable, don't do this.
```



#### 13) Use a space after the opening and before the closing brace for single line blocks or struct expressions.

``` java
// spacing for brackets example
void setNumber(int s){ this.s = s; } // <== if you must put it on one line, add spaces
void setNumber(int s){this.s = s;} // <== don't do this
```



#### 14) For multi-line function signatures, each new line should align with the first parameter.

``` java
// multi-line function argument example
void lottaArguments(
    int i,
    boolean b,
    double c
){
	// do something?
}

//                |
// Don't do this, V It looks really bad.
void lottaArguments(
    int i,
       boolean b,
 double c
){
	// do something?
}
```



#### 15) Idiomatic code should not use extra whitespace in the middle of a line to provide alignment.

``` java
// inline space for allignment example 

// Do this
int x = 2;
double mysteryNumber = 3.14;
String message = "4146";

// Don't do this
int    x             = 2;
double mysteryNumber = 3.14;
String message       = "4146";
```

