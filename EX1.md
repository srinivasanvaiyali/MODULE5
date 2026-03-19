# Ex.No:1
# Ex.Name: Write a CPP Program to insert five double elements in to Stack ADT (use STL for Stack)
## Date:
## Aim:
To write a C++ program to insert five character elements into Stack ADT using STL.

## Algorithm:
1. Start the program.

2. Declare a stack of type char.

3. Read five character elements from the user

4. Insert each element into the stack using push().

5. Display the elements of the stack by popping them one by one until the stack becomes empty.

6. Stop the program.




## Program:
```
#include<iostream>
#include<stack>
using namespace std;
int main()
{
    stack<char> stack;
    int n;
    char str;
    cin>>n;
    cout<<"Size of the stack: "<<n<<endl;
    for(int i=0;i<n;i++){
        cin>>str;
        stack.push(str);
    }
    while(!stack.empty()){
        cout<<stack.top()<<" ";
        stack.pop();
    }
}
```


## Output:
<img width="484" height="272" alt="518722900-6ae4ef15-a833-4ca1-abdb-59e65b733b54" src="https://github.com/user-attachments/assets/39fab92e-3805-42de-9147-cf6481c7f104" />



## Result:

The program successfully inserts five character elements into the stack using STL and displays them in LIFO (Last In First Out) order.

