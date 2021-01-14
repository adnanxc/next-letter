# next-letter
Write a C++ program to change every letter in a given  string with the letter following it in the alphabet (ie. a  becomes b, p becomes q, z becomes a).


#include <iostream>
using namespace std;

string modify (string a){
   string n;
   int length = a.length();

   for(int i=0; i<length; i++){
        int x = a[i];
        if(a[i]==' '){
            n+=' ';
        }

        else if(x>=65 && x<90 || x>=97 && x<122){
            n += (char)x+1;
        }
        else if(x==90 || x==122){
            n+= (char)x-25;
        }

   }
   return n;
}




int main(){
    string s;
    cout << "Enter your string: ";
    getline(cin,s);

    cout << "New string: " << modify(s);
}
