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
    // 1. Declare a pointer to the data type
    int* dynamicArray;
    int size;

    // 2. Get the array size from the user at runtime
    std::cout << "Enter the size of the array: ";
    std::cin >> size;

    // 3. Dynamically allocate memory for the array using 'new[]'
    // The 'new' operator returns the address of the first element.
    dynamicArray = new int[size];

    // Check if memory allocation was successful
    if (dynamicArray == nullptr) {
        std::cout << "Error: memory could not be allocated" << std::endl;
        return 1; // Exit with an error code
    }

    // 4. Input elements into the array
    std::cout << "Enter " << size << " elements:" << std::endl;
    for (int i = 0; i < size; i++) {
        std::cout << "Element " << i + 1 << ": ";
        std::cin >> dynamicArray[i];
    }

    // 5. Display the elements of the dynamically allocated array
    std::cout << "\nArray elements: ";
    for (int i = 0; i < size; i++) {
        // Access elements using array syntax or pointer arithmetic (dynamicArray[i] is same as *(dynamicArray + i))
        std::cout << dynamicArray[i] << " ";
    }
    std::cout << std::endl;

    // 6. Deallocate the dynamic array memory using 'delete[]'
    delete[] dynamicArray;
    dynamicArray = nullptr; // Good practice to set the pointer to null after deletion

    return 0;
}

4) write a c++ code to swap 2 numbers by using referencing


#include <iostream>

// Function to swap two integers using references
void swapNumbers(int& a, int& b) {
    int temp = a; // Store the value of 'a' in a temporary variable
    a = b;        // Assign the value of 'b' to 'a'
    b = temp;     // Assign the original value of 'a' (stored in 'temp') to 'b'
}

int main() {
    int num1 = 10;
    int num2 = 20;

    std::cout << "Before swap:" << std::endl;
    std::cout << "num1 = " << num1 << std::endl;
    std::cout << "num2 = " << num2 << std::endl;

    // Call the swap function, passing the variables by reference
    swapNumbers(num1, num2);

    std::cout << "\nAfter swap:" << std::endl;
    std::cout << "num1 = " << num1 << std::endl;
    std::cout << "num2 = " << num2 << std::endl;

    return 0;
}
