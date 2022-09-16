￼
# Pointers
## Unary address opreator
```
int a;
cout << &a; //here & represents the address of the variable
```
***
## Declaring a pointer variable
```
int a = 2;
int *p; //integer pointer variable
p = &a; //p will hold the momory address of a
cout<< *p; //it will print out the value of a
*p = *p +1 ; //it will increase the value of a by 1
// The size of the pointer depend on the compiler if 
//it is of 32 bit then it will be 4 byte and if its 
// a 64 bit then the memory will be 8 bytes
```
***
## Address arthmetic
```
int a, b;
int *c = &b; //c holds the memory address of b
c = c + 1; //Now it holds the momory address of a
// the memory location assignment works from the top //to bottomand for a 64 bit system if we add 1 then it //will jump 8 byte in the memory to hold the last one
​
```
***
## Explicit casting in case of pointer
```
int a;
int *temp = &a;
char *c = (char *)temp; //explicit casting in case of pointers
```
***
## Receiving pointers as paramerers in function
here if they are called by refrence then the value of the variable will change
```
#include <iostream>
​
using namespace std;
​
int main()
{
    int temp1 = 300, temp2 = 353;
    cout << "Address of temp1: " << (unsigned) &temp1 << endl;
    cout << "Address of temp2: " << (unsigned) &temp2 << endl;
    int *t2 = &temp2;
    cout << "Content of t2: " << (unsigned) t2 << endl;
    cout << "Content of the location: " << *t2 << endl;
    t2 = t2 + 1;
    cout << "Content of t2: " << (unsigned) t2 << endl;
    cout << "Content at location pointed by t2 " << *t2 << endl;
​
    char *k;
    k  = (char *)t2;
    cout << "*k is: " << *k << endl;
​
​
    k = (char *)&temp2;
    cout << "*k is: " << *k << endl;
    return 0;
}
```
***
