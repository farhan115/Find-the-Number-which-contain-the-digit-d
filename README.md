# Find-the-Number-which-contain-the-digit-d
//Find the Number which contain the digit d
// C++ program to print the number which
// contain the digit d from 0 to n

#include <bits/stdc++.h>
using namespace std;

// Returns true if d is present as digit

// in number x.

bool isDigitPresent(int x, int d)

{
	// Break loop if d is present as digit
	
	while (x > 0)
	{
		if (x % 10 == d)
			break;

		x = x / 10;
	}

	// If loop broke
	
	return (x > 0);
}

// function to display the values

void printNumbers(int n, int d)

{
	// Check all numbers one by one
	
	for (int i = 0; i <= n; i++)

		// checking for digit
		
		if (i == d || isDigitPresent(i, d))
		
			cout << i << " ";
}

// Driver code

int main()

{
	int n,d;
	
	cout<<"Enter the number n: ";
	
	cin>> n;
	
	cout<<"The number is : "<< n <<endl;
	
	cout<<"Enter the number d: ";
	
	cin>>d;
	
	cout<<"Numbers which contain digit d is: "; 
	
	printNumbers(n, d);
	
	return 0;
}
