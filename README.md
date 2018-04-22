# calculator
#include <iostream>
#include <string>
using namespace std;
int addition(int*, int*);
int substraction(int*, int*);
int multipliction(int*, int*);
int division(int*, int*);
int mod(int*, int*);
int main()
{
	int choice, x, z;
	int *ptr1, *ptr2;
	ptr1 = &x;
	ptr2 = &z;
	do
	{
		cout << "what oepration do you want to do.\n";
		cout << "press 1 for addition.\n";
		cout << "press 2 for subtraction.\n";
		cout << "press 3 for multipliction.\n";
		cout << "press 4 for division.\n";
		cout << "press 5 for mod.\n";
		cin >> choice;
		cout << "please enter a numbe:\n";
		cin >> x;
		cout << "please enter another numbe:\n";
		cin >> z;
		switch (choice)
		{
		case 1: cout<<"the result of addition tow numbers = " << addition(&x, &z) << endl;
			break;
		case 2: cout << "the result of subtract tow numbers = " << substraction(&x, &z) << endl;
			break;
		case 3: cout << "the result of multiple tow numbers = " << multipliction(&x, &z) << endl;
			break;
		case 4: cout << "the result of divide tow numbers = " << division(&x, &z) << endl;
			break;
		case 5:cout << "the result of mod tow numbers = " << mod(&x, &z) << endl;
			break;
		default: cout << "wrong input try again.\n";
		}
		cout << "do you want to contiue.\n";
	} while (choice);


	return 0;
}


int addition(int *a, int *b)
{
	int result;
	result = *a + *b;
    return result;
}
int substraction(int *a, int *b)
{
	int result;
	result = *a - *b;
	return result;
}
int multipliction(int *a, int *b)
{
	int result;
	result = *a * *b;
	return result;
}
int division(int *a, int *b)
{
     int result;
	if (b == 0)
	{
		cout << "error\n";
	}
	else
	{
		result = *a / *b;
		return result;
	}
}
int mod(int *a, int *b)
{
	int result;
	result = *a % *b;
	return result;
}
