```cpp
// Online C++ compiler to run C++ program online
#include <iostream>
using namespace std;

int a[10];
int temp;
int top=-1;
int isfull()
{
    if(top==10)
        return 1;
    else
        return 0;
}
int isempty()
{
    if(top==-1)
        return 1;
    else
        return 0;
}

void push(int z)
{
    if(isfull()==1)
        cout<<"Stack is full :("<<endl;
    else
    {
        top+=1;
        a[top]=z;
    }
}

void pop()
{
    if(isempty()==1)
        cout<<"Stack is underflow :("<<endl;
    else
    {
        temp=a[top];
        top--;
        cout<<"Poped element: "<<temp<<endl;
    }   
}

void display()
{
    if(isempty()==1)
        cout<<"Stack is empty: "<<endl;
        
    else
        {
            for(int i=top;i>=0;i--)
            {
                cout<<a[i]<<endl;
            }
        }
    
}


int main() {
    
    int m;
    int num;
    int flag=1;
    while(flag!=0){
        cout<<"1.Push"<<endl<<"2.Pop"<<endl<<"3.Display"<<endl<<"4.Quit"<<endl;
        cout<<"Enter the option: ";
        cin>>m;
        switch(m){
            case 1:
                cout<<"Enter the number: ";
                cin>>num;
                push(num);
                break;
            case 2:
                pop();
                break;
            case 3:
                display();
                break;
            case 4:
                flag=0;
                cout<<"Program Ends :)";
                break;
            
        }
    }
}
```
