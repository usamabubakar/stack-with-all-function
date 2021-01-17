#include <iostream>
#include<conio.h>
using namespace std;
class stack
{
	
	public:
		int a[5],top=-1;
		void push(int value)
		{
			if(top==5-1)
			{
				cout<<"stack is full\n";
				
			}
			else
			{
				top++;
				a[top]=value;
			}
		}
		int pop(int value)
		{
			if (top==-1)
			{
				cout<<"\nstack is empty\n";
			}
			else
			{
				top--;
			}
		}
		int show_top()
		{
			if (top==-1)
			{
				cout<<"\nstack is empty\n";
			}
			else
			{
			cout<<"\n\ntop element is :"<<a[top]<<"\n";
			}
			
		}
		int display()
		{
			if (top==-1)
			{
				cout<<"\nstack is empty\n";
			}
			else
			{
				cout<<"\n\n value: \n";
				for(int i=0;i<=top;i++)
				{
					cout<<a[i];
					cout<<"\n";
				}
			}
		}
};
int main()
{
	stack s;
	int b,value;
loop:
    cout<<"\t1:push\n";
	cout<<"\t2:pop\n";
	cout<<"\t3:top element\n";
	cout<<"\t4:all value\n";
 cin>>b;
 system("cls");
 switch(b)
 {
 	case 1:
 		cout<<"\nenter value :";
 		cin>>value;
 		s.push(value);
 		goto loop;
 		break;
 		case 2:
 			s.pop(value);
 			goto loop;
 			break;
 			case 3:
 				s.show_top();
 				goto loop;
 				break;
 				case 4:
 					s.display();
 					goto loop;
 					break;
 }
	
}
