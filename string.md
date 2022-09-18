## Read multiple lines
```
getline(cin,string_refrence);//cin is the object from which we want to read
      //string_refrence means the name of the string
```
***
## access the characters:
```
str.at(n);  // n is the index of the character in the string
str[n];
```
***
## accessing each characters
```
string str;
cin>> str;
for(char &p:str){
	cout << p <<endl;
}
```
```
#include <iostream>
#include <string>

using namespace std;

int main()
{
    string str = "Hello World";

    //cout << str[0] << ", " << str[str.length()-1];
    /*
    for(int i = 0; i < str.length(); ++i){
        //cout << str[i] << ", ";
        if (str.at(i) >= 'a' && str.at(i) <= 'z'){
           str.at(i) -= 32;
        }
    }
    cout << str;
    */

    for(char &p:str){
        //cout << p << ", ";
        if (p >= 'a' && p <= 'z'){
           p -= 32;
        }
    }

    cout << str << endl;
    cout << endl;
    return 0;
}
```
***
## transform a character string to lowercase
```
str s;
cin>> s;
transform(s.begin(),s.end(),s.begin(), ::tolower);
```
***
## using iterators for traversing the string
```
string::iterator it; //:: is called the scope resolution operator that results a scope
```
***
