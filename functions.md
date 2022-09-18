## Rules for declaring a function
* function name cant have spaces
* function name cant have any special character like single quote or double  quotes

***
***
# Rules for calling a function
A function can be called writting its name
```
void hello(){
	//code goes here
}

int main(){
	hello();
}
```

for a return value we have to use parameters
function called by value

```
#include <iostream>

using namespace std;

double totalPay(int hrsWorked, double ratePerHr){ //formal arguments
    double total = hrsWorked * ratePerHr;
    if (hrsWorked > 40){
        total = total + (hrsWorked - 40) * 2;
    }
    return total; //can only return 1 value
}


int main()
{
   int hours_worked;
   double rate;

   hours_worked = 41;
   rate = 10.0;

   double total = totalPay(hours_worked, rate); //actual arguments
   cout << "Total pay = " << total << endl;
   hours_worked = 47;
   rate = 10.5;

   total = totalPay(hours_worked, rate);
   cout << "Total pay = " << total << endl;


   return 0;
}
```
Default parameters method
```
#include<iostream>
using namespace std;
int add(int,int = 2);//the default value must be the secound one

int main(){
	int r = add(10);
	cout << r << endl;
	return 0;
}
int add(int a, int b){
	return a + b;
}

```
***
# Function prototype declaration
## Function called by value
The compilar always starts to compile the code from the begining to the end . So if we call a function that is defined below then it will not work
For that we need function prototype declaration
```
#include<iostream>
int multiple(int,int);
int main(){
	//mutiple called here
}
int multiple(int a, int b){
	//code goes here
}
```
***
## calling a function by refrence
passing a refrence variable
in this case refrence variable is used (&) insted of values
```
#include <iostream>

using namespace std;

void swap(int &a, int &b){ //here & means the refrence
    int temp = a;
    a = b;
    b = temp;
}

int main()
{
    int first {10}, second {20};
    cout << "First = " << first << ", Second = " << second << endl;

    swap(first, second);

    cout << "First = " << first << ", Second = " << second << endl;

    return 0;
}
```
***
## Function overloading, compile time polymorphism
here we can have diffrent functions with the same name
```
#include <iostream>

using namespace std;

int sum(int, int);
double sum(double, double);

int sum(int a, int b){
    cout << "Integer sum" << endl;
    return a + b;
}
double sum(double a, double b){
    cout << "Double sum" << endl;
    return a + b;
}
int sum(int a, int b, int c){
    cout << "3 integer sum" << endl;
    return a + b + c;
}

int main()
{
    cout << sum(3, 7) << endl;
    cout << sum(3.4, 7.5) << endl;
    cout << sum(3, 4, 5) << endl;
    return 0;
}

```
