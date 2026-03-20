# Ex.No:3
# Ex.Name: Write a CPP program for Postfix to Prefix Conversion using Stack STL
## Date:
## Aim:
To write a C++ program to convert a postfix expression to a prefix expression using the stack STL.

## Algorithm:
STEP 1: Start the program.

STEP 2: Include the and headers.

STEP 3: Read the postfix expression from the user.

STEP 4: Declare a stack of strings to store intermediate expressions.

STEP 5: Traverse each character of the postfix expression from left to right.

STEP 6: If the character is an operand, push it onto the stack as a string.

STEP 7: If the character is an operator, pop the top two elements from the stack.

STEP 8: Concatenate the operator before the two operands to form a new prefix expression.

STEP 9: Push the new prefix expression back onto the stack.

STEP 10: After traversal, the stack will contain the final prefix expression. Display it.




## Program:
```
#include<bits/stdc++.h>
using namespace std;
bool isOperator(char x)
{
    switch(x)
    {
        case '+':
        case '-':
        case '/':
        case '*':
        return true;
    }
    return false;
}
string postToPre(string post_exp)
{
    stack<string>s;
    int length =post_exp.size();
    for(int i=0; i<length; i++)
    {
        if (isOperator(post_exp[i]))
        {
            string op1=s.top();
            s.pop();
            string op2=s.top();
            s.pop();
            string temp =post_exp[i]+op2 +op1;
            s.push(temp);
        }
        else
        {
            s.push(string(1,post_exp[i]));
        }
    }
    string ans ="";
    while (!s.empty())
    {
        ans+=s.top();
        s.pop();
    }
    return ans;
}
int main()
{
    string post_exp;
    cin>>post_exp;
    cout<<"Postfix to Prefix expression:" <<endl;
    cout<<postToPre(post_exp);
    return 0;
}
```


## Output:
<img width="848" height="298" alt="519130459-939436c3-bafc-4c07-9428-7b6644e9d243" src="https://github.com/user-attachments/assets/6743f5d5-1e6a-4dcb-a785-5e48ebd7a6b6" />



## Result:
The program successfully converts any valid postfix expression into its corresponding prefix expression using stack STL.


