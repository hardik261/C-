#include<iostream>
using namespace std;
class alpha
{
	private:
		int data;
		public:
			alpha()         //no arg constructor
			{
			}
			alpha(int d)    //one arg constructor
			{
				data=d;
			}
			void display()  //display data
			{
				cout<<data; //overload=operator
			}
				alpha operator=(alpha& a)

			{
				data=a.data; //not done automaaticaaly
				cout<<"\n assignment operator invoked";
				return alpha(data); //return copy of this alpha
			}
};
int main()
{
alpha a1(37);
alpha a2;
a2=a1;
cout<<"\n a2=";                //invoke overload
a2.display();                  //display d2
alpha a3=a2;                   //does not invoke=
cout<<"\n a3=";
a3.display();                 //display a3
cout<<endl;
return 0;
}
