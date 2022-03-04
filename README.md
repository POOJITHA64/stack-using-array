# stack-using-array
#include<stdio.h>
int stack[100],x,i,n,top;
void push()
{
    if(top>=n-1)
    {
        printf("stack over flow occur");
    }
    else
    {
        printf("enter the value to be pushed\n");
        scanf("%d",&x);
        top++;
        stack[top]=x;
    }
}
void pop()
{
    if(top<=-1)
    {
        printf("stack under flow occur\n");
    }
    else
    {
        printf("enter the value to be poped\n,stack[top]");
        top--;
    }
}
void display()
{
    if(top>=0)
    {
    printf("operations on stacks is:");
    for(i=top;i>=0;i--)
   
        printf("%d",stack[i]);
        printf("press next choice");
    }
    else
    {
        printf("stack is empty");
    }
}
int main()
{
    top=-1;
    int choice=0;
    printf("\n Enter the size of STACK[MAX=100]:");
    scanf("%d",&n);
    printf("\n\t STACK OPERATIONS USING ARRAY");
    printf("\n\t--------------------------------");
    printf("\n\t 1.PUSH\n\t 2.POP\n\t 3.DISPLAY\n\t 4.EXIT");
    do
    {
        printf("\n Enter your Choice:");
        scanf("%d",&choice);
        switch(choice)
        {
            case 1:
            {
                push();
                break;
            }
            case 2:
            {
                pop();
                break;
            }
            case 3:
            {
                display();
                break;
            }
            default:
            {
                printf ("\n\t Please Enter a Valid Choice(1/2/3/4)");
            }
               
        }
    }
    while(choice<=4);
    return 0;
}
