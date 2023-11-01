'''cpp
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
    push(11);
    push(12);
    push(13);
    push(14);
    push(15);
    display();
    pop();
    pop();
    pop();
    display();
    return 0;
}
'''
