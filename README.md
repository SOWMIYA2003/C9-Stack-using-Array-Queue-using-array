# C9-Stack-using-Array-Queue-using-array
## STACK
### DISPLAY
```
float stack[100];
int top,i;
void display()
{
    for(i=top;i>=0;i--)
    {
        printf("%.1f ",stack[i]);
    }
    if(top==-1)
    {
        printf("stack is empty\n");
    }   
}
```
### POP
```
int top;
void pop ()
{
    if(top==-1)
    {
        printf("stack is empty\n");
    }
    else{
        top=top-1;
    }
}
```
### PEAK
```
int stack[100],top;
void peek()
{
    printf("%d",stack[top]);
}
```
### PUSH
```
float stack[100];
int size=3,top=-1;
void push (float data)
{
    if(top==size-1)
    {
        printf("stack is full\n");
    }
    else{
        top=top+1;
        stack[top]=data;
    }
}
```
## QUEUE
### DISPLAY
```
int queue[50], rear=-1, front=-1;
void display()
{
    int i=0;
    if(front==-1||front>rear)
    {
        printf("No elements to display\n");
    }
    else{
        for(i=front;i<=rear;i++)
        {
            printf("%d\n",queue[i]);
        }
    }
}
```
### PEAK
```
int queue[50];
int front;
void peek()
{
    printf("%d",queue[front]);
    return ;
}
```
### DELETE
```
int front, rear;
void dequeue()
{
    if(front==-1|| front>rear)
    {
        printf("Queue Underflow.\n");
        return;
    }
    else{
        front=front+1;
    }
}
```
### INSERT
```
int queue[50];
int size=10,rear=-1,front=-1;

void enqueue(int data)
{
    if(rear<size)
    {
        if(front==-1)
        {
            front=0;
        }
        rear=rear+1;
        queue[rear]=data;
    }
}
```
