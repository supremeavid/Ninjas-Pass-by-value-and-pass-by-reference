# Ninjas-Pass-by-value-and-pass-by-reference
#include <iostream>

using namespace std;
void Increment(int n){
    n++;
}
void IncrementWithreference(int &n){
    n++;
}
int f(int n){
    int a=n;
    return a;
}


int main()
{
    int i=10;
    int j=i;
    i++;
    cout<<j<<endl;  //No change in j as value of i get copied and pasted to j
    cout<<"Now we will pass i by reference"<<endl;
    int &k=i;
    i++;
    cout<<k<<endl;
    k++;
    cout<<i<<endl;
    //Test out the increment function using reference variable and also without using them
    cout<<"Without referencing and increment functioning"<<endl;
    Increment(i);
    cout<<i<<endl;
    cout<<"With referencing and increment functioning"<<endl;
    IncrementWithreference(i);
    cout<<i<<endl;
    //Use return and pass by value
    int m=f(i); //Only f(i) won't return k; we need a memory address also to store it which is provided by m
    cout<<m<<endl;

    return 0;
}
