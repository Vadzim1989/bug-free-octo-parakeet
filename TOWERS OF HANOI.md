/*Towers of Hanoi*/
#include <iostream>
  
using namespace std;

void hanoi(int n, int a, int b,int c);

void main()
{
  int n;
	cout << "Enter number of towers: ";
  cin >> n;
	hanoi(n, 1, 2, 3);
}

void move(int a, int b)
{
	cout << "from tower " << a << " to tower " << b << endl;
}

void hanoi(int n, int a, int b, int c)
{
	if (n == 0)
		return;
	hanoi(n - 1, a, c, b);
	move(a, c);
	hanoi(n - 1, c, b, a);
}
