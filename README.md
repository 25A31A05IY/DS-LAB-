# DS-LAB-
WEEK 1:
1)Write a c++ code to display name roll no branch section by using cout:

#include<iostream>
int main()
{
std::cout<<"B.AMRUTHA";
std::cout<<"25A31A05IY";
std::cout<<"CSE";
std::cout<<"F";
return 0;
}

2)Write a c++ code to identify biggest value among given three values

#include<iostream>
using namespace  std;
int main()
{
int a,b,c;
cout<<"enter any three numbers";
cin>>a>>b>>c;
if((a>b)&&(a>c))
cout<<("a is big");
else if(b>c)
cout<<("b is big");
else 
cout<<("c is big");
return 0;
}

3)write a c++ code display 1D array elements using dynamic memory allocation

#include <iostream>
int main() {
    int* dynamicArray;
    int size;
    cout << "Enter the size of the array: ";
    cin >> size;
    if (dynamicArray == nullptr) {
    cout << "Error: memory could not be allocated" << std::endl;
        return 1; 
    }

    cout << "Enter " << size << " elements:" << endl;
    for (int i = 0; i < size; i++) {
        cout << "Element " << i + 1 << ": ";
        cin >> dynamicArray[i];
    }
    cout << "\nArray elements: ";
    for (int i = 0; i < size; i++) {.       cout << dynamicArray[i] << " ";
    }
    cout <<endl;
    delete[] dynamicArray;
    dynamicArray = nullptr; 
    return 0;
}

4) write a c++ code to swap 2 numbers by using referencing


#include <iostream>
void swapNumbers(int& a, int& b) {
    int temp = a; 
    a = b;       
    b = temp;
    }

int main() {
    int num1 = 10;
    int num2 = 20;

   cout << "Before swap:" << endl;
    cout << "num1 = " << num1 << endl;
    cout << "num2 = " << num2 << endl;
    swapNumbers(num1, num2);

    cout << "\nAfter swap:" << endl;
    cout << "num1 = " << num1 << endl;
    cout << "num2 = " << num2 << endl;
    return 0;
}
