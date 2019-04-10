#include<iostream>
using namespace std;

int main()
{
	double arrx[2];
	double arrf[2];
	double x, lx;
	int h;
	system("color C");
	//----------------------------------------------
	cout << "________________LAGRANGE  POLYNOMIAL________________" << endl;
	cout << "                                                    " << endl;
	cout << "Enter 3 values For X :" << endl;
	for (int i = 0; i < 3; i++)
	{
		cout << "                                                " << endl;
		cout << "X" << i << endl;
		cin >> arrx[i];
	}
	cout << "Enter 3 values For F :" << endl;
	for (int j = 0; j < 3; j++)
	{
		cout << "F" << j << endl;
		cin >> arrf[j];
	}
	cout << "How Meany Value ?" << endl;
	cin >> h;
	for (int c = 1; c <= h; c++)
	{
		cout << "______________________________________________________" << endl;
		cout << "Enter f(Value) : " << endl;
		cin >> x;
		cout << "                                                     " << endl;                       //*****Start                                                                                  //****StartTwo            
		lx = ((((x - arrx[1])*(x - arrx[2])) / ((arrx[0] - arrx[1])* (arrx[0] - arrx[2]))) * (arrf[0])) + ((((x - arrx[0])*(x - arrx[2])) / ((arrx[1] - arrx[0])* (arrx[1] - arrx[2]))) * (arrf[1])) + ((((x - arrx[0])*(x - arrx[1])) / ((arrx[2] - arrx[0])* (arrx[2] - arrx[1]))) * (arrf[2]));
		cout << "f(" << x << ")" << "~=" << "L(" << x << ")" << " = " << lx << endl;
	}
	system("pause");
}