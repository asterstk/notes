# **cpp**
***
## variables
**unsigned** char 1 byte 0 to 255
**signed char** 1 byte -127 to 127
**int** 4 bytes - 2147483648 to 2147483647
**unsigned int** 4 bytes 0 to 4294967295
**signed int** 4 bytes -2147483648 to 2147483647
**short int** 2 bytes -32768 to 32767
**unsigned short int** 2 bytes 0 to 65,535
**signed short int** 2 bytes -32768 to 32767
**long int** 4 bytes -2,147,483,648 to 2,147,483,647
**signed long int** 4 bytes  same as long int
**unsigned long int** 4  bytes 0 to 4,294,967,295
**float** 4 bytes +/- 3.4e +/- 38 (~7 digits)
**double** 8 bytes +/- 1.7e +/- 308 (~15 digits)
```
auto myvar = 4.34;
cout<<typeid(myvar).name()<<\n;   //returns the type when used with the header "< typeinfo>"
```
***
## Refrence variable
```
int c = 10 ;
int &d = c ; //now if i change the value of d the value of c will change
```
***
## Arithmetic operators
+,-,*,/,%
Unary operators: +, -,*
***
## Explicit casting
```
int x = 5 ;
int y = 4;
float a = (float)x/y; //Here the x type will convert to float
```
***
## lvalue and rvalue
```
x = y ;		 // Here,x is the assignment operator or lvalue and y is the rvalue
// lvalue must be a variable
```
***
## Unary increment and decrement operators
**Unary increment operators** :a++ , ++a ; // int case of the first one the value will be assingned first then it will increment and for the secound one the opposite
**Unary decrement operators** : ```a-- ,--a ;```
***
## Relational operators
<,>,<=,>=,!=
```bool a = c<d;```
***
## Logical operators
**Logical and :** &&
**Logical or :** ||
**Logical not :** !
***
## Shortcut assignment operators
```
i +=3; // which means i = i + 3 
```
***
## Ascii character
```
ch a = a+32; // To change a uppercase letter to lowercase add 32 and vice versa
```
***
## if else statement
```
if (condition) {
	//code goes here
}
else if {
	//code goes here
}
else {
	//code goes here
}
***
## Conditional operator : ternary operator
(condition)? expression for true value :expression for false value ;
```
***
## Switch case statement
```
switch(variable name){
case 1 : 
	//code goes here
	break;
case 2 : 
	//code goes here
	break;
default :
	//code goes here
	break;
} 	//if break is not used than it will execute all the line from which it is true
```
***
##  while loop
```
int variable;
while(condition for the variable){
	//code goes here
increment or decrement ;
}
```
***
## do_while loop
```
do{
	// code goes here
} while ( condition ) ;	 //the semicolon is must after do....while
	//do_while will execute same number of times of while
```
***
##  for loop
```
for(initialization ; termination condition ; modification like increment or decrement){
	//code goes here
}
//we can use more than one variable in the initialization and other sections
//we can keep the sections empty but the use of semicolon is mandatory
```
***
## break keyword
```
for( ; ; ;){
	if(condition){
		break;	//the break keywords breaks the loop 
	}
}
```
***
## continue keyword
```
for(;;;){
	if(condition)
		continue;  //if continue is used then the loop will go for its next iteration without executiing the later part of the loop
	//code goes here;
}
```
***
## array
```
int arr[n]; //Here an integer array has been declared of number n
	//the name arr always refer to the refrence to the first element 
	
	
```
## string
